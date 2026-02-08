## CVLDocs — The Definitive Certora Knowledge Base

> **Complete documentation for Certora Prover and CVL (Certora Verification Language)**  
> Combining official Certora reference precision with RareSkills pedagogical excellence  
> **Version 2.0** — Reorganized February 8, 2026

---

## What Is This?

CVLDocs is the most comprehensive resource for learning and using the Certora Prover. It combines:

- **Official Certora Documentation** — Technical specifications, syntax references, EBNF grammars
- **RareSkills Certora Book** — 34 step-by-step tutorials with worked examples
- **Community Best Practices** — Design patterns, troubleshooting guides, production techniques

**83 markdown files** organized into:
- **29 Reference Docs** — Authoritative syntax and technical specs
- **41 Tutorials** — Hands-on learning from beginner to expert
- **11 Guides & Patterns** — How-to guides, design patterns, troubleshooting

---

## Quick Start

👉 **[Start Here: Complete INDEX.md](INDEX.md)**

The INDEX.md provides:
- Complete document catalog
- Learning pathways by topic
- Quick reference tables
- Cross-references to Certora-Fv-Framework

### First-Time Users

1. Read [Formal Verification Introduction](tutorials/certora-formal-verification-intro.md) (30 min)
2. Complete [Verify a Counter](tutorials/certora-verify-counter.md) (1 hour)
3. Follow [Learning Pathway 1](INDEX.md#pathway-1-complete-beginner--erc-20-verification) (8-10 hours)

### Experienced Users

- **Need syntax?** → [Reference Documentation](INDEX.md#reference-documentation)
- **Want examples?** → [Tutorials](INDEX.md#tutorials)
- **Solving problems?** → [Guides & Patterns](INDEX.md#guides-patterns)
- **Specific task?** → [Quick Reference Tables](INDEX.md#quick-reference-tables)

---

## Organization

```
CVLDocs/
├── INDEX.md                          ← START HERE (complete navigation)
├── README.md                         ← This file
│
├── reference/                        ← 29 technical specifications
│   ├── basic-syntax.md
│   ├── types.md
│   ├── ghosts.md
│   ├── hooks.md
│   ├── rules.md
│   ├── invariants.md
│   ├── methods-block.md
│   ├── cli-options.md
│   └── ... (21 more)
│
├── tutorials/                        ← 41 step-by-step tutorials
│   ├── certora-formal-verification-intro.md
│   ├── certora-verify-counter.md
│   ├── certora-storage-hooks-and-ghosts.md
│   ├── certora-formally-verify-erc-20-token.md
│   ├── certora-formally-verify-solady-weth.md
│   └── ... (36 more)
│
└── guides/                           ← 11 how-to guides & patterns
    ├── tracking-sums-pattern.md
    ├── timeout-troubleshooting-guide.md
    ├── cvl2-migration-guide.md
    └── ... (8 more)
```

---

## Learning Pathways

Curated sequences for different goals:

### 1. Complete Beginner → ERC-20 Verification (8-10 hours)
Master the fundamentals and verify your first token contract.  
**[View Full Pathway](INDEX.md#pathway-1-complete-beginner--erc-20-verification)**

### 2. Master Ghosts & Hooks (6-8 hours)
Learn to track custom state with ghosts and storage hooks.  
**[View Full Pathway](INDEX.md#pathway-2-master-ghosts--hooks)**

### 3. Master Invariants (5-7 hours)
Write and prove inductive invariants.  
**[View Full Pathway](INDEX.md#pathway-3-master-invariants)**

### 4. ERC-721 Complete Verification (10-12 hours)
Fully verify an NFT contract with all edge cases.  
**[View Full Pathway](INDEX.md#pathway-4-erc-721-complete-verification)**

### 5. Production Verification Skills (8-10 hours)
Real-world techniques for professional verification.  
**[View Full Pathway](INDEX.md#pathway-5-production-verification-skills)**

---

## Integration with Certora-Fv-Framework

CVLDocs complements the **Certora Formal Verification Framework** at:  
https://github.com/fjor1025/Certora-Fv-Framework.git

### When to Use Each

**Use Framework for:**
- Complete verification workflow (Phase 0 through Phase 11)
- Property discovery methodology
- Counterexample diagnosis
- Project-level verification strategy

**Use CVLDocs for:**
- CVL syntax deep dive
- Step-by-step learning tutorials
- Specific technical questions
- Production examples (ERC-20, WETH, ERC-721, OpenZeppelin)

**Best Practice:** Start with Framework for methodology, reference CVLDocs for technique.

---

## Quick Reference

### Common Tasks

| I Want To... | Read This |
|--------------|-----------|
| Write my first spec | [Verify a Counter](tutorials/certora-verify-counter.md) |
| Track sum of balances | [Tracking Sums Pattern](guides/tracking-sums-pattern.md) |
| Handle external calls | [Method Summarization](reference/method-summarization.md) |
| Fix timeouts | [Timeout Troubleshooting](guides/timeout-troubleshooting-guide.md) |
| Verify ERC-20 | [ERC-20 Complete](tutorials/certora-formally-verify-erc-20-token.md) |
| Verify ERC-721 | [ERC-721 Pathway](INDEX.md#pathway-4-erc-721-complete-verification) |
| Write invariants | [Invariants Tutorial](tutorials/certora-invariants.md) |
| Use ghosts | [Storage Hooks & Ghosts](tutorials/certora-storage-hooks-and-ghosts.md) |
| Model native ETH | [Persistent Ghosts](tutorials/certora-persistent-ghosts.md) |

### CVL Syntax Lookup

| Feature | Reference | Tutorial |
|---------|-----------|----------|
| `ghost` | [Ghosts](reference/ghosts.md) | [Storage Hooks & Ghosts](tutorials/certora-storage-hooks-and-ghosts.md) |
| `hook Sstore` | [Hooks](reference/hooks.md) | [Sstore Hooks](tutorials/certora-sstore-hooks-storage-mappings.md) |
| `invariant` | [Invariants](reference/invariants.md) | [Invariants Tutorial](tutorials/certora-invariants.md) |
| `rule` | [Rules](reference/rules.md) | [Verify Counter](tutorials/certora-verify-counter.md) |
| `methods {}` | [Methods Block](reference/methods-block.md) | [ERC-20 Complete](tutorials/certora-formally-verify-erc-20-token.md) |

**[See complete syntax table in INDEX.md](INDEX.md#syntax-quick-lookup)**

---

## What's New in Version 2.0

### Complete Reorganization (February 8, 2026)

**Before:** 67 files with inconsistent naming, duplicates, no organization  
**After:** 83 files (removed 25 duplicates, added 34 RareSkills tutorials, added 7 new docs)

**Improvements:**
- ✅ Consistent naming convention (lowercase-with-dashes)
- ✅ Logical folder structure (reference/tutorials/guides)
- ✅ Comprehensive INDEX.md with learning pathways
- ✅ Removed 25 duplicate files
- ✅ Added 34 RareSkills tutorials
- ✅ Cross-references to Certora-Fv-Framework
- ✅ Quick reference tables for common tasks
- ✅ Curated learning pathways by topic

---

## Sources

This knowledge base combines content from:

1. **Official Certora Documentation**  
   Technical specifications and authoritative references

2. **RareSkills Certora Book** (35 chapters, 60,000+ words)  
   https://github.com/RareSkills/certora-book  
   Pedagogical tutorials with worked examples

3. **Certora Community**  
   Best practices, patterns, troubleshooting guides

---

## Contributing

CVLDocs is part of the Certora knowledge ecosystem:

- **Framework Repository:** https://github.com/fjor1025/Certora-Fv-Framework.git  
- **Maintained By:** Brett (@fjor1025)  
- **Version:** 2.0 (February 8, 2026)

---

## Support

**Questions?**
1. Check [INDEX.md](INDEX.md) for navigation
2. Use [Quick Reference Tables](INDEX.md#quick-reference-tables)
3. Check [Certora Glossary](reference/certora-glossary.md)

**Need methodology?**
- See [Certora-Fv-Framework](https://github.com/fjor1025/Certora-Fv-Framework.git)

**Ready to start?**
- 👉 **[Go to INDEX.md](INDEX.md)**
