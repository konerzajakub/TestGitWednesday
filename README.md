# Monitorování cen nemovitostí
- Semestrální práce 04/2023

### Motivace
- Téma jsem si vybral, protože mi přišly ceny realit zajímavé a zároveň jsem si chtěl vyzkoušet parsování reálných JSON dat z webových zdrojů.

### Popis problému

- Aplikace bude podle kritérií sbírat data ze stránky "sreality.cz", zprůměruje ceny a uloží je do souboru.
- Později bude možné tento soubor zobrazit a porovnat stejné data ovšem z jiného dne.
- Zobrazí procentní nárust nebo pokles průměrné ceny.

## Řešení

| Dokumentace |                   |
| ------------- | ------------------------------ |
| Vytvořit readme.md      | 90%      |

| Data |                   |
| ------------- | ------------------------------ |
| Získat data z sreality.cz      | 100%      |
| Zdokumentovat získání specifických dat (typ reality a lokality) z sreality.cz      | 100%      |
| Získat JSON data     | 100%      |
| Zpracovat data z JSON souboru     | 100%      |
| Uložit data do souboru     | 100%      |

| Uživatelské rozhraní |                   |
| ------------- | ------------------------------ |
| Úvodní stránka     | 100%      |
| Tvorba nových dat     | 100%      |
| Prohlížení dat     | 100%      |
| Porovnání stejných nových a starých dat     | 100%      |

### Funkční specifikace
- Seznam funkcí z pohledu uživatele, které bude Váš program poskytovat např. formou větveného seznamu (stromu)
- Může sloužit následně jako podklad pro menu. Funkce očíslujte.

```mermaid
flowchart TD
    %% A = Úvodní stránka
    %% B = Výběr nových dat
    %% D = Volba mezi existujícími daty
    %% E = Získání dat z sreality.cz
    %% F = Zobrazení dat

    %% Úvodní stránka
    A[Úvodní stránka] --> newData(Vybrat nové data)
    A --> konec(Konec Aplikace)
    
    newData --> lokalita(Výběr kraje)

    lokalita(Výběr kraje)-->typ(Výběr typu reality)
    
    %% Výběr nových dat
    typ --> |Získání dat z sreality.cz| E(Data uložena)
    E --> A
    D --> |Chci vidět jeden soubor| F
    D --> |Chci porovnat dva soubory| F(Prezentace dat)

    F --> A

    

    %% Volba mezi existujícími daty
    A --> D(Volba mezi existujícími daty - preset)
    

    %% Go back
    %%B --> A 
    %%D --> A 
    %%F --> D 
```

### Popis struktury vstupních a výstupních souborů
- Jaké datové typy budou obsahovat, čím budou odděleny jednotlivé údaje, jestli je požadovaný určitý formát názvů souborů a pod.

### Class diagram
- Diagram tříd

## Testování

## Zdrojový kód
