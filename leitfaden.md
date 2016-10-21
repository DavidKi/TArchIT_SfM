> TArchIT Workshop

SfM mit VisualSFM, Meshlab und Blender V1.2

![](media/image1.jpg){width="6.3in" height="2.7284722222222224in"}

mit Jonas Abele M.A. und Marcel C. Hagner B.A.

04.07-05.07.2016

INHALT

[Kapitel 1: Erste Schritte in Visual SFM
3](#kapitel-1-erste-schritte-in-visual-sfm)

[1.1. Installation 3](#installation)

[1.2. Überblick Programmoberfläche Visual SfM (Start)
4](#überblick-programmoberfläche-visual-sfm-start)

[1.3. Schritt 1: Importieren der Fotos
5](#schritt-1-importieren-der-fotos)

[1.4. Schritt 2: Berechnung der dünnen Punktwolke
5](#schritt-2-berechnung-der-dünnen-punktwolke)

[1.5. Schritt 3: Berechnung der dichten Punktwolke
6](#schritt-3-berechnung-der-dichten-punktwolke)

[1.6. Zusammenfassung Workflow VisualSfM
7](#zusammenfassung-workflow-visualsfm)

[Kapitel 2: Erste Schritte in MeshLab
8](#kapitel-2-erste-schritte-in-meshlab)

[2.1. Installation 8](#installation-1)

[2.2. Überblick Programmoberfläche MeshLab
8](#überblick-programmoberfläche-meshlab)

[2.3. Laden der VisualSFM-Punktwolken
9](#laden-der-visualsfm-punktwolken)

[2.4. Bereinigung der dichten Punktwolke
10](#bereinigung-der-dichten-punktwolke)

[2.5. Konvertierung der dichten Punktwolke in ein Gitter
10](#konvertierung-der-dichten-punktwolke-in-ein-gitter)

[2.6. Bereinigung des Gitter (Non-Manifold Edges)
11](#bereinigung-des-gitter-non-manifold-edges)

[2.7. Parametrisierung der Textur / Export
12](#parametrisierung-der-textur-export)

[2.8. Zusammenfassung Workflow MeshLab
13](#zusammenfassung-workflow-meshlab)

[Kapitel 3: Erste Schritte in Blender
14](#kapitel-3-erste-schritte-in-blender)

[3.1. Installation und Allgemeines 14](#installation-und-allgemeines)

[3.2. Überblick Programmoberfläche Blender
14](#überblick-programmoberfläche-blender)

[3.3. Grundlegendes 15](#grundlegendes)

[3.4. Textur auflegen 15](#textur-auflegen)

[3.5. Animation „Rundflug“ 16](#animation-rundflug)

[3.6. Animation: Beleuchtung 17](#animation-beleuchtung)

[3.7. Animation: Videoexport 18](#animation-videoexport)

[4. Notizen 18](#notizen)

![](media/image3.png){width="2.7743055555555554in"
height="1.0638888888888889in"}![](media/image4.png){width="1.2583333333333333in"
height="1.175in"} SfM Workshop KuLa-Hof

4\. Juli 2016 bis 05. Juli 2016

Kapitel 1: Erste Schritte in Visual SFM
=======================================

1.1. Installation
-----------------

-   VisualSfM muss **nicht installiert** werden und kann z.B. von
    <http://ccwu.me/vsfm/> bezogen werden.

-   Mittels VisualSFM wird eine dichte Punktwolke aus Fotos erzeugt,
    welche im Anschluss in ein 3D-Modell überführt werden kann (siehe
    Kapitel 2 und 3).

-   Der gesamte Ordner „Visual\_SfM\_\*\*\*\*“ sollte schlicht auf die
    Festplatte, wenn möglich auf eine vorhandene SSD
    (**S**olid-**S**tate-**D**rive), kopiert werden. Es ist aber auch
    möglich VisualSfM von einem **USB-Stick, SD-Karte oder
    Netzwerklaufwerk** zu starten, wovon wir dringend abraten **(Verlust
    von Rechenleistung!)**.

-   Um das Programm leichter starten zu können, sollte eine
    **Verknüpfung der VisualSFM.exe** auf z.B. den **Desktop** oder
    **die Taskleiste** erstellt werden.

Hierzu genügt ein **Rechtsklick** auf die \*.**exe-Datei** im Ordner
„Visual\_SfM\_\*\*\*\*“. Im nun geöffneten Menü kann dann unter
**„Senden an“** „**Desktop (Verknüpfung erstellen)“ rasch eine passende
Verknüpfung auf den Desktop angelegt werden.**

![](media/image5.png){width="3.7416666666666667in"
height="2.163089457567804in"}

-   Per Doppelklick auf die \*.exe-Datei oder durch einen Klick auf die
    Verknüpfung, startet Visual SfM.

1.2. Überblick Programmoberfläche Visual SfM (Start)
----------------------------------------------------

![](media/image6.png){width="6.295833333333333in"
height="3.3916666666666666in"}

![](media/image7.png){width="6.208333333333333in" height="0.95in"}

I.  

<!-- -->

I.  **An-/Ausschalten des Protokoll-Fensters**

II. **Laden eines fertigen (dichten)
    Punktwolken-Modells (\*.nvm-Datei)**

III. **Laden von mehreren Bildern zur Durchführung der SfM-Berechnung**

IV. **Speichert die aktuelle Ansicht als u.a. \*.jpeg (Screenshot)**

V.  **Kopiert die aktuelle Ansicht (nicht als Bild!)**

VI. **Schaltet Bilder / Bildpaare nach links durch**

VII. **Schaltet Bilder / Bildpaare nach rechts durch**

VIII. **2D-3D- Wechsel**

IX. **Auf Miniaturansicht umschalten**

X.  **Zoom**

XI. **Ansicht wird zurückgesetzt**

XII. **Schaltet Einzel- und Multi-Modelle aus und ein**

XIII. **Zeigt Verknüpfungen an (2D-Modus)**

XIV. **Berechnet die Bildposition aller Fotos (rechenintensiv)**

XV. **Berechnung der dünnen Punktwolke**

XVI. **Weitere Berechnung der dünnen Punktwolke (z.B. mit einem
    zusätzlichen Bild)**

XVII. **Stoppt den laufenden Prozess**

1.3. Schritt 1: Importieren der Fotos
-------------------------------------

-   ![](media/image7.png){width="0.3541666666666667in"
    height="0.3333333333333333in"}Visual SfM nutzt Fotos **im
    JPEG-Format**

-   ![](media/image8.png){width="0.23333333333333334in"
    height="0.24166666666666667in"}**Fotos** können im Reiter : **File
    Open + Multi-Images** oder über den Schaltfläche **III
    geladen werden.**

-   Dort sind **alle Fotos auszuwählen**, die zur Modellberechnung
    verwendet werden sollten.

    -   Mit **\[Strg + A\]** können Sie u.a. alle Daten eines
        Ordners markieren.

    -   Mit **\[Strg\] + Linker-Maustaste** können einzelne
        Fotos/Dateien wieder

> (ab-)gewählt werden .

-   Das **Importieren** der Fotos dauert meist weniger **als
    eine Minute. Im Bereich der Informationszeile** wird über Drücken
    der **\[X\]-Taste** auf der Tastatur die bisherige **Rechendauer
    angezeigt,** im Bereich des **Protokollfensters** wird **„Loading
    image pixel data ...“** stehen. Je nach **Fotomenge** und der
    jeweiligen **Auflösung** der Aufnahmen dauert dieser Schritt
    **entsprechend länger**.

-   Die Bilder sollten nun als **Miniaturansicht im
    Modell/Fotofensterbereich** erscheinen.

-   Mittels **Rechtsklick** können Sie die **Bilder markieren** (rote
    Rahmung erscheint).

-   **Doppelklick auf eines der Bilder** im Modell/Fotofenster zur
    Vergrößerung des jeweiligen Bildes.

    -   Mit dem **Mausrad** kann gezoomt werden, Schaltfläche **X**
        bietet vordefinierte Zoomstufen an.

    -   Es ist möglich **die Bilder** mit den Knöpfen **VI** (links) und
        **VII** (rechts) **durchzuschalten**. Dies dient u.a. zur
        Kontrolle der Bilder auf Schärfe oder unerwünschte Störungen.

![](media/image7.png){width="0.28395450568678915in" height="0.28125in"}1.4. Schritt 2: Berechnung der dünnen Punktwolke
-----------------------------------------------------------------------------------------------------------------------

-   ![](media/image9.png){width="0.23392607174103236in"
    height="0.24166666666666667in"}Durch Drücken der Schaltfläche
    **XIV** (Compute Missing Matches) werden die Bilder verglichen zu
    ihren Positionen zugeordnet.

    -   **Dieser Prozess benötigt Zeit!** Sobald der Prozess
        abgeschlossen ist, werden zusätzliche Daten zu den
        Bildern hinzugefügt. Diese zusätzlichen Daten ermöglichen es,
        bei der nächsten Verwendung der Bilder den Rechenschritt
        (Compute Missing Matches) **zu überspringen.**

-   Das Ende des Prozesses kann im Protokoll-Fenster beobachten werden.

    -   Protokoll-Fenster: *„Compute Missing Pairwise
        Matching, finished“.*

<!-- -->

-   Nun folgt die Berechnung der **dünnen Punktwolke. **

-   Durch Drücken der Schaltfläche **XV** (Compute 3D
    Reconstruction)![](media/image9.png){width="0.23392607174103236in"
    height="0.24166666666666667in"}![](media/image7.png){width="0.3229166666666667in"
    height="0.28125in"} wird die dünne **Punktwolke aus den Bildern
    berechnet**. Dieser Schritt ist im Modell/Foto-fenster
    zu beobachten. Mittels der **rechten Maustaste** kann die
    entstehende Punktwolke während dieses Prozesses **gedreht werden**.

-   Das Ende des Prozesses können Sie im Protokoll-Fenster beobachten.

    -   Protokoll-Fenster: *„* *Run full 3D reconstruction, finished “*

<!-- -->

-   Durch Drücken der **\[Strg\]-Taste** und durch die **Betätigung des
    Mausrades** können die **Bildvorschaufenster vergrößert und
    verkleinert** werden.

-   Durch Drücken der **\[Shift\]-Taste** und durch die **Betätigung des
    Mausrades** können Sie die einzelnen **Punkte der Punktwolke
    vergrößern und verkleinern**.

-   Durch **einen Rechtsklick** aus eines der Bildvorschaufenster wird
    das jeweilige **Bild markiert**. Gleichzeitig leuchten in der
    Punktwolke die dazugehörigen Punkte rot auf. Dies dient schlicht zur
    Kontrolle der Bildqualität bzw. der Fotoposition.

1.5. Schritt 3: Berechnung der dichten Punktwolke
-------------------------------------------------

![](media/image10.png){width="0.3645833333333333in"
height="0.35138888888888886in"}*Um die dichten Punktwolke zu berechnen
wird ein weiteres Programm benötigt. Das Programm CMVS ist in der
TArchIT-Version von VisualSFM bereits mit im\
Programmordner von VisualSFM abgespeichert und muss somit nicht mehr
separat heruntergeladen und dorthin abgespeichert werden.*

-   ![](media/image9.png){width="0.23392607174103236in"
    height="0.24166666666666667in"}Direkt nachdem die dünne Punktwolke
    berechnet wurde (Schritt 2) können Sie über die nun **erweiterte**
    Schaltfläche CMVS auswählen **(links neben Schaltfläche XVII).**

-   Nach dem Klicken auf CMVS öffnet sich ein neues Fenster. Dort **muss
    der Workspace bzw. der Speicherort der dichten Punktwolke
    gewählt werden. **

    -   Es bietet sich an, **denselben Speicherort** für die dichte
        Punktewolke wie für die Fotos zu wählen.

    -   Nachdem der Speicherort gewählt wurde, **beginnt die aufwendige
        Berechnung der dichten Punktwolke.**

    <!-- -->

    -   ***ACHTUNG! Dieser Schritt ist ein aufwendiger Rechenprozess!***

<!-- -->

-   Je nach Bildmenge und Rechenleistung kann dieser Schritt sehr lange
    dauern! **Im Bereich der Informationszeile** wird über Drücken **der
    \[X\]-**Taste auf der Tastatur die bisherige
    **Rechendauer angezeigt.**

    -   Im Protokollfenster steht: *„This may take a little more time,
        waiting...”*

-   Sollte das Protokollfenster nicht mehr vorhanden sein, kann es
    entweder über einen Klick auf die Schaltfläche **I** oder über die
    Schaltfläche „**File New Window“** wieder geöffnet werden.

-   Das **Ende des Prozesses** kann im Protokoll-Fenster
    beobachten werden.

    -   Protokoll-Fenster: *„* *Run dense reconstruction, finished “*

<!-- -->

-   Durch betätigen der ***Tab-Taste*** können Sie nun zwischen der
    dichten und der der dünnen Punktwolke **hin und her wechseln.**

> *Wichtig: Die dichte Punktewolke ist kein Modell! Sie besteht nur aus
> Punkten und muss deshalb in einem weiteren Schritt vernetzt bzw.
> „vermesht“ werden. Hierzu wird z.B. Meshlab verwendet. Weiteres zu
> MeshLab in Kapitel 2.*

1.6. Zusammenfassung Workflow VisualSfM
---------------------------------------

(1) VisualSFM starten.

(2) Bilder laden ( **Schaltfläche III** oder File Open + Multi-Images).

    -   Warten bis die Bilder geladen sind.

(3) Drücken der **Schaltfläche XIV** (Compute Missing Matches).

    -   Warten bis der Prozess abgeschlossen ist.

(4) Drücken der **Schaltfläche XV** (Compute 3D Reconstruction).

    -   Warten bis der Prozess abgeschlossen ist.

(5) Drücken auf der nun erweiterten **Schaltfläche auf CMVS.**

    -   Warten bis der Prozess abgeschlossen ist.

(6) Dichte Punkte ist bereit zur Weiterverarbeitung -&gt; **weiter mit
    MeshLab…**

![](media/image10.png){width="0.5833333333333334in"
height="0.5622222222222222in"}![](media/image7.png){width="0.53125in"
height="0.5273436132983377in"}![](media/image7.png){width="0.6051695100612423in"
height="0.5270833333333333in"}![](media/image7.png){width="0.5974223534558181in"
height="0.5625in"}

![](media/image11.png){width="0.875in" height="0.8716087051618547in"}Kapitel 2: Erste Schritte in MeshLab
=========================================================================================================

2.1. Installation
-----------------

-   MeshLab kann über z.B. <https://sourceforge.net/projects/meshlab/>
    bezogen werden.

-   Nach der Installation kann **MeshLab gestartet werden**. Ein
    Verknüpfungssymbol sollte bereits **automatisch auf den Desktop**
    angelegt worden sein.

-   Aufgabe von MeshLab ist es, die aus VisualSFM **erstellt dichte
    Punktwolke** **zu „bereinigen“ und aus ihr ein Gitter (engl. mesh)
    zu erzeugen.**

 2.2. Überblick Programmoberfläche MeshLab 
-------------------------------------------

![](media/image12.png){width="5.572916666666667in"
height="0.8645833333333334in"}![](media/image13.png){width="6.3in"
height="3.4125in"}

I.  **Öffnen eines neuen Projektes **

II. **Öffnen eines gespeicherten Projektes **

III. **Import eines Gitters / Mesh**

IV. **Aktualisieren der Anzeige**

V.  **Export des aktuellen Gitters / Mesh**

VI. **Speichert die aktuelle Ansicht als u.a. als \*.jpeg (Screenshot)**

VII. **Öffnet die Layer-Anzeige (meist linker Bildschirmrand)**

VIII. **Raster-Modus**

IX. **Ansicht: Begrenzungsrahmen**

X.  **Ansicht: Punktwolke**

XI. **Ansicht: Draht-Gitter**

XII. **Ansicht: Draht-Gitter mit Flächenanzeige**

XIII. **Ansicht: Gitter/Modell „kantig“**

XIV. **Ansicht: Gitter/Modell „glatt“**

XV. **Ansicht: Gitter/Modell mit Textur**

XVI. **Künstliche Modellbeleuchtung an / ausschalten**

2.3. Laden der VisualSFM-Punktwolken
------------------------------------

-   Zunächst müssen die **Projektdaten (NView Match File)** aus
    VisualSFM in MeshLab geladen werden.

-   Dazu wird MeshLab geöffnet und über Schaltfläche **II** oder über
    **„File Open project“** das Projekt geöffnet. Benötigt werden hierzu
    **zwei Dateien**, die VisualSFM automatisch stets mit **derselben
    Bezeichnung abspeichert.**

    -   Geöffnet werden muss der **Speicherort des
        VisualSFM-Projektes** (z.B. der Ordner *Beispiel*.nvs.cvms).
        Dort befindet sich **ein Unterordner 00.**

    -   Im Unterordner 00 müssen Sie zunächst die Datei:
        **„bundle.rd.out“ auswählen.**

    -   Danach öffnet sich erneut ein Fenster und nun muss die
        **passende Textdatei „list“** im selben Verzeichnis
        (*Beispiel*.nvs.cvms\\00\\) ausgewählt werden.

<!-- -->

-   Nach einiger Zeit erscheint dann im Modellfenster die
    dünne Punktwolke.

***(Bitte abwarten) ***

-   Gleichzeitig öffnet sich am **rechten Bildschirmrand** ein neues
    Übersichtfenster **(Layer-Anzeige)** was mittels **VII** an und
    abgeschaltet werden kann.

    -   In der Layer-Anzeige werden alle Gitter/Punkten etc. des
        Projektes angezeigt.

-   Da das gewünschte Gitter mittels der dichten Punktwolke zu erstellen
    ist, **benötigen Sie die dünne Punktwolke nicht**. Mittels
    **Rechtsklick auf „0 model“ und der Auswahl „delete current match“**
    können Layer gelöscht werden.

-   Als nächstes muss die von CVMS erstellte **dichte Punktwolke
    geladen werden.** Über Schaltfläche **III** oder **„File Import
    mesh“** bzw. **\[Strg\] + \[I\]** können Sie diesen
    Schritt durchführen. Die Datei befindet sich dort, wo sie in
    **Kapitel 1.5. abgespeichert wurde**, meistens daher im s**elben
    Verzeichnis wie die Dünne Punkte**.

-   Im **Unterordner 00** gibt es einen weiteren **Unterordner
    „models“**. Dort befindet sich die dichte Punktewolke (z.B.
    option-0000).

2.4. Bereinigung der dichten Punktwolke
---------------------------------------

-   **Da bei SFM immer wieder ungewünschte „Punktwolken-Artefakte“
    auftreten können, muss die dichte Punktwolke bereinigt, bzw. Punkte
    gelöscht werden.**

-   Das Modell bzw. die Punktwolke kann:

    -   mittels gedrückter linken Maustaste **gedreht** werden

    -   mittels Mausrad **heran- und herausausgezoomt** werden

    -   mittels drücken des Mausrads kann die Ansicht auf **das Modell
        verschoben** werden.

-   ![](media/image14.png){width="0.4166666666666667in"
    height="0.4166666666666667in"}Zunächst müssen Sie die **zu löschende
    Punkte** mittels der Maus auswählen.

    -   ![](media/image9.png){width="0.23333333333333334in"
        height="0.24166666666666667in"}Hierzu muss die Schaltfläche
        **„select vertexes“** betätigt werden.

    -   Durch gedrückt halten der linken Maustaste ist es dann möglich
        ein **Markierungsrahmen aufzuziehen.**

    -   Das Drücken der **\[Strg\]-Taste** ermöglicht es, **weitere
        Punkte** immer wieder mittels **weiterem Rahmen hinzuzufügen.**

    -   Durch Gedrückt halten der **\[Shift\]-Taste** können Punkte im
        selben Prinzip auch **wieder abgewählt werden.**

    -   Um die richtigen Punkte markieren zu können, muss die Punktwolke
        **stetig gedreht und verschoben werden**. Dies erfordert *ein
        wenig Übung.*

<!-- -->

-   ![](media/image15.png){width="0.375in"
    height="0.3541666666666667in"}Sind nur die gewünschten Punkte
    markiert, können Sie diese löschen.

    -   ![](media/image9.png){width="0.23333333333333334in"
        height="0.24166666666666667in"}Hierzu bedienen Sie sich der
        Schaltfläche **„delete current set of vertices“**.

-   Sobald alle Punkte gelöscht wurden, kann die bereinigte Punktwolke
    als neue Datei abgespeichert werden. Hierzu wählen Sie in der
    Tab-Leiste „File Export Mesh as“. Die **neue Punktwolke sollte einen
    Hinweis enthalten,** dass es sich um die bereinigte Version
    handelt z.B. Modell\_clean.ply.

2.5. Konvertierung der dichten Punktwolke in ein Gitter
-------------------------------------------------------

-   Nun muss zwischen den Punkten der dichten Punktwolke **ein Gitter
    generiert** werden. Hierzu wird die Funktion **„Surface
    Reconstruction Poisson“** verwendet.

-   Über **„Filters Point Set Surface Reconstruction Poisson“** wird der
    Prozess gestartet.

-   Im neu erschienen Einstellungsfenster für „Surface Reconstruction
    Poisson“ können Sie **unterschiedliche Werte für die
    Gittererzeugung** wählen.

-   ***TArchIT empfiehlt hier: Octree depth: 12; Solver Divide: 10,
    Samples per node: 1; surface offsetting: 1.***

-   Sobald die Werte eingetragen wurden, wird **der Prozess über
    „apply“** gestartet.

    -   ***Dieser Prozess benötigt Rechenzeit!***

<!-- -->

-   Sobald der Prozess vollendet wurde**, erscheint das neue Gitter im
    Modellfenster** und in der **Layer-Anzeige.**

-   ![](media/image16.png){width="0.3854166666666667in"
    height="0.741185476815398in"}Nun können Sie entweder die dichten
    Punkte löschen oder ausblenden.

    -   Über **das Augensymbol** (links neben dem Layernamen) in der
        Layer-Anzeige kann ein **Layer an- und ausgeschalten werden**.

    -   **Rechts neben dem Layernamen** können **verschiedene
        Ansichten** ausgewählt werden (z.B. Gitter, Gitter mit
        Füllung etc.).

    -   *Der zu bearbeitende Layer muss stets in der Layer-Anzeige
        ausgewählt sein.*

<!-- -->

-   Ähnlich wie die **neue Punktwolke**, **speichern** Sie auch das neue
    Gitter über **„File Export Mesh as“** als neuer Zwischenschritt.

-   Auch das MeshLab-Projekt sollte spätestens jetzt gespeichert werden:
    **„File Project“.**

-   Genau wie in Kapitel 2.4. können Sie **das Gitter erneut
    bereinigen**. Es ist wichtig, die **Punktwolkenansicht des Gitters
    zu wählen**, da sonst **keine Punkte zur Bearbeitung bzw. zum
    Löschen ausgewählt werden können**.

2.6. Bereinigung des Gitter (Non-Manifold Edges)
------------------------------------------------

-   ![](media/image17.png){width="2.9194444444444443in"
    height="2.7909722222222224in"}Das Gitter muss **noch „gesäubert“**
    werden, bevor Sie **die Textur auflegen können.**

-   Hierzu muss das Gitter, ein **Manifold-Mesh** werden. *Ein
    Non-Manifold Mesh ist ein Mesh, bei dem eine oder mehrere Kanten zu
    mehr als zwei Flächen gehören*. ???? non oder nicht non?

-   Deshalb wählen Sie über **„Filters Selection select non-manifold
    edges“** und bestätigen dies im neuen Fenster über **„apply“**.
    *Sobald der Prozess abgeschlossen ist, können Sie das Fenster über
    „close“ schließen.*

-   ![](media/image9.png){width="0.23333333333333334in"
    height="0.24166666666666667in"}![](media/image15.png){width="0.375in"
    height="0.3541666666666667in"}Nun müssen die **gewählten,
    gefilterten Kanten gelöscht** werden. Hierfür wird die Schaltfläche
    **„delete current set of vertices“** betätigt.

-   Nun sollten Sie das Gitter erneut zwischenspeichern.

2.7. Parametrisierung der Textur / Export
-----------------------------------------

-   ![](media/image18.png){width="2.1898261154855643in"
    height="3.3124092300962378in"}Nun werden **die Bildinformationen der
    Fotos** an das Gitter **angepasst**, um später im **Blender die
    Textur auf das Modell auflegen zu können**.

-   Hierzu ist das Werkzeug **„Filters texture parameterization +
    texturing from registered rasters“** zu wählen. Die Einstellung
    sollten so angepasst werden, dass sie mit den Werten der Abbildung
    übereinstimmen

-   Dann mit **„apply“** bestätigen.

-   *Nun sind alle Vorbereitungen für die Weiterverarbeitung mit
    Blender abgeschlossen.*

-   Das fertige Gitter sollte jetzt über **„File Export Mesh
    as“ (z.B.)** als **\*.obj-Datei** exportiert werden.

2.8. Zusammenfassung Workflow MeshLab
-------------------------------------

(1) MeshLab starten.

(2) VisualSFM-Projektdaten laden (Schaltfläche **II** oder über „File
    Open project“).

    -   zunächst die Datei: **„bundle.rd.out“ auswählen.**

    -   dann die Datei **„list“ auswählen.**

    -   *Warten bis die Punktwolke geladen ist.*

(3) Dünne Punkte in der Layer-Anzeige **markieren und löschen.**

(4) Dichte Punktwolke einladen (Über Schaltfläche III oder File
    Import mesh).

    -   Warten bis die Punktwolke geladen ist.

(5) ![](media/image14.png){width="0.4166666666666667in"
    height="0.4166666666666667in"}![](media/image15.png){width="0.375in"
    height="0.3541666666666667in"}Punktwolke bereinigen.

> Punkte markieren Punkte löschen

-   Speichern

(1) „Surface Reconstruction Poisson“ durchführen.

    -   Filters Point Set Surface Reconstruction Poisson (12/10/1/1)

    -   Speichern

(2) Bereinigung des neuen Gitters (siehe Punkt 5).

(3) Bereinigung des Gitter (Non-Manifold Edges).

    -   „Filters Selection select non-manifold edges“.

(4) Textur berechnen.

    -   „Filters texture parameterization + texturing from
        registered rasters“.

(5) Das fertige Gitter über „File Export Mesh as“ als
    **\*.obj-Datei** exportieren.

![](media/image19.png){width="1.006674321959755in" height="0.8229166666666666in"}Kapitel 3: Erste Schritte in Blender
=====================================================================================================================

3.1. Installation und Allgemeines
---------------------------------

-   Blender können Sie über **https://www.blender.org/beziehen**.

-   Nach der Installation kann **Blender gestartet werden**. Ein
    Verknüpfungssymbol sollte bereits automatisch auf den Desktop
    angelegt worden sein.

-   Die Aufgabe von Blender ist es, das Gitter aus MeshLab mit Textur zu
    versehen und aus dem 3D-Modell ein anschauliches Video
    zu generieren.

*Blender ist ein sehr komplexes Programm und bietet erstaunlich viele
Anwendungsmöglichkeiten und Funktionen.*

![](media/image20.png){width="6.692909011373579in" height="3.537399387576553in"}3.2. Überblick Programmoberfläche Blender
-------------------------------------------------------------------------------------------------------------------------

1)  Tool-Shelf: Werkzeuge.

2)  Properties-Shelf: Eigenschaften von Objekten ändern (Position,
    Größe, Rotation u.v.m.).

3)  Outliner: Alle Elemente im Projekt, "Inhaltsverzeichnis".

4)  Properties-Fenster: Zugriff auf Einstellungen für Beleuchtung,
    Kamera, Oberflächenbeschaffenheit und anderen Detaileigenschaften.

5)  Zeitleiste: Ablauf der Animation.

6)  3D-Fenster: Arbeitsbereich.

3.3. Grundlegendes
------------------

-   ***Navigation***

    -   *Zoom: Mausrad*

    -   *Links/Rechts: \[STRG\]+Mausrad*

    -   *Hoch/Runter: \[STRG\]+Mausrad*

    -   *frei bewegen: Mausrad drücken und Maus bewegen*

-   ***Ansichten***

    -   *4-Fenster-Ansicht öffnen/schließen: \[STRG\]+\[ALT\]+\[Q\]*

    -   *Definierte Ansichten, Vorne/Rechts/Oben/Unten: \[Num 1/3/7/9\]*

    -   *Gesamte Szene anzeigen: \[Pos 1\]*

-   ***Auswählen***

    -   *Objekte auswählen: rechte Maustaste, mit \[Shift\] mehre
        Auswählen oder einzelne abwählen*

-   ***Kamera***

    -   *\[Strg\]+\[Alt\] + \[0\] setzt die Kamera auf die aktuelle
        Blickposition*

    -   *\[Num 0\] Kamerasicht ein / aus*

<!-- -->

-   ***Modellberechnung***

<!-- -->

-   *\[F12\] Render-Vorschau/Modus*

3.4. Textur auflegen
--------------------

-   Blender starten.

-   **\[Entf\] + \[Enter\]: entfernt den Standardwürfel.**

<!-- -->

-   *Import der SFM-Datei:.*

    -   Unter **„File Import“**: **Dateiformat \*.obj wählen** und dann
        den Speicherort des aus **MeshLab exportieren Gitters auf der
        Festplatte** auswählen.

    -   *Warten bis das Gitter geladen ist.*

<!-- -->

-   ***Modell/Gitter mit der rechten Maustaste auswählen.***

![](media/image21.png){width="0.38333333333333336in"
height="0.38960958005249346in"}*Fotos als Oberflächenmaterial*

-   Im Properties-Fenster **(4)** auf die ***Textur-Schaltfläche***
    klicken **(Schachbrett)**

![](media/image9.png){width="0.23333333333333334in"
height="0.24166666666666667in"} und im Menübereich darunter das
**Runde-Schachbrettsymbol** auswählen.

> ![](media/image22.png){width="1.1966108923884515in"
> height="0.45326115485564306in"}
>
> ![](media/image9.png){width="0.23333333333333334in"
> height="0.24166666666666667in"}

-   Im **Image-Tab-Bereich** (*NICHT SOURCE*) auf **„Open
    (Ordner-Symbol)“** klicken.

> ![](media/image23.png){width="2.321527777777778in"
> height="0.21736111111111112in"}
>
> ![](media/image9.png){width="0.23333333333333334in"
> height="0.24166666666666667in"}

-   Jetzt laden Sie die zu dem Gitter **dazugehörige PNG-Datei**, die
    MeshLab in Punkt 2.7 erstellt hat.

-   Diese Datei heißt **„texture.png“** und befindet sich in
    *Beispiel*.nvm.cmvs\\ 00\\models\\.

-   ![](media/image22.png){width="0.4in"
    height="0.45245297462817147in"}Diese Datei muss ausgewählt werden.

<!-- -->

-   In der Haupt-Tab-Leiste **(4)** gehen Sie nun auf Material
    **(Schachbrett).**

-   ![](media/image9.png){width="0.23333333333333334in"
    height="0.24166666666666667in"}Im Material-Bereich **unter Shading
    den Haken bei shadeless setzen.**

![](media/image24.png){width="2.253416447944007in"
height="1.0520833333333333in"}

-   \[F12\] öffnet **den „Render-Modus“** und zeigt das Ergebnis,
    **\[ESC\] schließt ihn wieder.**

3.5. Animation „Rundflug“
-------------------------

-   Objekt platzieren:

    -   **4-er-Fenster** aktivieren: \[STRG\]+\[ALT\]+\[Q\].

    -   **Objekt markieren** (rechte Maustaste).

    -   Oberhalb der Zeitleiste **(5)**, links der Schaltfläche
        **„Global“** den **blauen Bogen anwählen** und im **3D-Fenster
        durch klicken** mit der linken Maustaste auf die **Achsen des
        Drehkreuzes das Objekt rotieren.**

> ![](media/image25.png){width="1.6in" height="0.21736111111111112in"}

-   Dann wieder oberhalb der Zeitleiste **(5)** auf den Pfeil klicken
    und das Objekt **in den Raumesrichtungen verschieben.**

> ![](media/image26.png){width="1.6in" height="0.2263888888888889in"}

-   Pfad hinzufügen:

    -   Oberhalb der Zeitleiste **(5)**: „Add &gt; Curve &gt; Circle“.

    -   **Am blauen Pfeil mit linker Maustaste** nach oben auf **die
        Höhe**, auf der später die Kamera kreisen soll, ziehen.

    -   Mit dem Cursor in die Mitte des Kreises zielen **und \[S\]
        drücken**, dann Maus bewegen, bis **der Kreis etwas größer als
        die gesamte Szene ist**. Mit **linker Maustaste abschließen.**

-   *Kamera einstellen*

    -   **Kamera markieren.**

    -   mit den oben beschrieben Methoden in die Nähe des Kreises
        schieben **(linke Maustaste auf die Koordinatenachsen).**

    -   Dann **\[Shift\]+ rechte Maustaste auf den Kreis.**

    -   **\[STRG\]+\[P\] „Follow path“** auswählen → ***Kamera folgt
        dem Kreispfad.***

    -   **Kamera auswählen und mit \[Shift\]** **zusätzlich das
        Objekt markieren.**

    -   **\[Shift\]+\[T\] &gt;“Track to Constraint“ auswählen** → Kamera
        **fokussiert immer automatisch Zielobjekt.**

    -   **\[ALT\]+\[A\] startet die Kamerafahrt** (die „Animation“),
        stoppen mit \[ESC\].

    -   **\[Num 0\] schaltet die Kamerasicht ein/aus**. Jetzt nochmal
        die Animation starten.

    -   Ggf. muss der Fokuspunkt der Kamera geändert werden.

        -   Dazu das **3D-Objekt markieren.**

        -   mit **\[N\] das Properties-Shelf öffnen.**

        -   unter **3D-Cursor den 3D-Cursor auf die Stelle setzten, auf
            die die Kamera fokussieren soll.**

        -   Dann im Tool-Shelf unter **„Tools“ auf „Set-Origin“ klicken
            und „Origin to 3D-Cursor“ wählen.**

        -   Der **Kamerafokus sollte sich jetzt geändert haben.**

    -   Kamera nun so positionieren, **dass das gesamte Objekt
        sichtbar ist.**

-   *Geschwindigkeit der Kamera regulieren*

    -   **Kreis markieren.**

    -   im **Properties-Fenster das Kurven-Symbol** markieren.

    -   **unter „Path Animation“ die Frame-Anzahl erhöhen**, um die
        Geschwindigkeit zu verringern und umgekehrt.

3.6. Animation: Beleuchtung
---------------------------

-   **Lampe markieren und im Properties-Fenster auf das
    Lampensymbol klicken.**

    -   Hier können verschiedene **Lampenarten gewählt** werden. **Hemi
        leuchtet** dabei die komplette Szene **ohne Schatten aus**.

    -   Um den Effekt zu sehen, sollte man oberhalb der Zeitleiste,
        rechts der Schaltfläche „Object Mode“ auf das Kreissymbol
        klicken und „Texture“ wählen.

    -   Die Lampe kann anschließend wie die anderen Objekte
        transformiert werden (**verschieben, Rotieren, skalieren**), um
        den **Schattenwurf zu kontrollieren.**

    -   **mit \[LEERTASTE\] und dem Befehl „Add Lamp“ können weiter
        Lampen hinzugefügt werden.**

3.7. Animation: Videoexport
---------------------------

-   *Video exportieren*

    -   Im Properties-Fenster **auf die Kamera klicken**

    -   Unter „**Output“ ein Verzeichnis** und einen Namen wählen und
        als Dateiformat ein Videoformat wählen**, z. B. AVI JPEG**

    -   Dann im oberen Bereich auf **„Animation“ klicken** und **warten
        bis der Prozess durchgelaufen ist** (Je nach Modell, Länge der
        Animation, Auflösung, der Hardware etc. kann *dieser Prozess
        einige Zeit benötigen*)

    -   Unter dem oben angegebenem Pfad sollte nun **eine Videodatei zu
        finden** sein, die z. B. **in Präsentation eingebunden**
        werden kann.

    -   *Alternativ kann auch ein Bild einer bestimmten Kameraposition
        exportiert werden. Dazu beim Dateityp ein Bildformat wählen und
        auf Animation klicken. Dann werden alle Frames als
        Bild gespeichert.*

4. Notizen
==========

*\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
*
