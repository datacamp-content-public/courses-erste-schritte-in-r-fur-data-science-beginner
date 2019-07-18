---
title: 'Wie R funktioniert'
description: 'Mit kleinen Schritten zu den Basics in R'
free_preview: true
---

## Hallo und herzlich Willkommen!

```yaml
type: NormalExercise
key: 5d0fa43d72
xp: 100
```

Sie sind unser/e neue/r Mitarbeiter/in in dem **Team Business Intelligence & Data Analytics der Bambergus Airuber GmbH**, einem Unternehmen das Segelflieger und Motorenflugzeuge produziert und verkauft. Um neue Geschäftsfelder zu erschließen wurde die Firma Airuber GmbH Anfang Q1 2019 akquiriert. Die Firma entwickelt Paketdrohnen und wird ins Stammunternehmen eingegliedert. Sie sollen im Zuge der Akquisition erste Umsatzzahlen analyisieren, bei Fragen und Problemen zur Datenintegration aushelfen und einen Report erstellen. 

Im Zuge dieser Anforderungen befassen Sie sich mit der Programmiersprache R, da sich diese für die statistische Auswertung besonders gut eignet, frei zugänglich ist und in Ihrem Team damit vorrangig gearbeitet wird. 

![Inhalt_l](https://assets.datacamp.com/production/repositories/5035/datasets/85c15e1bd4babd4fceb2be3825e291fc99348dc9/Inhalt_l%C3%A4ngs.PNG)

`@instructions`
Ihr Chef Herr Müller ist mit der Akquisition sehr beschäftigt und hat für Sie direkt verschiedene Aufgaben, die zeitnah erledigt werden müssen. Lassen Sie uns beginnen!

- Wir fangen mit einem kleinen Testprogramm an, sodass Sie mit der Console vertraut werden:
	- Dafür schreiben Sie bitte: **print("Start!")** in das Skript und drücken bitte auf 'Submit Answer'.

`@hint`
Keine Angst - einfach ```
print("Start!")
``` in das Skript schreiben und auf 'Submit Answer' drücken.

Im Bereich **Instruktionen** bekommen Sie ihre Aufgabe, die Sie auch mit Unterstützung dieser Hints lösen sollen.

**script.R** ist ihre Kommandozeile mit der Sie Ihre Befehle und Ihren Code in der Programmiersprache R eingeben, die in der Console darunter ausgegeben werden.

`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
# Ihr erstes Programm:

```

`@solution`
```{r}
# Ihr erstes Programm: "Start!"
print("Start!")
```

`@sct`
```{r}
ex() %>% check_output("Start!", fixed=TRUE, missing_msg= "So ist das nicht ganz richtig. Beachten Sie Fehler im Code und auch mögliche Tippfehler. R ist eine case sensitive Programmiersprache!")
success_msg("Ihr erstes Programm ist vollendet - Gut gemacht! Nun geht es richtig los!")
```

---

## Rechnen mit R

```yaml
type: TabExercise
key: c09b1c46a5
xp: 100
```

R kann in seiner Basisfunktion als Rechner verwendet werden. Beachten Sie folgende arithmetische Rechenoperatoren:	 

Nützliche Operatoren:
```
 Addition: + 
 Subtraktion: - 
 Multiplikation: *
 Division: / 
 Potenzierung: ^
 Modulo: %%
```

`@pre_exercise_code`
```{r}

```

***

```yaml
type: NormalExercise
key: 20b1df54bc
xp: 50
```

`@instructions`
- 1. Sie sollen die Umsätze der letzten drei Monate der Bambergus Airuber GmbH errechnen und somit den Umsatz für das Quartal Q1 2019 erstellen und analysieren, wie sich der Umsatz durch den Zukauf entwickelt hat.

```
Umsatz in €: Januar 2500000 | Februar 2780000 | März 3200000
```

Beachten Sie, dass es Unterschiede in den Zeilen gibt - sie beinhalten Code und mit dem **'#'** werden Kommentare gekennzeichnet.

`@hint`
Stellen Sie sicher, dass Sie die Summe aus ```
2500000 + 2780000 + 3200000 
``` in einer neuen Zeile eingefügt haben. Starten Sie die Zeile nicht mit einem '#'-Zeichen, ansonsten wird der geschriebene Code nicht wie gewünscht ausgeführt, da damit Kommentare gekennzeichnet werden!

`@sample_code`
```{r}
# 1.Quartalsumsatz Q1:

```

`@solution`
```{r}
# Quartalsumsatz Q1:
2500000 + 2780000 + 3200000
```

`@sct`
```{r}
#ex() %>% check_output(145, fixed=TRUE, missing_msg= "So ist das nicht richtig - Sie müssen sich verrechnet haben!")
ex() %>% check_output(8480000, fixed=TRUE, missing_msg="Sie müssen sich verrechnet haben. Beachten Sie auch mögliche Tippfehler!")
success_msg("Ja, genau - der Umsatz im ersten Quartal beträgt 8480000€!")
```

***

```yaml
type: NormalExercise
key: c6b8ec88ac
xp: 50
```

`@instructions`
- 2. Die Umsätze steigen laut Prognose im Quartal Q2 2019 aufgrund der verzögerten, aber positiven Marktresonanz der Drohnen um **2.2% im Monat**. Welches realistische Umsatzziel geben Sie für das Ende Q2 2019 ab? Nehmen Sie den Ausgangswert von **8480000** am Ende von Q1 2019 an.

`@hint`
Beachten Sie, dass das Wachstum von 2.2% **im Monat** stattfindet und ein Quartal aus drei Monaten besteht. Hier kommt die Zinzeszinsrechnung zur Einsatz - ein exponentielles, kein lineares Wachstum! Achten Sie auch auf die richtige Umrechnung der Prozentzahl.

![Zinseszinsformel](https://assets.datacamp.com/production/repositories/5035/datasets/0e7c37e673c699f3cd9b26cf769aca5676d94a6c/ZInseszinsformel.PNG)

Beachten Sie, dass in R anstatt dem Komma als Dezimaltrennzeichen der Punkt verwendet wird!

`@sample_code`
```{r}
# Umsatzprognose Q2

```

`@solution`
```{r}

8480000*(1.022^3)
```

`@sct`
```{r}
ex() %>% check_output(9052083, fixed=TRUE, missing_msg="So ist das nicht ganz richtig - haben Sie jeweils das monatliche Umsatzwachstum für das Quartal berechnet?")
success_msg("Richtig - die Zinsen wachsen exponentiell an! Und nun zum nächsten Inhaltsblock - den Variablen! (1/6 abgeschlossen)")
```

---

## Variablen

```yaml
type: NormalExercise
key: 57b9e61b19
xp: 100
```

Ein grundlegendes Konzept in der (statistischen) Programmierung sind Variablen. Eine Variable ermöglicht es einen Wert (z.B. 8) oder eine Zeichenkette (z.B. "Funktionsbeschreibung") in R zu speichern. Später können Sie den Namen der Variablen nutzen, um einfach auf den Wert oder das Objekt zuzugreifen.

- Beispiel: So können Sie der Variable my_var den Wert 8 zuweisen: ```
my_var <- 8
```

![Variablen vergleichen](https://assets.datacamp.com/production/repositories/5035/datasets/31809ce821fec1a9a0931f929b8f83aa4bfb34a0/Variablen%20vergleichen.PNG)

`@instructions`
Ist es richtig, dass das letzte Halbjahr 2018 erfolgreicher war als das Halbjahr 2019 sich zu entwickeln scheint, wie Herr Müller vermutet, da die Kunden mit dem Kauf der Paketdrohnen zögern und ein Forderungsausfall sich in Q1 2019 auch negativ auf den Umsatz auswirkt?

1. Um besser die Werte vergleichen zu können, ordnen Sie bitte die Quartalszahlen aus **2019 Q1: 8480000** und **Q2: 9052083** den Variablen **x** und **y** zu.

2. In der Variable **z** wurden die Quartalszahlen aus **Q3 & Q4 2018** bereits hinterlegt und zugewiesen. Überprüfen Sie die Vermutung von Herrn Müller und lassen Sie sich bzgl. der Aussage einen booleschen Wert (TRUE oder FALSE) ausgeben.

`@hint`
Schauen Sie bitte in die Exercisebox. Hier ist die Zuweisung anhand eines Beispiels verdeutlicht. Lesen Sie bitte genau die Instruktionen. Der Wert für Variable z wurde bereits im System hinterlegt und der Variable z zugewiesen. 

Entwickeln Sie den Code so, dass ein boolescher Wert (TRUE oder FALSE) ausgegeben wird.

`@pre_exercise_code`
```{r}
z <- 15550000
```

`@sample_code`
```{r}
# 1.Q1:

# Q2

# 2.Vergleich der halbjährlichen Umsätze aus 2018 und 2019: 

```

`@solution`
```{r}
# Q1
x <- 8480000
# Q2
y <- 9052083
# 2.Vergleich der Umsätze
z > (x+y)
```

`@sct`
```{r}
ex() %>% check_object("x") %>% check_equal(8480000)
ex() %>% check_object("y") %>% check_equal(9052083)
ex() %>% check_output("FALSE", fixed=TRUE, missing_msg= "Da haben Sie etwas falsch verglichen bei Aufgabe 2 oder die Aussage von Herrn Müller nicht konkret überprüft!")
success_msg("Ja, genau. Es sieht so aus als hätten Sie die Variablenzuweisung verstanden und Herr Müller lag mit seiner Prognose falsch. Kommen wir zum nächsten Inhaltsblock, den Datentypen (2/6 abgeschlossen)")
```

---

## Datentypen in R

```yaml
type: TabExercise
key: b704b35535
xp: 100
```

R arbeitet mit zahlreichen Datentypen und ist sensitiv auf Groß- und Kleinschreibung. Einige der grundlegendsten Datentypen sind:

![Datentypen](https://assets.datacamp.com/production/repositories/5035/datasets/191a79dc42ee4882a386eb662bea0623f92ba0bb/Basisdatentypen_%C3%9Cbersicht_final.PNG.png)

**Wichtig:** Zeichenketten werden in "Anführungszeichen" gesetzt.

Von der Tochtergesellschaft hat Ihr Chef Herr Müller einen Datensatz der Mitarbeiter angefordert, um einen Überblick über die hinzugewonnen Mitarbeiter und deren Personaldaten zu bekommen. Er sagt Ihnen, dass die Mitarbeiter dort noch nicht vertraut mit dem kürzlich eingeführten ERP-System seien und Fehler bei den Datentypen, die im Zuge der Datenintegration wahrscheinlich passiert sind, schon aufgefallen seien. Deswegen sollen Sie sich nun mit den Personaldaten und den Datentypen beschäftigen.

`@pre_exercise_code`
```{r}
Anzahl_Mitarbeiter <- "Fabian Jung"
```

***

```yaml
type: NormalExercise
key: 0d1ead9f62
xp: 50
```

`@instructions`
Schauen Sie sich bitte zuerst den Datentyp an.
- 1. Die Variable **Anzahl_Mitarbeiter** müsste natürlich ein numerischer Basisdatentyp sein. Überprüfen Sie dies bitte, da dort in letzter Zeit häufig Fehler aufgetreten sind.

`@hint`
Schreiben Sie bitte den Code so, damit als Output ein boolescher Wert (TRUE oder FALSE) ausgegeben wird! Schauen Sie in die Übersichtstabelle in der Zeile **Abfrage (Query)** nach.

`@sample_code`
```{r}
#1.Überprüfung Datentyp Anzahl_Mitarbeiter:

```

`@solution`
```{r}
#1.Überprüfung Variable Anzahl_Mitarbeiter:
is.numeric(Anzahl_Mitarbeiter)
```

`@sct`
```{r}
ex() %>% check_output(c(FALSE, "character"), fixed=TRUE, missing_msg= "Da stimmt etwas nicht. Schreiben Sie bitte den Code so, damit als Output ein boolescher Wert ausgegeben wird! Beachten Sie weiterhin die case sensitivität von R")
success_msg("Super, es ist keine numerische Variable hinterlegt, da muss bei der Datenintegration der Tochtergesellschaft etwas falsch zugewiesen worden sein!")
```

***

```yaml
type: NormalExercise
key: e8d49fb162
xp: 50
```

`@instructions`
Da ist wohl bei der Datenintegration im System etwas mit der Zuordnung schief gelaufen.
- 2. Lassen Sie sich bitte die Variable **Anzahl_Mitarbeiter** ausgeben. Wenn nicht die Anzahl von **17** hinterlegt ist, tun Sie dies bitte. 

Klicken Sie zur Zwischenausgabe auf 'Run Code'.

`@hint`
Eine Zuweisung (<-) funktioniert mit diesem Zeichen in R. Weisen Sie der Variablen den numerischen Wert 17 zu.

`@sample_code`
```{r}
#1.numerische Variable?
is.numeric(Anzahl_Mitarbeiter)
#Den Befehl class(Anzahl_Mitarbeiter) können Sie auch verwenden. Durch ihn wird direkt der Datentyp ausgegeben.
#Ausgabe
print(Anzahl_Mitarbeiter)
#2.Zuweisung:

```

`@solution`
```{r}
#2.1 Ausgabe und ggf. neue Zuweisung
print(Anzahl_Mitarbeiter)

Anzahl_Mitarbeiter <- 17
```

`@sct`
```{r}
ex() %>% check_code(c("Anzahl_Mitarbeiter<-17", "17->Anzahl_Mitarbeiter"), fixed=TRUE, missing_msg= "Nicht richtig. Schreiben Sie bitte den Code so, damit als Output 17 ausgeben wird!")
success_msg("Super, nun ist der richtige Wert zugewiesen worden!")
```

---

## Datentypen (Q)

```yaml
type: PureMultipleChoiceExercise
key: dbbb20e7e4
xp: 50
```

Sie sehen in der Personaldatenbank, dass die Büronummern der Mitarbeiter nicht einheitlich gepflegt sind. Welchen Datentyp würden Sie für die Büronummern, z.B. ```
Air2/03.077
``` 
verwenden?

- 1: einen booleschen Datentyp (logical).
- 2: eine Ganz- oder Fließkommazahl (numeric).
- 3: eine Zeichenkette (character).
- 4: eine Kategorie (fact).

_Sie können den Tipp (HINT) wählen, um eine erneute Übersicht zu bekommen._

`@hint`
Hier haben Sie noch einmal eine Übersicht mit Beispielen. 

- zu 1: Boolesche Werte: TRUE, FALSE
- zu 2: Ganzzahlen: 1; 1.5
- zu 3: Zeichenkette: "Hallo", "09:45 Uhr"
- zu 4: Kategorie: A

`@possible_answers`
- 1
- 2
- [3]
- 4

`@feedback`
- Nicht richtig, da liegen Sie völlig falsch. Boolesche Werte geben als Ausgabe nur TRUE oder FALSE Werte.
- Leider nicht richtig, es kommen Zahlen vor, jedoch nicht ausschließlich!
- Richtig - eine Zeichenkette (character) eignet sich hier als Datentyp, da sowohl Zahlen als auch Buchstaben vorkommen und bei Zeichenketten/Strings eine Zuordnung möglich ist. Sie haben schon einiges erledigt - die Hälfte haben Sie geschafft **(3/6 abgeschlossen)!** Weiter geht es nun mit **Vektoren!**
- Leider nicht richtig, überlegen Sie noch einmal! Nein es ist keine Kategorie. Korridore z.B. B könnten mit dem Datentyp fact bezeichnet werden.

---

## Vektoren

```yaml
type: TabExercise
key: 72efcbb708
xp: 100
```

Ein Vektor ist die einfachste Datenstruktur in R. Als "einzelnes Objekt, das aus einer Ansammlung von Daten besteht" wird ein Vektor im R-Handbuch definiert. Wir behandeln in dieser Einheit zum Einstieg nur numerische Vektoren, also Vektoren, die alle Arten von Zahlen enthalten können.

Um einen Vektor mit einer Folge von Zahlen von 1 bis 3 zu erzeugen, gehen Sie wie folgt vor:

```
c(1,2,3) oder kürzer c(1:3)


Wichtige Befehle:

str(): Typ eines Vektors bestimmen u. Überblick verschaffen.

mean(): Durchschnitt ausrechnen.
```

`@pre_exercise_code`
```{r}
service.time <- c(8,8,8,8,9,6)
revenue.day <- c(21600, 28000, 33600, 37600, 45990, 19800)
revenue.tenfridays <- c(38300, 40800, 43300, 44100, 44900, 46500, 47900, 48400, 49800, 55900)
```

***

```yaml
type: NormalExercise
key: 22b76c6200
xp: 35
```

`@instructions`
Nachdem Sie nun die Personaldaten analysiert und die Fehler darin behoben haben, sollen Sie sich nun dem neu administrierten Kundencenter widmen.

Da sich verschiedene Kunden über die Öffnungszeiten und die lange Wartezeit beschwert haben, suchen Sie bitte den längsten Servicetag heraus, da dieser Tag erst um eine Stunde verlängert wurde und die Auslastungsrate zurzeit noch gering ist. 

- 1. Erstellen Sie dazu zuerst einen Vektor, der die Zahlen von 1 bis 6 beinhaltet und weisen Sie ihm bitte den Variablennamen **open.vec** zu. Die Zahlen stehen jeweils für einen Servicestag (1 = "Montag").

`@hint`
Schauen Sie bitte in die Exercisebox. Dort sind konkrete Beispiele gegeben, die Ihnen weiterhelfen!

`@sample_code`
```{r}
# Servicetage

```

`@solution`
```{r}

open.vec <- c(1:6)
```

`@sct`
```{r}
ex() %>% check_object("open.vec") %>% check_equal("c(1,2,3,4,5,6)", "c(1:6)", fixed=TRUE, missing_msg="So ist das nicht ganz richtig!")
success_msg("Ja, genau!")
```

***

```yaml
type: NormalExercise
key: d34d6e1231
xp: 35
```

`@instructions`
- 2. In dem Vektor **service.time** ist die Zeit für jeden Servicetag hinterlegt. Verschaffen Sie sich bitte einen Überblick über den Vektor und wann zeitlich der längste Servicetag ist.

`@hint`
Die Funktion **str()** haben Sie in der Kontextbeschreibung gegeben.

`@sample_code`
```{r}
#Servicezeit

```

`@solution`
```{r}

str(service.time)
```

`@sct`
```{r}
ex() %>% check_code(c("str(service.time)", "service.time"), fixed=TRUE, missing_msg="Verwenden Sie bitte die Funktionen aus der Kontextbeschreibung!") 
success_msg("Ja, genau. Die Funktion str() ist sehr hilfreich und verschafft Ihnen einen guten Überblick über einen Vektor und die darin enthaltenen Servicezeiten.")
```

***

```yaml
type: NormalExercise
key: d114af75ea
xp: 30
```

`@instructions`
Am Freitag bietet das Kundencentercenter seit zehn Wochen 9h anstatt 8h ihre Leistungen an, um den Kundennachfragen gerecht zu werden. Sie haben die Umsatzdaten der zehn neunstündigen Freitage aus dem ERP-System aufbereitet und in die Variable **revenue.tenfridays** abgelegt. Im ERP-System finden Sie den Branchenbenchmark, der aussagt, dass ein Kundencenter ihrer Größe **5000€ durchschnittlichen Umsatz pro Stunde** erwirtschaften muss, um als profitabel angesehen zu werden. 

- 3. Welchen **stündlichen** Umsatz erwirtschaftet das Center **seit der Umstellung** auf den neunstündigen Freitag? Lassen Sie sich bitte mit einer Codezeile den konkreten Wert ausgeben, da dieser direkt an das Management des Kundencenters übermittelt wird.

`@hint`
Denken Sie nicht kompliziert - es wird der Durchschnitt des Vektors benötigt und dann müssen Sie noch eine einfache Division durch 9h durchführen, um auf den stündlichen Umsatz zu kommen - tun Sie dies bitte alles in einem Codekommando.

`@sample_code`
```{r}
# Durchschnittlicher stündlicher Freitagsumsatz

```

`@solution`
```{r}
mean(revenue.tenfridays)/9
```

`@sct`
```{r}
ex() %>% check_output(5110, fixed=TRUE, missing_msg="Nicht richtig, da haben Sie sich verrechnet oder einen Fehler im Code! Haben Sie den stündlichen Umsatz berechnet oder den durchschnittlichen Umsatz der neunstündigen Freitage?")
success_msg("Richtig. Am neunstündigen Freitag wurden 5110€ Umsatz pro Stunde erwirtschaftet. Dies ist als gerade so profitabel anzusehen! Ein dickes Lob an Sie, Sie lernen schnell - nur noch 2 kurze Einheiten (4/6 abgeschlossen)")
```

---

## Matrizen

```yaml
type: TabExercise
key: b0d2909445
xp: 100
```

Matrizen sind rechteckige, zweidimensionale Anordnungen von Elementen, ähnlich wie Tabellen. In R können Matrixoperationen einfach und effizient durchgeführt werden. Anhand von Matrizen können im Gegensatz zu Vektoren nun mehrere Zeilen in ein und derselben Matrix des gleichen Datentyps gespeichert werden (de Vries/Meys 2018).

Vektoren in einer Matrix zusammenführen: 
- **rbind():** Funktion mit der Vektoren zu Zeilen ein und derselbe Matrix zusammengefügt werden können.   
  ```
  Matrix <- rbind(Vektor, Vektor)
  ```
- **cbind():** Funktion mit der Vektoren als Spalten zu einer Matrix zusammengefügt werden.

Werte einer Matrix ersetzen:
- Um den Wert in der dritten Zeile und zweiten Spalte der Matrix zu 5 zu ändern: ```
my.matrix[3,2] <- 8
```

Zeilen- und Spaltennamen verändern: 

- Zeilennamen verändern: Bsp. ```rownames(Matrix) <- c("Region", "Umsätze")```

- Spaltennamen verändern: Bsp. ```
colnames(Matrix) <- c("Januar", "Februar")
```

`@pre_exercise_code`
```{r}
report.weeksales <- matrix(1:18, ncol=6)
report.final <- matrix(1:18, ncol=6)
sell.time <- c(8,88,8,8,9,6)
revenue.day <- c(21600, 28000, 33600, 37600, 45990, 19800)
average.byday <- c(21600/8, 28000/8, 33600/8, 37600/8, 45660/9, 19800/6)
report.final <- rbind(sell.time, revenue.day, average.byday) 
```

***

```yaml
type: NormalExercise
key: b49123677e
xp: 50
```

`@instructions`
Herr Müller bittet Sie einen Wochenreport mit dem Variablennamen **report.weeksales** für das Kundencenter zu erstellen.

- 1. Ihre Aufgabe ist es eine Matrix aus den Vektoren **sell.time und revenue.day** zu erstellen und der Variablen vom Typ Matrix **report.weeksales** zuzuordnen.

`@hint`
Schauen Sie bitte in die Exercisebox und verwenden Sie bitte eine Funktion, um Zeilenvektoren zusammen zu führen und verweisen (<-) Sie diese auf report.weeksales.

`@sample_code`
```{r}
# report.weeksales

```

`@solution`
```{r}

report.weeksales <- rbind(sell.time, revenue.day)
```

`@sct`
```{r}
ex() %>% check_code(c("report.weeksales <- rbind(sell.time, revenue.day)", "rbind(sell.time, revenue.day) -> report.weeksales"), fixed=TRUE, missing_msg="Da stimmt etwas bei dem Erstellen der Matrix nicht. Verwenden Sie bitte die Funktionen aus der Kontextbeschreibung!") 
success_msg("Ja, genau - Schauen Sie sich gern Ihre selbst erstellte Tabelle an!")

#ex() %>% check_object("report.weeksales") %>% check_equal("rbind(sell.time, revenue.day)", fixed=TRUE, missing_msg="So ist das nicht ganz richtig!")
#success_msg("Ja, genau!")
```

***

```yaml
type: NormalExercise
key: 18ef5dab58
xp: 50
```

`@instructions`
Sie haben den Report Herrn Müller übergeben. Er lässt Ihnen die Nachricht zukommen, ob Ihnen aufgefallen sei, dass sich ein Zahlenfehler eingeschlichen hat. Sie müssen das nächste Mal genauer die Werte kontrollieren, bevor Sie den Report an das Management übergeben.

- 2. Lassen Sie sich den erstellten Report (**report.weeksales**) einmal in der Console ausgeben und korrigieren Sie ihn anschließend bitte.

`@hint`
Haben Sie den falschen Wert entdeckt, ein Tag hat nur 24h! - Alles darüber ist natürlich falsch - statt 88h muss hie reine 8 stehen. report.weeksales[Zeile, Spalte] <- Wert

`@sample_code`
```{r}
# report.weeksales
report.weeksales <- rbind(sell.time, revenue.day)
# Ausgabe (Click 'Run Code')
print(report.weeksales)
# 2.Änderung vornehmen

```

`@solution`
```{r}
# Ausgabe
print(report.weeksales)
# Änderung vornehmen
report.weeksales[1,2] <- 8
```

`@sct`
```{r}
ex() %>% check_code(c("report.weeksales[1,2] <- 8","8 -> report.weeksales[1,2]"), fixed=TRUE, missing_msg="Der Code für die Änderung des Wertes ist nicht korrekt! Haben Sie die richtige Indizierung zur Korrektur des Wertes ausgewählt?") 
success_msg("Ja, genau - sonst wären falsche Umsatzzahlen an die Verkaufsniederlassung weitergegeben worden!")
```

---

## Matrizen (Q)

```yaml
type: PureMultipleChoiceExercise
key: 174850fc0b
xp: 50
```

Da Sie nun mit Matrizen arbeiten können, hat Ihnen Herr Müller einen großen Datensatz zukommen lassen - Sie sehen aber auf den ersten Blick, dass es damit Probleme zu geben scheint oder täuschen Sie sich?
- 3. Warum ist es möglich oder **nicht** möglich diese Tabelle mit weiteren 3500 Zeilen in eine Matrix zu speichern?

![Beispiel](https://assets.datacamp.com/production/repositories/4810/datasets/81e60fc1e3769bcf2010d82dec9b050ab3c87ca3/Data_frame_bsp..PNG.png)

1. weil der Datensatz unterschiedliche Datentypen nämlich Zeichenketten (character) und numerische Werte (numeric) enthält.
2. weil der Datensatz unterschiedliche Datentypen nämlich numerische Werte und boolesche Werte enthält.
3. weil der Datensatz zu groß ist und deswegen nicht geladen werden kann.
4. er lässt sich ohne weitere Bearbeitung in eine Matrix speichern, da es keine Probleme geben wird.

`@hint`
Schauen Sie sich bitte die Tabelle und **die verschiedenen Datentypen** genau an.

`@possible_answers`
- [1]
- 2
- 3
- 4

`@feedback`
- Richtig - in Matrizen können nur gleiche Datentypen gespeichert werden. In Data Frames können Elemente unterschiedlichen Typs gleicher Zeilenlänge gespeichert werden. Innerhalb der Spalten müssen aber die Datentypen gleich sein! --fast fertig, auf geht es zur letzten Einheit! - 
- Leider nicht richtig, es kommen in dem Datensatz keine boolschen Werte vor!
- Leider nicht richtig, dies ist für R kein Problem.
- Leider nicht richtig, unterschiedliche Datentypen lassen sich nicht einer Matrix speichern. Überlegen Sie noch einmal

---

## Data Frames

```yaml
type: TabExercise
key: 61afc92d00
xp: 100
```

Die **letzte** Aufgabe: Nach den Vektoren und Martrizen, kommen wir nun zur Spezialform von Listen, den **Data Frames**. 
Data Frames sind Listen mit Vektoren gleicher Länge, die bei der Datenanalyse in R sehr häufig Anwendung finden, da in einem Data Frame unterschiedliche Datentypen gespeichert werden können  (Grolemund 2019, S.55).

Nützliche Funktionen: 
- **nrow() bzw. ncol()**: Anzahl der Zeilen bzw. Spalten.
- **names()**: Funktionen zum Abrufen oder Einstellen der Namen eines Objekts.
- **colnames()**: Abrufen oder setzen der Zeilen- oder Spaltennamen eines matrixartigen Objektes.
- **head()** | **tail()**: Liefert den ersten oder letzten Teil eines Datenobjektes.
- **str()**: Erstellt eine kompakte Darstellung der internen Struktur.
- **summary()**: Generische Funktion für Ergebniszusammenfassungen.

`@pre_exercise_code`
```{r}
Neukundendaten <- read.csv2("https://assets.datacamp.com/production/repositories/5035/datasets/1d77d5e1370affba0512be4d17291ad649d6b86a/Kundendaten4.csv")
```

***

```yaml
type: NormalExercise
key: 8df763ce8d
xp: 50
```

`@instructions`
Die Neukundengewinnung ist eines ihrer Hauptziele mit der neuen Akquisition. Der Datensatz **Neukundendaten**, der aus der Datenbank des ERP-Systems stammt, enthält verschiedene Neukundeninformationen, die einen Service- bzw. Support im Quartal Q1 & Q2 2019 in Anspruch genommen haben. Im Datensatz sind alle Neukunden vermerkt. Er wurde eingelesen und der Variablen **Neukundendaten** zugewiesen. 

1. **Wie viele Kunden** sind im Neukundendatensatz aufgelistet, wenn Sie annehmen, dass es keine doppelten Kunden in der Tabelle gibt?

`@hint`
In jeder Zeile ist ein Neukunde gelistet. Lassen Sie sich einfach die Anzahl der Zeilen ausgeben.

`@sample_code`
```{r}
# Anzahl Neukunden

```

`@solution`
```{r}

nrow(Neukundendaten)
```

`@sct`
```{r}
ex() %>% check_output(98, fixed=TRUE, missing_msg="So ist das nicht richtig - vielleicht haben Sie auch nur eine Ausgabefunktion vergessen. Ihr Ziel ist es, dass die Anzahl der Kunden als Ausgabe in der Konsole erscheinen")
success_msg("Hervorragend - so einfach kommt man zu einem Ergebnis!")
```

***

```yaml
type: NormalExercise
key: 392db7ccef
xp: 50
```

`@instructions`
Herr Müller möchte nun weitere Analysen bzgl. der Daten des Service- und Supportcenters analysieren lassen. Dazu sollen Sie sich über den Datensatz einen Überblick verschaffen und ihm berichten, ob Sie auf den ersten Blick mögliche Ausreißer und Auffälligkeiten entdecken können.

- 2. Verschaffen Sie sich bitte mithilfe _einer_ Funktion einen **Überblick über den Serviceumsatz:**

`@hint`
Schauen Sie in die Exercisebox - die Befehle, die **zusammenfassende** Funktionen anwenden, sind sehr hilfreich.

`@sample_code`
```{r}
# Überblick Neukundendaten

```

`@solution`
```{r}
summary(Neukundendaten)
```

`@sct`
```{r}
ex() %>% check_code(c("str(Neukundendaten)", "summary(Neukundendaten)", "head(Neukundendaten)", "tail(Neukundendaten)"), fixed=TRUE, missing_msg="Verwenden Sie bitte die Funktionen aus der Kontextbeschreibung!") 
success_msg("Ja, genau. Die Funktion str() und summary() sind sehr hilfreich und verschaffen Ihnen einen kompakten Überblick über den Datensatz. Sie haben Ihren Arbeitstag so gut wie geschafft und alle Aufgaben mit höchster Genauigkeit und hohem Engagement absolivert (5.5/6)")
```

---

## Data Frame - Kundendatensatz (Q)

```yaml
type: PureMultipleChoiceExercise
key: b09f6d3720
xp: 50
```

Fällt Ihnen bei den **Werten des Servicesumsatzes** etwas auf? 

![summary(Kundendaten)](https://assets.datacamp.com/production/repositories/5035/datasets/2f142f3171d44abcfb68bfef9e664e9fff08020a/summary(Kundendaten).PNG.png)

Welche Aussage bzgl. des Überblicks der Neukundendaten stimmt **nicht**:
- 1. Der durchschnittliche Serviceumsatz des ersten Halbjahres 2019 wird in der Nähe des Medians liegen.
- 2. Der durchschnittliche Serviceumsatz des ersten Halbjahres 2019 wird in der Nähe des Means liegen.
- 3. Der Maximalwert des Serviceumsatzes ist unrealistisch im Vergleich zu den anderen Werten und wahrscheinlich ein Fehler in den Daten.
- 4. Es kommen NA (fehlende Werte) vor - zur Vollständigkeit müssten diese noch nachgetragen oder durch andere stat. Methoden ersetzt werden.

`@hint`
Schauen Sie sich die summary() des Serviceumsatzes an und beachten Sie bitte mögliche Ausreißerwerte, NA (fehlende Werte), den Mean (der Durchschnitt aller Werte) und den Median (Messwert oder Lageparameter, der genau in der Mitte liegt 50% darunter, 50% darüber).

`@possible_answers`
- 1
- [2]
- 3
- 4

`@feedback`
- Nein, diese Aussage trifft zu. Der Median repräsentiert in diesem Fall den durchschnittlichen Umsatz besser als der Mean, da Fehlerwerte den Mean verfälschen. 
- Ja, die gewählte Aussage stimmt nicht. Der Mean ist durch Fehlerwerte verfälscht.
- Nein, diese Aussage ist richtig. Der Maximalwert kommt sehr unrealistisch vor, wenn man ihn mit dem Median vergleicht und auch die Quartile als Maßstab heranzieht. Es wird sich um einen Fehler in den Daten handeln. 
- Nein, diese Aussage ist richtig. Es kommen NA Werte, die die Anzahl an fehlenden Werten repräsentiert im Datensatz vor.

---

## Glückwunsch!

```yaml
type: PureMultipleChoiceExercise
key: 60e18923e3
xp: 50
```

Ihr verdienter Badge (Abzeichen) zum erfolgreich absolvierten Kurzeinstieg in R :)
![Badge](https://assets.datacamp.com/production/repositories/5035/datasets/9194e649dcb1fcbcdef15b71e344f1be3883fd18/Kurs%20Badge%202.jpg)

Herzlichen Dank für Ihre Teilnahme - ich hoffe, Sie hatten ein gutes Lernerlebnis und Sie konnten etwas für sich mitnehmen. Bitte nehmen Sie an der **folgenden Umfrage teil (!!!)**, die essentieller Bestandteil meiner Masterarbeit ist und nur auf diese Daten ich Zugriff habe und die in die Auswertung einfließen.
**Link**

`@hint`
- Nehmen Sie nun bitte an der Umfrage teil - die essentieller Bestandteil meiner Masterarbeit ist: ```
**Link**
```****

`@possible_answers`
- 1
- 2
- [3]

`@feedback`
- Link
- Link
- Link
