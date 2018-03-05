# apache2_vagrant
Vorbereitung
----------
Damit unser Service laufen kann muss folgendes gemacht werden:
1.Unter devops/vagrant mit mkdir das Verzeichniss "apache" erstellen.
2. In das Verzeichniss wechseln mit cd apache
3. vagrant init -m -f ausführen, damit das Vagrant file generiert wird.
Die Vorbereitung ist somit zu Ende
Config
=============
Damit die config ins Vagrantfile eingefügt werden kann muss:
1. Das neu generiete File mit "nano VAGRANTFILE" geöffnet werden
2. Den Inhalt aus VAGRANTFILE (im github) einfügen
3. Nano Editor mit ctrl + x dann y und dann enter schliessen.
Die config wurde von uns erstellt.
Installation
==============
Damit unsere configuration aus dem VAGRANTFILE installiert wird, muss folgendes gemacht werden:
1. In das Verzeichniss /devops/vagrant/apache wechseln
2. mit "vagrant up" die installation starten
