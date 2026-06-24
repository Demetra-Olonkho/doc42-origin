2026-06-08 2051

https://chatgpt.com/s/t_6a2bd4453340819187d21a0e0a277ad4

Согласен. Более того, мне кажется, что сейчас мы подошли к одному из ключевых архитектурных решений всего проекта.

Потому что от ответа на вопрос:

> Что является частью ядра, а что может определяться пользователем?

будет зависеть буквально всё:

- модель данных;

- API;

- система хранения;

- плагины;

- импорт/экспорт;

- интеграция с VTT;

- интеграция с Publishing Pipeline;

- возможность использовать систему для совершенно чужих сеттингов.

---

# Первый принцип: различать Platform и Setting

Я бы сразу разделил:

```text
Platform
```

и

```text
Setting
```

Платформа поставляет механизмы.

Сеттинг поставляет содержимое.

Например:

```text
Platform знает:
- что такое сущность;
- что такое связь;
- что такое источник;
- что такое версия.

Platform не знает:
- что такое эльф;
- что такое джедай;
- что такое дом Атрейдес;
- что такое Империя.
```

---

# Что должно быть жёстко зафиксировано в ядре

Я бы сделал максимально маленькое ядро.

## Entity

Базовая сущность.

```text
Entity
```

Минимум:

```text
ID
Type
Attributes
Metadata
```

---

## Relationship

Связь.

```text
Entity A
      │
      ▼
Relation
      │
      ▼
Entity B
```

---

## Source

Источник сведений.

```text
Document
Book
Article
Campaign
```

---

## Revision

Версия данных.

---

## Taxonomy

Классификаторы.

---

## Schema

Описание пользовательских типов.

---

Фактически ядро должно знать только это.

---

# Что не должно быть зафиксировано

Например, многие проекты сразу делают:

```text
Character
Location
Organization
Item
```

частью движка.

Я бы этого избегал.

Потому что завтра пользователь придёт с сеттингом про:

```text
Космические корабли
Корпорации
Планеты
ИИ
```

и половина модели окажется бесполезной.

---

# Тогда возникает вопрос

Если Character не часть ядра, что тогда?

Ответ:

```text
Character = расширение схемы
```

---

Например:

```yaml
entity_type:
  id: character
  parent: entity
```

---

и далее:

```yaml
fields:
  - name
  - biography
  - birth_date
  - death_date
```

---

Для другого мира:

```yaml
entity_type:
  id: starship
```

---

```yaml
fields:
  - class
  - registry_number
  - displacement
```

---

Система ничего не знает про персонажей и корабли.

Она знает только про типы сущностей.

---

# Что я бы оставил полуфиксированным

Есть вещи, которые встречаются почти везде.

Например:

```text
Character
Location
Organization
Event
Document
```

---

Их можно поставлять как:

```text
Core Content Pack
```

или

```text
Default Ontology
```

---

Но не как часть движка.

---

# Второй принцип: типы связей должны быть расширяемыми

Я бы не зашивал:

```text
member_of
owns
located_in
```

в код.

---

Вместо этого:

```yaml
relation_type:
  id: member_of

from:
  character

to:
  organization
```

---

Или:

```yaml
relation_type:
  id: commands

from:
  character

to:
  starship
```

---

Или:

```yaml
relation_type:
  id: worships

from:
  culture

to:
  deity
```

---

# Третий принцип: документы тоже сущности

Мне кажется, это будет одной из сильнейших сторон системы.

Например:

```text
Character
Location
Organization
```

и

```text
Book
Gazetteer
Campaign
Article
```

существуют в одном графе.

---

Тогда автоматически появляются связи:

```text
appears_in

described_in

introduced_in

mentioned_in
```

---

Это очень пригодится для Publishing Pipeline.

---

# Четвёртый принцип: плагины должны расширять модель, а не код

Очень важный момент.

Частая ошибка:

```text
Плагин = новый функционал
```

---

Для Lore Database важнее другое:

```text
Плагин = новый домен знаний
```

---

Например:

### TTRPG Plugin

Добавляет:

```text
Character Sheet
Creature
Spell
Class
Skill
```

---

### Historical World Plugin

Добавляет:

```text
Dynasty
Treaty
Battle
Province
```

---

### Science Fiction Plugin

Добавляет:

```text
Starship
Planet
Corporation
```

---

Ядро при этом не меняется.

---

# Пятый принцип: всё должно иметь собственную схему

Я бы даже сделал обязательным наличие схем.

Например:

```text
Entity Type
Field Definition
Relation Definition
Validation Rules
```

---

Тогда система сможет:

```text
валидировать данные;

генерировать формы;

строить API;

строить документацию;

строить интерфейс редактора.
```

автоматически.

---

# Что я бы сейчас предложил считать границей ядра

Если свести всё к минимуму:

```text
Core
│
├─ Entity
├─ Relation
├─ Source
├─ Revision
├─ Taxonomy
├─ Schema
└─ Plugin
```

Всё остальное, включая:

```text
Character
Location
Organization
Book
Campaign
Spell
Monster
Starship
Corporation
```

должно существовать как данные и расширения.

Если удастся удержать эту границу и не начать добавлять в ядро сущности конкретных жанров и сеттингов, то получится действительно универсальная платформа, которую можно использовать и для небольшого авторского мира, и для крупной издательской экосистемы с несколькими авторами, VTT, энциклопедией и издательским конвейером.
