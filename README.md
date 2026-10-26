# BaufiBlick-Leistbarkeits-Index (Open Data, CC BY 4.0)

Modellhaft finanzierbarer Immobilien-Kaufpreis eines Zweipersonenhaushalts in den **16 deutschen Bundesländern** auf Basis amtlicher Primärdaten:

1. **Verfügbares Einkommen der privaten Haushalte je Einwohner** — Arbeitskreis „Volkswirtschaftliche Gesamtrechnungen der Länder" (VGRdL, Berichtsjahr 2024).
2. **Effektiver Jahreszins für Wohnungsbaukredite an private Haushalte (5–10 Jahre Zinsbindung)** — Deutsche Bundesbank, MFI-Zinsstatistik (`BBIM1.M.DE.B.A2C.I.R.A.2250.EUR.N`).
3. **Grunderwerbsteuersätze der Bundesländer** (3,5 % bis 6,5 %, Stand Oktober 2026).

- **Primärquelle & interaktive Dokumentation:** [https://baufiblick.de/leistbarkeits-index/](https://baufiblick.de/leistbarkeits-index/)
- **Archivausgabe 08/2026:** [https://baufiblick.de/leistbarkeits-index-2026-08/](https://baufiblick.de/leistbarkeits-index-2026-08/)
- **Länderübersicht & Grunderwerbsteuer:** [https://baufiblick.de/bundeslaender/](https://baufiblick.de/bundeslaender/)
- **Zinsreihe (Bundesbank MFI):** [https://baufiblick.de/bauzinsen/](https://baufiblick.de/bauzinsen/)

## Enthaltene Datensätze

| Datei | Ausgabe | Modellzins (Sollzins) | Bundesbank-Referenz (5–10 J.) | Kaufpreis Bundesschnitt |
|---|---|---|---|---|
| `baufiblick-leistbarkeits-index-2026-10.csv` | `2026-10` | 3,8 % p. a. | 3,81 % (August 2026) | 234.560 € (−4.976 € ggü. 08/2026) |
| `baufiblick-leistbarkeits-index-2026-08.csv` | `2026-08` | 3,7 % p. a. | 3,74 % (Mai/Juni 2026) | 239.536 € |

## Methodik & Modellannahmen

- **Haushalt:** 2 Personen mit dem durchschnittlichen verfügbaren Einkommen des jeweiligen Bundeslandes (`Einkommen_Kopf × 2`).
- **Tragbare Gesamtbelastung:** 30 % des verfügbaren Haushaltsnettoeinkommens.
- **Bewirtschaftungspauschale:** 4,00 €/m² für 100 m² Wohnfläche (= 400 €/Monat für Betriebskosten + Instandhaltungsrücklage) werden **vor** der Kreditrate abgezogen.
- **Annuität:** 3,8 % Sollzins p. a. (Ausgabe 10/2026) bzw. 3,7 % Sollzins p. a. (Ausgabe 08/2026) + 2,0 % anfängliche Tilgung.
- **Eigenkapital & Kaufnebenkosten:** 40.000 € Eigenkapital; davon werden Grunderwerbsteuer (länderspezifisch 3,5 % bis 6,5 %) und Notar-/Grundbuchkosten (2,0 % Modellwert) gedeckt, ohne Maklerprovision.

## Lizenz & Zitierweise

Veröffentlicht unter **Creative Commons Attribution 4.0 International (CC BY 4.0)**.
Bei Verwendung in Medien, Forschung oder Datenprojekten bitte nennen:

> Quelle: BaufiBlick-Leistbarkeits-Index (Florian Schröder, https://baufiblick.de/leistbarkeits-index/), Lizenz CC BY 4.0.
