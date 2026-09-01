# Architekture

Das Testprodukt besteht aus drei Schichten:

- **Client** — rendert die Dokumentationsseiten.
- **Server** — durchsucht GitHub nach `mkdocs.yml`-Dateien und liefert den geparsten Inhalt.
- **GitHub-Repository** — speichert die `mkdocs.yml` und die Markdown-Quelldateien.
