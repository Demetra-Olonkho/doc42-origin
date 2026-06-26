2026-06-14 815

https://chatgpt.com/s/t_6a2eca9d83d88191b7c1fabd5df7b3a3

Согласен. Учитывая нашу договорённость, это будет именно **DEM-P0001**, а не DEM-000X, поскольку документ ещё не утверждён и фактически является первым черновиком общей модели, которая только начинает складываться.

Также сразу учту достигнутые ранее соглашения:

- документ двуязычный;

- сначала русский текст, затем английский;

- в русской части используются русские наименования с английскими в скобках;

- документ относится к категории черновиков (Draft);

- документ описывает не только паспорта, но и систему идентификации сущностей в целом.

---

# DEM-P0001

# Система идентификации и паспортов сущностей (Entity Identification and Passport System)

Статус: Черновик (Draft)

Версия: 0.1

---

# Русская версия

## 1. Назначение

Настоящий документ определяет предварительную модель идентификации, описания и связывания сущностей в рамках проекта «Деметра Олонхо» (Demetra Olonkho).

Документ является черновиком и предназначен для обсуждения принципов, которые впоследствии могут лечь в основу нормативной документации проекта.

---

## 2. Предпосылки

В ходе проектирования проекта «Деметра Олонхо» было установлено, что объектами учёта и сопровождения являются не только документы, файлы и иные физические объекты, но также темы обсуждений, концепции, требования, решения, связи и другие логические конструкции.

Следовательно, система должна обеспечивать единообразную работу как с физическими, так и с логическими сущностями.

---

## 3. Основные положения

### 3.1. Сущность (Entity)

Сущностью считается любой объект модели знаний, который может быть идентифицирован, описан и связан с другими объектами.

Каждая сущность должна обладать:

- идентификатором;

- типом;

- состоянием жизненного цикла;

- набором атрибутов;

- набором связей с другими сущностями.

---

### 3.2. Физическая сущность (Physical Entity)

Физическая сущность имеет непосредственное представление в некотором носителе информации.

Примеры:

- пространство обсуждений (Discussion Space);

- обсуждение (Discussion);

- сообщение (Message);

- документ (Document);

- файл (File);

- репозиторий (Repository).

---

### 3.3. Логическая сущность (Logical Entity)

Логическая сущность существует как результат анализа, интерпретации или структурирования информации.

Примеры:

- тема (Topic);

- ветка (Thread);

- концепция (Concept);

- требование (Requirement);

- решение (Decision);

- термин (Term);

- отношение (Relation).

---

### 3.4. Равноправие сущностей

Физические и логические сущности являются равноправными объектами модели знаний.

Физическое существование сущности не определяет её значимость.

Логическая сущность может иметь большее значение для модели знаний, чем физические объекты, из которых она была выделена.

---

## 4. Идентификаторы сущностей

Каждая сущность должна иметь уникальный идентификатор.

Идентификатор принадлежит сущности, а не конкретному документу или представлению сущности.

Одна и та же сущность может иметь несколько представлений при сохранении единого идентификатора.

Пример:

PROJECT-0001

может иметь:

- паспорт;

- YAML-представление;

- JSON-представление;

- HTML-представление;

- иные формы представления.

При этом идентификатор остаётся неизменным.

---

## 5. Паспорт сущности (Entity Passport)

Паспорт сущности представляет собой стандартизованное описание сущности.

Паспорт не является сущностью.

Паспорт является документированным представлением сущности.

Назначение паспорта:

- идентификация сущности;

- описание сущности;

- фиксация состояния;

- фиксация основных связей.

---

## 6. Типы сущностей и типы документов

Типы сущностей и типы документов должны рассматриваться как различные категории.

Примеры типов сущностей:

- PROJECT;

- ORGANIZATION;

- DISCUSSION;

- TOPIC;

- THREAD;

- DOCUMENT;

- PERSON.

Примеры типов документов:

- PASSPORT;

- REGISTRY;

- SPECIFICATION;

- REPORT;

- LOG.

---

## 7. Происхождение знаний (Knowledge Provenance)

Для модели знаний принципиально важным является происхождение информации.

Первичной единицей происхождения знаний в пространстве обсуждений считается сообщение (Message).

Из одного или нескольких сообщений могут быть сформированы:

- темы;

- ветки;

- требования;

- решения;

- концепции;

- иные логические сущности.

Пример:

MESSAGE-0042

может являться источником возникновения:

- TOPIC-0007;

- DECISION-0003;

- CONCEPT-0011.

---

## 8. Структура обсуждений

Обсуждения рассматриваются как совокупность сообщений.

Темы и ветки не являются контейнерами сообщений.

Темы и ветки являются логическими сущностями, выделяемыми из множества сообщений.

Одно сообщение может относиться одновременно к нескольким темам и нескольким веткам.

---

## 9. Предварительная модель

Сущность (Entity)

↓

Идентификатор (Identifier)

↓

Паспорт (Passport)

↓

Связи (Relations)

↓

Представления (Representations)

---

## 10. Самоприменение

Проект «Деметра Олонхо» рассматривается как один из первых потребителей собственной модели знаний.

Документация, обсуждения, решения и иные артефакты проекта могут использовать данную модель до появления программной реализации системы.

---

# English Version

## 1. Purpose

This document defines a preliminary model for identification, description, and interconnection of entities within the Demetra Olonkho project.

The document is a draft intended to support discussion and future standardization.

---

## 2. Background

During the design of Demetra Olonkho it became clear that the system must operate not only with physical artifacts such as files and documents, but also with logical constructs such as topics, concepts, requirements, decisions, and relationships.

Therefore, a unified model is required.

---

## 3. Core Principles

### 3.1 Entity

An Entity is any object within the knowledge model that can be identified, described, and linked to other objects.

Each entity shall possess:

- an identifier;

- a type;

- a lifecycle state;

- attributes;

- relationships.

---

### 3.2 Physical Entity

A Physical Entity has a direct representation in an information carrier.

Examples:

- Discussion Space;

- Discussion;

- Message;

- Document;

- File;

- Repository.

---

### 3.3 Logical Entity

A Logical Entity exists as a result of interpretation, analysis, or structuring of information.

Examples:

- Topic;

- Thread;

- Concept;

- Requirement;

- Decision;

- Term;

- Relation.

---

### 3.4 Equality of Entities

Physical and logical entities are equal participants in the knowledge model.

Physical existence does not imply greater importance.

---

## 4. Entity Identifiers

Every entity shall possess a unique identifier.

Identifiers belong to entities rather than their representations.

Multiple representations may exist for a single entity while preserving a single identifier.

---

## 5. Entity Passport

An Entity Passport is a standardized description of an entity.

A passport is not an entity itself.

A passport is a documented representation of an entity.

Its purpose is to provide:

- identification;

- description;

- state information;

- relationship information.

---

## 6. Entity Types and Document Types

Entity types and document types shall be treated as distinct categories.

Entity type examples:

- PROJECT;

- ORGANIZATION;

- DISCUSSION;

- TOPIC;

- THREAD;

- DOCUMENT;

- PERSON.

Document type examples:

- PASSPORT;

- REGISTRY;

- SPECIFICATION;

- REPORT;

- LOG.

---

## 7. Knowledge Provenance

Knowledge provenance is considered a fundamental principle.

Within discussion environments, the Message is the primary unit of knowledge origin.

Topics, concepts, requirements, decisions, and other logical entities may be derived from one or more messages.

---

## 8. Discussion Structure

Discussions are considered collections of messages.

Topics and threads are not message containers.

Instead, they are logical entities identified across sets of messages.

A single message may belong to multiple topics and threads simultaneously.

---

## 9. Preliminary Model

Entity

↓

Identifier

↓

Passport

↓

Relations

↓

Representations

---

## 10. Self-Application

Demetra Olonkho is considered one of the first consumers of its own knowledge model.

Project documentation and design artifacts may adopt this model before a software implementation exists.

На мой взгляд, это уже полноценный **DEM-P0001 v0.1**, который фиксирует все основные концептуальные выводы последних обсуждений и создаёт фундамент для следующего шага — проектирования конкретных типов паспортов (TOPIC, PROJECT, ORGANIZATION, DOCUMENT и т.д.) и последующего формирования **TOPIC-0001** для организационного обсуждения.
