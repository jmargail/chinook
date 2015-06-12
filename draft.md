## Chinook 2

Infos/Réflexions sur la mise en place de Chinook 2


### Outils / Méthodes
- GitHub. 
  - 1 compte "officiel" : chinook-geo / chinook-websig / chinook-platform
  	- plusieurs dépôts (ck-core, ck-viewer, ck-admin / ck-server, ck-...)
  	- des branchs par dev ou des dépôts par dev avec fork ?
  - Utiliser le dépôt, issues voir wiki
  - utiliser pour écrire un gide (penflip, gotbook, prose, readthedocs)
  
- Composer (gestion des install script PHP)
- Sencha CMD (gestion des app, conf, packages JS)

- Docker ? 


### Frameworks
Client:	
- Sencha Ext 6 GPL
- OpenLayers 3
- Proj4js
- turfjs (jsts)
- GuiBuilder
- CodeMirror ?
	
Serveur:
- Zend 2 / apigility
- PHPWord
- PHPExcel
- SQLParser
- CSSParser
- html2pdf
	

### Code
- commentaires anglais
- doc API (swagger pour PHP - API REST via apigility, JSDuck pour JS)
- multilangue (PHP retourne des codes erreur > traduction 'externe')

- tests unitaires ?


### Architecture
- notion de repository / héritage : no
- utilisation des dossiers / XML : no

- séparation plus forte :
	- client : module admin à part
    - plus de point d'entré unique. l'app, l'admin, les services ogc...
    - l'app se lance sur un html simple, tout est appel ajax / API rest après. mise en cache sur le localstorage.
- utilisation de plugins (comment unifier le JS et PHP)
- mise en place d'une Bdd (sqlite ou postgres)
- Utilisation de OWS Context - OWC dans sa forme JSON
- Notions :
	- contexts
    	- layers
        
> génère 1 mapfile par contexte. mapserver gère seul les flux OGC (WMS, WFS...)



### Les grandes lignes de la version 2
- Migration vers Github
- Full UTF8
- Version mobile avancée, responsive design
- Mode déconnecté
- Système de plugin plus performant
- Catalogue en ligne / synchro / diffusion …
- Catalogues en ligne de styles, pictos, cartes… (échanges / diffusion)
- Système de notification, cache
- Privilégier l’affichage type vecteur (WebGL)
- Utilisation des Websocket / cache SQLite / LocalStorage…
- Système gestion des droits (json + js via xtype + ID)
- Admin avec générateur d’application
- Et toujours : modularité, performances, sécurité
