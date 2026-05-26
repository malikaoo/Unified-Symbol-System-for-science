# Unified Symbol System (USS) for All Sciences

**A machine-first symbolic language for encoding the foundational equations of mathematics and physics.**

[![Version](https://img.shields.io/badge/version-1.1-blue)](./USS_Project_Report_Enhanced_v1.1.md)
[![Status](https://img.shields.io/badge/status-research%20proposal-orange)](./)
[![Grammar](https://img.shields.io/badge/grammar-EBNF-green)](./USS_Project_Report_Enhanced_v1.1.md#55-formal-grammar-specification)

---

## What is USS?

The Unified Symbol System (USS) is a rigorous, machine-parseable symbolic language designed to eliminate the ambiguity that plagues traditional mathematical and scientific notation. Every concept, constant, variable, and operator is assigned exactly one unique token — making equations readable by machines, searchable in databases, and translatable across scientific branches without context-dependent disambiguation.

### Key Principles

- **Machine-First**: Humans can tolerate ambiguity. Machines cannot.
- **Branch-Aware**: Every token carries its scientific origin (Math, Physics, Chemistry, Biology, etc.)
- **Unambiguous**: Four-letter underscore-delimited tokens with strict case-based taxonomy
- **SQL-Native**: Designed for database storage, dependency linking, and automated querying
- **Grammar-Defined**: Formal EBNF specification ensures deterministic parsing

### Token Format

```
_MXXX_  → Math constant/term     (e.g., _MPI_ = π)
_mxxx_  → Math variable          (e.g., _mvar_ = generic variable)
_PXXX_  → Physics constant/term    (e.g., _MBOL_ = Boltzmann constant)
_pxxx_  → Physics variable       (e.g., _pvel_ = velocity)
_UXXX_  → Unit                   (e.g., _ULEN_ = meter)
```

---

## Repository Contents

| File | Description |
|------|-------------|
| [`USS_Project_Report_Enhanced_v1.1.md`](./USS_Project_Report_Enhanced_v1.1.md) | **Full project report** — specification, grammar, schema, roadmap, and pilot examples |
| [`README.md`](./README.md) | This file |
| [`LICENSE`](./LICENSE) | Intellectual property and usage terms |

---

## Quick Start: Pilot Examples

### Quadratic Formula
```
_mvar_ = (_mvar_b_ * _MMNS_ + _MSQT_(_mvar_b_ ^ 2 _MMNS_ 4 * _mvar_a_ * _mvar_c_)) / (2 * _mvar_a_)
```

### Newton's Second Law
```
_vec_F_ = _mvar_m_ * _vec_a_
```

### Schrödinger Equation
```
_MIMG_ * _MBOL_ * _MDER_(_mpsi_, _UTIM_) = _MHAM_ * _mpsi_
```

See the full report for complete database schema, 1,000-equation scope breakdown, and 12-month implementation roadmap.

---

## Project Status

This repository contains the **research proposal and specification** for USS v1.1. The project is currently in the **specification phase**.

### Roadmap

| Phase | Timeline | Status |
|-------|----------|--------|
| Symbol Registry Lock & EBNF Grammar | Months 1–2 | 🔵 Planned |
| Core Equation Harvesting (100 pilot) | Months 3–4 | 🔵 Planned |
| Translation Pipeline & Verification | Months 5–6 | ⚪ Future |
| Dependency Graph & Proof Engine | Months 7–8 | ⚪ Future |
| Cross-Branch Expansion | Months 9–10 | ⚪ Future |
| Public API & Query Interface | Months 11–12 | ⚪ Future |

---

## Intellectual Property

The USS specification, symbol registry, database schema, and implementation are original work by **Tarek Mohammed Nasser**.

- **Specification** (grammar, encoding rules, EBNF definition): Available for academic reference
- **Database & Registry**: Proprietary — usage requires explicit permission
- **Commercial use**: Licensed separately

See [`LICENSE`](./LICENSE) for full terms.

---

## Contact

**Author:** Tarek Mohammed Nasser  
**Email:** malikao@gmail.com

For collaboration inquiries, academic references, or licensing discussions, please open an issue or contact directly.

---

*"The underlying idea of a unified scientific notation is not new — Leibniz dreamed of it centuries ago. But the specific engineering choices constitute a novel implementation."*
