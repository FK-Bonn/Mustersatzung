# Mustersatzung
## Verwendung der Mustersatzung
Diese Mustersatzung ist mit der Textsatzsprache LaTeX geschrieben - für diejenigen, die mit LaTeX nicht vertraut sind, mag das abschreckend wirken, deshalb soll hier kurz erklärt werden, wie die Mustersatzung auf die individuelle Fachschaft angepasst werden kann.
Um die Dateien zu bearbeiten, können entweder diverse Offline-Editoren verwendet werden, online geht es zum Beispiel mit [Overleaf](www.overleaf.com).

### Erabeitung der Beschlussvorlage
Um die Mustersatzung so zu individualiseren, dass sie der Fachschaft zum Beschluss vorgelegt werden kann, müssen einige Variablen angepasst werden. Diese befinden sich direkt zu Beginn des Dokuments im Bereich "Variablen".
``` 
%=================== VARIABLEN ========================
\newcommand{\fachschaft}{Musterfachschaft}
\newcommand{\beschlussgremium}{FSV} %FSV oder FSVV
\newcommand{\beschlussdatum}{01.01.2020} %DD.MM.YYYY
\newcommand{\vorsitz}{Max Mustermann} %Vorsitzender
\setboolean{publish}{false} %1 - Beschlussvorlage, 2 - Veröffentlichung
\newcommand{\fsrgroesse}{neun}
%====================================================
```
#### Name der Fachschaft
Mit `\newcommand{\fachschaft}{Musterfachschaft}` wird der Name der Fachschaft eingestellt. Einfach Musterfachschaft durch den Namen der Fachschaft ersetzen.

#### Größe des FSR
Mit `\newcommand{\fsrgroesse}{neun}` wird die Größe des FSR festgelegt. Diese Größe muss nach der Fachschaftswahlordnung zwischen 5 und 9 liegen. Um bei Abstimmungen ein Patt zu vermeiden, sollte eine ungerade Zahl, also 5, 7 oder 9 gewählt werden. Die Variable wird geändert, indem anstelle von "neun" die gewünschte Zahl kleingeschrieben eingefügt wird, sodass sie sich in den Satz "Der FSR besteht aus **neun** regulären Mitgliedern." einfügt.

#### Beschlussgremium
Mit `\newcommand{\beschlussgremium}{FSV}` wird das Gremium, welches die Satzung beschließt, angepasst. Dafür kommt entweder die Fachschaftsvertretung (FSV) oder die Fachschaftsvollversammlung (FSVV) in Frage. 
