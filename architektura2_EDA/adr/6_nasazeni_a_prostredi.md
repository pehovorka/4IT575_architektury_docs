# Nasazení systému a vývojová prostředí

- ID: 6
- Datum: 15. 1. 2022

## Stav

Schváleno.

## Kontext

Pro urychlení vývoje potřebujeme mít správně nastavenou CI/CD pipeline. Vývoj aplikace musí probíhat odděleně od produkčního prostředí.

## Rozhodnutí

Budou existovat 3 vývojová prostředí:

1. Development
1. Staging
1. Production

Každé prostředí bude běžet nezávisle na ostatních. V těchto oddělených prostředích bude provozována jak frontendová aplikace, tak webový server a jeho součásti.

Samotná CI/CD pipeline se bude starat o sestavení jednotlivých součástí aplikace, jejich otestování a následné nasazení do konkrétního vývojového prostředí. Běh pipeline se spustí pushem změn do odpovídajících větví jednotlivých prostředí v git repozitáři. Například push do větve `development` spustí pipeline, která bude ukončena nasazením aplikace do `development` prostředí.

## Důsledky

CI/CD pipeline nám umožní rychle a spolehlivě nasazovat aplikaci do jednotlivých dev. prostředí. Její součástí je i spouštění unit, integračních a E2E / UI testů. Tento krok byl popsán v [#5](5_automatizace_testovani.md).
