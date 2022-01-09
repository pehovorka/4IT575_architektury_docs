# REST vs. GraphGL vs. gRPC

- ID: 2
- Datum: 9. 1. 2022

## Status

Schváleno.

## Kontext

V [#1](1_architektura_systemu.md) bylo rozhodnuto, že uživatelské rozhraní nebude renderováno na serveru, ale až JavaScriptem přímo v prohlížeči uživatele (single-page application). Pro přenos dat mezi serverem a klientskou aplikací musí být využito nějakého API.

## Rozhodnutí

Pro komunikaci se serverem budeme využívat GraphQL.

## Důsledky

GraphQL bylo zvoleno zejména z důvodu silné typové kontroly, což je výhoda oproti typickým implementacím REST API. Další výhodou oproti RESTu je potenciální eliminace množství přenesených dat i počtu požadavků, které je nutné na server odeslat, jelikož server vždy vrátí pouze taková data, o která požádáme – nevrátí vše, jako v případě dotazu na REST API endpoint (tzv. overfetching). Současně se GraphQL spoléhá stejně jako REST na formát dat JSON, který je jednoduše čitelný a debugovatelný. To je velká výhoda oproti binárnímu přenosu dat v případě gRPC. Největší výhodou, ale i problémem gRPC je nutnost využití HTTP/2 protokolu. Problémem v tomto případě je to, že tento protokol není plně podporován ve všech webových prohlížečích a je proto nutné využívat proxy. Z tohoto důvodu nebylo gRPC dále uvažováno jako vhodná varianta.
