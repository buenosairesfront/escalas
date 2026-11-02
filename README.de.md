[English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · **Deutsch** · [日本語](README.ja.md) · [中文](README.zh.md) · [हिन्दी](README.hi.md)

# U-MA Escalas

Ein Tonleiter-Labor fürs Klavier: Wähle einen Grundton und eine von **61 Tonleitern**, und die App zeigt dir Töne und Intervalle, den Fingersatz für beide Hände, die Arpeggien, die Akkorde darin – und du kannst diese Akkorde zu einer Progression mit sauberer Stimmführung verketten.

**▶ App öffnen:** https://buenosairesfront.github.io/escalas/

Nichts zu installieren. Die Oberfläche ist auf Spanisch.

## So funktioniert's

Die Seite ist ein technisches Datenblatt in fünf nummerierten Abschnitten, mit einem **Monitor** oben (eine Tastatur, die aufleuchtet, was klingt, plus Anzeigen für Tonleiter, Ton, Stufe und Akkord) und einer festen **Transportleiste** unten.

### 01 · Tonleiter
- **Grundton:** die 12 Töne (schwarze Tasten zeigen beide Schreibweisen, z. B. Cis / Des).
- **Familie:** Dur und seine Modi, melodisch Moll, harmonisch Moll, harmonisch Dur, Pentatonik & Blues, symmetrische, Bebop und Skalen aus aller Welt. Oder im Feld **Tonleiter suchen** tippen. Jede Karte zeigt die Form der Tonleiter als 12 Punkte.
- **Übersicht:** der große Name, jeder Ton korrekt geschrieben mit seiner Stufe (1, ♭3, ♯4…), ein farbiger Balken der Schritte (S Halbton, T Ganzton, 1½ anderthalb Töne, 2T zwei Ganztöne), **die Tonleiter in Noten** und eine **Uhr** mit ihrer Form im Kreis der 12 Töne.

### 02 · Tastatur und Fingersatz
Die Tonleiter auf einer großen Tastatur, mit Farbkreis und Fingernummer auf jeder Taste (Daumen, Zeige-, Mittel-, Ring-, kleiner Finger), für rechts, links oder beide Hände. Ansicht **Tastatur** oder **Notensystem**. Darunter eine Tabelle mit jedem Ton und seinem Finger. Dur- und Molltonleitern nutzen den **traditionellen** Fingersatz; für alle anderen **berechnet** die App einen (den mit den wenigsten unbequemen Spreizungen und Daumen auf schwarzen Tasten) und kennzeichnet ihn so.

### 03 · Arpeggien
**Stufe**, **Typ** (Dreiklang, mit Septime oder Quartenakkord) und **Umkehrung** wählen. Das Arpeggio erscheint über zwei Oktaven mit Fingersatz, traditionell oder berechnet.

### 04 · Harmonisierung
Die Tonleiter **geschichtet** in Drei- oder Vierklängen: eine Karte pro Stufe mit römischer Ziffer, Name, Qualität (Dur, Moll, vermindert, übermäßig…), Intervallkette, Mini-Tastatur und Funktion (T Tonika, SD Subdominante, D Dominante), wenn die Tonleiter Dur oder Moll ist. Jede Karte hat **▶** zum Anhören und **+ PROG**, um sie der Progression hinzuzufügen.

### 05 · Progression
Bis zu 16 Akkorde, je ein 4/4-Takt. Lade eine Vorlage (I–IV–V–I, ii–V–I, I–vi–IV–V, I–V–vi–IV, vi–IV–I–V, I–vi–ii–V, andalusische Kadenz, Quintenzirkel, alle Stufen) oder bau deine eigene. Die Stimmen **gehen zur nächstgelegenen Umkehrung**, wie ein Pianist es tun würde, und während des Spielens zeigt eine große Anzeige den aktuellen Akkord und Takt.

### Transport (untere Leiste)
- **Was klingt:** Tonleiter, Arpeggio, harmonisiert (die Akkorde der Tonleiter) oder Progression.
- **▶ / ■** und **loop**, Tempo und Metronom mit Schlaglichtern.
- **Hände:** beide, rechts (MD) oder links (MI). **Richtung:** ↑ oder ↑↓. **Oktaven:** 1 oder 2.
- **Klang:** Piano, EP (E-Piano) oder Pad.

Im Kopfbereich lassen sich die Notennamen (**Do Re Mi** oder **C D E**) und das helle / dunkle Design umschalten. Alle Einstellungen bleiben im Browser gespeichert.

## Unter der Haube

Eine einzige `index.html` ohne Abhängigkeiten. Jede Tonleiter ist als Stufenformel notiert (`1 2 ♭3 4 5 6 ♭7`), daher bekommt jeder Ton für den gewählten Grundton den richtigen Buchstaben; Akkordnamen und römische Ziffern werden aus den tatsächlichen Intervallen abgeleitet. Berechnete Fingersätze stammen aus einer Suche mit dynamischer Programmierung über die fünf Finger jeder Hand. Gezeichnet wird mit `<canvas>` und SVG; die drei Klänge werden live mit Web Audio synthetisiert (keine Samples).

## Lokal starten

`index.html` herunterladen und öffnen oder den Ordner ausliefern:

```
python3 -m http.server 8000
```

<!-- u-ma:more -->
**Mehr von U-MA:** alle Instrumente und Werkzeuge an einem Ort → [U-MA-Übersicht](https://github.com/buenosairesfront/U-ma/blob/main/README.de.md)
<!-- /u-ma:more -->

## Credits

Traditionelle Fingersätze für Tonleitern und Arpeggien, wie sie in Klavierschulen gelehrt werden. App von U-MA サウンド · [Buenos Aires Front](https://www.instagram.com/buenos.aires.front/).
