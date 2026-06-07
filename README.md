# Unified Symbol System (USS) for All Sciences

**A machine-first symbolic language for encoding the foundational equations of mathematics and physics.**

[![Version](https://img.shields.io/badge/version-1.4-blue)](./USS_Project_Report_Enhanced_v1.4.md)
[![Status](https://img.shields.io/badge/status-research%20proposal-orange)](./)
[![Grammar](https://img.shields.io/badge/grammar-EBNF-green)](./USS_Project_Report_Enhanced_v1.4.md#511-formal-grammar-specification)

---

## What is USS?

The Unified Symbol System (USS) is a rigorous, machine-parseable symbolic language designed to eliminate the ambiguity that plagues traditional mathematical and scientific notation. Every concept, constant, variable, and operator is assigned exactly one unique token — making equations readable by machines, searchable in databases, and translatable across scientific branches without context-dependent disambiguation.

### Key Principles

- **Machine-First**: Humans can tolerate ambiguity. Machines cannot.
- **Branch-Aware**: Every token carries its scientific origin (Math, Physics, Chemistry, Biology, etc.)
- **Strict 4-Letter Enforcement**: Exactly four letters must exist between the enclosing underscores (e.g., `_MCPI_`).
- **Mnemonic Mapping**: Uppercase tokens map to names/phonetics (`_MCHB_` for ℏ); lowercase tokens map the final letter to the traditional variable (`_mvrx_` for x).
- **Explicit Prohibitions**: No overloading (same symbol, multiple meanings), no font decorations, and no subscript disambiguation.
- **Diacritical Replacement**: Font decorations (hats, vectors, bars) are replaced by modifier operator tokens (`_MVEC_`, `_MHAT_`, `_MDOT_`, `_MBAR_`).
- **SQL-Native**: Designed for database storage, dependency linking, and automated querying
- **Grammar-Defined**: Formal EBNF specification ensures deterministic parsing

### Token Format

```
_MXXX_  → Math constant/operator (e.g., _MCPI_ = π, _MCHB_ = ℏ, _MSIN_ = sine, _MMNS_ = minus)
_mxxx_  → Math variable/index    (e.g., _mvrx_ = x, _mvrm_ = mass m, _midi_ = index i)
_PXXX_  → Physics constant/operator (e.g., _POHM_ = Hamiltonian)
_pxxx_  → Physics variable       (e.g., _pvrp_ = Psi, _pvrt_ = time t)
_UXXX_  → Unit                   (e.g., _ULEN_ = meter)
_TXXX_  → Type                   (e.g., _TVEC_ = Vector, _TMAT_ = Matrix)
```

### Enumeration & Decorations
Since subscripts and font decorations are prohibited, USS uses bracket syntax for enumeration and modifier tokens for diacritics:
- $x_1 \rightarrow$ `_mvrx_[1]`
- $A_{i,j} \rightarrow$ `_mvra_[_midi_, _midj_]`
- $\vec{F} \rightarrow$ `_MVEC_(_pvrf_)`
- $\dot{x} \rightarrow$ `_MDOT_(_mvrx_)`

---

## Repository Contents

| File | Description |
|------|-------------|
| [`USS_Project_Report_Enhanced_v1.4.md`](./USS_Project_Report_Enhanced_v1.4.md) | **Full project report** — specification, grammar, schema, roadmap, and pilot examples |
| [`README.md`](./README.md) | This file |
| [`LICENSE`](./LICENSE) | Intellectual property and usage terms |

---

## Quick Start: Pilot Examples

### Quadratic Formula
```
_mvrx_ = ( _MMNS_ _mvrb_ _MPMN_ _MSQT_(_mvrb_ ^ 2 _MMNS_ 4 * _mvra_ * _mvrc_) ) / ( 2 * _mvra_ )
; _mvra_ != 0
```

### Newton's Second Law
```
_MVEC_(_pvrf_) = _mvrm_ * _MVEC_(_pvra_)
; _mvrm_ > 0
```

### Schrödinger Equation
```
_MCIM_ * _MCHB_ * _MDER_(_pvrp_(_MVEC_(_pvrr_), _pvrt_), _pvrt_) = _POHM_(_pvrp_(_MVEC_(_pvrr_), _pvrt_))
```

See the full report for complete database schema, 1,000-equation scope breakdown, and 12-month implementation roadmap.

---

## Project Status

This repository contains the **research proposal and specification** for USS v1.4. The project is currently in the **specification phase**.

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

*"The underlying idea of a unified scientific notation is not new — Leibniz dreamed of it centuries ago. But the specific engineering choices—strictly enforced 4-letter underscore-delimited tokens, branch-prefix namespace, case-based taxonomy, explicit overloading prohibitions, diacritical operator replacement, formal EBNF grammar, SQL-native storage—constitute a novel implementation."*
