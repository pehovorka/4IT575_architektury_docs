# Balíčky

## UML diagram balíčků

![Packages diagram](/assets/diagrams/out/soa/packages/packages.png)

## Katalog elementů

### Web API

- **services** – implementace jednotlivých služeb
- **constants** – konstanty
- **config** – konfigurační údaje
- **scripts** - skripty – například pro spouštění v CRONu apod.
- **tests** - unit/integrační Jest testy
- **typeDefs** - definice GraphQL schématu
- **utils** - utility funkce
- **migrations** - migrace DB
- **seeds** - počáteční sady dat databáze
- **monitoring** - funkce pro logování a monitoring

### Frontend APP

- **components** – UI komponenty aplikace
- **hooks** – React Hooky
- **styles** – styly
- **services** – soubory pro state-management (knihovna Redux)
- **constants** - konstanty
- **translations** - překlady
- **config** - konfigurační údaje
- **tests** - UI/E2E Cypress testy
- **routes** - routes s cestami jednotlivých stránek
- **utils** - utility funkce

### DB

- **tables** - tabulky
- **users** - uživatelé
- **indexes** - indexy

### Node/Python/Java runtime

- **services** – implementace jednotlivých služeb
- **tests** – testy
- **utils** – utility funkce
- **constants** – konstanty
- **config** – konfigurační údaje
- **monitoring** – funkce pro logování a monitoring

### Cloud logging

- **logging** – centralizované logování

### Shared

- **types** – TypeScript typy. Částečně automaticky vygenerované z GraphQL schématu.

## Kód diagramu

PlantUML kód je k dispozici [zde](/assets/diagrams/src/soa/packages.puml).
