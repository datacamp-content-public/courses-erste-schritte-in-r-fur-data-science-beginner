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

Sie sind unser/e neue/r Mitarbeiter/in in dem **Team Business Intelligence & Data Analytics der Bambergus Airuber GmbH**, einem Unternehmen das Segelflieger, Motorenflugzeuge und nun auch Paket-Drohnen produziert und verkauft. Die Firma möchte sich neue Geschäftsbereiche erschließen und sich dazu eine Firma, die sich auf die Herstellung von Paketdrohnen spezialiert hat, aufgekauft. Sie sollen im Zuge der Akquisition erste Umsatzzahlen analyisieren, Optimierungsmöglichkeiten finden und Reportstandards überüfen. Im Zuge dieser Anforderungen sollen Sie befassen mit der Programmiersprache R befassen, da sich diese für die statistische Auswertung von strukturierten und unstrukturierten Daten besonders gut eignet und in ihrem Team damit gearbeitet wird. 
Ihr Chef Herr Müller hat Ihnen verschiedene Aufgaben gegeben, die Sie schon mit einfachen R-Fähigkeiten bearbeiten können und die für das Unternehmen der Bambergus Airuber GmbH aktuell erledigt werden müssen. 

![Unternehmen](https://assets.datacamp.com/production/repositories/5035/datasets/fe857b8590bc5004a77f37284f572e0876cc3c69/Unternehmen_Bambergus_AirUber.PNG)

Lasst uns starten :)!

`@instructions`
- Wir fangen mit dem kleinen Testprogramm an mit dem fast alle Programmierbücher starten, sodass Sie mit den Eingabebereichen vertraut werden:
	- Dafür schreiben Sie bitte: **print("Hello World!")** in das Skript und drücken auf 'Submit Answer'.

`@hint`
Keine Angst - einfach ```
print("Hello World!")
``` in das Skript schreiben und auf 'Submit Answer' drücken.

Im Bereich **Instruktionen** bekommen Sie ihre Aufgabe, die Sie mithilfe auch von Hints lösen sollen
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
# Ihr erstes Programm: "Hello World!"
print("Hello World!")
```

`@sct`
```{r}
ex() %>% check_output("Hello World!", fixed=TRUE, missing_msg= "So ist das nicht ganz richtig. Beachten Sie Fehler im Code und auch mögliche Tippfehler. R ist eine case sensitive Programmiersprache!")
success_msg("Ihr erstes Programm ist vollendet - Gut gemacht! Weiter geht´s!")
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
 
Der Operator Modulo (%%) liefert den Rest der Division der linken Zahl durch die rechte Zahl. Z.B.: 7 %% 2 ist 1.

`@pre_exercise_code`
```{r}

```

***

```yaml
type: NormalExercise
key: 20b1df54bc
xp: 25
```

`@instructions`
Im Editor auf der rechten Seite gibt es einige Beispiel-Codes. Beachten Sie, dass es Unterschiede in den Zeilen gibt - sie beinhalten Code und mit dem **'#'** werden Kommentare gekennzeichnet.

- 1) Sie sollen die Umsätze der letzten drei Monate der Bambergus Airuber GmbH zusammenrechnen und somit den Umsatz für das Quartal Q1 2019 erstellen, ob der Zukauf der Firma, die nun als Tochtergesellschaft in das Unternehmen eingegliedert wurde, sich schon auf die Umsätze ausgewirkt hat.

```
Umsatz in €: Jannuar 234000 | Februar 320000 | März 294000
```

`@hint`
Stellen Sie sicher, dass Sie die Summe aus ```
234000 + 320000 + 294000
``` in einer neuen Zeile eingefügt haben. Starten Sie die Zeile nicht mit einem '#'-Zeichen, ansonsten wird der geschriebene Code nicht wie gewünscht ausgeführt, da damit Kommentare gekennzeichnet werden!

`@sample_code`
```{r}
# Beispielcode Addition:
67+78
# 1.Quartalsumsatz Q1:


```

`@solution`
```{r}
# Beispielcode Addition 
67+78
# Quartalsumsatz Q1:
234000 + 320000 + 294000
```

`@sct`
```{r}
#ex() %>% check_output(145, fixed=TRUE, missing_msg= "So ist das nicht richtig - Sie müssen sich verrechnet haben!")
ex() %>% check_output(848000, fixed=TRUE, missing_msg="Sie müssen sich verrechnet haben. Beachten Sie auch mögliche Tippfehler!")
success_msg("Ja, genau - der Umsatz im ersten Quartal beträgt 848000€!")
```

***

```yaml
type: NormalExercise
key: def4e97e1b
xp: 25
```

`@instructions`
- 2. Sie hatten im Quartal Q1 2019 einen Umsatz von **848000€** zuerst ausgegeben. Aufgrund eines Forderungsausfalles hinsichtlich des neuen Zukaufs und einer falschen Kapitalbewertung der Tochterfirma von **42800€** müssen diese negativ am Quartalsumsatz berücksichtigt werden. Wie lautet der aktualisierte Quartalsumsatz Q1 2019:

`@hint`
Denken Sie nicht kompliziert. Hier müssen Sie nur zwei Werte voneinander subtrahieren!

`@sample_code`
```{r}
# Rückstellung berücksichtigen

```

`@solution`
```{r}

848000-42800
```

`@sct`
```{r}
ex() %>% check_output(805200, fixed=TRUE, missing_msg= "So ist das nicht richtig - beachten Sie Tippfehler!")
success_msg("Richtig! Wir haben nun einen Umsatz in Q1 2019 von 805200€ zu verzeichnen")
```

***

```yaml
type: NormalExercise
key: 21601bbeab
xp: 25
```

`@instructions`
- 3. Es ist auf den Umsatz von **295005€** im Januar eine Umsatzsteuer in Höhe von **56050.95€** für die neuen leistungsstärkeren Drohnenmotoren aufgeschlagen worden. Wie viel Prozent an Umsatzsteuer wurden zur späteren Weitergabe an den Kunden aufgeschlagen, wenn die gesamte Steuer weitergegeben wurde? Lassen Sie bitte das **Ergebnis in Prozent** ausgeben:

`@hint`
Überlegen Sie sich, wie Sie eine Verhältnisgleichung aufstellen. Es kann Ihnen helfen, an den Dreisatz aus Ihrer Schulzeit zu denken. 

![Anregung](https://assets.datacamp.com/production/repositories/5035/datasets/76cc29840b27bf2ee87f7eb9b766956be88da898/Hint_Dreisatz.PNG)

Den nächsten Gedanken- und Rechenschritt schaffen Sie nun zur Lösung der Aufgabe!

Beachten Sie, dass in R anstatt dem Komma als Dezimaltrennzeichen der Punkt verwendet wird!

`@sample_code`
```{r}
# Ausrechnen der Umsatzsteuer

```

`@solution`
```{r}
56050.95/(295005/100)
```

`@sct`
```{r}
ex() %>% check_output("19", fixed=TRUE, missing_msg="Nicht ganz richtig - beachten Sie Tippfehler!")
success_msg("Richtig und die nächste Aufgabe!")
```

***

```yaml
type: NormalExercise
key: c6b8ec88ac
xp: 25
```

`@instructions`
- 4. Die Umsätze sollen in Q2 2019 aufgrund der verzögerten, aber positiven Marktresonanz der Drohnen um **2.2% im Monat** steigen. Welche Prognose geben Sie für die Umsatzzahlen am Ende des Q2 2019 ab? Nehmen Sie den Ausgangswert von **805200€** am Ende von Q1 an.

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

805200*(1.022^3)
```

`@sct`
```{r}
ex() %>% check_output(859520.9, fixed=TRUE, missing_msg="So ist das nicht ganz richtig - haben Sie jeweils das monatliche Umsatzwachstum für das Quartal berechnet?")
success_msg("Richtig - die Zinsen wachsen exponentiell an! Und nun zum nächsten Inhaltsblock - den Variablen! Den ersten von fünf Lerneinheiten haben Sie abgeschlossen")
```

---

## Variablen

```yaml
type: NormalExercise
key: 57b9e61b19
xp: 100
```

Variablen zuweisen und vergleichen:

Ein grundlegendes Konzept in der (statistischen) Programmierung sind Variablen. Eine Variable ermöglicht es einen Wert (z.B. 5) oder eine Zeichenkette (z.B. "Funktionsbeschreibung") in R zu speichern. Später können Sie den Namen der Variable nutzen, um einfach auf den Wert oder das Objekt zuzugreifen, die innerhalb dieser Variablen hinterlegt sind (de Vries/ Meys 2018, S.45 & 86).
- Beispiel: So können Sie der Variable my_var den Wert 5 zuweisen: **my_var <- 5**

```
Variablen vergleichen:
x == y 		TRUE, wenn x exakt mit y übereinstimmt
x != y 		TRUE, wenn x von y abweicht
x > y  		TRUE, wenn x größer y
x >= y		TRUE, wenn x größer gleich y
x & y 		x logisch-und y
x | y  		x logisch-oder y
!x    		nicht x
xor(x, y) 	exklusiv x logisch-oder y

```

`@instructions`
Ist es richtig, dass das letzte Halbjahr 2018 erfolgreicher war als das Halbjahr 2019 sich zu entwickeln scheint, wie Herr Müller vermutet, da die Kunden mit dem Kauf der Paketdrohnen zögern und der Forderungsausfall auch in die Quartalsbilanz fällt?

1. Sie sollen nun die Quartalszahlen aus 2019 Q1: **805200€** und Q2: **859520.9€** den Variablen
**x** und **y** zuordnen, um besser die Werte vergleichen zu können. 

2. In der Variable **z** wurden die Quartalszahlen aus **Q3 & Q4 2018** bereits hinterlegt und zugewiesen. Überprüfen Sie die Vermutung von Herrn Müller und lassen Sie sich bitte einen booleschen Wert (TRUE oder FALSE) ausgeben:

`@hint`
Schauen Sie bitte in die Exercisebox. Hier ist die Zuweisung anhand eines Beispiels verdeutlicht. Lesen Sie bitte genau die Instruktionen. Der Wert für Variable z wurde bereits im System hinterlegt und der Variable z zugewiesen. 

Entwickeln Sie den Code so, dass ein boolescher Wert (TRUE oder FALSE) ausgegeben wird.

`@pre_exercise_code`
```{r}
z <- 1655000
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
x <- 805200
# Q2
y <- 859520.9
# 2.Vergleich der Umsätze
z > (x+y)
```

`@sct`
```{r}
ex() %>% check_object("x") %>% check_equal(805200)
ex() %>% check_object("y") %>% check_equal(859520.9)
ex() %>% check_output("FALSE", fixed=TRUE, missing_msg= "Da haben Sie etwas falsch verglichen bei Aufgabe 2 oder die Aussage von Herrn Müller nicht direkt überprüft!")
#ex() %>% check_code(c("54320.9", "y-x", "859520.9-805200"), fixed=TRUE, missing_msg= "Da stimmt etwas bei Aufgabe 3. nicht!")
success_msg("Ja, genau - es sieht so aus als hätten Sie die Variablenzuweisung verstanden und Herr Müller lag mit seiner Prognose falsch. Deshalb ist eine Überpüfung anhand von Daten für fundierte Aussagen und unternehmensrelevante Entscheidungen immer notwendig und wird in Zukunft weiter an Bedeutung zunehmen! Kommen wir zum nächsten Inhaltsblock, den Datentypen (2/6 abgeschlossen)")
```

---

## Datentypen in R

```yaml
type: TabExercise
key: b704b35535
xp: 100
```

R arbeitet mit zahlreichen Datentypen und ist sensitiv auf Groß-/Kleinschreibung. Einige der grundlegendsten Datentypen sind:

![Datentypen](https://assets.datacamp.com/production/repositories/5035/datasets/fdc12d4dad7b9c7be22919631b46eae27ae1d3f9/Basisdatentypen_%C3%9Cbersicht_final.PNG.png)

**Wichtig:** Zeichenketten werden in "Anführungszeichen" gesetzt.

Von der kleinen Tochtergesellschaft hat Ihr Chef Herr Müller einen Datensatz der Mitarbeiter angefordert, um einen Überblick über die neuen Mitarbeiter zu bekommen. Er sagt Ihnen, dass die Mitarbeiter dort noch nicht vertraut mit den neuen ERP-System seien und Fehler in der Administration der Datentypen bereits schon festgestellt  wurden. Deswegen sollen Sie sich nun damit beschäftigen, um dies zu überprüfen.

`@pre_exercise_code`
```{r}
Anzahl_Mitarbeiter <- "Schmidt, Klaus"
```

***

```yaml
type: NormalExercise
key: 0d1ead9f62
xp: 35
```

`@instructions`
- 1. Die Variable **Anzahl_Mitarbeiter** müsste ein numerischer Basisdatentyp sein. Überprüfen Sie dies bitte.

`@hint`
Schreiben Sie bitte den Code so, damit als Output ein boolescher Wert (TRUE oder FALSE) ausgegeben wird! Schauen Sie in die Tabelle unter in der Zeile **Abfrage (Query)** nach.

`@sample_code`
```{r}
#1.Überprüfung Datentyp Variable Anzahl_Mitarbeiter:

```

`@solution`
```{r}
#1.Überprüfung Variable Anzahl_Mitarbeiter:
is.numeric(Anzahl_Mitarbeiter)
```

`@sct`
```{r}
ex() %>% check_output(c(FALSE, "character"), fixed=TRUE, missing_msg= "Da stimmt etwas nicht. Schreiben Sie bitte den Code so, damit als Output ein boolescher Wert ausgegeben wird! Beachten Sie weiterhin die case sensitivität von R")
success_msg("Super, es ist keine numerische Variable hinterlegt, da müssen die Mitarbeiter der Tochtergesellschaft etwas falsch zugewiesen haben!")
```

***

```yaml
type: NormalExercise
key: e8d49fb162
xp: 35
```

`@instructions`
Da ist wohl im ERP-System etwas mit der Zuordnung schief gelaufen.
- 2. Lassen Sie sich bitte die Variable **Anzahl_Mitarbeiter** ausgeben und wenn nicht die Anzahl von **17** hinterlegt ist, tun Sie dies bitte. Klicken Sie zur Zwischenausgabe auf 'Run Code'.

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
ex() %>% check_code(c("Anzahl_Mitarbeiter <- 17", "17->Anzahl_Mitarbeiter"), fixed=TRUE, missing_msg= "Nicht richtig. Schreiben Sie bitte den Code so, damit als Output 17 ausgeben wird!")
success_msg("Super, nun ist der richtige Wert zugewiesen worden!")
```

***

```yaml
type: NormalExercise
key: c5fa4ac3a0
xp: 30
```

`@instructions`
- 3. Ihr Chef Herr Müller hat für den Mitarbeiter Maximilian Flix, der extra für die neue Tochtergesellschaft der Bambergus Airuber Gmbh angworben wurde und mit Ihnen in Zukunft zusammenarbeiten soll, ein neues Büro renovieren lassen. Nennen Sie das Büro **Office_33** bitte in **Nordwand** um.

`@hint`
Verweisen Sie auf die Variable Office_33 einfach den neuen Namen. Beachten Sie, dass Nordwand eine "Zeichenkette/ein String" ist.

`@sample_code`
```{r}
#1.numerische Variable?
is.numeric(Anzahl_Mitarbeiter)
#2.Ausgabe + Zuweisung
print(Anzahl_Mitarbeiter)
Anzahl_Mitarbeiter <- 17
#3.Umbenennung Büro

```

`@solution`
```{r}

Office_33 <- "Nordwand"
```

`@sct`
```{r}
ex() %>% check_code(c(Office_33 <- "Nordwand", "Nordwand"-> Office_33), fixed=TRUE, missing_msg= "Da haben Sie etwas nicht richtig zugewisen. Verweisen Sie auf die Variable Office_33 den neuen Namen")
success_msg("Super - weiter geht´s, wir haben keine Zeit zu verlieren!")
```

---

## Assessment Datentypen

```yaml
type: PureMultipleChoiceExercise
key: dbbb20e7e4
xp: 50
```

Was ist ```
"53.Stock"
``` für ein Basisdatentyp?

- 1: Es ist ein boolescher Wert (logical).
- 2: Es ist eine Ganzzahl oder Fließkommazahl (numeric).
- 3: Es ist eine Zeichenkette (character).
- 4: Es ist eine Kategorie (fact).

`@hint`
Beachten Sie die Anführungszeichen.

- zu 1: Boolesche Werte: TRUE, FALSE
- zu 2: Ganzzahlen: 1; 1.5
- zu 3: Zeichenkette: "Hallo Herr Müller"
- zu 4: Kategorie: A

`@possible_answers`
- 1
- 2
- [3]
- 4

`@feedback`
- Leider nicht richtig, überlegen Sie noch einmal!
- Leider nicht richtig, überlegen Sie noch einmal!
- Richtig - es ist eine Zeichenkette (String), da der Wert in Anführungszeichen notiert ist. Sie haben schon einiges erledigt und lernen schnell - die Hälfte haben Sie geschafft (3/6 abgeschlossen)! - Weiter geht es nun mit **Vektoren!**
- Leider nicht richtig, überlegen Sie noch einmal!

---

## Vektoren

```yaml
type: TabExercise
key: 72efcbb708
xp: 100
```

Ein Vektor ist die einfachste Datenstruktur in R. Als "einzelnes Objekt, das aus einer Ansammlung von Daten besteht" wird ein Vektor im R-Handbuch definiert. Wir behandeln in dieser Einheit zum Einstieg nur numerische Vektoren, also Vektoren, die alle Arten von Zahlen enthalten können (de Vries/Meys 2018).

Um einen Vektor mit einer Folge von Zahlen von 1 bis 3 zu erzeugen:  
```
c(1,2,3) oder kürzer c(1:3)
```

Wichtige Befehle:

**str()**: Typ eines Vektors bestimmen und Überblick verschaffen.

**mean()**: Durchschnitt ausrechnen.

`@pre_exercise_code`
```{r}
sell.time <- c(8,8,8,8,9,6)
revenue.day <- c(2700, 3500, 4200, 4700, 5103, 3300)
```

***

```yaml
type: NormalExercise
key: 22b76c6200
xp: 25
```

`@instructions`
Sie sollen als Mitarbeiter des Business Intelligence & Data Analyticsteam die Verkaufszeiten ihres einzigen Verkaufsstores analyisieren, da verschiedene Kunden sich über die Öffnungszeiten beschwert haben und Sie prüfen möchten, ob dieser noch profitabel ist, da schon jetzt ihr Umsatz zu 93% über ihren Webstore generiert wird. 
Gehen wir zuerst die Kundenbeschwerde an:
- 1. Erstellen Sie dazu einen Vektor, der die Zahlen von 1 bis 6 beinhaltet und weisen Sie ihm bitte den Variablennamen **open.vec** zu. Die Zahlen stehen jeweils für einen Verkaufstag (1 = "Montag")

`@hint`
Schauen Sie bitte in die Exercisebox. Dort sind konkrete Beispiele gegeben, die Ihnen weiterhelfen.

`@sample_code`
```{r}
# Verkaufstage

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
xp: 25
```

`@instructions`
- 2. In dem Vektor **sell.time** ist die Verkaufszeit für jeden Verkaufstag hinterlegt. Lassen Sie sich bitte die Informationen über Typ und Struktur des Vektors **sell.time** ausgeben. Beurteilen Sie bitte, ob dieser nur numerische Zahlen enthält und welcher Tag der zeitlich längste ist.

`@hint`
Die Funktion **str()** haben Sie in der Kontextbeschreibung gegeben.

`@sample_code`
```{r}
#Verkaufszeit

```

`@solution`
```{r}

str(sell.time)
```

`@sct`
```{r}
ex() %>% check_code("str(sell.time)", fixed=TRUE, missing_msg="Verwenden Sie bitte die Funktionen aus der Kontextbeschreibung!") 
success_msg("Ja, genau. Die Funktion str() ist sehr hilfreich und verschafft Ihnen einen guten Überblick über den Vektor. Es ist nützlich, den Befehl immer im Hinterkopf zu behalten!")
```

***

```yaml
type: NormalExercise
key: cfddb579f1
xp: 25
```

`@instructions`
- 3. Am längsten Arbeitstag wurden 52020€ Umsatz generiert. Wie viel wurde pro Stunde umgesetzt?

![Drohen-Skizze](https://assets.datacamp.com/production/repositories/5035/datasets/7ede58abe5f7241798aaefb6b00478b95710a5ea/Drohnen_Skizze_klein.jpg)

`@hint`
Eine Divisionsaufgabe - denken Sie nicht kompliziert und tippen Sie es ein. Der längste Arbeitstag ist der Freitag, der fünfte Tag in der Woche.

`@sample_code`
```{r}
# Umsatz pro Stunde am längsten Arbeitstag:

```

`@solution`
```{r}

52020/9
```

`@sct`
```{r}
ex() %>% check_output(5780, fixed=TRUE, missing_msg="Nicht richtig, da haben Sie sich verrechnet oder einen Fehler im Code!")
success_msg("Richtig. Am Freitag wurden 5780€ Umsatz pro Stunde erwirtschaftet!")
```

***

```yaml
type: NormalExercise
key: 3a78346b6f
xp: 25
```

`@instructions`
- 4. Berechnen Sie bitte die durchschnittliche Verkaufszeit pro Verkaufstag in der Woche.

`@hint`
Benutzen Sie die Funktion aus der Exercisebox und verwenden Sie die passende Variable.

`@sample_code`
```{r}
# Durchschnittliche Verkaufszeit:

```

`@solution`
```{r}

mean(sell.time)
```

`@sct`
```{r}
ex() %>% check_output(7.833333, fixed=TRUE, missing_msg="Nicht ganz richtig!")
success_msg("Richtig - die durchnittliche tägliche Verkaufszeit beträgt 7,83 h! Kommen wir zu dem nächsten Aufgabenblock, den Matrizen! Ein dickes Lob an Sie, Sie lernen schnell. Sie haben nur noch 2 Einheiten vor sich")
#ex() %>% check_code(c("47/6","mean(sell.time)", "(8+8+8+8+9+6)/6)"), fixed=TRUE, missing_msg="Nicht ganz richtig!")
#success_msg("Richtig - die durschnittliche tägliche Verkaufszeit beträgt 7,83 h!")
```

---

## Matrizen

```yaml
type: TabExercise
key: b0d2909445
xp: 100
```

Matrizen sind rechteckige, zweidimensionale Anordnungen von Elementen, ähnlich wie Tabellen. In R können Matrixoperationen einfach und effizient durchgeführt werden. Anhand von Matrizen können im Gegensatz zu Vektoren nun mehrere Zeilen in ein und derselben Matrix gespeichert werden (de Vries/Meys 2018).

Vektoren in eine Matrix zusammenführen: 
- **rbind():** Funktion mit der Vektoren zu Zeilen ein und derselbe Matrix zusammengefügt werden können.   Matrix <- rbind(Vektor, Vektor)
- **cbind():** Funktion mit der Vektoren als Spalten einer Matrix zusammengefügt werden.

Werte einer Matrix ersetzen:
- Um den Wert in der dritten Zeile und zweiten Spalte der Matrix zu 5 zu ändern: my.matrix[3,2] <- 5

Zeilen- und Spaltennamen verändern: 
- Zeilennamen verändern: Bsp. **rownames(Matrix)** <- c("Region", "Umsätze")
- Spaltennamen verändern: Bsp. **colnames(Matrix)** <- c("Januar", "Februar")

`@pre_exercise_code`
```{r}
report.weeksales <- matrix(1:18, ncol=6)
report.final <- matrix(1:18, ncol=6)
sell.time <- c(8,88,8,8,9,6)
revenue.day <- c(2700, 3500, 4200, 4700, 5103, 3300)
average.byday <- c(2700/8, 3500/8, 4200/8, 4700/8, 5103/9, 3300/6)
report.final <- rbind(sell.time, revenue.day, average.byday) 
```

***

```yaml
type: NormalExercise
key: b49123677e
xp: 35
```

`@instructions`
Herr Müller bittet Sie einen Report mit dem Namen **report.weeksales** für die Tochterfirma zu erstellen.

- 1. Ihre Aufgabe ist es eine Matrix aus den Vektoren **sell.time und revenue.day** zu erstellen und der Variable vom Typ Matrix **report.weeksales** zuzuordnen. Schauen Sie, ob Sie es richtig gemacht haben mit der Ausgabe in der Console.

`@hint`
Schauen Sie bitte in die Exercisebox und verwenden Sie bitte die Funktion um Zeilenvektoren zusammen zu führen und verweisen (<-) Sie diese auf report.weeksales.

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
xp: 35
```

`@instructions`
Sie haben den Report bei Herrn Müller abgegeben. Er kommt auf Sie zu und entgegnet Ihnen, ob Ihnen aufgefallen sei, dass sich noch ein Zahlenfehler eingeschlichen hat.

- 2. Lassen Sie sich die Matrix **report.weeksales** ausgeben ('Run code') und korrigieren Sie bitte den Report.

`@hint`
Haben Sie den falschen Wert entdeckt, ein Tag hat nur 24h! - alles darüber ist natürlich falsch. report.weeksales[Zeile, Spalte] <- Wert

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

#Wirft bei Check object die Lösung aus
#ex() %>% check_object("report.weeksales[1,2]") %>% check_equal(8, fixed=TRUE, missing_msg="Der Code für die Änderung des Wertes ist nicht korrekt!")
#success_msg("Ja, genau - da war wohl jemand unaufmerksam. Gut, dass Sie es geändert haben, sonst wären falsche Umsatzzahlen an die Verkaufsniederlassung weitergegeben worden!")
```

***

```yaml
type: NormalExercise
key: ea9fe14e83
xp: 30
```

`@instructions`
Sie hatten für Freitag schon den durchschnittlichen Umsatz pro Stunde ausgerechnet. In dem Vektor **average.byday** wurde der Umsatz pro Stunde für alle sechs Verkaufstage errechnet und dem Report hinzugefügt. Der neue Report wurde der Variablen **report.final** zugeordnet. 

Nun ist der finale Report für die Tochtergesellschaft fast fertig. Es fehlt noch eine eindeutige Benennung, damit dem Management der Tochtergesellschaft auf einen schnellen Blick ersichtlich ist, was dargestellt und analyisiert wurde. 

- 3. Bitte benennen Sie bei dem erstellten finalen Report die Zeilen- oder Spaltennamen:
		
    - **Sales time in h, Revenue, Revenue per hour**

`@hint`
Schauen Sie dazu in die Exercisebox. Die Beispiele verdeutlichen die notwendige Programmierung sehr gut. Achten Sie darauf, dass die Benennungen ```
Zeichenketten
``` sind.

`@sample_code`
```{r}
# 1.report.weeksales
report.weeksales <- rbind(sell.time, revenue.day)
# 2.Ausgabe + Änderung vornehmen
print(report.weeksales)
report.weeksales[1,2] <- 8
# Vektor hinzufügen
report.final <- rbind(sell.time, revenue.day, average.byday) 
# 3.Spalten- bzw. Zeilennamen benennen

```

`@solution`
```{r}
# Zeilennamen benennen
rownames(report.final) <- c("Sales time in h", "Revenue", "Revenue per hour")
## Spaltennamen bennen
#colnames(report.final) <- c("Monday","Tuesday", "Wednesday", "Thursday", "Friday", "Saturday")
```

`@sct`
```{r}
ex() %>% check_code(rownames(report.final) <- c("Sales time in h", "Revenue", "Revenue per hour"), fixed=TRUE, missing_msg="Haben Sie beachtet, dass die Benennungen Zeichenketten sind und dementsprechend gekennzeichnet werden müssen?") 
success_msg("Ja, genau! So behalten Sie die Übersicht und auch andere können Ihre Ergebnisse leichter nachvollziehen! Kommen wir nun zum letzten Inhaltsblock dieser Kurzeinführung - den in der stat. Programmierung sehr häufig verwendeten Data Frames.")
#ex() %>% check_code(colnames(report.final) <- c("Monday","Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"), fixed=TRUE, missing_msg=" Haben Sie alle Wochentage ohne Tippfehler und als Zeichenkette gekennzeichnet erstellt? Verwenden Sie bitte die Funktionen aus der Kontextbeschreibung") 
#success_msg("Ja, genau - so behalten Sie die Übersicht und auch andere können Ihre Ergebnisse leichter nachvollziehen!")
```

---

## Assessment Matrizen

```yaml
type: PureMultipleChoiceExercise
key: 174850fc0b
xp: 50
```

Warum ist es nicht möglich diese Tabelle mit weiteren 3500 Zeilen in eine Matrix zu speichern?

![Beispiel](https://assets.datacamp.com/production/repositories/4810/datasets/81e60fc1e3769bcf2010d82dec9b050ab3c87ca3/Data_frame_bsp..PNG.png)

1. weil der Datensatz unterschiedliche Datentypen nämlich Zeichenketten (character) und numerische Werte (numeric) enthält.
2. weil der Datensatz unterschiedliche Datentypen nämlich numerische Werte und boolesche Werte enthält.
3. weil der Datensatz zu groß ist und deswegen nicht geladen werden kann.
4. er lässt sich ohne weitere Bearbeitung in eine Matrix speichern.

`@hint`
Schauen Sie sich bitte die Tabelle und die Datentypen genau an.

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

Nach den Vektoren und Martrizen, kommen wir nun zur Spezialform von Listen, den **Data Frames**. 
Data Frames sind Listen mit Vektoren gleicher Länge, die bei der Datenanalyse in R sehr häufig Anwendung finden, da in einem Data Frame unterschiedliche Datentypen gespeichert werden können  (Grolemund 2019, S.55).

Nützliche Funkionen: 
- **nrow() bzw. ncol()**: Anzahl der Zeilen bzw. Spalten
- **names()**: Funktionen zum Abrufen oder Einstellen der Namen eines Objekts
- **colnames()**: Abrufen oder setzen der Zeilen- oder Spaltennamen eines matrixartigen Objektes
- **head()** | **tail()**: Liefert den ersten oder letzten Teil eines Datenobjektes
- **str()**: Erstellt eine kompakte Darstellung der internen Struktur
- **summary()**: Generische Funktion für Ergebniszusammenfassungen

`@pre_exercise_code`
```{r}
Kundendaten <- read.csv2("https://assets.datacamp.com/production/repositories/5035/datasets/f54dfd57d7897d15486fb6bde4aaccc7924d40cf/Kundendaten3.csv")
```

***

```yaml
type: NormalExercise
key: 8df763ce8d
xp: 50
```

`@instructions`
Der Datensatz aus Ihrem Unternehmen Bambergus AirUber, der aus der zentralen Kundendatenbank stammt, enthält verschiedene Kundeninformationen. Die Kundeninformationen beziehen sich auf die Anzahl der mit Ihrer neuartigen Belieferungsdrohne angeflogenen Kunden. Er wurde eingelesen und der Variable **Kundendaten** zugewiesen. Um zu erfahren, wie die neuartige Belieferungsmethode angeommen wurde, sollen Sie die Daten analyieren.

![Drohne](https://assets.datacamp.com/production/repositories/5035/datasets/2e93b24ab11762e4a023c378ebd0861de122f99b/Bef%C3%B6rderungsdrohne_klein.jpg)

1. Wie viele Kunden sind im Kundendatensatz aufgelistet, wenn Sie annehmen, dass es keine doppelten Kunden in der Tabelle gibt?

`@hint`


`@sample_code`
```{r}
# Anzahl Kunden

```

`@solution`
```{r}

nrow(Kundendaten)
```

`@sct`
```{r}
ex() %>% check_output(98, fixed=TRUE, missing_msg="So ist das nicht richtig - vielleicht haben Sie auch nur eine Ausgabefunktion vergessen. Ihr Ziel ist es, dass die Anzahl der Kunden als Ausgabe in der Konsole erscheinen")
success_msg("Hervorragend - so einfach bekommt man an ein Ergebnis!")
```

***

```yaml
type: NormalExercise
key: 392db7ccef
xp: 50
```

`@instructions`
- 2. Verschaffen Sie sich bitte einen Überblick über den Kundendatensatz und beachten Sie die Umsatzdaten.

`@hint`
Schauen Sie in die Exercisebox - die Befehle, die zusammenfassende Funktionen anwenden, sind sehr hilfreich.

`@sample_code`
```{r}

```

`@solution`
```{r}
summary(Kundendaten)
```

`@sct`
```{r}
ex() %>% check_code(c("str(Kundendaten)", "summary(Kundendaten)", "head(Kundendaten)", "tail(Kundendaten)"), fixed=TRUE, missing_msg="Verwenden Sie bitte die Funktionen aus der Kontextbeschreibung!") 
success_msg("Ja, genau. Die Funktion str() und summary() sind sehr hilfreich und verschaffen Ihnen einen kompakten Überblick über den Kundendatensatz. Es ist nützlich, die Befehle immer im Hinterkopf zu behalten!")
```

---

## Data Frame - Kundendatensatz

```yaml
type: PureMultipleChoiceExercise
key: b09f6d3720
xp: 50
```

Ist Ihnen etwas bei den Umsatzwerten des Kundendatensatzes aufgefallen? (Wenn Sie es nicht mehr im Kopf haben, wählen Sie bitte HINT - da nochmal eine Übersicht aufgeführt)

- 1. Nichts auffälliges.
- 2. Die Maximalwerte des Kundendatensatzes sind sehr unrealistisch im Vergleich zu den anderen Werten.
- 3. Es kommen NA (fehlende) Werte vor - zur Vollständigkeit müssten diese noch nachgetragen werden.
- 4. Es kommen sowohl NA Werte als auch zu hohe Ausreißerwerte im der Spalte des Kundendatensatzes vor.

`@hint`
Schauen Sie sich die summary() des Kundendatensatzes an und beachten Sie bitte mögliche Ausreißer, NA (fehlende) Werte etc. 
![summary(Kundendaten)](https://assets.datacamp.com/production/repositories/5035/datasets/486423d2cc1f9d82fc4f39f8a4d69722d3505961/summary(Kundendaten).PNG)

`@possible_answers`
- 1
- 2
- 3
- [4]

`@feedback`
- Falsch - da haben Sie nicht genau mit den Daten befasst!
- Ja, dies ist fast richtig, jedoch fehlt noch ein Teil! Lesen Sie bitte noch einmal genauer! 
- Ja, dies ist fast richtig, jedoch fehlt noch ein Teil! Lesen Sie bitte noch einmal genauer!
- Richtig! [Glückwunsch](https://assets.datacamp.com/production/repositories/5035/datasets/9194e649dcb1fcbcdef15b71e344f1be3883fd18/Kurs%20Badge%202.jpg)
