# Strategie sdílení typů mezi FE a BE aplikacemi

- ID: 4
- Datum: 14. 1. 2022

## Stav

Schváleno.

## Kontext

Chceme sdílet deklarace TypeScript typů mezi frontendovou aplikací a webovým serverem.

## Rozhodnutí

Celý projekt – frontendová aplikace i webový server bude v jednom monorepu.

## Důsledky

Díky umístění všech součástí do jednoho monorepa bude možné jednoduše sdílet kód (nejen typy) mezi jednotlivými aplikacemi. Alternativně by kód šel sdílet například publikováním `npm` balíčku. Tento přístup byl ale vyhodnocen jako zbytečně složitý.

Využití monorepa má ale i své nevýhody – v našem případě například složitější konfiguraci CI/CD pipeline.
