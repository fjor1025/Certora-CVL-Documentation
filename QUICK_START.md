# CVLDocs Quick Start Guide  

**Get started with Certora verification in 30 minutes**

---

## Step 1: Your First Rule (5 minutes)

Create a file `MyContract.spec`:

```cvl
methods {
    function getValue() external returns (uint256) envfree;
    function setValue(uint256 x) external;
}

rule valueNeverDecreases() {
    uint256 before = getValue();
    
    env e;
    method f;
    calldataarg args;
    f(e, args);
    
    uint256 after = getValue();
    
    assert after >= before;
}
```

**What this does:** Proves that no function can decrease `value`.

---

## Step 2: Run the Prover (10 minutes)

Create `MyContract.conf`:

```json
{
    "files": ["MyContract.sol"],
    "verify": "MyContract:MyContract.spec",
    "rule": ["valueNeverDecreases"]
}
```

Run:
```bash
certoraRun MyContract.conf
```

**What happens:** Prover tests all functions against the rule.

---

## Step 3: Understand the Result (10 minutes)

### ✅ Rule Passes
Your contract is safe — no function can decrease value!

### ❌ Rule Fails (Counterexample)
Prover found a function that violates the rule. Read the call trace to see how.

**Common issues:**
- Missing `envfree` — Add to methods block
- Wrong assumption — Your property might be too strong

---

## Step 4: Level Up (5 minutes)

**Want more?** Pick your path:

### Path A: Token Verification
→ [ERC-20 Complete Tutorial](tutorials/certora-formally-verify-erc-20-token.md) (3-4 hours)  
Learn: Parametric rules, invariants, ghosts

### Path B: Deep Dive
→ [Learning Pathway 1](INDEX.md#pathway-1-complete-beginner--erc-20-verification) (8-10 hours)  
Master: CVL fundamentals, types, statements, expressions

### Path C: Specific Problem
→ [Quick Reference Tables](INDEX.md#quick-reference-tables)  
Find: Syntax, examples, troubleshooting

---

## Common First Questions

### "What is `envfree`?"
Marks functions that don't use `msg.sender`, `msg.value`, etc. Makes them easier to call in rules.

**Read:** [msg.sender & msg.value Tutorial](tutorials/certora-msgsender-msgvalue.md)

### "What is a `method wildcard`?"
```cvl
method f;
```
Means "any function in the contract." Used for parametric rules.

**Read:** [Parametric Rules Tutorial](tutorials/certora-parametric-rules.md)

### "How do I track sum of balances?"
Use ghosts + hooks to intercept storage writes.

**Read:** [Tracking Sums Pattern](guides/tracking-sums-pattern.md)

### "Prover timed out. What now?"
Try: `--smt_timeout 600`, split rules, add constraints.

**Read:** [Timeout Troubleshooting Guide](guides/timeout-troubleshooting-guide.md)

### "How do I handle external calls?"
Use the `methods` block with summaries (HAVOC, NONDET, DISPATCHER).

**Read:** [Method Summarization Reference](reference/method-summarization.md)

---

## Essential Syntax

### Core Statements
```cvl
require x > 0;          // Assumption (input constraint)
assert x > 0;           // Property to prove
satisfy x > 0;          // Prove witness exists
```

### Logical Operators
```cvl
x => y                  // Implication: "if x then y"
x <=> y                 // Biconditional: "x if and only if y"
x && y                  // And
x || y                  // Or
!x                      // Not
```

### Key Types
```cvl
mathint                 // Infinite precision integer
uint256                 // Bounded (Solidity type)
address
bool
```

### Method Calls
```cvl
env e;                  // Environment (msg.sender, block.timestamp, etc.)
method f;               // Any function
calldataarg args;       // Any arguments

f(e, args);             // Call any function
specificFunction(e, x); // Call specific function
```

---

## Next Steps

1. **Complete your first real verification:**  
   [Verify a Counter](tutorials/certora-verify-counter.md) ← Start here

2. **Master the fundamentals:**  
   [Learning Pathway 1](INDEX.md#pathway-1-complete-beginner--erc-20-verification)

3. **Explore by topic:**  
   [Complete INDEX](INDEX.md)

4. **Get methodology:**  
   [Certora-Fv-Framework](https://github.com/fjor1025/Certora-Fv-Framework.git)

---

**Questions?** → [INDEX.md](INDEX.md) | **Need help?** → [Glossary](reference/certora-glossary.md)
