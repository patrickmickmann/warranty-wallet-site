# Warranty Wallet Website

Eigenständige statische Website. Kein Build-Schritt, kein JavaScript, keine Frameworks, keine Analytics, keine Cookies durch den Website-Code und keine externen Fonts oder Ressourcen. Dark Mode folgt der Systemeinstellung. GitHub verarbeitet beim Hosting technische Verbindungsdaten; die Privacy-Seite erläutert diese Abgrenzung.

## Repository-Struktur

```text
warranty-wallet-site/
├── .nojekyll
├── index.html
├── styles.css
├── privacy/
│   └── index.html
├── support/
│   └── index.html
└── README.md
```

Nur diese sechs Dateien gehören in das öffentliche Repository. Keine App-Dateien, App-Git-Historie oder internen Dokumente hinzufügen. Das private App-Repository bleibt separat und privat. Dieses Website-Projekt hat eine eigene Git-Historie, unabhängig vom privaten App-Repository.

## Vor Veröffentlichung

- Support-Kontakt: [warrantywallet.support@protonmail.com](mailto:warrantywallet.support@protonmail.com), auf der Privacy- und Support-Seite verlinkt.
- Anbietername „Patrick Mickmann“ in Privacy und Footer mit dem tatsächlichen App-Store-Anbieter abgleichen.
- Sobald vorhanden, den Absatz „App-Store-Link folgt“ und dessen Hinweis in `index.html` durch einen Link zur tatsächlichen App-Store-Produktseite ersetzen. Keine erfundene App-ID verwenden. Für die Veröffentlichung der Support-/Privacy-URLs darf der angekündigte App-Store-Link zunächst stehen bleiben.
- Die Datenschutzerklärung entspricht der App-Policy Version 1.0 vom 8. September 2026, in Deutsch und Englisch. Interne Veröffentlichungshinweise wurden entfernt; Support-/Privacy-URL-Platzhalter sind relative Links auf diese Website. Bei Änderungen der App-Datenflüsse die öffentliche Policy erneut abgleichen.
- Die Website ersetzt nicht die Release-Freigabe der iOS-App. Finale Kontaktadresse und beide URLs anschließend auch in den Release-Metadaten des privaten App-Projekts eintragen.

## GitHub Pages einrichten

1. Bei GitHub ein **neues öffentliches Repository** namens `warranty-wallet-site` erstellen. Nicht das App-Repository importieren, forken oder dessen Sichtbarkeit ändern. Du kannst das neue Repository mit einer README initialisieren; der Standardbranch soll `main` heißen.
2. Im neuen Repository **Add file → Upload files** öffnen. Ausschließlich die oben aufgeführten Website-Dateien und die Ordner `privacy` und `support` hochladen. `index.html` muss direkt im Repository-Root liegen, nicht in einem weiteren Ordner `warranty-wallet-site`. Die initialisierte README durch diese README ersetzen. Auch die versteckte leere Datei `.nojekyll` hochladen oder mit **Add file → Create new file** anlegen. Änderungen auf `main` committen.
3. Im neuen Website-Repository **Settings → Pages** öffnen.
4. Unter **Build and deployment → Source** die Option **Deploy from a branch** wählen. Branch **main**, Ordner **/(root)** auswählen und **Save** klicken.
5. Auf den erfolgreichen Pages-Deploy warten. Die endgültige URL steht unter **Settings → Pages → Visit site**. Für diesen Repository-Namen lautet das Muster `https://patrickmickmann.github.io/warranty-wallet-site/`. Der GitHub-Benutzername dieses Projekts ist `patrickmickmann`.
6. Alle drei Seiten über die veröffentlichte URL öffnen, Links und Kontaktadresse prüfen und anschließend die beiden folgenden URLs in App Store Connect eintragen.

Offizielle Anleitung: [GitHub – Publishing source konfigurieren](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## URLs für App Store Connect

| Zweck | URL-Muster |
| --- | --- |
| Website / optional Marketing URL | `https://patrickmickmann.github.io/warranty-wallet-site/` |
| Privacy Policy URL | `https://patrickmickmann.github.io/warranty-wallet-site/privacy/` |
| Support URL | `https://patrickmickmann.github.io/warranty-wallet-site/support/` |

Diese URLs gehören zur GitHub-Pages-Veröffentlichung dieses Repositorys. Ein anderer Repository-Name ändert den jeweiligen Pfad. Relative Navigation und CSS funktionieren auch unter einem GitHub-Pages-Projektpfad.

## Lokal ansehen

Im Website-Ordner ausführen:

```sh
python3 -m http.server 8080 --bind 127.0.0.1
```

Dann `http://127.0.0.1:8080/` öffnen. Mit `Ctrl+C` beenden. Kein Installations- oder Build-Schritt erforderlich.
