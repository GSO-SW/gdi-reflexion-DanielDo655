[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/OwH8KTXH)
# GDI+
Eine Sammlung von Tipps und Tricks zum Thema Grafikprogrammierung mit GDI+.

## Klassen / Ereignisse
### Timer
Ein Timer führt in regelmäßigen Abständen ein `Tick`-Event aus. Der [`System.Windows.Forms`.`Timer`](https://learn.microsoft.com/de-de/dotnet/api/system.windows.forms.timer?view=windowsdesktop-8.0&viewFallbackFrom=net-6.0) kann über die Toolbox auf die GUI gezogen werden. 

Anschließend können wir 
- die Zeit zwischen jedem `Tick`-Event einstellen (`+ Interval { get; set; }: int`) und
- den Timer starten (`+ Start():void`) oder
- stoppen (`+ Stop():void`) oder
- den Zustand abfragen. (`+ Enabled{ get; set; }: bool`) (Standard ist ausgeschaltet: `enabled = false`)



## Tipps und Tricks
Ergänzen Sie hier die notwendigen Code-Ausschnitte, um zu zeigen, wie man es macht. 
- Sie können [CodeBlöcke mit Syntax-Highlighting](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks#syntax-highlighting) einsetzen
- Wird es zu unübersichtlich? Sie können auch Unterordner mit Beispiel-Code anlegen und auf die entsprechenden Dateien verlinken. [Inspiration](https://github.com/gsoTH/flaskShowcase/tree/master/datenbanken).
- Die folgende Liste kann gerne ergänzt werden :)

### sounds bei click 
bei sounds on click wird noch ein sound beim keydown event abgespielt 
 private SoundPlayer soundPlayer = new SoundPlayer("move_sound.wav");
dort wird der sound der in der debug datei gespeichert ist als ein sounplayer gespeichert 
das wird dann beim get key down event eingefügt und sieht dann so aus 
 if (e.KeyCode == Keys.Up)
 {
     spieler.Y = spieler.Y - hoeheJeBereich;
     soundPlayer.Play();
 }
 dort wird bei jedem click der soundplayer abgespielt 
  

### Objekte mit Tasten steuern
    ein get key down event führt bei einem klick auf der tastatur ein even aus wo das objekt sich in eine richtung der x oder y achse bewegt 
	 if (e.KeyCode == Keys.Up) der keycode sit das event was ausgeführt wird aber nur wenn der hoch button auf der tastatur gedrückt wird 
 {
     spieler.Y = spieler.Y - hoeheJeBereich;
 }
 
### Verhindern, dass ein Spieler aus dem Bild läuft
dabei habe ich nur eine begrenzung gestzt das wenn er zu weit leuft das er dann nicht wieter geht und an seiner 	
bei links war es deutlich komplezierter da musste ihc es schaffen das wenn er 
da muss man mit clientsize.With arbeiten und den Spiler auf seine vorherige position mit spiler.y zurück setzten 

### Ihr schönstes Ergebnis

bilder mit bitmap für gegner eingefügt 
mit bitmap kann man ein bild laden das man auch in die debug gespeichert wird 
ich habe dabei es so gemacht das jeder zweite gegner das bild hat für eine art von variation 
das habe ich mit einer verzweigung gemacht um sie bei jedem zweiten tick einen dose anzuzeigen 
 e.Graphics.DrawImage(Image, aktuellesHindernis.X, aktuellesHindernis.Y, aktuellesHindernis.Width, aktuellesHindernis.Height); }
 draw image ahbe ich genutz damit da bild eingesetzt wird ich habe das bild dann einfach in das rectangle gepeichert 




