# LLM-Vergleich für juristische Aufgaben: Pilotstudie Verkehrsrecht

Fünf Sprachmodelle bearbeiten drei echte Mandatskonstellationen aus dem Verkehrsrecht. Jede Antwort wird gegen eine
juristische Musterlösung mit Prüfpunkte-Checkliste bewertet und von einem Juristen gegengeprüft. Herausgeber ist die
[Legal Data Technology GmbH](https://legaldata.tech), Hersteller der Legal-Tech-Plattform
[DEPLAW](https://legaldata.tech/was-ist-deplaw). Die aufbereitete Fassung mit allen Antworten steht unter
**[legaldata.tech/ressourcen/llm-vergleich](https://legaldata.tech/ressourcen/llm-vergleich/verkehrsrecht)**.

## Ergebnisse

Score 0 bis 100, Bewertung gegen die Musterlösung, nach Juristen-Review.

| Modell | Fahrradfahrer, Zebrastreifen, Kreisverkehr | Leasing, Vorschaden | Arbeitsunfall, ungeklärte Haftung | Durchschnitt |
|---|---:|---:|---:|---:|
| GPT-6 Astra | 93 | 95 | 81 | **90** |
| Claude Fable 5.1 | 76 | 95 | 81 | **84** |
| Claude Opus 5.0 | 60 | 85 | 92 | **79** |
| Kimi K3 | 63 | 81 | 42 | **62** |
| GPT-5.6 Luna | 32 | 60 | 60 | **51** |

## Methodik

1. **Aufgabenstellung:** Jeder Fall ist ein vollständiger Mandanten-Sachverhalt, formuliert wie eine echte
   Mandanten-E-Mail. Alle Modelle erhalten denselben Systemprompt und denselben Sachverhalt, ohne modellspezifische
   Anpassung.
2. **Musterlösung und Checkliste:** Vor dem Modelllauf entsteht eine juristisch geprüfte Musterlösung mit 9 bis 14
   Prüfpunkten (Anspruchsgrundlagen, Passivlegitimation, Bezifferung, Kostenrisiko). Diese Checkliste ist der Maßstab.
3. **Richter-Modell:** Claude Opus 5.0 bewertet jede Antwort gegen die Musterlösung: je Prüfpunkt erfüllt oder nicht
   erfüllt mit Begründung, Abweichungen als „Manko“ oder „stilistisch“ eingestuft, dazu ein Score von 0 bis 100.
4. **Menschliche Endkontrolle:** Ein Jurist hat jede Bewertung gegengeprüft und korrigiert, wo er anderer Ansicht war.
   In 10 von 15 Läufen gab es mindestens eine Korrektur. Angegeben ist der juristisch bestätigte oder korrigierte Wert.

## Grenzen

- Drei Fälle aus einem Rechtsgebiet sind eine kleine Stichprobe. Die Zahlen zeigen Tendenzen, keine Rangfolge mit
  statistischer Sicherheit.
- Das Richter-Modell (Claude Opus 5.0) ist zugleich einer der bewerteten Teilnehmer. Die juristische Endkontrolle
  aller Läufe soll diese Verzerrung ausgleichen.
- Modellnamen und Ergebnisse geben den Stand der Läufe wieder (September 2026). Neuere Modellversionen können anders
  abschneiden.

## Dateien

| Datei | Inhalt |
|---|---|
| `data/faelle-und-bewertungen.json` | Fälle, Prüfpunkte, Richter-Zusammenfassung und je Modell Score, Prüfpunkt-Status, Abweichungen, Tokens, Laufzeit |
| `data/laeufe.jsonl` | ein Lauf je Zeile: Fall, Modell, Scores, Begründung, Prüfpunkte, Abweichungen, vollständige Antwort |
| `data/sachverhalte-und-musterloesungen/` | Sachverhalt und Musterlösung je Fall (Markdown) |
| `data/modellantworten/` | die vollständigen Antworten aller Modelle (Markdown) |

Derselbe Datensatz liegt auf Hugging Face: [DEPLAW/legal-llm-vergleich](https://huggingface.co/datasets/DEPLAW/legal-llm-vergleich).

## Zitieren

Legal Data Technology GmbH (2026): *LLM-Vergleich für juristische Aufgaben: Pilotstudie Verkehrsrecht.*
https://legaldata.tech/ressourcen/llm-vergleich

## English summary

Five large language models answer three realistic German traffic-law cases. Each answer is scored against a reference
solution with a 9 to 14 point checklist by an LLM judge (Claude Opus 5.0) and reviewed by a lawyer, who corrected at
least one point in 10 of 15 runs. Published by Legal Data Technology GmbH, maker of the legal tech platform
[DEPLAW](https://legaldata.tech/en/what-is-deplaw). Small pilot sample; the judge model is also one of the contestants.

## Lizenz

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de): frei nutzbar mit Namensnennung
„Legal Data Technology GmbH (DEPLAW)“.
