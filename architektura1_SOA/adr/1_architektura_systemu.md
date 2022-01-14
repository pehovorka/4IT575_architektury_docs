# Architektura systému

- ID: 1
- Datum: 9. 1. 2022

## Stav

Schváleno.

## Kontext

Je nutné zvolit architekturu pro novou aplikaci sloužící k automatizovanému hodnocení studentských programátorských úloh.

## Rozhodnutí

Bylo rozhodnuto, že základem architektury aplikace bude Service Oriented Architecture (SOA). Webový server bude poskytovat API pro frontendovou aplikaci (SPA), která bude hostována odděleně a bude běžet přímo v prohlížeči uživatele (nebude renderována na serveru).

## Důsledky

Pro komunikaci webového serveru a frontendové aplikace bude nutné zvolit způsob výměny dat ([#2](2_rest_graphql_grpc.md)).
