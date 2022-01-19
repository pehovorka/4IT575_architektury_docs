# Komponenty

## UML diagram komponent

![Components diagram](/assets/diagrams/out/eda/components/components.png)

## Katalog elementů

### Aplikačný server

Node.js aplikace webového serveru, která se stará o komunikaci s frontendovou React aplikací. Obsahuje veškerou business logiku systému pro automatické hodnocení studentských programovacích úloh.

- **GraphQL server** – služba, která poskytuje _GraphQL endpoint_, jakožto rozhraní pro komunikaci s frontendovou aplikací.

- **Auth služba** – stará se o autentizaci a autorizaci uživatelů. Data o uživatelích získává ze _single sign-on API Studijního IS univerzity_.

- **Služba uploadu vypracovaných úloh** – slouží pro nahrávání vypracovaných úloh studenty (a správných řešení vyučujícími). Tyto úlohy jsou následně uloženy do úložiště a metadata zaznamenány v databázi.

- **Služba spouštění a běhu úloh** – stará se o obsluhu služeb běhu zdrojového kódu. Dále má na starosti vyhodnocení jednotlivých běhů na základě stanovených kritérií. Hodnocení předává službě synchronizace studijních výsledků. Také se dotazuje antiplagiátorské služby, zda se studenti nedopustili nějakých nekalých praktik. Veškeré údaje o jednotlivých bězích ukládá do databáze.

- **Služba vytváření a editace zadání** – slouží vyučujícím k vytváření a úpravám zadání úloh.

- **Antiplagiátorská služba** - komunikuje s _TurnItIn API_, kde zjišťuje, zda nedošlo k plagiátorství.

- **Služba synchronizace studijních výsledků** - synchronizuje výsledky běhů s _API studijního IS_

- **ORM** – služba objektově-relačního mapování

### Frontend aplikace

Single-page aplikace vytvořená pomocí JS knihovny React, která komunikuje s webovým serverem pomocí protokolu WebSocket.

### Aplikace Node/Python/Java runtime

Aplikace, které se starají o exekuci a vyhodnocení studentských programovacích úloh.

- **Služba běhu zdrojového kódu** – slouží k běhu studentských úloh. Zdrojové kódy jsou získány z úložiště.

### PostgreSQL

- **Databáze**.

### Cloud Storage

- **Úložiště nahraných úloh**.

## Kód diagramu

PlantUML kód je k dispozici [zde](/assets/diagrams/src/eda/components.puml).
