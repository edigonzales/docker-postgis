# Docker Image sogis/postgis:16-3.4-bookworm

Dieses Image wurde im Rahmen des Auftrags https://sogis.openproject.com/work_packages/2465/activity erstellt.
Ziel war, ein Image für Processing-DBs zu erstellen, das GEOS 3.11 enthält.

Gegen Ende der Arbeiten sind wir zum Schluss gekommen, dass künftig die Processing-DB möglicherweise schon auch ein Alpine-Image sein dürfte und also dieses Image hier nicht zwingend notwendig wäre.
Denn mit Alpine wäre es wohl einfacher, die gewünschten GEOS-Versionen etc. zu erhalten, weil es in der Regel aktuellere Softwareversionen enthält.
Und unterdessen ist das Alpine-Image vermutlich ebenfalls in OpenShift lauffähig, weil es nun wie das Debian-Image die Möglichkeit bietet, unter einem beliebigen User zu laufen.
Wichtig ist hierfür wahrscheinlich auch bei diesem Image, die Umgebungsvariable `PGDATA` auf einen noch nicht existierenden Unterordner des Default-Pfades zu setzen:
https://github.com/docker-library/docs/blob/master/postgres/README.md#pgdata
