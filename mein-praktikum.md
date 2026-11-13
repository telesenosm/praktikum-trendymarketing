# Mein Praktikum bei trendymarketing

Florian, 2. bis 13. November 2026

## Tag 1, Mo 2.11.: Ankommen und die Landkarte

### Landkarte der Werkzeuge

| Werkzeug | Kosten | Schwierigkeit | Wofür |
|---|---|---|---|
| WordPress | teuer | schwer | Um Webseiten zu bauen und zu verwalten |
| Lovable | günstig | leicht | Extrem schnell Webseiten bauen/designen und automatisch coden lassen. |
| Claude Code | kostenlos | leicht | coden und schreiben mit KI-Hilfe |
| Astro | kostenlos | mittel | schnelle Websites bauen |
| n8n | kostenlos | mittel | Workflows automatisieren |
| Make | günstig | leicht | Workflows automatisieren ohne Codes |
| Zapier | günstig | leicht | einfache Autamatisierungen von insbesndere Apps |
| Claude | günstig | leicht | schnelle KI-Antworten zu allem |
| ChatGPT | kostenlos | leicht | schnelle KI-Antworten zu allem |
| Gemini | kostenlos | leicht | schnelle KI-Antworten zu allem |

### Lerntagebuch

**Gelernt:** Was n8n genau ist, wie man einen Workflow erstellt und dass Lovable wortwörtlich Lovable ist

**Schwer:** Aufgrund eines buggs haben die letzten zwei schriftlichen Aufgaben im Test nicht funktioniert. Dafür brauchte ich also überdurchschnittlich lange.

**Frage an Michael:** alle Fragen gestellt ;)

## Tag 2, Di 3.11.: Wie Programme miteinander reden

### Lerntagebuch

**Gelernt:** Ich habe heute gelernt, wie man einen Workflow mit einem Absender und Empfänger inklusive Weiche baut.

**Schwer:** Das enzig schwere waren kleine Schussel-Fehler, die so offensichtlich waren, dass amn sie schon übersehen hat.

**Frage an Michael:** Alle Fragen geklärt :)

**Mitgeschaut:** Zuhören von Terminen mit Michis Kunden und Arbeitskollegen

## Tag 3, Mi 4.11.: Erst planen, dann bauen

### Teil 1 · Pflichtenheft Firmen-Check

**Ziel in einem Satz**
Der Firmencheck ist dafür da, um Webseiten von Firmen zu analysieren und zu checken, um nachzuschauen, wo potenzielle Fehler liegen, das die Kunden abschrecken oder desinteressieren könnten.

**Wer benutzt ihn?**
Nutzer gibt URL ein und bekommt dadurch das Ergebniss der Analyse.

**Eingabe**
Die Webseite-URL, der Firma, die man checken will.

**Ausgabe**
Eine Liste aller Dinge, die potenzielle Kunden abschrecken könnte und desinteressieren könnte. 

**Wo liegen die Daten?**
Die Ergebnisse werden in n8n Datatable gespeichert. Die Mail kommt bei der Person an, die die Analyse durchführen lassen hat.

**Was gehört ausdrücklich nicht dazu?**
-Die Ladezeit zum Beispiel wird nicht automatisch gemessen. Das macht man selbst.
-Es werden auch keine automatischen Lösungsvorschläge genannt.



**Fertig ist er, wenn …**
Kommt die Mail an? Sind die Daten richtig in der Tabelle? Stimmt die Analyse von Claude? 

### Teil 2 · SEO-Prüfung von drei Websites

| Website | Title Zeichen | Description Zeichen | H1 | H2 | Ort | PageSpeed | Angebot klar |
|---|---|---|---|---|---|---|---|
| trendymarketing.de | 44 | 157 | Externer Marketingleiter für&nbsp;inhabergeführte Mittelständler | ja | nicht nötig | 100 | ja |
| http://meinfuss24.de/index.html | 27 | 253 | 0 | nein | nein | 100 | ja |
| https://www.burg-beeskow.de/ | 12 | 308 | 2 | nein | ja | 78 | ja |

### Teil 3 · Deine Checkliste für die KI

**Welche Punkte soll die KI ab morgen prüfen? Ein Punkt pro Zeile.**
-Wenn du auf der Website bist, öffne den Quellentext.
-Suche danach nach dem Title über die Suchfunktion im Quellentext.
-Suche danach nach der Metadiscription über die Suchfunktion im Quellentext.
-Suche danach nach dem H1 über die Suchfunktion im Quellentext.
-Suche danach nach dem H2 über die Suchfunktion im Quellentext.
-Mit diesen von dir gesammelten Informationen aus dem Quellentext stellst du mir eine ausarbeitung der Analyse zusammen.



### Lerntagebuch

**Gelernt:** Wie man eine Webseite mithilfe eines Quellentextes richtig analysiert, was ein Pflichtheft ist und wozu man es braucht.

**Schwer:** Heute hat alles geklappt und es war auch alles ziemlich einfach.

**Frage an Michael:** /

**Mitgeschaut:** /

## Tag 4, Do 5.11.: KI als Baustein

### Mein Prompt für Claude

```
Du bist Analyst bei trendymarketing, einer Agentur für Online-Marketing und KI-Vertriebssysteme. Du bekommst die wichtigsten Daten von der Startseite einer Firma. Daraus schreibst du ein kurzes Briefing für ein Erstgespräch.

Prüfe die SEO-Grundlagen mit dieser Checkliste:
1. -Wenn du auf der Website bist, öffne den Quellentext.
2. -Suche danach nach dem Title über die Suchfunktion im Quellentext.
3. -Suche danach nach der Metadiscription über die Suchfunktion im Quellentext.
4. -Suche danach nach dem H1 über die Suchfunktion im Quellentext.
5. -Suche danach nach dem H2 über die Suchfunktion im Quellentext.
6. -Mit diesen von dir gesammelten Informationen aus dem Quellentext stellst du mir eine ausarbeitung der Analyse zusammen.

Regeln:
- Die Zeichenzahlen und die Anzahl der H1 stehen schon in den Daten. Verlass dich darauf und zähle nicht selbst.
- Erfinde nichts. Was aus den Daten nicht hervorgeht, schreibst du als "nicht erkennbar".
- seo_note ist eine Schulnote von 1 bis 6 für die SEO-Grundlagen.
- seo_schwaechen und ansatzpunkte sind jeweils höchstens drei kurze Sätze.

Antworte ausschließlich mit JSON, ohne Text davor oder danach und ohne Codeblock, genau in diesem Format:
{"firma": "", "branche": "", "angebot": "", "seo_note": 3, "seo_schwaechen": "", "ansatzpunkte": "", "fazit": ""}
```

### Bonus-Test zur Zusatzaufgabe

**1. Drei Fehler von Claude**
1. Webseite: https://www.burg-beeskow.de/ Title ist mit 12 Zeichen deutlich zu kurz (optimal: 50-60 Zeichen): das sagte Claude, er hat zwar recht, dass das deutlich zu kurz ist, aber bei einer Sache hat er unrecht:  Denn optimal sind nur 30-60 Zeichen und nicht ganze 50-60.
2. Webseite: Trendyimmo.de  H1 vorhanden, obwohl mehrere H2-Überschriften existieren. Das hat Claude geschrieben und als negativ empfunden. Obwohl das der absolute optimalfall ist.
3. Webseite: https://www.burg-beeskow.de/ Nur eine H1 vorhanden, obwohl die Seite mehrere thematische Bereiche abdeckt. Das sagte Claude, obwohl es gut ist, wenn eben nur eine H1 existiert.

**2. Warum ist das passiert?**
Es fehlten offensichtlich die Grundinformationen darüber, was genaue Optimalfall ist und was nicht. Außerdehm stehen meine nachgeaddeten Regeln in dem Fall doppelt drinnen. Das überfordert nur, und bringt Claude durcheinander.

**3. Gleiche Firma, gleiche Note?**
Alle Noten waren gleich. Das heißt, alles läuft glatt.

**4. Kosten**
Das passt alles.

**5. Deine seo_note-Prüfung**
Ich habe im zweiten Sabotagetest 50 maximale Tokens benutzt statt 1200. Und das bedeutet, dass automatisch geschaut wird, ob überhaupt Zahl von 1-6 benutzt wurde, oder nicht.

**6. Warum reicht der Prompt allein nicht?**
Da Claude gerne mal Halluziniert oder sich nicht an Regeln hält.

**7. Denkaufgabe**
mit solch einem eingebautem Node ( if ) der dann prüft, ob alles übereinstimmt. denn wenn nicht, dann iwird abgebrochen.

### Lerntagebuch

**Gelernt:** Ich habe heute gelernt, welche Regeln in einen Prompt gehören und wieso, was die üblichen neuen Begriffe bedeuten und wie man in einem Workflow eine richtige, automatisierte Website-Checkliste baut.

**Schwer:** Heute hat ausnahmsweise mal alles geklappt, nur bei einigen Dingen, die bei n8n nicht wirklich funktioniert haben, musste ich KAI fragen


**Frage an Michael:** keine offenen Fragen :)

**Mitgeschaut:** /

## Tag 5, Fr 6.11.: Speichern und zurückschicken

### Test mit zehn Firmen

| Website | Mail angekommen? | SEO-Note | Auffällig bzw. Fehlercode |
|---|---|---|---|
| https://claude.ai | Fehler-Mail | / | Fehler 403 |
| https://www.shutterstock.com | Fehler-Mail | / | Fehler 403 |
| https://www.meta.com | ja | 4 | / |
| https://www.facebook.com | ja | 6 | Angebot nicht erkennbar |
| https://www.instagram.com/ | ja | 5 | Keine H1-Überschrift vorhanden |
| https://github.com/ | ja | 4 | Title ist zu lang (70 Zeichen) und enthält redundante Keywords ('GitHub' dreifach |
| https://lovable.dev | Fehler-Mail | / | Fehlercode 403 |
| https://schwamm.de/ | ja | 5 | Meta-Description fehlt komplett (0 Zeichen). |
| https://www.wdrmaus.de/ | ja | 4 | Title ist mit 28 Zeichen sehr kurz und nutzt das SEO-Potenzial nicht aus (optimal: 50-60 Zeichen). Es fehlen H2-Überschriften zur Strukturierung der Inhalte. Die Meta-Description könnte prägnanter formuliert werden, um mehr Klicks zu generieren. |
| https://www.zdf.de/ | ja | 2 | Title ist mit 62 Zeichen optimal, Meta-Description mit 150 Zeichen gut strukturiert. Nur eine H1 vorhanden, was SEO-Standards entspricht. H2-Überschriften sind jedoch eher Inhaltsbezeichnungen als strukturelle Hierarchie-Elemente. |

### Wochenrückblick

**Was war diese Woche am schwersten?**
In dieser Woche waren die freien Antworten in den Lextionstests am schwersten!

**Was hat am meisten Spaß gemacht?**
Auf jeden Fall das Bauen der ganzen Workflows.

**Was soll in Woche 2 anders laufen?**
Es kann von mich aus alles so bleiben, wie es ist!

### Bonus-Fragen zur Zusatzaufgabe

**1. Wo gehört der Doppelt-Check hin?**
Sicherlich vor Claude analysiert, denn dann kostet Claude kein geld, da es ja automatisch nichts zu tun hat.

**2. Was passiert mit einer Firma, die schon in der Tabelle steht?**
Ja, Michael bekommt eine Mail. Das ist nicht gut, da doppelte Checks nur Verwirrung stiften.

**3. Denkaufgabe**
Ja, es wird erkannt.

### Lerntagebuch

**Gelernt:** Ich habe heute gelernt, wie man einen Worklfow reitheoretisch so erweitern kann, wie man will.

**Schwer:** Heute waren die letzten beiden Lextionsaufgaben mit Abstand am schwersten.

**Frage an Michael:** Keine offenen Fragen :)

**Mitgeschaut:** /

## Tag 6, Mo 9.11.: Design ist eigene Arbeit

### Warum so

**Überschrift der Seite**
Wie gut ist diese Website wirklich?

**Unterzeile**
Der Firmencheck wird durchgeführt.

**Beispiel im Eingabefeld**
baeckerei-mueller.de  (bitte gewünschte url hier eingeben) 

**Text auf dem Knopf**
Firmencheck durchführen 

**Meldung nach dem Absenden**
Danke, das Briefing kommt in etwa einer Minute per Mail. 

**Look in einem Satz**
 ruhig, viel Weißraum, große Schrift, Lila als Grundfarbe, Orange nur für den Knopf.

**Warum so? Begründe deine zwei wichtigsten Entscheidungen**
Die Farben: Man kann unterscheiden, was einen Informationen, Hinweise und Tipps liefert (lila) und welche Felder zum interagieren da sind (orange)
Die signalisierte Überschrift: Die Überschrift sollte groß, dick und in einer anderen Schrift geschrieben sein, weil das zeigt und verdeutlicht, dass das eine Überschrift ist.

### Deine Test-URL aus n8n

**Test-URL vom Webhook**
https://trendymarketing.app.n8n.cloud/webhook-test/firmen-check

### Lerntagebuch

**Gelernt:** Heute habe ich gelernt, wie man auf Lovable eine Website baut und diese anschließend mit n8n verbindet.

**Schwer:** Es gab Schwierigkeiten beim verstehen gewisser Teile der Anleitung.

**Frage an Michael:** Keine Fragen offen :)

**Mitgeschaut:** /

## Tag 7, Di 10.11.: Live gehen

### SEO-Prüfung deiner Seite

| Website | Title Zeichen | Description Zeichen | H1 | H2 | Ort | PageSpeed | Angebot klar |
|---|---|---|---|---|---|---|---|
| https://firmen-check-neu.vercel.app/ | 65 | 142 | Kostenlose Website-Analyse & SEO-Check  (1) | ja | nein | ~90–98 / 100 | ja |

### Kostenrechnung

Ein Check: 0.45 Cent. 100 Checks im Monat: 0.45 Dollar für Claude. Feste Kosten: n8n ? Euro, Vercel ? Euro, Lovable ? Euro.

### Lovable oder Claude Code?

**Was war an Lovable gut, was hat dich gestört?**
Es war sage und schreibe alles gut und es hat mich nichts gestört.

**Michael erklärt dir Claude Code. Was wäre damit anders gewesen, beim Tempo, bei den Kosten und bei der Kontrolle?**
Bei den kosten: Es gehen kosten bei jedem kleinen Schritt drauf
Was wäre anders gewesen: Claude Code würde dir den kompletten Code direkt schreiben und erklären, statt dass du eine visuelle Oberfläche hast wie bei Lovable. Du müsstest den Code dann selbst in GitHub hochladen und verwalten, hättest aber mehr Kontrolle über jede Zeile. Lovable macht das automatisch für dich und verbindet sich direkt mit GitHub, das ist für dein Praktikum einfacher und schneller

**Was würdest du beim nächsten Projekt nehmen, und warum?**
Auf jeden Fall Lovable, weil es intigrierte Vorschläge mit beinhaltet und voll Automatisch läuft.

### Lerntagebuch

**Gelernt:** Ich habe heute gelernt, wie man eine Webseite auf Lovable mit Vercel und GitHub verbindet und was man damit anfangen kann.

**Schwer:** Heute hatten wir beim verbinden Schwierigkeiten. Sonst lief alles top.

**Frage an Michael:** Keine offenen Fragen :)

**Mitgeschaut:** /

## Tag 8, Mi 11.11.: Sicherheit

### Sicherheitsprotokoll

**Was hast du vor der Absicherung in den Entwicklertools gesehen?**
Beim Durchlauf habe ich POST und GET gesehen.

**Was kam beim Aufruf ohne Schlüssel zurück?**
Problem in node ‘Angriff‘  Forbidden - perhaps check your credentials?

**Was passiert, wenn du „hallo“ ins Formular schreibst?**
Da steht dann als Fehlermeldung: Das sieht nicht wie eine Website-Adresse aus.

**Hat ein normaler Check danach noch funktioniert?**
ja

**Welche Schichten schützen den Firmen-Check jetzt, und wovor?**
Der Türsteher (Vercel) schützt jetzt den "Eingang" vor Angriffen

### Lerntagebuch

**Gelernt:** Heute habe ich gelernt, wie man Vercel in seinen Workflow mit einbaut und als Türsteher einstellt.

**Schwer:** Es gab mehrere Fehlermeldungen bei bestimmten Bereichen. Zum schluss hat aber alles geklappt und darauf kommt es an.

**Frage an Michael:** Keine offenen Fragen :)

**Mitgeschaut:** /

## Tag 9, Do 12.11.: MCP und Puffer

### Das Experiment

**Was hat Claude schneller geschafft als du?**
Claude hat das bauen des Firmen-Checks in n8n schneller gemacht.

**Wo lag Claude falsch oder hat etwas anders gemacht?**
-Statt ein Webhook-Trigger hat Claude ein Formular-Trigger benutzt
-Der Data-Table-Node heißt nicht "Node schon geprüft?", sondern "Schon geprüft?"
-Nach dem Node "Wichtiges auslesen", hat Claude zwei andere Nodes benutzt: "Fakten sammeln" und "SEO-Regeln prüfen".
-Den Anthrophic-Node hat Claude nich "Claude analysiert" genannt, sondern "Claude schreibt Briefing".
-Nach dem Anthrophic-Node hat Claude einen Node namens "Antwort prüfen" benutzt, statt "Antwort auspacken".
-In all den Fehlermeldungen steht davor jetzt noch "[Claude-Nachbau] Firmen-Check: Website nicht erreichbar"

**Was hättest du vor zwei Wochen nicht gemerkt?**
Alles, da ich dort den Workflow noch nicht gebaut hatte :D

### Deine Präsentation, höchstens 10 Minuten

**1. Das Problem**
Der Firmen-Checck löst mit einer der größten Probleme, die Michael hat. Seine Zeit. Statt selbst auf Webseiten zu gehen und unnötig lange die nötigen Daten für die SEO-Grundlagen zu filtern, kann er nun einfach seine beliebige Webseite in das Eingabefekd einsetzen und innerhalb unter einer Minute eine komplette, fertig gestellte Auswertung per Mail bekommen.

**2. Die Lösung**
Du trägst deine Webseite in das Eingabefeld ein, das URL wird an n8n geschickt und von Claude wird die Webseite analysiert. Danach geht die Auswertung an deine eigene Email-Adresse raus.

**3. Live-Demo mit dieser Firma**
https://www.nike.com/de/

**4. So funktioniert es**
Der Workflow funktioniert so: In der Webseite kommt eine Url rein. das ist das "GO" für den Webhook-Trigger (der Auslöser). Dann wird durch "Adresse aufräumen" die URL gereinigt. Danach wird durch den Node "node schon geprüft?" in die Datatable geschaut, ob die Webseite schonmal geprüft wurde. Danach wird durch "Webseite holen" im Internet geprüft, ob es die Webseite überhaupt gibt. Wenn nicht, dann wird eine Mail mit der Fehlermeldung: "Firmen-Check: Website nicht erreichbar" abgeschickt. Wenn es aber keine Probleme gibt, werden durch den Node "Wichtiges auslesen" alle nötigen Daten für die SEO-Analyse aus der Seite gefiltert. Dann werden die Daten durch den Node "für Claude vorbereiten" wieder gefiltert. Danach gelangen die Daten zum Node: "Claude analysiert" und wie es der Name schon sagt, werden die Daten von Claude entgültig analysiert. Danach gehen die analysierten Daten zum Node: "Antwort auspacken". Dort werden die von Claude analysierten Daten ausgespuckt. Dann kommt eine Node mit einer Weiche ins Spiel die "Analyse ok?" heißt. Dort wird analysiert, ob bei der Analyse fehler von Claude gemacht wurden, oder nicht. Wenn alles glatt lief, werden die Daten in der Tabelle gespeichert und das Briefing wird per Mail an den Kunden geliefert. Aber wenn Fehler entdeckt wurden, wird eine Mail mit der Fehlermeldung "Firmen-Check: Analyse fehlgeschlagen" rausgeschickt.

**5. Was ich gelernt habe**
Ich habe gelernt, wie man mit Lovable und n8n eine vollautomatische Website-Analyse baut.

**6. Was schwer war und wie ich es gelöst habe**
Eigentlich war nichts wirklich "schwer".

**7. Was ich als Nächstes bauen würde**
Als nächstes würde ich gerne eine App und eine Webseite bauen, in der es darum geht, dass man eine beliebige Social-Media-App auswählt und dort per Zahlung und Knopfdruck einen Craeler auf die App schickt. Der filtert dann anutomatisch nach Dingen, die grade im Trend sind. Und jenachdem, was er sonst noch alles filtern soll, bezahlt man dann ebend dementsprechend mehr.

### Lerntagebuch

**Gelernt:** Heute habe ich gelernt, wie man ein eigen-gebautes Projekt mit einer Kopie von Claude vergleicht.

**Schwer:** Heute hat wiedermal alles geklappt :D

**Frage an Michael:** Keine offenen Fragen :D

**Mitgeschaut:** /

