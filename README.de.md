<p align="center"><a href="https://bestimage.ai/"><img src="assets/bestimage-logo.svg" width="72" alt="Logo von bestimage.ai"></a></p>

# Awesome Wan 3.0 Prompts — Deutscher Leitfaden

**148 Regievorlagen für Videos in 14 Kategorien, überarbeitet und gepflegt vom Team von [bestimage.ai](https://bestimage.ai/).** Beschreiben Sie ein klares Ereignis, weisen Sie Eingaben feste Aufgaben zu und planen Sie Kamera, Ton und Kontinuität.

[Englischer Leitfaden](README.md) · [Alle 15 Sprachen](locales/README.md) · [Vollständiges Verzeichnis](prompts/README.md) · [Mitwirken](CONTRIBUTING.md)

![Konzeptbild: Eine Person aus dem Archiv öffnet im Morgenlicht einer Sternwarte eine Sternkarte](assets/wan-3-prompt-collection-hero.png)

*Statisches Konzeptbild aus dem integrierten Bildgenerator, kein mit Wan 3.0 erzeugtes Video. Siehe [Bildanweisungen und Herkunft](assets/README.md).*

## Inhalt und Einstieg

**148 Video-Regievorlagen in 14 Kategorien**. Die ersten sechs Kategorien enthalten chinesische Regievorlagen, die übrigen acht englische. In 15 Sprachen stehen Einstiegsleitfäden und eine gemeinsame Vergleichsvorlage bereit, **keine vollständigen Übersetzungen aller 148 Vorlagen**. Übersetzungen und Vergleichsvorlage zählen nicht als zusätzliche Katalogeinträge.

1. Wählen Sie eine Vorlage im [vollständigen Verzeichnis](prompts/README.md).
2. Passen Sie die Variablen an und bereiten Sie alle benötigten Eingaben vor. Referenzen beschreiben Aufgaben; die entsprechenden Dateien liegen diesem Repository nicht bei.
3. Wählen Sie den passenden Modus und stellen Sie Dauer, Seitenverhältnis, Auflösung und Ton in der Oberfläche ein. Text allein konfiguriert keine API-Anfrage.
4. Erzeugen Sie einen kleinen Test und prüfen Sie Handlung, Geometrie, Identität, zeitlichen Ablauf und Ton anhand des Prüfziels der Vorlage.

## Formel mit acht Ebenen

```text
[Ausgabe] Dauer + Seitenverhältnis + visuelles Medium
[Motiv] wiedererkennbare Identitätsmerkmale + unveränderliche Details
[Umgebung] Zeit + Ort + Wetter + räumliche Tiefe
[Handlung] Auslöser → durchgehende Bewegung → sichtbares Ergebnis
[Kamera] Einstellungsgröße + Winkel + ein Weg + Schlussbild
[Gestaltung] Licht + Farbpalette + Materialien + Bewegungsdarstellung
[Ton] Atmosphäre + Geräusche + Musik + Dialog
[Grenzen] zu erhaltende Elemente + wahrscheinlichste Fehler
```

Nutzen Sie eine Hauptsprache für die Bildbeschreibung und legen Sie Dialogsprache und genaue Sätze getrennt fest. Funktionen und Einstellungen können je nach Produkt, Region und Plattform abweichen.

## Vollständige Vergleichsvorlage

**Modus:** Text zu Video · **Einstellungen:** 10 Sekunden, 16:9, Ton eingeschaltet · **Eingaben:** keine

```text
Erzeuge eine 10 Sekunden lange dokumentarische Einstellung im Format 16:9 in einer ruhigen gemeinschaftlichen Werkzeugbibliothek. Eine erwachsene ehrenamtliche Person mit kurzen lockigen Haaren, einer senfgelben Schürze und einem marineblauen Hemd mit hochgekrempelten Ärmeln repariert einen kleinen roten Tischventilator, dessen Stecker gezogen ist. Von Sekunde 0 bis 3 legt die Person das abgenommene Schutzgitter neben den stillstehenden Ventilator. Von Sekunde 3 bis 7 wischt sie mit einem weichen Tuch Staub von einem Rotorblatt, während die Kamera auf Tischhöhe langsam nach rechts gleitet. Von Sekunde 7 bis 10 legt sie das Tuch ab und richtet das Gitter am Gehäuse aus, ohne den Ventilator einzustecken oder einzuschalten. Fensterlicht macht abgenutztes Metall und die Baumwollstruktur sichtbar. Ton: das Reiben des Tuchs, ein leises Klicken des Gitters und ruhige Raumatmosphäre; keine Sprache und keine Musik. Bewahre dieselbe Person, denselben Ventilator, seine drei Rotorblätter, das rote Gehäuse und das nicht eingesteckte Kabel. Keine rotierenden Rotorblätter, zusätzlichen Werkzeuge, lesbaren Etiketten, Untertitel oder Schnitte.
```

**Variablen:** Schürzenfarbe, Ventilatorfarbe, Raumlicht. **Prüfung:** Der Ventilator bleibt vom Stromnetz getrennt und steht still; die Zahl der Rotorblätter und die Berührung durch die Hände bleiben konsistent. Dies ist ein kreatives Konzept, keine Anleitung für elektrische Reparaturen.

## Wan 3.0 API auf bestimage.ai

Die englischen Modellseiten zeigen die Testoberfläche und öffentliche Anfragebeispiele.

| Modus | Vorbereitung und Zweck |
|---|---|
| [Text zu Video](https://bestimage.ai/models/alibaba/wan-3-0-text-to-video/) | Eine vollständige Szene mit Ursache, Zwischenhandlung und sichtbarem Ergebnis. |
| [Bild zu Video](https://bestimage.ai/models/alibaba/wan-3-0-image-to-video/) | Anfangsbild **und Endbild** für den dokumentierten Modus; Übergang erklären und Geometrie sowie Komposition erhalten. |
| [Referenzen zu Video](https://bestimage.ai/models/alibaba/wan-3-0-reference-to-video/) | Optionale Referenzen für Identität, Objekt, Raum, Bewegung oder Ton; jeder Datei eine Aufgabe zuweisen. |
| [Videobearbeitung](https://bestimage.ai/models/alibaba/wan-3-0-video-edit/) | Ausgangsvideo und eine klar begrenzte Änderung; Darstellung, Dauer, Kamera und unveränderte Bereiche bewahren. |

Der [API-Leitfaden zur Kostenkontrolle](guides/bestimage-wan-3-api.md) erklärt Anfragen, Statusabfragen und die Testplanung. **Der API-Host von bestimage.ai ist `https://api.flaq.ai`.** Verwenden Sie einen API-Schlüssel aus Ihrem bestimage.ai-Konto.

Prüfen Sie Modellseite und Konto, bevor Sie Guthaben verbrauchen. Die genannten Modi entsprechen der Dokumentation von bestimage.ai; nicht jedes Wan-Produkt muss dieselben Einstellungen anbieten.

## GPT Image 2 für Referenzbilder

[GPT Image 2](https://bestimage.ai/models/openai/gpt-image-2/) erzeugt Standbilder; [GPT Image 2 Edit](https://bestimage.ai/models/openai/gpt-image-2-edit/) bearbeitet Bilder und kombiniert visuelle Referenzen. Damit lassen sich Figurenübersichten, Produktreferenzen oder freigegebene Anfangs- und Schlusskompositionen für eine spätere Videoaufgabe vorbereiten.

Dies sind **eigenständige Bildmodelle**, keine Videoschnittstellen von Wan. Exportieren und prüfen Sie die Bilder, bevor Sie diese dem passenden Wan-Modus übergeben. Das Repository automatisiert diese Übergabe nicht und behauptet nicht, dass seine Konzeptbilder mit diesen APIs erzeugt wurden. Siehe den [Arbeitsablauf für Referenzbilder](guides/bestimage-wan-3-api.md#gpt-image-2-reference-frame-workflow).

## Verzeichnis, Leitfäden und Beiträge

Das [Verzeichnis aller 148 Vorlagen](prompts/README.md) erschließt Filmgeschichten, Produkte, nutzergenerierte Inhalte, Essen und Reisen, Sport, Animation, Musik, Dienstleistungen, Wissenschaft, Architektur, Produktion, Handel, Dialoge, Natur und Industrie.

Die Leitfäden zur [Formulierung](guides/prompting-guide.md), zu [Fähigkeiten und Grenzen](guides/model-capabilities.md) und zur [Fehlersuche](guides/troubleshooting.md) sind auf vereinfachtem Chinesisch verfasst. Der API-Leitfaden ist englisch. Ein Konzeptbild belegt weder zeitliche Kontinuität noch Lippensynchronität, Modellgenauigkeit oder die Sicherheit eines dargestellten Ablaufs.

Lesen Sie vor dem Einreichen von Texten oder Medien die [Beitragsrichtlinien](CONTRIBUTING.md). Nennen Sie genaue Einstellungen, Eingaberollen, Nutzungsrechte, Beobachtungen und ehrlich, ob das Beispiel getestet wurde. Teilen Sie keine Zugangsdaten, privaten Dokumente oder ablaufenden signierten Medienlinks. Bereiten Sie die erforderlichen Angaben mit der [Formularvorlage](.github/ISSUE_TEMPLATE/prompt.yml) vor.

## Über bestimage.ai

Das Team von [bestimage.ai](https://bestimage.ai/) kuratiert und pflegt diese Prompt-Sammlung. Sie verbindet praktische kreative Arbeitsabläufe mit APIs für Bild- und Videomodelle.

## Mit dem bestimage.ai Affiliate-Programm verdienen

Veröffentlichen Sie Tutorials, Prompts oder API-Integrationen? Werden Sie Teil des [bestimage.ai Affiliate-Programms](https://bestimage.ai/affiliate-program/) und erhalten Sie Provisionen, wenn Sie bestimage.ai Ihrem Publikum empfehlen.

- **20 %** auf die erste gültige bezahlte Bestellung eines geworbenen Nutzers.
- **10 %** auf dessen weitere gültige bezahlte Bestellungen innerhalb von **60 Tagen nach seiner Registrierung**.

Für berechtigte Bestellungen und Auszahlungen gilt die [aktuelle Affiliate-Vereinbarung](https://bestimage.ai/affiliate-agreement/).

## Lizenz

[MIT](LICENSE).
