# Přístup k automatizovanému testování

- ID: 5
- Datum: 15. 1. 2022

## Stav

Schváleno.

## Kontext

Chceme kontinuálně automaticky testovat všechny zásadní součásti aplikace.

## Rozhodnutí

Webový server budeme testovat jednotkovými a integračními testy napsanými pomocí frameworku [Jest](https://github.com/facebook/jest). Pro load/stress testing využijeme nástroj [k6](https://github.com/grafana/k6). Pro E2E/UI testy frontendové aplikace použijeme [Cypress](https://github.com/cypress-io/cypress).

## Důsledky

Běh jednotkových, integračních a E2E/UI při každém každém pushi do repozitáře nám poskytne v případě kvalitně vytvořených testů jistotu, že nejnovější změny nerozbily dosavadní funkcionalitu. Aby tento přístup fungoval, bude nutné mít kód pokrytý testy v dostatečné míře a tyto testy udržovat.

Pomocí load testů budeme pravidelně ověřovat výkonnost a škálovatelnost aplikace. Díky tomu budeme moci regresně ověřit, zda poslední změny neměly negativní vliv na výkon.
