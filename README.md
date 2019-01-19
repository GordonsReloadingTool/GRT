# Gordons Reloading Tool

Dies ist die Projektseite für das GRT. 

GORDONS RELOADING CHANNEL
https://youtube.com/GordonsReloading
gordonsreloading@gmail.com

================================================================================
 G O R D O N S  R E L O A D I N G  T O O L
 I N N E N B A L L I S T I K
================================================================================

  Copyright (c) Gordons Reloading Channel, all rights reserved
  Commercial use without written permission is strictly prohibited.

--------------------------------------------------------------------------------
ERLÄUTERUNG (und wie es dazu kam)
--------------------------------------------------------------------------------
Diese Software ist das Ergebnis meiner Nachforschungen und Recherche zur
innenballistischen Berechnung anhand eines mathematischen Simulationsmodells.

Intern wird eine Simulationsrechnung vorgenommen, welche den Abbrand des
Pulvers, der dabei entstehenden Gase, Drücke und Energie anhand eines
Formalismus berechnet, der auf wissenschaftliche Untersuchungen
beruht, deren Entwicklung wiederum bis über 100 Jahre zurück reichen.

Die durch die Umsetzung der Treibladung freigesetzte chemische
Energie teilt sich bei der Schussentwicklung im wesentlichen auf in:

 - translatorische Geschossenergie
 - rotatorische Geschossenergie
 - Strömungsenergie der Pulvergase
 - Innere Energie der Pulvergase
 - Wärmeverluste an Rohr, Geschoß und Hülse
 - Reibung und Wärmeübergang
 - Arbeit gegen den Ausziehwiderstand
 - Arbeit beim Einpressen des Geschosses in die Züge
 - Energie der rücklaufenden Waffenteile
 - Energie zum Antrieb (halb-)automatischer Waffen

Der Anteil des Waffenrücklaufs sowie gegebenenfalls der Antriebsenergie von
automatischen Waffen an der Gesamtenergie beträgt insgesamt weniger als 1%
und wird daher vernachlässigt.

Die Strömungsenergie der Pulvergase läßt sich durch Hinzufügen eines
Anteils der Ladung (Mitführungsfaktor, Sebertscher Faktor) zu der zu
beschleunigenden Geschossmasse in der Rechnung erfassen. Man rechnet also,
wie auch in anderen Bereichen der Physik üblich, mit einer effektiven Masse.
Auch andere Energieverluste lassen sich hier in der effektiven Masse
berücksichtigen, wie z.B. die Energieverluste durch Wärmeeintrag.

URSPRUNG/QUELLENANGABE

Primär basiereren die Algorithmen in der Basis auf Informationen, welche
im "Waffentechnische Taschenbuch" von Rheinmetall zu finden sind.
Dort wird im Detail u.A. anhand eines Beispiels beschrieben, wie eine solche
Rechnung aussehen kann. Davon mal abgesehen, dass dieses Taschenbuch auch
sonst hoch interessant ist, fällt dabei auf das auch die Software "QuickLOAD"
hier dieselben Bezeichner für entsprechende Basiswerte nutzt, wie z.B. "Ba" für
den Abbrandkoeffizienten uvm. Da in modernerer Literatur sonst andere Bezeichner
gewählt werden, die Ergebnisse sich frappierend ähneln, ist es ziemlich
plausibel das der Formalismus in QuickLOAD ebenfalls genau jene Algorithmen
zur Basis haben, welche im Waffentechnischen Taschenbuch von Rheinmetall
vereinfacht aufgezeigt werden.

Wen das Interessiert, sucht nach dem Titel

"Rheinmetall Waffentechnisches Taschenbuch"

Im Waffentechnischen Taschenbuch wird ab Seite 70 die innenballistische
Kalkulation im Detail inkl. eines Beispiels erläutert. Die dort angeführten
Differentialgleichungen sind ALS BASIS für die Rechnungen zu verstehen.
Sie behandeln den Fall für ein Treibladungspulver das gleichmäßig abbrennt,
weil die Gleichungen dafür wesentlich einfacher sind.

Die verschiedenen Treibladungspulver haben verschiedene Abbrandcharakteristika,
d.h. je nach Typ verbrennt das Pulver im Laufe der Druckentwicklung mit
UNTERSCHIEDLICH schneller Geschwindigkeit! Solche Pulver sind dann progressiv,
degressiv bzw. eine Kombination daraus. Die Begriffe "progressiv" und "offensiv"
schließen sich hier bei nicht aus, denn auch ein offensives Pulver kann
stark progressiv ausfallen.

Mit dem unterschiedlichen Abbrandverhalten lässt sich beeinflussen, ob z.B.
ein Geschoss in einem längeren Lauf stärker beschleunigt wird und gleichzeitig
aber der Druck dabei niedrig bleiben kann.

Diese Charakteristik wird durch eine sog. FORMFUNKTION spezifiziert und diese
Formfunktion beschreibt dann mathematisch angenähert das Verhalten des
Pulvers während des Abbrands. FÜR EINE KORREKTE IMPLEMENTIERUNG MUSS MAN
ALSO DIE DIFFERENTIALGLEICHUNG AUS DEM TASCHENBUCH MIT EINGEBAUTER FORMFUNKTION
NEU LÖSEN. Dies macht das Testprogramm und das ist augenscheinlich wohl auch
der Formalismus, den auch QuickLOAD in einer eigenen Form für seine
Simulationsrechnung nutzt.

Gordon
06.01.2019
