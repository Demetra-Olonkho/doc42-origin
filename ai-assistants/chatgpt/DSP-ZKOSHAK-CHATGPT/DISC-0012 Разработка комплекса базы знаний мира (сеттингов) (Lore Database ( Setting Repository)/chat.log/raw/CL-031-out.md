2026-06-10 1845

https://chatgpt.com/s/t_6a2cb66d2e948191bddb82f368eabb1d

Да, поместить обе версии в одном сообщении получится. Более того, это позволит сразу проверить согласованность терминологии между русской и английской версиями.

Я бы рекомендовал в репозитории хранить их всё равно раздельно:

```text
docs/
├── 1_ru/
│   └── architecture/
│       └── DEM-0000-project-identity.md
│
└── 2_en/
    └── architecture/
        └── DEM-0000-project-identity.md
```

Но для обсуждения и согласования можно публиковать их парами.

Ниже привожу русскую версию в редакции, учитывающей принятую языковую политику.

# DEM-0000 — Идентичность проекта и основополагающие решения

Версия: 1.0

Статус: Accepted

Дата принятия: TBD

---

# 1. Назначение документа

Настоящий документ фиксирует идентичность проекта Деметра Олонхо (Demetra Olonkho) и основные решения, принятые на этапе концептуального проектирования.

Цель документа — сохранить исходное видение проекта, его назначение, границы ответственности и ключевые принципы, которые должны учитываться при дальнейшем развитии архитектуры и реализации.

Данный документ относится к числу основополагающих документов проекта.

---

# 2. Наименование проекта

Полное наименование проекта:

```
Деметра Олонхо (Demetra Olonkho)
```

Краткое наименование проекта:

```
Деметра (Demetra)
```

Краткое наименование допускается использовать:

- в названиях репозиториев;

- в исходном коде;

- в документации;

- в пользовательских интерфейсах;

- в публичных упоминаниях проекта.

Полное наименование используется в официальной документации и при описании проекта в целом.

---

# 3. Видение проекта

Деметра Олонхо представляет собой универсальную платформу управления знаниями.

Проект предназначен для работы со структурированными знаниями в различных предметных областях, включая, но не ограничиваясь:

- художественными вселенными;

- литературными циклами;

- игровыми сеттингами;

- настольными ролевыми играми;

- энциклопедическими проектами;

- исследовательскими проектами;

- архивными и справочными системами.

Проект не ограничивается какой-либо одной областью применения.

---

# 4. Основная цель проекта

Основной целью проекта является создание открытой и расширяемой платформы для накопления, структурирования, анализа, сопровождения и распространения знаний.

Проект должен обеспечивать:

- долгосрочное хранение знаний;

- сохранение происхождения знаний;

- поддержку различных точек зрения;

- многоязычность;

- интеграцию с внешними системами;

- возможность дальнейшего расширения.

---

# 5. Архитектурное положение проекта

Деметра Олонхо является самостоятельным проектом.

Проект не является частью других систем.

Напротив, другие системы могут использовать Деметру Олонхо как источник знаний и сервисов.

Примеры таких систем:

- издательские конвейеры (Publishing Pipeline);

- виртуальные настольные игровые системы (Virtual Tabletop, VTT);

- wiki-платформы;

- документационные системы;

- исследовательские системы;

- внешние сервисы и приложения.

Деметра Олонхо рассматривается как независимый уровень управления знаниями.

---

# 6. Базовые принципы проекта

## 6.1. Знание важнее объекта

Система управляет не объектами как таковыми, а знаниями об объектах.

Для проекта первичны не:

- персонажи;

- места;

- организации;

- предметы;

а знания о них.

---

## 6.2. Происхождение знания имеет значение

Любое знание должно иметь возможность быть связано со своим происхождением.

Происхождение знания может включать:

- источник;

- автора;

- документ;

- публикацию;

- редакцию;

- свидетельство;

- иной носитель информации.

---

## 6.3. Сосуществование различных интерпретаций

Система не обязана принудительно устранять противоречия.

Различные версии знаний могут сосуществовать одновременно.

Задачей системы является сохранение и описание таких различий.

---

## 6.4. Многоязычность как фундаментальный принцип

Поддержка множества языков должна быть встроена в архитектуру проекта с самого начала.

Ни один язык не должен иметь привилегированного положения внутри модели знаний.

---

## 6.5. Расширяемость как обязательное требование

Архитектура проекта должна допускать:

- появление новых типов данных;

- появление новых предметных областей;

- появление новых способов хранения знаний;

- появление новых способов интеграции.

---

# 7. Открытость культурным традициям

Проект осознанно не привязывается к какой-либо одной культурной традиции.

При формировании терминологии, символики и внутренней номенклатуры допускается использование:

- исторических личностей;

- мифологических персонажей;

- культурных традиций различных народов;

- литературного наследия различных эпох.

Одной из целей проекта является уважительное отношение к культурному многообразию.

---

# 8. Целевая аудитория проекта

Проект ориентирован на широкий круг пользователей, включая:

- писателей;

- редакторов;

- издателей;

- исследователей;

- разработчиков игр;

- мастеров настольных ролевых игр;

- разработчиков программного обеспечения;

- архивистов;

- специалистов по управлению знаниями.

---

# 9. Стратегическое направление развития

Проект создаётся как универсальная платформа общего назначения.

Архитектурные решения должны приниматься исходя из возможности использования платформы за пределами первоначальных сценариев её применения.

Проект не должен зависеть от:

- конкретного сеттинга;

- конкретной игры;

- конкретного издательства;

- конкретного программного продукта.

---

# 10. Связанные документы

Настоящий документ связан со следующими документами:

- DEM-0001 — Терминологическая и символическая архитектура;

- DEM-0002 — Языковая политика проекта;

- DEM-0003 — Политика ведения документации.

---

# 11. Статус

На момент принятия настоящего документа считаются определёнными:

- идентичность проекта;

- назначение проекта;

- область применения проекта;

- положение проекта относительно внешних систем;

- базовые архитектурные принципы;

- стратегическое направление развития.

Дальнейшее развитие проекта должно учитывать положения настоящего документа.

Конец документа.

# DEM-0000 — Project Identity and Foundational Decisions

Version: 1.0

Status: Accepted

Adoption Date: TBD

---

# 1. Purpose

This document defines the identity of the Demetra Olonkho project and records the foundational decisions adopted during the conceptual design phase.

Its purpose is to preserve the original vision of the project, its scope, responsibilities and guiding principles that shall be considered during future architectural and implementation work.

This document is one of the foundational documents of the project.

---

# 2. Project Name

Full project name:

```
Demetra Olonkho
```

Short project name:

```
Demetra
```

The short name may be used:

- in repository names;

- in source code;

- in documentation;

- in user interfaces;

- in public references.

The full name should be used in official documentation and when referring to the project as a whole.

---

# 3. Project Vision

Demetra Olonkho is a universal knowledge management platform.

The project is intended for structured knowledge domains, including but not limited to:

- fictional universes;

- literary series;

- game settings;

- tabletop role-playing games;

- encyclopedic projects;

- research projects;

- archival and reference systems.

The project is not limited to any single application domain.

---

# 4. Primary Goal

The primary goal of the project is to create an open and extensible platform for collecting, structuring, analysing, maintaining and distributing knowledge.

The platform should provide:

- long-term knowledge preservation;

- provenance preservation;

- support for multiple viewpoints;

- multilingual capabilities;

- integration with external systems;

- future extensibility.

---

# 5. Architectural Position

Demetra Olonkho is an independent project.

It is not a component of any other system.

Instead, other systems may consume its knowledge and services.

Examples include:

- Publishing Pipelines;

- Virtual Tabletops (VTT);

- wiki platforms;

- documentation systems;

- research systems;

- external services and applications.

Demetra Olonkho is considered an independent knowledge management layer.

---

# 6. Core Principles

## 6.1. Knowledge Is More Important Than Objects

The system manages knowledge about entities rather than entities alone.

The primary concern is not:

- characters;

- locations;

- organizations;

- items;

but knowledge about them.

---

## 6.2. Provenance Matters

Every piece of knowledge should be traceable to its origin.

Knowledge provenance may include:

- sources;

- authors;

- documents;

- publications;

- editions;

- testimonies;

- other information carriers.

---

## 6.3. Coexistence of Interpretations

The system is not required to eliminate contradictions.

Different versions of knowledge may coexist.

The role of the platform is to preserve and describe such differences.

---

## 6.4. Multilingualism as a Foundational Principle

Multilingual support shall be built into the architecture from the beginning.

No language shall have a privileged position within the knowledge model.

---

## 6.5. Extensibility as a Requirement

The architecture shall support:

- new data types;

- new domains;

- new storage mechanisms;

- new integration methods.

---

# 7. Cultural Openness

The project is intentionally not tied to any single cultural tradition.

Terminology, symbolism and internal nomenclature may draw inspiration from:

- historical figures;

- mythological characters;

- cultural traditions;

- literary heritage.

One of the goals of the project is to maintain respect for cultural diversity.

---

# 8. Target Audience

The project is intended for:

- writers;

- editors;

- publishers;

- researchers;

- game developers;

- tabletop role-playing game masters;

- software developers;

- archivists;

- knowledge management professionals.

---

# 9. Strategic Direction

The project is developed as a general-purpose platform.

Architectural decisions should favour applicability beyond the original use cases.

The platform should not depend on:

- a specific setting;

- a specific game;

- a specific publisher;

- a specific software product.

---

# 10. Related Documents

This document is related to:

- DEM-0001 — Terminology and Symbolic Architecture;

- DEM-0002 — Language Policy;

- DEM-0003 — Documentation Policy.

---

# 11. Status

At the time of adoption, the following are considered defined:

- project identity;

- project purpose;

- application scope;

- architectural position;

- foundational principles;

- strategic direction.

Future project development shall take this document into account.

End of document.

Я бы ещё внёс одно изменение в DEM-0002, которое мы будем писать следующим: формально закрепил бы там правило **«Русский термин (English Term) при первом упоминании в русскоязычных документах»**, поскольку теперь это уже не стилистическая рекомендация, а часть принятой политики проекта.
