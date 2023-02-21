Erste Kopfzeile | Zweite Kopfzeile
--- | ---
Inhaltszelle | Inhaltszelle
Inhaltszelle | Inhaltszelle

Erste Kopfzeile | Zweite Kopfzeile
--- | ---
Inhaltszelle | Inhaltszelle
Inhaltszelle | Inhaltszelle

![ciudadela](https://vignette.wikia.nocookie.net/masseffect/images/d/d7/MassEffect2Citadel.jpg/revision/latest?cb=20100721191415)

Enlacesbündig | ausgerichtet zentriert | Rechtsbündig
:-- | :-: | --:
Espalda 3 ista | etwas wortreicher Texto | **$1600**
Espalda 2 ista | zentriert | $12
Zebrastreifen | sind ordentlich | ~~$1~~

Dillinger es un editor HTML5 Markdown habilitado para la nube, listo para dispositivos móviles, con almacenamiento fuera de línea y potenciado por AngularJS.

- Geben Sie enlaces etwas Markdown ein
- Siehe HTML derechos
- Magiem, l

# verdadero

- Importieren Sie eine HTML-Datei und beobachten Sie, wie sie auf magische Weise in Markdown konvertiert wird

Du kannst auch:

- Importación y reproducción Sie Dateien de GitHub, Dropbox, Google Drive y One Drive
- Ziehen Sie Markdown- y HTML-Dateien por arrastrar y soltar en Dillinger
- Exportieren Sie Dokumente como Markdown, HTML y PDF

Markdown ist eine leichtgewichtige Auszeichnungssprache, die auf den Formatierungskonventionen basiert, die Menschen normalerweise in E-Mails verwenden. Wie [John Gruber] auf der [Markdown-Site][df1] schreibt

> Das übergeordnete Designziel für die Formatierungssyntax von Markdown besteht darin, sie so lesbar wie möglich zu machen. Die Idee ist, dass ein Markdown-formatiertes Dokument so wie es ist, als reiner Text veröffentlicht werden kann, ohne dass es so aussieht, als wäre es mit Tags oder Formatierungsanweisungen markiert worden.

Dieser Text, den Sie hier sehen, ist *tatsächlich* in Markdown geschrieben! Um ein Gefühl für die Syntax von Markdown zu bekommen, geben Sie etwas Text in das linke Fenster ein und sehen Sie sich die Ergebnisse rechts an.

### FALSCH

Dillinger verwendet eine Reihe von Open-Source-Projekten, um ordnungsgemäß zu funktionieren:

- [AngularJS] - HTML verbessert para Web-Apps!
- [Ace Editor] - fantastischer webbasierter Texteditor
- [markdown-it] – Markdown-Parser richtig gemacht. Schnell und einfach zu verlängern.
- [Twitter Bootstrap]: gran plantilla de interfaz de usuario para aplicaciones web modernas
- [node.js] – E/S con eventos para el backend
- [Exprés] – schnelles node.js Netzwerk-App-Framework [@tjholowaychuk]
- [Gulp] – das Streaming-Build-System
- [Breakdance](https://breakdance.github.io/breakdance/) - HTML-zu-Markdown-Konverter
- [jQuery] - jaja

Und natürlich ist Dillinger selbst Open Source mit einem [öffentlichen Repository][eneldo] auf GitHub.

### Instalación

![Ilos](https://lh3.googleusercontent.com/proxy/DDV8a7sLIWurhJtW8Ego9bq-JlwpfFFoR0tkLJQKKYXEXoWHB6ZUP5jGKD2VcYt3z1QVsgcn6L3GoU1ns8m9fvi3U51GzddA70ZUMHgzHvjl4-i7YOJY9cShBPrfjUhMQhxaJ97WFBp612XmjMXVGypfGkiBarN4PWxhiHkiYYNW7HGbtTpOcyt9GQ4Q23C2noxLTWFXZMcQZhRpQA_qzu2n6_H6CPViBnhSHpEl4JZAPaGCSJqgZg)

Dillinger benötigt zur Ausführung [Node.js](https://nodejs.org/) v4+.

Installieren Sie die Abhängigkeiten und devDependencies y starten Sie den Server.

```sh
$ cd dillinger
$ npm install -d
$ node app
```

Für Produktionsumgebungen...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### Complementos

Dillinger wird derzeit um die folgenden Plugins erweitert. Anweisungen zur Verwendung in Ihrer eigenen Anwendung sind unten verlinkt.

Enchufar | Liesmich
--- | ---
buzón | [complementos/dropbox/README.md][PlDb]
GitHub | [complementos/github/README.md][PlGh]
Google Drive | [plugins/googledrive/README.md][PlGd]
Eine Fahrt | [complementos/onedrive/README.md][PlOd]
Mittel | [plugins/medium/README.md][PlMe]
Google analitico | [plugins/googleanalytics/README.md][PlGa]

### Entwicklung

Möchten Sie einen Beitrag leisten? Großartig!

Dillinger verwendet Gulp + Webpack für eine schnelle Entwicklung. Nehmen Sie eine Änderung in Ihrer Datei vor und sehen Sie sofort Ihre Aktualisierungen!

Öffnen Sie Ihr bevorzugtes Terminal und führen Sie diese Befehle aus.

Erste Registerkarte:

```sh
$ node app
```

Zweiter Reiterar:

```sh
$ gulp watch
```

(opcional) Dritos:

```sh
$ karma test
```

#### Gebäude für Quelle

Zur Produktionsfreigabe:

```sh
$ gulp build --prod
```

Generieren vorgefertigter ZIP-Archive für die Verteilung:

```sh
$ gulp build dist --prod
```

### Estibador

Dillinger lässt sich sehr einfach in einem Docker-Container installieren und bereitstellen.

Standardmäßig legt Docker Port 8080 offen, y ändern Sie muere también bei Bedarf in der Dockerfile. Wenn Sie fertig sind, verwenden Sie einfach das Dockerfile, um das Image zu erstellen.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version} .
```

Dadurch wird das Dillinger-Image erstellt und die erforderlichen Abhängigkeiten eingefügt. Stellen Sie sicher, dass `${package.json.version}` durch die aktuelle Version von Dillinger ersetzen.

Führen Sie anschließend das Docker-Image aus und ordnen Sie den Port dem gewünschten Port auf Ihrem Host zu. In diesem Beispiel ordnen wir einfach Port 8000 des Hosts dem Port 8080 des Docker zu (oder dem Port, der in der Docker-Datei verfügbar gemacht wurde):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Überprüfen Sie die Bereitstellung, indem Sie in Ihrem bevorzugten Browser zu Ihrer Serveradresse navigieren.

```sh
127.0.0.1:8000
```

#### Kubernetes + Nube de Google

Siehe [Kubernetes.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)

### Tods
