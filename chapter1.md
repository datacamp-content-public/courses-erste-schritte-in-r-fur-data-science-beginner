---
title: 'Wie R funktioniert'
description: 'Mit kleinen Schritten zu den Basics in R'
free_preview: true
---

## Motivation | Einstieg | Was  ist Data Science

```yaml
type: VideoExercise
key: bb50a6f713
xp: 50
```

`@projector_key`
6d51347f047bd021feea1f24da985a1e

---

## Wie R in Data Camp funktioniert

```yaml
type: NormalExercise
key: 9634ac451e
xp: 100
```

Die Hauptfunktionen von DataCamp

Die linke Funktionsseite:
- 1) Hier im **Exercisebereich** wird immer die grundlegende Theorie dargestellt sein, die dann direkt in der Übung angewendet wird. 
- 2) Im Bereich der **Instruktion** bekommen Sie die Erläuterung, was genau Ihre Aufgabe ist, die Sie anschließend lösen sollen. 
- 3) Die **Hints** können Sie nutzen, wenn Sie nicht mehr weiter kommen und einen Hinweis benötigen.

Die rechte Funktionsseite:
- 4) **script.R** ist ihre Kommandozeile mit der Sie Ihre Befehle und Ihren Code in der Programmiersprache R eingeben.
- 5) Mithilfe des Buttons **Run Code** kompilieren Sie nur den Code mit **Submit Answer** führen Sie ihn aus.
- 6) Die **Console** ist in diesem Fall eine Oberfläche in der Sie sehen können, wie Ihr geschriebener Code ausgeführt wird und welche Ausgaben er liefert. 

Lasst uns mit der ersten Aufgabe starten! Let´s go!

`@instructions`
Hallo und herzlich Willkommen,

Sie sind unser/e neue/r MitarbeiterIn in der **Abteilung Business Intelligence & Data Analytics** und befassen sich das erste Mal mit der Programmiersprache R. Ihr Chef Herr Müller hat Ihnen verschiedene Aufgaben gegeben - nun fangen wir aber erstmal leicht an. 

![](https://assets.datacamp.com/production/repositories/4810/datasets/44f5b387423e2b1a9a47c24d837c1bd4f3184ee0/IT_Mitarbeiter.jpg)

- Wir fangen mit dem Programm an mit dem fast alle Programmierbücher starten:
	- Dafür schreiben Sie bitte: **print("Hello World!")** in das Skript und drücken auf 'Submit Answer'.

`@hint`
Keine Angst - einfach print("Hello World!") in das Skript schreiben und auf 'Submit Answer' drücken.

`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}

```

`@solution`
```{r}
# Ihr erstes Programm: "Hello World!"
print("Hello World!")
```

`@sct`
```{r}
ex() %>% check_output("Hello World!", fixed=TRUE, missing_msg= "So ist das nicht ganz richtig - Beachten Sie Tippfehler!")
success_msg("So ihr erstes Programm ist vollendet! ![Welt](https://assets.datacamp.com/production/repositories/4810/datasets/efdb2635ca5a59a67d67dedea62813ca4cf68a0d/hello_welt.jpg)")
```

---

## Rechnen mit R

```yaml
type: TabExercise
key: c09b1c46a5
xp: 100
```

R kann in seiner Basisfunktion als Rechner verwendet werden. Beachten Sie folgende arithmetische Rechenoperatoren:	 

```
 Addition: + 
 Subtraktion: - 
 Multiplikation: *
 Division: / 
 Potenzierung: ^
 Modulo: %%
```
 
Der Operator Modulo (%%) liefert den Rest der Division der linken Zahl durch die rechte Zahl. Z.B.: 7 %% 2 ist 1.

Behalten Sie diese Informationen im Hinterkopf und befolgen Sie sie in den nachfolgenden Aufgaben, um die Übung erfolgreich abzuschließen.

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

- 1) Sie sollen die Umsätze der letzten drei Monate zusammenrechnen und somit den Umsatz für das Quartal Q1 erstellen. Fügen Sie bitte eine weitere Codezeile, die Rechnung, hinzu und klicken Sie danach auf "Submit Answer".

```
Umsatz in €: Jannuar 234000 | Februar 320000 | März 294000
```

`@hint`
Stellen Sie sicher, dass Sie die Summe aus 234000 + 320000 + 294000 in einer neuen Zeile eingefügt haben. Starten Sie die Zeile nicht mit einem '#'-Zeichen, ansonsten wird der geschriebene Code nicht wie gewünscht ausgeführt, da damit Kommentare gekennzeichnet werden!

`@sample_code`
```{r}
# Beispielcode Addition 
67+78
#1.Quartalsumsatz Q1:

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
- 2. Sie hatten im Quartal Q1 einen Umsatz von 848000€ zuerst ausgegeben. Aufgrund eines Forderungsausfalles von 42800€ müssen diese am Umsatz berücksichtigt werden.

`@hint`
Hier müssen Sie nur zwei Werte voneinander substrahieren.

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
success_msg("Richtig! Wir haben nun einen Umsatz in Q1 von 805200€")
```

***

```yaml
type: NormalExercise
key: 21601bbeab
xp: 25
```

`@instructions`
- 3. Es sind auf den Umsatz von 295005€ im Januar eine Umsatzsteuer in Höhe von 56050.95€ aufgeschlagen worden. Wie viel Prozent an Umsatzsteuer wurden zur späteren Weitergabe an den Verbraucher aufgeschlagen, wenn die gesamte Steuer weitergegeben wurde? Geben Sie bitte das **Ergebnis in Prozent** aus!

`@hint`
Schauen Sie nochmal konkret auf Ihre Berechnung und überlegen Sie sich, wie Sie eine Verhältnisgleichung aufstellen. Es kann Ihnen helfen, an den Dreisatz aus Ihrer Schulzeit zu denken. Beachten Sie, dass in R anstatt dem Komma als Dezimaltrennzeichen der Punkt verwendet wird!

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
- 4. Die Umsätze sollen in Q2 um 2.2% im Monat steigen. Welche Prognose geben Sie für die Umsatzzahlen am Ende des Q2 ab? Nehmen Sie den  Ausgangswert von 805200€ am Ende von Q1 an.

`@hint`
Beachten Sie, dass die Prozente jeweils im Monat steigen. Beachten Sie, dass in R anstatt dem Komma als Dezimaltrennzeichen der Punkt verwendet wird!

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
ex() %>% check_output(859520.9, fixed=TRUE, missing_msg="So ist das nicht ganz richtig - haben Sie den monatlichen Umsatzwachstum berechnet und beachtet, dass es sich um 3 Monate handelt?!")
success_msg("Richtig und die nächste Aufgabe!")
```

---

## Rechnen Assessment

```yaml
type: PureMultipleChoiceExercise
key: 49b959ddb4
xp: 50
```

- 6. Herr Müller braucht für weitere Abrechnungen die Information, an welchem Tag (Zahl) wir uns innerhalb der aktuellen Kalenderwoche befinden. Wir haben heute den 11.05.2019 und das Jahr hat 365 Tage. Es ist also der 131 Tag. 
- An welchem Tag liegen wir in der angebrochenen Kalenderwoche?

**Hinweis:** Da das Ergebnis direkt in die Abrechnung einfließst, ist es die Vorgabe, das Ergebnis mit einer Rechenoperation ausgeben zu lassen.

`@hint`
Versuchen Sie es doch mal mit dem Modulo-Operator (%%). Sie können die Console in R verwenden. Modulo bedeutet auch Division mit Rest.

`@possible_answers`
- 4
- [5]
- 6
- 7
- 18

`@feedback`
- Da liegen Sie nicht richtig
- Richtig. Genau, der Modulooperator von 131%%7 ergibt einen Rest von 5 Tagen. Es ist also der 5 Tag in der Woche.
- Da liegen Sie nicht richtig
- Da liegen Sie nicht richtig
- Da liegen Sie nicht richtig

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
x > y  
x >= y
x & y 		x logisch-und y
x | y  		x logisch-oder y
!x    		nicht x
xor(x, y) 	exklusiv x logisch-oder y

```

`@instructions`
Herr Müller bittet Sie sich mit den Quartalszahlen der letzten und aktuellen Quartale vertraut zu machen.

1. Sie sollen nun die Quartalszahlen 2019 aus Q1: 805200€  und Q2: 859520.9€ den Variablen x und y zuordnen, um besser die Werte vergleichen zu können. 
2. In der Variable z wurden die Quartalszahlen aus Q3 & Q4 bereits hinterlegt und zugewiesen. Ist es richtig, dass das letzte Halbjahr 2018 erfolgreicher war als das Halbjahr 2019 sich zu entwickeln scheint, wie Herr Müller vermutet?
3. Berechnen Sie die Differenz aus den zwei Quartalen Q2 (Prognosewert 2019) und Q1 (2019) und weisen Sie Ihre Rechnung der Variablen **d** zu.

`@hint`
Schauen Sie bitte in die Exercisebox. Hier ist die Zuweisung anhand eines Beispiels verdeutlicht. Lesen Sie bitte genau die Instruktionen. Der Wert für Variable z wurde bereits zugewiesen.

`@pre_exercise_code`
```{r}
z <- 1655000
```

`@sample_code`
```{r}
# 1.Q1:

# Q2

# 2.Vergleich der halbjährlichen Umsätze aus 2018 und 2019: 

# 3.Verweisen Sie die Differenz aus Q2 (Prognosewert) und Q1 (2019) der Variable d zu:

```

`@solution`
```{r}
# Q1
x <- 805200
# Q2
y <- 859520.9
# 2.Vergleich der Umsätze
z > (x+y)
# 3.Verweisen Sie die Differenz aus Q2 und Q1 der Variable d zu:
d <- (y-x)
```

`@sct`
```{r}
ex() %>% check_object("x") %>% check_equal(805200)
ex() %>% check_object("y") %>% check_equal(859520.9)
ex() %>% check_output("FALSE", fixed=TRUE, missing_msg= "Da haben Sie etwas falsch verglichen bei Aufgabe 2 oder die Aussage von Herrn Müller nicht direkt überprüft!")
ex() %>% check_code(c("54320.9", "y-x", "859520.9-805200"), fixed=TRUE, missing_msg= "Da stimmt etwas bei Aufgabe 3. nicht!")
success_msg("Ja, genau - es sieht so aus als hätten Sie die Variablenzuweisung verstanden und Herr Müller lag mit seiner Prognose falsch. Deshalb ist eine Überpüfung anhand von Daten für fundierte Aussagen und unternehmensrelevante Entscheidungen immer notwendig und wird in Zukunft weiter an Bedeutung zunehmen!")
```

---

## Datentypen in R

```yaml
type: TabExercise
key: b704b35535
xp: 100
```

R arbeitet mit zahlreichen Datentypen und ist sensitiv auf Groß-/Kleinschreibung. Einige der grundlegendsten Datentypen sind:

![Datentypen](https://assets.datacamp.com/production/repositories/4810/datasets/893260b55479a71ff88107db16b1a96fc6bd4116/Basisdatentypen_R.PNG)

**Wichtig:** Zeichenketten werden in "Anführungszeichen" gesetzt.

Von einer kleinen Tochtergesellschaft hat Ihr Chef Herr Müller einen Kundendatensatz zugeschickt bekommen. Er sagt Ihnen, dass die Mitarbeiter dort noch nicht vertraut mit den Datentypen seien. Deswegen müssen Sie sich damit beschäftigen, um dies zu überprüfen.

`@pre_exercise_code`
```{r}
Anzahl_Mitarbeiter <- "Schmidt, Klaus"
```

***

```yaml
type: NormalExercise
key: 0d1ead9f62
xp: 50
```

`@instructions`
- 1. Die Variable **Anzahl_Mitarbeiter** müsste ein numerischer Basisdatentyp sein. Überprüfen Sie dies bitte.

`@hint`
Schreiben Sie bitte den Code so, damit als Output ein boolescher Wert (TRUE oder FALSE) ausgegeben wird! Schauen Sie in die Tabelle unter **Abfrage (Query)**

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
ex() %>% check_output(c(FALSE, "character"), fixed=TRUE, missing_msg= "Nicht richtig. Schreiben Sie bitte den Code so, damit als Output ein boolescher Wert ausgegeben wird!")
success_msg("Super, es ist keine numerische Variable hinterlegt, da müssen die Mitarbeiter der Tochtergesellschaft etwas falsch zugewiesen haben!")
```

***

```yaml
type: NormalExercise
key: e8d49fb162
xp: 50
```

`@instructions`
- 2. Lassen Sie sich bitte die Variable **Anzahl_Mitarbeiter** ausgeben und wenn nicht die Anzahl von **17** hinterlegt ist, tun Sie dies bitte. Klicken Sie zur Zwischenausgabe auf 'Run Code'.

`@hint`
Eine Zuweisung (<-) funktioniert mit diesem Zeichen in R. Weisen Sie der Variablen den numerischen Wert 17 zu.

`@sample_code`
```{r}
#1.numerische Variable?
is.numeric(Anzahl_Mitarbeiter)
#class(Anzahl_Mitarbeiter) funktioniert auch, gibt direkt den Basisdatentyp aus. Dies können Sie an anderer Stelle verwenden.
#2.Ausgabe + Zuweisung


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
