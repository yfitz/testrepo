# Merge Konflikte vermeiden

## Strategien

**1. Häufig pullen & pushen**
```bash
git pull --rebase origin main   # vor dem Arbeiten
git push                        # nach jedem abgeschlossenen Feature
```
Je seltener du pullst, desto größer die Divergenz.

**2. Kurze, fokussierte Branches**
- Branch nur für **eine** Aufgabe
- Schnell mergen, nicht tagelang parallel arbeiten

**3. Kommunikation im Team**
- Abmachen, wer an welcher Datei arbeitet
- Große Refactorings ankündigen — die sind die häufigste Konfliktquelle

**4. Kleine, häufige Commits**
```bash
git commit -m "fix: button farbe"   # gut
# vs. einen riesigen Commit nach 3 Tagen
```

**5. Feature Flags statt langer Branches**
Neuen Code hinter einem Flag verstecken → direkt auf `main` committen → kein langer Branch → kein Konflikt.

**6. Klare Dateistruktur**
Jede Person/jedes Modul hat "eigene" Dateien → weniger Überschneidungen.

---

## Wenn Konflikte trotzdem kommen

```bash
git fetch origin
git rebase origin/main   # statt merge — sauberere History
```
`rebase` bringt Konflikte früher und einzeln ans Tageslicht, statt alles auf einmal.

---

**Kurz gesagt:** Das Hauptrezept ist — **oft synchronisieren, kleine Einheiten, klare Zuständigkeiten**.
