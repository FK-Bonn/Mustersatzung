# Mustersatzung
## Verwendung der Mustersatzung
Diese Mustersatzung ist mit der Textsatzsprache LaTeX geschrieben - für diejenigen, die mit LaTeX nicht vertraut mag das abschreckend wirken, deshalb soll hier kurz erklärt werden, wie die Mustersatzung auf die individuelle Fachschaft angepasst werden kann.

### Erabeitung der Beschlussvorlage
Um die Mustersatzung so zu individualiseren, dass sie der Fachschaft zum Beschluss vorgelegt werden kann, müssen einige Variablen angepasst werden. Diese befinden sich direkt zu Beginn des Dokuments im Bereich "Variablen".
``` %=================== VARIABLEN ========================
\newcommand{\fachschaft}{Musterfachschaft}
\newcommand{\beschlussgremium}{FSV} %FSV oder FSVV
\newcommand{\beschlussdatum}{01.01.2020} %DD.MM.YYYY
\newcommand{\vorsitz}{Max Mustermann} %Vorsitzender
\setboolean{publish}{false} %1 - Beschlussvorlage, 2 - Veröffentlichung
\newcommand{\fsrgroesse}{neun}
%====================================================
```
