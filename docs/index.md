# Vision

Ein Javascript-XML-Editor, welcher die Schemasprachen XSD und Schematron browserseitig unterstützt. Der XML-Inhalt wird in echtzeit gegen das Schema überprüft und im Fehlerfall an der entsprechenden Stelle angezeigt. Das Einfügen von neuen Elementen soll entsprechend dem Schema vorgeschlagen werden. 

# Anforderungen an Umsetzung

1. Ist rein in Javascript implementiert (ohne Server calls)
2. Verwendet ausschliesslich freie Software-Bibliotheken. 
3. Die Lösung wird mit Typescript entwickelt
4. Die Lösung wird als Vue.js-Komponente entwickelt
5. Es kann ein XSD- als auch ein Schematron-Schema verwendet werden.
6. Der Editor-Inhalt wird in echtzeit gegen das Schema geprüft
7. Im Schema-Fehler-Fall wird an der verursachten Position der Fehler angezeigt.
8. Neue Elemente werden gemäss XSD-Definition vorgeschlagen
9. XML-Elemente können für die Editor-Ansicht als HTML/CSS beschrieben werden (Template Block pro XML-Element)
10. Tastenbefehle können für Element- oder Attribut-Auswahl definiert werden.
11. HTML/CSS Templates können als Themes gewechselt werden

# Vorgeschlagene Technologie

## Applikation

- [Vue.js](https://vuejs.org/)

## XML/Schema

- [node-schematron](https://www.npmjs.com/package/node-schematron) JS Lib für Schema-Validierung
- [xsd2sch](https://github.com/Schematron/schematron/tree/master/trunk/xsd2sch) XSD zu Schematron XSL-Konvertierung. Für ein einheitliches Validations-Handling in Javascript
- [schxslt](https://github.com/schxslt/schxslt/releases) XSLT für Schematron Transformationen
