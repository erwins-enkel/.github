# .github

Organisationsweite Dateien für [@erwins-enkel](https://github.com/erwins-enkel).

| Pfad | Was darin steht |
| --- | --- |
| `profile/README.md` | Wird auf der Organisationsseite über dem Repositoryverzeichnis angezeigt. |
| `branding/` | Das Signet als Zeichendatei und als PNG in vier Größen. |

## Das Signet

Drei Einträge, je eine Endmarke (4 × 4) und ein Balken (16 / 10 / 14 × 4) auf den
Zeilen 6, 14 und 22 eines 32er-Rasters. Alle Kanten liegen auf geraden Einheiten —
so fällt bei 16 px jede Kante auf einen ganzen Pixel.

Quelle ist `design/marke/signet-flaeche.svg` im Repository `enkels-web`; dort steht
auch das Handbuch (`DESIGN.md`) mit Schutzraum, Mindestgröße und den Regeln, was mit
dem Zeichen nicht geschehen darf. `branding/logo.svg` ist eine Kopie davon, die PNGs
werden daraus erzeugt:

```sh
for s in 64 128 256 512; do
  rsvg-convert -w $s -h $s branding/logo.svg -o branding/logo-$s.png
done
```

Jede Größe ist ein ganzzahliges Vielfaches des Rasters (2 / 4 / 8 / 16 px je Einheit).
`branding/logo-512.png` ist zugleich die Datei für das Profilbild der Organisation —
das lässt sich nur von Hand hochladen, einen API-Endpunkt dafür gibt es nicht.
