# Datensatz Anne Will – Ukraine 2022

Codebuch Stand 2026-11 erstellt von Liv Krautwasser

## Inhalt

- edgelist.csv (Edgelist)
- nodelist.csv (Nodelist)
- codebook.md (Codierung der Datensätze)

## Ursprung und Datenerhebung

Der Datensatz basiert auf der Gästeliste der Talkshow *Anne Will*. Untersucht werden die Folgen 500 bis 503 aus dem Jahr 2022, in denen das Thema Ukraine behandelt wurde.

Die Datenerhebung umfasst die teilnehmenden Gäste, die Talkshow sowie die Parteizugehörigkeiten der Gäste.

Das Netzwerk ist ein *gerichtetes Netzwerk two-mode Netzwerk*. Die Beziehungen werden in zwei Kategorien unterteilt:

**Teilnahmenetzwerk**

Die Beziehung zwischen einem Gast und einer Sendung beschreibt, an welcher Folge der jeweiligen Talkshow die Person teilgenommen hat.

**Parteizugehörigkeit**

Die Beziehung zwischen einem Gast und einer Partei beschreibt die Parteizugehörigkeit des jeweiligen Gastes.

Die Beziehungen werden gerichtet erhoben. Der Ausgangsknoten (erste Spalte) ist immer der Gast, der Zielknoten (zweite Spalte) die jeweilige Sendung oder Partei.

# EDGE-Attribute

**from**

Enthält die ID des Gastes, von dem die Beziehung ausgeht. Die IDs der Gäste werden aus den Initialen des Vor- und Nachnamens gebildet, beispielsweise lk für Lars Klingbeil.

**to**  

Enthält die ID der Sendung oder Partei, zu der die Beziehung besteht. Die Sendungen werden über ihre Folgenummer (500 bis 503), die Parteien über ihre üblichen Abkürzungen in Kleinbuchstaben codiert.

**relationship**  
(Beziehungsart zwischen den Knoten)

1 = Gast: Bei dieser gerichteten Beziehung nimmt der Gast (erste Spalte) an der entsprechenden Anne-Will-Sendung (zweite Spalte) teil.

2 = Mitgliedschaft: Bei dieser gerichteten Beziehung wird die Parteizugehörigkeit des Gastes (erste Spalte) zur entsprechenden Partei (zweite Spalte) dargestellt.

Beispiele:

lk,500,1 = Lars Klingbeil nimmt an Folge 500 teil.

lk,spd,2 = Lars Klingbeil gehört der SPD an.

# NODE-Attribute

**id**  
(Eindeutige Codierung des Knotens)

Jeder Knoten erhält eine eindeutige ID. Bei Gästen werden die Initialen des Vor- und Nachnamens verwendet, bei Sendungen die jeweilige Folgenummer und bei Parteien die üblichen Parteikürzel in Kleinbuchstaben.

**name**  
(Vollständiger Name des Knotens)

Bei Gästen wird der vollständige Vor- und Nachname angegeben. Bei Sendungen wird die jeweilige Folgenummer angegeben, beispielsweise Folge 500. Bei Parteien wird der vollständige Parteiname verwendet.

**type**  
(Art des Knotens)

1 = Gast (teilnehmende Person der Talkshow)

2 = Sendung (Anne-Will-Folge 500 bis 503)

3 = Partei (politische Partei eines Gastes)

**party**  
(Parteizugehörigkeit des Gastes)

Gibt die Parteizugehörigkeit des jeweiligen Gastes an. Die Parteien werden mit ihren üblichen Abkürzungen erfasst:

SPD = Sozialdemokratische Partei Deutschland

CDU = Christlich Demokratische Union

GRUENE = Bündnis 90/Die Grünen

FDP = Freie Demokratische Partei

LINKE = Die Linke

Bei Gästen ohne bekannte Parteizugehörigkeit bleibt das Feld frei. Bei Sendungs- und Parteiknoten wird dieses Attribut ebenfalls nicht ausgefüllt.

**sector**  
(Gesellschaftlicher bzw. beruflicher Bereich des Gastes)

Beschreibt den beruflichen oder gesellschaftlichen Bereich, dem der Gast zugeordnet wird:

Politik

Journalismus

Wissenschaft

Militaer 

Bei Sendungs- und Parteiknoten bleibt das Feld frei.

**country**  
(Land des Gastes)

Gibt das Land an, dem der jeweilige Gast zugeordnet wird. Die Länder werden ausgeschrieben angegeben:

Deutschland

Ukraine

Niederlande

Bei Sendungs- und Parteiknoten bleibt das Feld frei.

# Untersuchungszeitraum

Untersucht werden die Anne-Will-Sendungen 500, 501, 502 und 503 aus dem Jahr 2022 mit dem Thema Ukraine.

Die Datengrundlage bildet der Episodenguide von Fernsehserien.de:

https://www.fernsehserien.de/anne-will/episodenguide
