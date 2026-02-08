# Certora CVL Documentation — Complete Knowledge Base

> **The definitive resource for Certora Prover and CVL (Certora Verification Language)**  
> Combining official reference documentation with RareSkills tutorial excellence  
> **Version:** 2.0 (Reorganized February 8, 2026)

---

## Quick Start

**New to Certora?** Follow this learning path:
1. Read [Formal Verification Introduction](#tutorials) (tutorial)
2. Learn [CVL Basics](#reference-core-language) (syntax reference)
3. Try [Verifying a Counter](#tutorials) (hands-on tutorial)
4. Master [Storage Hooks and Ghosts](#tutorials) (advanced tutorial)

**Looking for something specific?** Jump to:
- [Reference Documentation](#reference-documentation) — Syntax, technical specs, EBNF grammars
- [Tutorials](#tutorials) — Step-by-step learning with examples
- [Guides & Patterns](#guides-patterns) — How-to guides, design patterns, troubleshooting
- [Learning Pathways](#learning-pathways) — Organized curricula by topic

---

## Document Organization

### Reference Documentation

Complete technical specifications, syntax references, and EBNF grammars.

#### Core Language
| Document | Description | Use When |
|----------|-------------|----------|
| [CVL Basic Syntax](reference/basic-syntax.md) | Comments, identifiers, literals | Starting with CVL |
| [CVL Types](reference/types.md) | Type system, mathint, mappings | Working with types |
| [Statements](reference/statements.md) | require, assert, satisfy, if/else | Writing rule logic |
| [Expressions](reference/expressions.md) | Operators, precedence, evaluation | Writing conditions |
| [Functions](reference/functions.md) | CVL functions, definitions | Code reuse |

#### Ghosts & Hooks
| Document | Description | Use When |
|----------|-------------|----------|
| [Ghosts](reference/ghosts.md) | Ghost variables syntax | Tracking custom state |
| [Hooks](reference/hooks.md) | Sstore, Sload, CALL hooks | Intercepting storage ops |
| [Persistent Ghosts](tutorials/certora-persistent-ghosts.md) | Non-havocing ghosts | Native balance tracking |

#### Rules & Invariants
| Document | Description | Use When |
|----------|-------------|----------|
| [Rules](reference/rules.md) | Rule syntax and structure | Writing verification rules |
| [Invariants](reference/invariants.md) | Invariant syntax, preserved blocks | State invariants |
| [Parametric Rules](tutorials/certora-parametric-rules.md) | Method wildcards | Testing all functions |
| [Partially Parametric](tutorials/certora-partially-parametric-rules-erc-721.md) | Selective parametric | Constraining method sets |
| [Built-in Rules](reference/built-in-rules.md) | Sanity checks | Pre-verification validation |

#### Methods Block
| Document | Description | Use When |
|----------|-------------|----------|
| [Methods Block](reference/methods-block.md) | Complete methods block reference | Configuring verification |
| [Method Summarization](reference/method-summarization.md) | HAVOC, NONDET, AUTO, DISPATCHER | Handling external calls |
| [Import & Use](reference/import-use.md) | Import/use statements | Multi-file specs |

#### Advanced Features
| Document | Description | Use When |
|----------|-------------|----------|
| [Uninterpreted Sorts](reference/uninterpreted-sorts.md) | Abstract types | Identity tracking |
| [Transient Storage](reference/transient-storage.md) | EIP-1153 transient storage | Modeling TSTORE/TLOAD |
| [Definitions](reference/definitions.md) | Reusable CVL expressions | Code reuse patterns |
| [Call Trace Storage](reference/call-trace-storage.md) | Storage visualization | Debugging |

#### CLI & Configuration
| Document | Description | Use When |
|----------|-------------|----------|
| [CLI Options](reference/cli-options.md) | Complete flag reference | Running prover |
| [Storage Layout](reference/storage-layout.md) | EIP-7201, annotations | Complex storage |
| [Prover Techniques](reference/prover-techniques.md) | Control flow splitting | Understanding optimization |

#### Hashing & Types
| Document | Description | Use When |
|----------|-------------|----------|
| [Hashing Model](reference/hashing-model.md) | Keccak256 modeling | Hash verification |
| [EIP-7201](reference/eip-7201.md) | Namespaced storage | Upgradeable contracts |

#### CVL 2.0 & Migration
| Document | Description | Use When |
|----------|-------------|----------|
| [CVL 2 Migration Guide (Official)](cvl-2-migration-guide.md) | Complete CVL 1→2 migration guide (630 lines) | Upgrading existing specs |
| [CVL2 Migration Guide (Quick)](guides/cvl2-migration-guide.md) | Quick migration reference | Fast syntax updates |

#### Glossary
| Document | Description | Use When |
|----------|-------------|----------|
| [Certora Glossary](reference/certora-glossary.md) | Complete terminology | Looking up terms |

---

### Tutorials

Step-by-step learning materials with complete worked examples.

#### Beginner (Start Here)
| Tutorial | Topics Covered | Difficulty |
|----------|----------------|------------|
| [Formal Verification Introduction](tutorials/certora-formal-verification-intro.md) | What is formal verification, why use it | ⭐ Beginner |
| [Verify a Counter](tutorials/certora-verify-counter.md) | First spec, rules, running prover | ⭐ Beginner |
| [Verify Conditional Statements](tutorials/certora-verify-conditional-statements.md) | if/else logic verification | ⭐ Beginner |

#### Intermediate
| Tutorial | Topics Covered | Difficulty |
|----------|----------------|------------|
| [require, assert, satisfy](tutorials/certora-require-assert-and-satisfy.md) | Core statements, vacuous truth | ⭐⭐ Intermediate |
| [Implication](tutorials/certora-implication.md) | `=>` operator, logical patterns | ⭐⭐ Intermediate |
| [Biconditional](tutorials/certora-biconditional.md) | `<=>` operator, equivalence | ⭐⭐ Intermediate |
| [mathint & Overflow](tutorials/certora-overflow-and-mathint.md) | Infinite precision, type casting | ⭐⭐ Intermediate |
| [msg.sender & msg.value](tutorials/certora-msgsender-msgvalue.md) | Environment variables | ⭐⭐ Intermediate |
| [Testing Reverts](tutorials/certora-testing-revert-call.md) | @withrevert, lastReverted | ⭐⭐ Intermediate |
| [Loops in CVL](tutorials/certora-loops-in-cvl.md) | Loop handling, loop_iter | ⭐⭐ Intermediate |

#### Advanced — Storage & Ghosts
| Tutorial | Topics Covered | Difficulty |
|----------|----------------|------------|
| [Storage Hooks & Ghosts](tutorials/certora-storage-hooks-and-ghosts.md) | Complete ghost/hook introduction | ⭐⭐⭐ Advanced |
| [Sstore Hooks](tutorials/certora-sstore-hooks-storage-mappings.md) | Write interception | ⭐⭐⭐ Advanced |
| [Sload Hooks](tutorials/certora-sload-hooks-storage-mappings.md) | Read interception | ⭐⭐⭐ Advanced |
| [Persistent Ghosts](tutorials/certora-persistent-ghosts.md) | Non-havocing ghosts + CALL hook | ⭐⭐⭐ Advanced |
| [Constraining Ghosts in Rules](tutorials/certora-constraining-ghost-values-in-rules.md) | Ghost validation patterns | ⭐⭐⭐ Advanced |
| [Constraining Ghosts in Invariants](tutorials/certora-constraining-ghosts-in-invariants.md) | Invariant ghost patterns | ⭐⭐⭐ Advanced |
| [Account Balances](tutorials/certora-account-balances.md) | nativeBalances, ETH tracking | ⭐⭐⭐ Advanced |

#### Advanced — Invariants
| Tutorial | Topics Covered | Difficulty |
|----------|----------------|------------|
| [Invariants Deep Dive](tutorials/certora-invariants.md) | Inductive proofs, preserved blocks | ⭐⭐⭐ Advanced |
| [requireInvariant](tutorials/certora-requireinvariant.md) | Using invariants in rules | ⭐⭐⭐ Advanced |
| [Preserved Block](tutorials/certora-preserved-block.md) | Invariant preservation | ⭐⭐⭐ Advanced |
| [Verifying with Ghost Hook](tutorials/certora-verifying-invariant-using-ghost-hook.md) | Ghost-based invariants | ⭐⭐⭐ Advanced |

#### Production Examples
| Tutorial | Project | Difficulty |
|----------|---------|------------|
| [ERC-20 Complete](tutorials/certora-formally-verify-erc-20-token.md) | Full ERC-20 verification (22 rules) | ⭐⭐⭐ Advanced |
| [WETH (Solady)](tutorials/certora-formally-verify-solady-weth.md) | Solvency invariants, persistent ghosts | ⭐⭐⭐⭐ Expert |
| [ERC-721 Invariants](tutorials/certora-invariants-erc-721.md) | NFT invariants | ⭐⭐⭐ Advanced |
| [ERC-721 Mint/Burn](tutorials/certora-mint-burn-erc-721.md) | Mint/burn rules | ⭐⭐⭐ Advanced |
| [ERC-721 Transfer/Approval](tutorials/certora-transfer-and-approval-rules-erc-721.md) | Transfer rules, DISPATCHER | ⭐⭐⭐ Advanced |
| [ERC-721 SafeMint/SafeTransfer](tutorials/certora-safemint-and-safetransfer-erc-721.md) | Callback handling | ⭐⭐⭐⭐ Expert |
| [ERC-721 Parametric](tutorials/certora-partially-parametric-rules-erc-721.md) | Parametric rule patterns | ⭐⭐⭐ Advanced |

#### OpenZeppelin Contracts
| Tutorial | Contract | Difficulty |
|----------|----------|------------|
| [Ownable.sol](tutorials/certora-verify-ownablesol.md) | Access control verification | ⭐⭐ Intermediate |
| [Initializable.sol](tutorials/certora-verify-initializablesol.md) | Upgrade pattern verification | ⭐⭐⭐ Advanced |
| [Nonces.sol](tutorials/certora-verify-noncessol-openzeppelin.md) | Nonce verification | ⭐⭐ Intermediate |

#### Multi-Contract & Specifications
| Tutorial | Topics | Difficulty |
|----------|--------|------------|
| [Multi-Contract Tutorial](tutorials/multi-contract-tutorial.md) | Working with multiple contracts | ⭐⭐⭐ Advanced |
| [Specification Patterns](tutorials/certora-specification.md) | Organizing large specs | ⭐⭐⭐ Advanced |
| [Method Properties](tutorials/certora-method-properties.md) | Property categorization | ⭐⭐ Intermediate |

---

### Guides & Patterns

How-to guides, design patterns, and troubleshooting.

#### Verification Patterns
| Guide | Use When |
|-------|----------|
| [Tracking Sums Pattern](guides/tracking-sums-pattern.md) | Sum of balances = total supply |
| [Require Invariants Pattern](guides/require-invariants-pattern.md) | Using invariants in rules |
| [Safe Assumptions Pattern](guides/safe-assumptions-pattern.md) | When to use require |
| [Positive Examples Pattern](guides/positive-examples-pattern.md) | Using satisfy statements |

#### Specification Design
| Guide | Use When |
|-------|----------|
| [Designing Specifications](guides/designing-specifications-guide.md) | Planning verification |
| [Using Opcode Hooks](guides/using-opcode-hooks-guide.md) | Low-level hooks |

#### Troubleshooting
| Guide | Problem |
|-------|---------|
| [Timeout Troubleshooting](guides/timeout-troubleshooting-guide.md) | Prover timeouts |
| [Understanding EVM Gaps](guides/understanding-evm-gaps-guide.md) | High vs low-level code |
| [Coverage Info](guides/coverage-info-guide.md) | Understanding coverage reports |

#### Migration
| Guide | Version |
|-------|---------|
| [CVL2 Migration Guide](guides/cvl2-migration-guide.md) | CVL 1.x → CVL 2.0 |

---

## Learning Pathways

Curated learning sequences by topic.

### Pathway 1: Complete Beginner → ERC-20 Verification

**Goal:** Verify your first ERC-20 token (8-10 hours)

1. **Start:** [Formal Verification Introduction](tutorials/certora-formal-verification-intro.md) (30 min)
2. **First Spec:** [Verify a Counter](tutorials/certora-verify-counter.md) (1 hour)
3. **Core Statements:** [require, assert, satisfy](tutorials/certora-require-assert-and-satisfy.md) (1 hour)
4. **Logical Operators:** [Implication](tutorials/certora-implication.md) (30 min)
5. **Types:** [mathint & Overflow](tutorials/certora-overflow-and-mathint.md) (1 hour)
6. **Environment:** [msg.sender & msg.value](tutorials/certora-msgsender-msgvalue.md) (45 min)
7. **Parametric Rules:** [Parametric Rules](tutorials/certora-parametric-rules.md) (1 hour)
8. **Production Example:** [ERC-20 Complete](tutorials/certora-formally-verify-erc-20-token.md) (3-4 hours)

**Reference alongside:** [CVL Basic Syntax](reference/basic-syntax.md), [Rules](reference/rules.md)

---

### Pathway 2: Master Ghosts & Hooks

**Goal:** Track custom state with ghosts and hooks (6-8 hours)

**Prerequisites:** Complete Pathway 1 or equivalent

1. **Introduction:** [Storage Hooks & Ghosts](tutorials/certora-storage-hooks-and-ghosts.md) (2 hours)
2. **Write Tracking:** [Sstore Hooks](tutorials/certora-sstore-hooks-storage-mappings.md) (1 hour)
3. **Read Tracking:** [Sload Hooks](tutorials/certora-sload-hooks-storage-mappings.md) (1 hour)
4. **Pattern:** [Tracking Sums Pattern](guides/tracking-sums-pattern.md) (45 min)
5. **Advanced:** [Persistent Ghosts](tutorials/certora-persistent-ghosts.md) (1.5 hours)
6. **Production:** [WETH Verification](tutorials/certora-formally-verify-solady-weth.md) (2-3 hours)

**Reference alongside:** [Ghosts](reference/ghosts.md), [Hooks](reference/hooks.md)

---

### Pathway 3: Master Invariants

**Goal:** Write and prove inductive invariants (5-7 hours)

**Prerequisites:** Complete Pathway 1

1. **Fundamentals:** [Invariants Deep Dive](tutorials/certora-invariants.md) (2 hours)
2. **Preservation:** [Preserved Block](tutorials/certora-preserved-block.md) (1 hour)
3. **Using Invariants:** [requireInvariant](tutorials/certora-requireinvariant.md) (1 hour)
4. **With Ghosts:** [Verifying with Ghost Hook](tutorials/certora-verifying-invariant-using-ghost-hook.md) (1.5 hours)
5. **Production:** [ERC-721 Invariants](tutorials/certora-invariants-erc-721.md) (1.5-2 hours)

**Reference alongside:** [Invariants](reference/invariants.md)

---

### Pathway 4: ERC-721 Complete Verification

**Goal:** Fully verify an ERC-721 NFT contract (10-12 hours)

**Prerequisites:** Pathways 1, 2, and 3

1. [ERC-721 Invariants](tutorials/certora-invariants-erc-721.md) (1.5 hours)
2. [ERC-721 Mint/Burn](tutorials/certora-mint-burn-erc-721.md) (2 hours)
3. [ERC-721 Transfer/Approval](tutorials/certora-transfer-and-approval-rules-erc-721.md) (2.5 hours)
4. [ERC-721 SafeMint/SafeTransfer](tutorials/certora-safemint-and-safetransfer-erc-721.md) (3 hours)
5. [ERC-721 Parametric](tutorials/certora-partially-parametric-rules-erc-721.md) (2 hours)

**Reference alongside:** [Methods Block](reference/methods-block.md), [Method Summarization](reference/method-summarization.md)

---

### Pathway 5: Production Verification Skills

**Goal:** Real-world verification techniques (8-10 hours)

**Prerequisites:** All previous pathways

1. **Multi-Contract:** [Multi-Contract Tutorial](tutorials/multi-contract-tutorial.md) (2 hours)
2. **Organization:** [Specification Patterns](tutorials/certora-specification.md) (1 hour)
3. **Timeouts:** [Timeout Troubleshooting](guides/timeout-troubleshooting-guide.md) (1 hour)
4. **Upgradeable:** [Initializable.sol](tutorials/certora-verify-initializablesol.md) (2 hours)
5. **Advanced Storage:** [EIP-7201](reference/eip-7201.md) + [Storage Layout](reference/storage-layout.md) (2 hours)
6. **Expert Example:** [WETH Verification](tutorials/certora-formally-verify-solady-weth.md) (3 hours)

---

## Cross-References to Certora-Fv-Framework

This documentation integrates with the **Certora Formal Verification Framework** located at `/home/brett/dual-governance/Certora-Fv-Framework`:

### Complementary Resources

| Framework Document | CVLDocs Equivalent | Use Case |
|--------------------|-------------------|----------|
| **CVL_LANGUAGE_DEEP_DIVE.md** | [Reference Documentation](#reference-documentation) | Language mastery — Framework doc for quick lookup, CVLDocs for exhaustive syntax |
| **VERIFICATION_PLAYBOOKS.md** | [Production Examples](#production-examples) | Worked examples — Framework has complete specs, CVLDocs has step-by-step tutorials |
| **CERTORA_SPEC_FRAMEWORK.md** | [Reference → Rules](#rules-invariants) | CVL templates — Framework for patterns, CVLDocs for syntax |
| **BEST_PRACTICES_FROM_CERTORA.md** | [Guides & Patterns](#guides-patterns) | Verification patterns — Framework for methodology, CVLDocs for implementation |
| **CERTORA_MASTER_GUIDE.md** | [Learning Pathways](#learning-pathways) | Verification workflow — Framework for process, CVLDocs for technique |

### When to Use Which

- **Start with Framework** if you're verifying a complete project (methodology, workflow, property discovery)
- **Use CVLDocs** for:
  - Deep CVL syntax questions
  - Step-by-step learning tutorials
  - Specific technical reference (e.g., "How does DISPATCHER work?")
  - OpenZeppelin contract examples

---

## Contributing & Updates

**Repository:** This is part of the Certora knowledge ecosystem  
**Framework Repository:** https://github.com/fjor1025/Certora-Fv-Framework.git  
**Last Updated:** February 8, 2026  
**Version:** 2.0 (Complete reorganization)

**Sources:**
- Official Certora documentation
- RareSkills Certora Book (35 chapters)
- Community best practices

---

## Quick Reference Tables

### Common Tasks

| I Want To... | Read This |
|--------------|-----------|
| Write my first spec | [Verify a Counter](tutorials/certora-verify-counter.md) |
| Track sum of balances | [Tracking Sums Pattern](guides/tracking-sums-pattern.md) + [Sstore Hooks](tutorials/certora-sstore-hooks-storage-mappings.md) |
| Handle external calls | [Method Summarization](reference/method-summarization.md) |
| Fix timeouts | [Timeout Troubleshooting](guides/timeout-troubleshooting-guide.md) |
| Verify ERC-20 | [ERC-20 Complete](tutorials/certora-formally-verify-erc-20-token.md) |
| Verify ERC-721 | [ERC-721 Pathway](#pathway-4-erc-721-complete-verification) |
| Use parametric rules | [Parametric Rules](tutorials/certora-parametric-rules.md) |
| Write invariants | [Invariants Deep Dive](tutorials/certora-invariants.md) |
| Model native ETH | [Persistent Ghosts](tutorials/certora-persistent-ghosts.md) + [Account Balances](tutorials/certora-account-balances.md) |
| Migrate to CVL2 | [CVL2 Migration Guide](guides/cvl2-migration-guide.md) |

### Syntax Quick Lookup

| CVL Feature | Reference Doc | Tutorial |
|-------------|---------------|----------|
| `ghost` | [Ghosts](reference/ghosts.md) | [Storage Hooks & Ghosts](tutorials/certora-storage-hooks-and-ghosts.md) |
| `hook Sstore` | [Hooks](reference/hooks.md) | [Sstore Hooks](tutorials/certora-sstore-hooks-storage-mappings.md) |
| `invariant` | [Invariants](reference/invariants.md) | [Invariants Deep Dive](tutorials/certora-invariants.md) |
| `rule` | [Rules](reference/rules.md) | [Verify a Counter](tutorials/certora-verify-counter.md) |
| `methods {}` | [Methods Block](reference/methods-block.md) | [ERC-20 Complete](tutorials/certora-formally-verify-erc-20-token.md) |
| `require` / `assert` | [Statements](reference/statements.md) | [require, assert, satisfy](tutorials/certora-require-assert-and-satisfy.md) |
| `satisfy` | [Statements](reference/statements.md) | [Positive Examples Pattern](guides/positive-examples-pattern.md) |
| `=>` (implication) | [Expressions](reference/expressions.md) | [Implication](tutorials/certora-implication.md) |
| `mathint` | [Types](reference/types.md) | [mathint & Overflow](tutorials/certora-overflow-and-mathint.md) |
| `@withrevert` | [Functions](reference/functions.md) | [Testing Reverts](tutorials/certora-testing-revert-call.md) |

---

**Ready to start?** → [Formal Verification Introduction](tutorials/certora-formal-verification-intro.md)  
**Have questions?** → Check [Certora Glossary](reference/certora-glossary.md)  
**Need methodology?** → See [Certora-Fv-Framework](https://github.com/fjor1025/Certora-Fv-Framework.git)
