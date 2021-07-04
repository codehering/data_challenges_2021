# Data Challanges - Numismatic 2021 Repository
Dieses Repository beinhaltet alle Skripte und Experimente, die im Rahmen der Vorlesung Data Challenges erstellt wurden. Im Folgenden wird dabei kurz auf die einzelnen Verzeichnisse eingegangen.

## Technische Umsetzung
Für die technische Umsetzung des Projektes wurden die Programmiersprache Python und die statistische Skriptsprache R verwendet. Dabei wurde vor allem im ersten Schritt für die jeweiligen Experimente und explorativen Analysen Python mit der Erweiterung Jupyter Notebook verwendet. Für das interaktive Dashboard wurde wiederum das sehr einfach gehaltene High-level Framework Shiny verwendet. 

## Verzeichnisstruktur:

### dashboard:
Beinhaltet alle Skripte die für das Dashboard benötigt werden, inklusive der Skripte, die die Daten in geeigneter Weise aufbereiten, so dass diese vom Dashboard verarbeitet werden können. Dabei wird unteschieden zwischen:

**-Frontend:**

Unter Frontend sind nur Skripte die für das das Dashboard selbst benötigt werden. Also alle Skripte die für die interaktive Darstellung notwendig sind (inklusive Login, das Laden der Daten und Aggregation der Daten.

**-Backend:**

Unter Backend sind alle Skripte die notwendig sind, um die Daten in ein für das Dashboard geeignetes Format zu bringen (rds format) (ETL.R). Des Weiteren liegt in diesem Verzeichnis rf_classifer.R. Dieses Skript trainiert die RandomForest modelle die für den Coin Finder des Dashboards notwendig sind, um ähnliche Münzen anhand bestimmter Kriterien finden zu können.
### data_prep:
Unter data_prep finden sich alle Skripte die für die Aufbereitung der daten Notwendig waren. Dabei existieren Entitätsspezifische Skripte,w ei auch Skripte die sich mit der Aufbereitung des RDF-Datensatzes beschaftigen. Als wichtigstes Skript kann hier data_preperation_for_analysis.py gesehen werden, welches die über eine SPARQL-Query gezogenen Daten für die weiteren Analyseschritte aufbereitet.
### experiments:
In dem Verzeichnis experiments liegen alle Skripte, welche uns geholfen haben entweder die Daten an sich oder verschiedene datengetriebene Methoden zu verstehen. Wichtig ist, dass nicht alle Ideen und Methoden, die in diesem Verzeichnis angewandt wurden, auch später weiter verfolgt und ausgebaut worden sind. Insofern kann dieses verzeichnis als Sammelstelle aller für das Projekt essenziell wichtiger Teile betrachetet werden, auch wennn vieles keinen direkten Einfluss auf die Ergebnisse unseres Projektes hatten.
### plots:
Im plots Verzeichnis sind unsere Bilder (wie etwa Korrelationsmatrix, ergebnisse aus kmeans, etc.) gespeichert.

## Das Dashboard
Zentraler Bestandteil unserer Arbeit war neben der explorativen Analyse der Münzdaten auch ein R Shiny Dashboard, welches als self-service Analysetool gesehen werden kann. Das Dashboard wurde von uns eingeführt, da wir Probleme hatten einzelne Cluster oder Gruppen von Münzen mit klassischen Plots und Tabellen zu analysieren. Insbesondere die zeitliche Untersuchung verschiedener Entitäten ist mit einem einfachen Plot und der Tatsache, dass über 500 verschiedene Entitäten existieren, sehr schwierig. Aus diesen Gründen haben wir uns dazu entschieden ein einfaches dashboard mit interaktiven Elementen und verschiedenen Filtern zu programmieren. Eventuell können auch Numismatiker von diesem Dashboard profitierern, indem diese eigenständige Analysen durchführen können. Dabei ist das Dashboard in verschiedene Tabs unterteilt, diese werden durch einen Help-Tab unterstützt, der die den Umgang mit dem Tool erklären soll:
### Coin Explorer
Der Coin Explorer hat das Ziel der Clusteranalyse und insbesondere der UMAP Dimensionsreduzierung darzustellen. 
### Entity Explorer
### Coin Finder



