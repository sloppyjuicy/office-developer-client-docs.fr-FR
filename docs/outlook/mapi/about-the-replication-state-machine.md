---
title: À propos de la machine à états de réplication
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf36c6cb-57b4-7b2b-e23d-e0bc8696de96
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a0644e4bf5c6847d61cc59e203d50f61ad142e84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329749"
---
# <a name="about-the-replication-state-machine"></a>À propos de la machine à états de réplication

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique contient une vue d'ensemble de la machine à États pour Microsoft Outlook 2013 et la réplication des données Microsoft Outlook 2010.
  
> [!NOTE]
> L'API de réPlication doit être entièrement implémentée conformément aux instructions de cette rubrique pour être utile ou prise en charge. L'API de réPlication est disponible exclusivement pour répliquer Outlook 2013 ou Outlook 2010 vers et à partir d'un serveur. 
  
## <a name="iostx-and-the-state-machine"></a>IOSTX et ordinateur d'État

Un client appelle **[IOSTX:: SyncBeg](iostx-syncbeg.md)**, **[IOSTX:: SyncEnd,](iostx-syncend.md)**, **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)** et **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)** dans une séquence pour synchroniser les dossiers et les éléments Outlook 2013 ou Outlook 2010 entre un magasin local et un serveur. La séquence d'appels réelle dépend des données à répliquer (par exemple, une hiérarchie de dossiers Outlook 2013 ou Outlook 2010, un dossier Outlook 2013 ou Outlook 2010, des éléments de courrier, des éléments de calendrier, etc.) et le sens de la synchronisation (que chargement depuis le magasin local vers le serveur, ou téléchargement à partir du serveur vers le magasin local). Voici une séquence d'appels classique: 
  
1. Le client appelle **IOSTX:: SyncBeg** pour commencer la réplication, en spécifiant un identificateur d'État et un pointeur vers une adresse d'une structure de données correspondante. 
    
2. Outlook 2013 ou Outlook 2010 alloue la structure de données et initialise la structure de données avec les informations nécessaires pour le client. 
    
3. Le client effectue la réplication, mettant à jour la structure de données pour transmettre au magasin local toutes les informations nécessaires à propos de la réplication.
    
4. Après avoir effectué la réplication, le client appelle **[IOSTX:: SetSyncResult](iostx-setsyncresult.md)** et **IOSTX:: SyncEnd,** pour informer le magasin local de la fin de la réplication spécifique. 
    
> [!NOTE]
> Le client appelle toujours **IOSTX:: SyncEnd,** pour mettre fin à une réplication démarrée par le client pour un certain état. En fonction des données globales que le client doit synchroniser, le client peut appeler la paire d'appels **IOSTX:: SyncBeg** et **IOSTX:: SyncEnd,** plusieurs fois. 
  
## <a name="state-table"></a>Table d'État

> [!NOTE]
> Le tableau suivant répertorie tous les États valides dans la machine à États de réplication, ainsi que les identificateurs d'État et les structures de données correspondantes. Dans la colonne **données répliquées** , le terme «éléments» inclut les éléments courrier, calendrier, contact, note, Journal et tâche. Lors de la réplication des modifications de la banque locale sur le serveur, utilisez des identificateurs d'État spécifiant «télécharger» et des structures de données avec le préfixe «UP» (par exemple, **LR_SYNC_UPLOAD_HIERARCHY** et **[hier](uphier.md)** ). Lors de la réplication des modifications entre le serveur et le magasin local, utilisez des identificateurs d'État spécifiant «télécharger» et des structures de données avec le préfixe «DN» (par exemple, **LR_SYNC_DOWNLOAD_HIERARCHY** et **[DNHIER](dnhier.md)** ). 
  
|||||
|:-----|:-----|:-----|:-----|
|**State** <br/> |**Données répliquées** <br/> |**Identificateur d'État** <br/> |**Structure de données** <br/> |
|[État inactif](idle-state.md) <br/> | *None*  <br/> |**LR_SYNC_IDLE** <br/> | *None*  <br/> |
|[Synchronisation de l’état](synchronize-state.md) <br/> |Dossiers ou éléments  <br/> |**LR_SYNC** <br/> |**[SYNCHRONI](sync.md)** <br/> |
|[Charger l'état de la hiérarchie](upload-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**[UPHIER](uphier.md)** <br/> |
|[Télécharger l'état du dossier](upload-folder-state.md) <br/> |Folder  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**[UPFLD](upfld.md)** <br/> |
|[Synchroniser l'état du contenu](synchronize-contents-state.md) <br/> |Éléments  <br/> |**LR_SYNC_CONTENTS** <br/> |**[SYNCCONT](synccont.md)** <br/> |
|[Charger l'état de la table](upload-table-state.md) <br/> |Éléments  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |**[UPTBL](uptbl.md)** <br/> |
|[Charger l'état du message](upload-message-state.md) <br/> |Élément  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |**[UPMSG](upmsg.md)** <br/> |
|[Télécharger l'état de l'état de lecture](upload-read-status-state.md) <br/> |Éléments  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |**[UPREAD](upread.md)** <br/> |
|[Télécharger l'état de l'état de suppression](upload-delete-status-state.md) <br/> |Éléments  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |**[UPDEL](updel.md)** <br/> |
|[Télécharger l'état de la hiérarchie](download-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |**[DNHIER](dnhier.md)** <br/> |
|[Télécharger l'état de la table](download-table-state.md) <br/> |Éléments  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |**[DNTBL](dntbl.md)** <br/> |
|[Télécharger l'état de l'en-tête du message](download-message-header-state.md) <br/> |En-tête de message  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
   
## <a name="state-transition-diagram"></a>Diagramme de transition d'État

Le diagramme suivant montre les transitions d'État qui se produisent lors du téléchargement ou de l'exécution d'une synchronisation complète (téléchargement suivi d'un téléchargement) de dossiers ou de contenus de dossiers (messages, calendrier, contact, note, tâche ou journal). 
  
@ @ @ @ @NEED INSÉRER ICI UNE ILLUSTRATION MANQUANTE @ @ @ @ @ @
  
## <a name="example-uploading-a-folder-hierarchy"></a>Exemple: chargement d'une hiérarchie de dossiers

 Lors du chargement d'une hiérarchie de dossiers, la séquence d'étapes suivante a lieu: 
  
|||||
|:-----|:-----|:-----|:-----|
|**Étape** <br/> |**Action** <br/> |**State** <br/> |**Structure de données associée** <br/> |
|1.  <br/> |Le client lance le chargement de la hiérarchie avec **IOSTX:: SyncBeg**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|2.  <br/> |Outlook 2013 ou Outlook 2010 remplit la fonction **hier** avec des informations pour le client. Cela inclut l'initialisation des paramètres [out]: *iEnt* est défini sur 0 et *cEnt* sur le nombre de dossiers dans la hiérarchie qui nécessite un téléchargement.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|3.  <br/> |Le client effectue le chargement de la hiérarchie réelle. Par exemple, si le *pourcentage* est 10, pour chacun des 10 dossiers, le client appelle **IOSTX:: SyncBeg**, en spécifiant l'identificateur d'État et la structure de données appropriés pour le téléchargement d'un dossier.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|4.  <br/> |Outlook 2013 ou Outlook 2010 remplit **UPFLD** en initialisant ses paramètres [out], notamment la raison du chargement du dossier, le pointeur vers l'objet Folder et l'ID d'entrée du dossier.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|5.  <br/> |Le client télécharge le dossier spécifié.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|6.  <br/> |Le client informe le magasin local de la fin du chargement du dossier: en cas de réussite, le client définit le paramètre [in] *ulFlags* dans **UPFLD** avec **UPF_OK**, puis appelle **IOSTX:: SetSyncResult (S_OK)** et **IOSTX:: SyncEnd, **. En cas de défaillance, le client ne définit pas *ulFlags* avec l'indicateur **UPF_OK** . Il appelle **IOSTX:: SetSyncResult**, en transmettant la valeur **HRESULT** et **IOSTX:: SyncEnd,**.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|7.  <br/> |Si **UPF_OK** est défini, Outlook 2013 ou Outlook 2010 efface la demande interne de téléchargement du dossier. Ensuite, quel que soit l'état de *ulFlags* , il nettoie toutes les informations de suivi internes. Bien qu'il y ait toujours des dossiers dans la hiérarchie à télécharger (*iEnt* est toujours inférieur à *cEnt*), le client et outlook 2013 ou Outlook 2010 répètent les étapes 3 à 7.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|8.  <br/> |Le client informe le magasin local de la fin du chargement de la hiérarchie: en cas de réussite, le client définit l'indicateur [in **** ] dans la **UPH_OK**, puis appelle **IOSTX:: SetSyncResult (S_OK)** et **IOSTX:: SyncEnd,**. En cas de défaillance, le client ne définit pas l'indicateur **UPH_OK** . Il appelle **IOSTX:: SetSyncResult**, en transmettant la valeur **HRESULT** et **IOSTX:: SyncEnd,**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|9.  <br/> |Si **UPH_OK** est défini, Outlook 2013 ou Outlook 2010 efface la demande interne de téléchargement de la hiérarchie. Ensuite, quel que soit l'état de *ulFlags* , il nettoie toutes les informations de suivi internes.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
   
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[SYNCSTATE](syncstate.md)

