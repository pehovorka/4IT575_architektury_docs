# Nasazení

## UML diagram nasazení

![Deployment diagram](/assets/diagrams/out/eda/deployment/deployment.png)

## Katalog elementů

### Zařízení uživatele aplikace

Zařízení s webovým prohlížečem.

### Server studijního IS

Server, na kterém běží centrální studijní IS.

### Server TurnItIn

Server, na kterém antiplagiátorská služba.

### Google Cloud Platform

Sada služeb pro cloud computing od společnosti Google.

### Cloud Run

„Serverless“ prostředí pro běh Docker kontejnerů s vysokou škálovatelností.

### Web API container

Docker kontejner, ve kterém běží aplikace webového API.

### Web server container

Node.js aplikace webového serveru, která působí jako mediátor a reaguje na zprávy z React aplikace. Obsahuje veškerou business logiku systému pro automatické hodnocení studentských programovacích úloh.

### Runtimes containers

Docker kontejnery, ve kterých běží Node.js, Python a Java prostředí pro exekuci a vyhodnocení studentských programovacích úloh.

### Cloud SQL

Databáze jako služba (DBaaS).

### PostgreSQL

Open-source databázový systém.

### DB systému hodnocená studentských prog. úloh

Databáze sloužící k uložení dat o jednotlivých zadáních, bězích a podobně.

### Firebase Hosting

Web hosting vhodný pro single-page aplikace.

### Frontend React aplikace

Single-page aplikace vytvořená pomocí JS knihovny React, která komunikuje s webovým API pomocí dotazovacího jazyka GraphQL. Statické soubory jsou uloženy na Firebase Hostingu a samotná aplikace běží ve webovém prohlížeči uživatele.

### Cloud Storage

Webová služba úložiště.

## Kód diagramu

PlantUML kód je k dispozici [zde](/assets/diagrams/src/eda/deployment.puml).
