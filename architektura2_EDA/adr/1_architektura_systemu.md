# Architektúra systému

- ID: 1
- Dátum: 19. 1. 2022

## Stav

Schválené.

## Kontext

Je nutné zvoliť architektúru pre novú aplikáciu slúžiacu k automatizovanému hodnoteniu študentských programátorských úloh.

## Rozhodnutie

Bolo rozhodnuté, že základom architektúry aplikácie bude Event Driven Architecture (EDA). Aplikácia, ktorá bude bežať v prehliadači užívateľa sa bude pripájať na webový server, ktorý bude fungovať ako mediátor. Udalosti budú posielať správy do fronty, ktorá ich predá mediátorovi a ten ich presmeruje na relevantné služby.

## Dôsledky

Pre komunikáciu webového servera a frontendovej aplikácie bude nutné zvoliť spôsob výmeny dát ([#2](2_websocket_webhook.md)).
