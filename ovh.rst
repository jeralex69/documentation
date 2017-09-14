=================================================
Installation, configuration des serveurs OVH
=================================================

Cette page liste les guides relatifs à l'installation et à la configuration de
serveur appartenant à OVH .

Configuration d'un volume RAID matériel
=======================================

Sur un serveur fraÎchement commandé et déployé, les 2 disques durs ne sont pas
en volume RAID sur la carte RAID matériel, seuls les 2 SSD sont aggrégés dans un
volume RAID (volume créé lors de la première installation ou à la mise en place
du serveur).

Prérequis : carte de type LSI Megaraid et de deux disques durs identiques au minimum.

Commande à executer pour créer un nouveau volume :

.. code-block:: bash

  root@rescue:~# storcli /c0 add vd type=r1 drives=252:0,252:1
