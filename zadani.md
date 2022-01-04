# Zadání seminární práce z předmětu 4IT575 – Softwarové Architektury

Jméno: Marcel Farkaš, Peter Mato, Petr Hovorka

## Úkol:

1. Na základě níže popsaných požadavků navrhněte dvě architektury vhodné pro implementaci dané aplikace.
2. Navržené architektury zdokumentujte.
3. V závěru zhodnoťte, která z vybraných architektur je výhodnější a proč.

## Poznámka:

Pokud ze zadání přímo nevyplyne nějaká skutečnost, kterou potřebujete znát, domluvte se ve skupině, a sami ji dodefinujte, tak jako byste se na ni doptali zákazníka.

## Popis aplikace:

Univerzita výrazně rozšířila svůj kurz programování a chce být schopna automatizovat hodnocení jednoduchých programátorských úloh.

### Uživatelé:

300+ studentů ročně, plus zaměstnanci a administrátoři.

### Požadavky:

- Studenti musí mít možnost nahrát svůj zdrojový kód, který bude spuštěn a oznámkován.
- Známky a běhy musí být trvalé a kontrolovatelné.
- Je třeba zaintegrovat systém odhalování plagiátorství zahrnující porovnávání s jinými odevzdanými pracemi a také odesílání do webové služby (TurnItIn).
- Nutná integrace se systémem řízení výuky univerzity.
- Vyučující stanoví datum a čas odevzdání, po jehož uplynutí jsou odevzdané práce odmítnuty.
- Studenti mohou odevzdat tolik pokusů, kolik chtějí, aby si zlepšili známku.
- Vyučující určují kritéria hodnocení, která mohou zahrnovat metriky a/nebo testy

### Další souvislosti:

- Univerzitní informační systém je dodáván třetí stranou a je poměrně obtížné v něm provádět změny.
- Známky jsou každoročně kontrolovány státním regulačním orgánem.
- Univerzita má velmi malý rozpočet na IT, protože staví náhradní stadion pro sportovní fotbal.
- Univerzita je rekordmanem v počtu nejlepších absolventů CS v zemi.
