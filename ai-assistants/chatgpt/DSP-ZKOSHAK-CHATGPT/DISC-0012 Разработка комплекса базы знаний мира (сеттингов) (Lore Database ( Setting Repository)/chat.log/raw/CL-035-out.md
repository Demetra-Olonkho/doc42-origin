2026-06-10 2029

https://chatgpt.com/s/t_6a2d7a5060e4819191a4697e7e0c4771

Да, на текущем этапе русскоязычный DEM-0001 выглядит завершённым. В процессе дальнейшей работы в него почти наверняка будут вноситься дополнения (особенно разделы о резерве имён и правилах именования подсистем), но его базовая часть уже сформирована.

Соответственно, ниже привожу англоязычную версию для размещения в:

```text
docs/
└── 2_en/
    └── architecture/
        └── DEM-0001-terminology-and-symbolic-architecture.md
```

# DEM-0001 — Terminology and Symbolic Architecture

Version: 1.0

Status: Accepted

Adoption Date: TBD

---

# 1. Purpose

This document defines the terminology, symbolic architecture and naming principles of the Demetra Olonkho project.

Its purpose is to ensure consistency in naming, preserve the conceptual integrity of the architecture and document the cultural and symbolic foundations of the project's nomenclature.

This document is one of the foundational documents of the project.

---

# 2. General Principles

The project employs a meaningful naming system.

Names are not treated merely as technical identifiers but as elements of the architectural language of the system.

Names should help communicate the purpose of a component and reflect its role within the overall structure of the project.

---

# 3. Principle of Semantic Naming

When selecting names, preference shall be given to names with intrinsic semantic meaning.

Preferred sources include:

- historical figures;

- mythological characters;

- cultural traditions;

- literary heritage;

- folklore.

A name should reflect the purpose of a component rather than implementation details.

Preferred decision sequence:

```
Meaning
    ↓
Purpose
    ↓
Name
```

Purely technical names should be avoided whenever a meaningful alternative exists.

---

# 4. Symbolic Architecture of the Project

## 4.1. Demetra

Name:

```
Demetra
```

Status:

```
Platform name.
```

Symbolic meaning:

- preservation of knowledge;

- development of knowledge;

- dissemination of knowledge;

- accessibility of knowledge;

- continuity of knowledge.

Demetra is the name of the platform as a whole.

---

## 4.2. Olonkho

Name:

```
Olonkho
```

Status:

```
Knowledge model name.
```

Provisional technical designation:

```
Olonkho Knowledge Model
```

Symbolic meaning:

- living tradition;

- transmission of knowledge;

- provenance of knowledge;

- historical memory;

- continuity between generations.

Olonkho defines the conceptual model used to represent knowledge within the platform.

---

## 4.3. Irida

Name:

```
Irida
```

Status:

```
Exchange layer name.
```

Provisional technical designation:

```
Irida Exchange Layer
```

Symbolic meaning:

- information transfer;

- mediation;

- interconnection;

- communication.

Irida is intended to facilitate interaction between the platform and external systems.

---

## 4.4. Irina

Name:

```
Irina
```

Status:

```
Reconciliation subsystem name.
```

Provisional technical designation:

```
Irina Reconciliation Engine
```

Symbolic meaning:

- peacemaking;

- reconciliation;

- coexistence;

- conflict resolution;

- preservation of harmony.

Irina is intended to manage conflicting knowledge, competing interpretations and multiple canon variants.

---

# 5. Naming Reserve

The project may maintain a reserve pool of names for future components.

The presence of a name in the reserve does not imply that a corresponding component will necessarily be created.

---

## 5.1. Primary Reserve

Names with a direct semantic relationship to the existing symbolic architecture.

Current list:

- Iris;

- Eirene.

---

## 5.2. Secondary Reserve

Names considered potentially suitable for future use.

The list remains open.

---

# 6. Cultural Naming Policy

The project is not tied to any single cultural tradition.

Names and symbolic references may be drawn from a broad range of cultural sources.

Preference is given to:

- cultural diversity;

- respectful use of source traditions;

- preservation of the original meaning of names.

The naming system should contribute to cultural awareness and intellectual curiosity among project participants.

---

# 7. Principle of Internal Consistency

New names should remain compatible with the established symbolic architecture.

Ideally, a new name should:

- possess independent meaning;

- reflect the purpose of the component;

- remain consistent with existing symbolism;

- be suitable for international use.

---

# 8. Name Documentation Rules

In English-language documentation, official English forms of names shall be used.

Examples:

```
Demetra
Olonkho
Irida
Irina
```

Where appropriate, documentation may reference the symbolic meaning of a name and its role within the overall architecture.

---

# 9. Related Documents

This document is related to:

- DEM-0000 — Project Identity and Foundational Decisions;

- DEM-0002 — Language Policy;

- DEM-0003 — Documentation Policy.

---

# 10. Status

At the time of adoption, the following are considered defined:

- project naming principles;

- symbolic architecture;

- foundational nomenclature;

- naming expansion rules;

- documentation rules for symbolic names.

Future development of project terminology should take this document into account.

End of document.

Я бы также предложил небольшое улучшение перед переходом к DEM-0002 и DEM-0003.

Сейчас в разделе 5 у нас фигурирует термин:

```text
Резерв именования
Naming Reserve
```

Но для проекта, связанного с управлением знаниями, мне кажется более удачным и красивым термин:

```text
Реестр имён
Registry of Names
```

или даже:

```text
Символический реестр
Symbolic Registry
```

Потому что "резерв" подразумевает пассивное хранение, а "реестр" уже становится частью архитектуры проекта и может впоследствии превратиться в вполне реальный документ вроде:

```text
DEM-NAM-0001
Project Symbolic Registry
```

где будут учитываться все используемые, зарезервированные и выведенные из употребления имена проекта. И, учитывая характер Demetra Olonkho, такой документ выглядит вполне естественным.
