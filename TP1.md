**Partie1: Preparer et installer VirtualBox**

1/ la virtualisation est bien activée quand je tape ctrl+maj+echap
![virtualisation](<Capture d'écran /Capture d'écran 2026-10-13 165749.png>)


2/ bcdedit/enum | finstr hypervisorlaunchtype : On obtient hypervisorlaunchtype auto

   systeminfo | findstr/C:"Hyper-V"   Configurtion requise:hyper-V detecté

3/ le téléchargement et l'istallation de VirtualBox ont reussi

4/  $env:Path += ";C:\Program Files\Oracle\VirtualBox" : noud restons dans le meme repertoire

VBoxManage --version : Nous donne 7.2.6r172322

VBoxManage list hostinfo: voir capture

**REPONSES AUX QUESTIONS**

1/**Un hyperviseur de type 1** est logiciel qui fonctionne directement sur le materiel physique.

**Un hyperviseur de type2** est un logiciel qui fonctionne sur un système d'exploitation déjà installé.
C'est le cas de la VirtualBox qui est hyperviseur de type2.

2/ La virtualisation matérielle(VT-x/AMD-V)  est indispensable car elle aide le processeur à mieux exécuter les systèmes virtuels éfficacement

3/Nous avons la version 7.2.6r172322 de VirtualBox.
 VBoxManage list hostinfo : coeur processeur:4
RAM : 3412Mbyte.
