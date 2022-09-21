# Mustersatzung
## Verwendung der Mustersatzung
Diese Mustersatzung ist mit der Textsatzsprache LaTeX geschrieben - für diejenigen, die mit LaTeX nicht vertraut sind, mag das abschreckend wirken, deshalb soll hier kurz erklärt werden, wie die Mustersatzung auf die individuelle Fachschaft angepasst werden kann.
Um die Dateien zu bearbeiten, können entweder diverse Offline-Editoren verwendet werden, online geht es zum Beispiel mit [Overleaf](https://www.overleaf.com).

### Erarbeitung der Beschlussvorlage
Um die Mustersatzung so zu individualiseren, dass sie der Fachschaft zum Beschluss vorgelegt werden kann, müssen einige Variablen angepasst werden. Diese befinden sich direkt zu Beginn des Dokuments im Bereich "Variablen".
``` 
%=================== VARIABLEN ========================
\newcommand{\fachschaft}{Musterfachschaft}
\newcommand{\beschlussgremium}{FSV} %FSV oder FSVV
\newcommand{\beschlussdatum}{01.01.2020} %DD.MM.YYYY
\newcommand{\vorsitz}{Max Mustermann} %Vorsitzender
\setboolean{publish}{false} %false - Beschlussvorlage, true - Veröffentlichung
\newcommand{\fsrgroesse}{neun}
%======================================================
```
#### Name der Fachschaft
Mit `\newcommand{\fachschaft}{Musterfachschaft}` wird der Name der Fachschaft eingestellt. Dazu wird `Musterfachschaft` zwischen den geschweiften Klammern durch den Namen der Fachschaft ersetzt. Am Beispiel der Fachschaft Romanistik sähe das dann so aus: `\newcommand{\fachschaft}{Romanistik}`.

#### Größe des FSR
Mit `\newcommand{\fsrgroesse}{neun}` wird die Größe des FSR festgelegt. Diese Größe muss nach der Fachschaftswahlordnung zwischen 5 und 9 liegen. Um bei Abstimmungen ein Patt zu vermeiden, sollte eine ungerade Zahl, also 5, 7 oder 9 gewählt werden. Die Variable wird geändert, indem anstelle von "neun" die gewünschte Zahl kleingeschrieben eingefügt wird, sodass sie sich in den Satz "Der FSR besteht aus **neun** regulären Mitgliedern." einfügt.

#### Beschlussgremium
Mit `\newcommand{\beschlussgremium}{FSV}` wird das Gremium, welches die Satzung beschließt, angepasst. Dafür kommt entweder die Fachschaftsvertretung (FSV) oder die Fachschaftsvollversammlung (FSVV) in Frage. 

### Beschluss der Satzung
Nach Anpassung der Beschlussvorlage wird das Dokument kompiliert und das resultierende PDF an das zuständige Beschlussorgan geschickt. Soweit eine Fachschaftsvertretung (FSV) besteht, beschließt sie mit der absoluten Mehrheit von 2/3 ihrer Mitglieder; Ansonsten beschließt die FSVV mit der absoluten Mehrheit der anwesenden Fachschaftsmitglieder. Die Satzung kann **nicht** durch einen Fachschaftsrat beschlossen werden, auch wenn dieser direkt gewählt wurde.

### Fertigstellung für die Veröffentlichung
#### Aktivierung der finalen Version
Um die "Beschlussempfehlung"-Markierungen zu entfernen, muss die Variable `\setboolean{publish}{false}` von `false` auf `true` geändert werden.

#### Beschlussgremium
Bei `\newcommand{\beschlussgremium}{FSV}` wird das Organ, welches die Satzung beschlossen hat, eingetragen, also entweder `FSV`oder `FSVV`.

#### Beschlussdatum
Bei `\newcommand{\beschlussdatum}{01.01.2020}` wird das Datum, an dem die Satzung beschlossen wurde, im Format DD.MM.YYYY eingetragen.

#### Vorsitz des Beschlussgremiums
Bei `\newcommand{\vorsitz}{Max Mustermann}` wird der Name des/der Vorsitzenden des Beschlussgremiums, also entweder dem FSV-Vorsitzenden oder dem Versammlungsleiter der FSVV, eingetragen.

### Bekanntmachung
Die Satzung wird kompiliert und ist damit fertig, das resultierende PDF sollte aber sicherheitshalber noch einmal kontrolliert werden. Die fertige Fassung wird **vor dem Beschluss** per Email zur Kenntnisnahme an das [Fachschaftenreferat](http://www.asta-bonn.de/Fachschaftenreferat) und das [Präsidium des Studierendenparlaments](https://www.sp.uni-bonn.de/kontakt/) geschickt, und **nach dem Beschluss** an die [Öffentlichkeitsbeauftragte](https://sp.uni-bonn.de/bekanntmachungen/howto) zur Bekanntmachung.
