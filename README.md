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
| `baufiblick-leistbarkeits-index-2026-10.csv` | `2026-10` | 3,8 % p. a. | 3,81 % (August 2026) | 235.407 € (−4.130 € ggü. 08/2026) |
| `baufiblick-leistbarkeits-index-2026-08.csv` | `2026-08` | 3,7 % p. a. | 3,74 % (Mai/Juni 2026) | 239.537 € |

## Methodik & Modellannahmen

Die Dateien sind byte-gleich mit den CSV-Downloads auf baufiblick.de (Semikolon als Trennzeichen, UTF-8 mit BOM). Der „Bundesschnitt" ist das ungewichtete Mittel der 16 Länderwerte.

```
Einkommen je Kopf   = Verfügbares Einkommen der privaten Haushalte 2024 (VGRdL, Berechnungsstand August 2025)
                      ÷ Bevölkerung am 31.12.2024 (Destatis, Fortschreibung auf Grundlage des Zensus 2022)
Haushaltseinkommen  = Einkommen je Kopf ÷ 12 × 2                      (Zweipersonenhaushalt)
Wohnfolgekosten     = 130 m² × 5,00 €                                 (Betrieb 3,50 € + Rücklage 1,50 €) = 650 €
Tragbare Rate       = Haushaltseinkommen × 35 % − Wohnfolgekosten
Darlehen            = Rate × 12 ÷ (Sollzins + 2 % Tilgung)            (Sollzins 3,8 % in 10/2026, 3,7 % in 08/2026)
Nebenkostensatz     = Grunderwerbsteuer des Landes + 2,0 % Notar und Grundbuch + 3,57 % Makler
Kaufpreis           = Darlehen ÷ (0,8 + Nebenkostensatz)              (20 % Eigenkapital als Anteil am Kaufpreis)
```

Notar und Grundbuch (2,0 %) und Makler (3,57 %) sind Modellannahmen, keine Gebühren. Alle Werte lassen sich mit diesen Formeln aus den amtlichen Ausgangsdaten nachrechnen.

**Korrektur 17.11.2026:** Die am 26.10.2026 veröffentlichte Fassung dieses Pakets enthielt andere Einkommenswerte (14 von 16 Länder wichen von der amtlichen Rechnung ab) und ein anderes Modell (festes Eigenkapital von 40.000 €, 30 % Belastungsquote, ohne Makler). Sie passte nicht zu den Zahlen auf baufiblick.de. Maßgeblich sind die Dateien in diesem Stand.

## Lizenz & Zitierweise

Veröffentlicht unter **Creative Commons Attribution 4.0 International (CC BY 4.0)**.
Bei Verwendung in Medien, Forschung oder Datenprojekten bitte nennen:

> Quelle: BaufiBlick-Leistbarkeits-Index (Florian Schröder, https://baufiblick.de/leistbarkeits-index/), Lizenz CC BY 4.0.
