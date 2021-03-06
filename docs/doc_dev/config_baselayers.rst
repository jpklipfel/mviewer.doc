.. Authors : 
.. mviewer team

.. _configbaselayers:

Configurer - Les couches de fond
=================================

``<Baselayers>``
***************************

Paramétrages de la liste des fonds de plan.

**Syntaxe**

.. code-block:: xml
       :linenos:
	
        <baselayers style="">
            <baselayer />
            <baselayer />
        </baselayers>

**Paramètre**

* ``style``: paramètre optionnel de type texte à  choisir parmi (default/gallery) et  définissant le style du contrôle permettant de changer de fond de carte. Valeur par défaut **default**.

Le mode "default" active le contrôle suivant :

.. image:: ../_images/dev/config_baselayers/config_baselayers_default.png
              :alt: Configurer la liste des couches de fond
              :align: center

Le mode "gallery" active une liste à deux états :
un état déplié :

.. image:: ../_images/dev/config_baselayers/config_baselayers_gallery_1.png
              :alt: Configurer la liste des couches de fond
              :align: center
              
un état replié:

.. image:: ../_images/dev/config_baselayers/config_baselayers_gallery_2.png
              :alt: Configurer la liste des couches de fond
              :align: center
              
``<baselayer>``
******************
Elément enfant de ``<baselayers>`` permettant le paramétrage de chaque fond de plan.

**Syntaxe**

.. code-block:: xml
       :linenos:
	
	<baselayer type="" 
		id="" 
		label="" 
		title="" 
		maxscale="" 
		thumbgallery="" 
		url="" layers="" 
		format="" 
		visible="" 
		fromcapacity=""
		attribution="" 
		style="" 
		matrixset="" 
		maxzoom=""
	/>

**Paramètres**

* ``type``: paramètre obligatoire de type texte qui définit le type de la couche. Les options sont (OSM, WMTS, WMS, fake)
* ``id``: paramètre obligatoire de type texte pour attribuer un identifiant unique et interne à la couche
* ``label``: paramètre obligatoire de type texte pour définir le nom du fond de plan
* ``title``: paramètre obligatoire de type texte pour définir le sous-titre du fond de plan. Utilisé avec le mode "gallery"
* ``maxscale``: paramètre optionnel définissant l'échelle max du fond de plan
* ``thumbgallery``: paramètre obligatoire de type url permettant de sélecionner l'imagette à associer au fond de plan.
* ``url``: paramètre obligatoire de type url définissant l'URL du service web OSM, WMTS ou WMS.
* ``layers``: paramètre optionnel de type texte définissant l'identifiant technique de la couche. (Obligatoire pour les couches de type WMS et WMTS)
* ``format``: paramètre optionnel de type texte définissant le Format d'image retourné par le serveur. (Obligatoire pour les couches de type WMS et WMTS) 
* ``visible``: paramètre obligatoire de type booléen (true/false) précisant si la couche est visible au démarrage.
* ``fromcapacity``: paramètre optionnel de type booléen (true/false)spécifique aux fonds de plan WMTS. Permet la construction de la couche à  partir des capacités du service WMTS.
* ``attribution``: paramètre obligatoire alimentant le contrôle attributions de la carte ( |CreditsIcon| ).
* ``style`` : paramètre optionnel précisant le style à associer à la couche. Paramètre obligatoire pour les couches de type WMTS
* ``matrixset`` : paramètre optionnel précisant le style à associer à la couche. Paramètre obligatoire pour les couches de type WMTS si le paramètre **fromcapacity** n'est pas activé
* ``maxzoom``: paramètre optionnel de type numérique définissant le zoom maximum pour la couche.


.. |CreditsIcon| image:: ../_images/user/credits/credits_icon.png
              :alt: Credits
	      :width: 16 pt




