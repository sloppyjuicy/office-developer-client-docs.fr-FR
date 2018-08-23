---
title: À propos de la machine à états de réplication
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf36c6cb-57b4-7b2b-e23d-e0bc8696de96
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 30dd43a3ac9a315cd41919872b918bee639ca259
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593052"
---
# <a name="about-the-replication-state-machine"></a>À propos de la machine à états de réplication

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette rubrique contient une vue d’ensemble de la machine à états pour la réplication de données Microsoft Outlook 2013 et Microsoft Outlook 2010.
  
> [!NOTE]
> L’API de réplication doit être entièrement implémentée conformément aux instructions de cette rubrique pour pouvoir être utile ou pris en charge. L’API de réplication est disponible en mode exclusif pour répliquer les modifications Outlook 2013 ou Outlook 2010 vers et à partir d’un serveur. 
  
## <a name="iostx-and-the-state-machine"></a>IOSTX et la Machine à États

Un client appelle **[IOSTX::SyncBeg](iostx-syncbeg.md)**, **[IOSTX::SyncEnd](iostx-syncend.md)**, **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** et **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** dans une séquence de synchronisation des dossiers Outlook 2013 ou Outlook 2010 et éléments entre un magasin local et un serveur. La séquence d’appels réelle dépend des données qui doivent être répliquées (par exemple, une hiérarchie de dossiers Outlook 2013 ou Outlook 2010, un Outlook 2013 ou dossier Outlook 2010, éléments de courrier, éléments de calendrier et ainsi de suite) et la direction de la synchronisation (si téléchargement à partir du magasin local sur le serveur ou le téléchargement à partir du serveur dans le magasin local). Voici une séquence classique d’appels : 
  
1. Le client appelle **IOSTX::SyncBeg** pour commencer la réplication, en spécifiant un identificateur d’état et un pointeur vers l’adresse d’une structure de données correspondant. 
    
2. Outlook 2013 ou Outlook 2010 alloue de la structure de données et initialise la structure de données avec les informations nécessaires pour le client. 
    
3. Le client effectue la réplication, mise à jour de la structure de données pour transmettre les informations nécessaires sur la réplication du stockage local.
    
4. Après avoir effectué la réplication, le client appelle **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** et **IOSTX::SyncEnd** pour notifier le magasin local de la fin de la réplication spécifique. 
    
> [!NOTE]
> Le client appelle toujours **IOSTX::SyncEnd** pour mettre fin à une réplication que le client a commencé pour un état particulier. En fonction de données globales que le client a besoin pour synchroniser, le client peut appeler plusieurs fois la paire d’appels **IOSTX::SyncBeg** et **IOSTX::SyncEnd** . 
  
## <a name="state-table"></a>Table d’état

> [!NOTE]
> Le tableau suivant répertorie tous les états valides sur l’ordinateur d’état de réplication, ainsi que les identificateurs d’état correspondants et les structures de données. Dans la colonne de **Données répliquées** , le terme « éléments » inclut le courrier, calendrier, contacts, note, journal et éléments de tâche. Lors de la réplication du stockage local sur le serveur, utilisez les identificateurs d’état indiquant « Télécharger » et les structures de données avec le préfixe « UP » (par exemple, **LR_SYNC_UPLOAD_HIERARCHY** et **[UPHIER](uphier.md)** ). Lors de la réplication des modifications dans le magasin local à partir du serveur, utilisez les identificateurs d’état indiquant « Télécharger » et les structures de données avec le préfixe « DN » (par exemple, **LR_SYNC_DOWNLOAD_HIERARCHY** et **[DNHIER](dnhier.md)** ). 
  
|||||
|:-----|:-----|:-----|:-----|
|**State** <br/> |**Données répliquées** <br/> |**Identificateur d’état** <br/> |**Structure de données** <br/> |
|[État inactif](idle-state.md) <br/> | *None*  <br/> |**LR_SYNC_IDLE** <br/> | *None*  <br/> |
|[État de synchronisation](synchronize-state.md) <br/> |Dossiers ou éléments  <br/> |**LR_SYNC** <br/> |**[SYNC](sync.md)** <br/> |
|[Télécharger l’état de la hiérarchie](upload-hierarchy-state.md) <br/> |Dossiers  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**[UPHIER](uphier.md)** <br/> |
|[Télécharger l’état du dossier](upload-folder-state.md) <br/> |Folder  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**[UPFLD](upfld.md)** <br/> |
|[Synchroniser le contenu d’un état](synchronize-contents-state.md) <br/> |Items  <br/> |**LR_SYNC_CONTENTS** <br/> |**[SYNCCONT](synccont.md)** <br/> |
|[Télécharger l’état de la table](upload-table-state.md) <br/> |Items  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |**[UPTBL](uptbl.md)** <br/> |
|[Télécharger l’état du message](upload-message-state.md) <br/> |Item  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |**[UPMSG](upmsg.md)** <br/> |
|[Télécharger l’état de lecture](upload-read-status-state.md) <br/> |Items  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |**[UPREAD](upread.md)** <br/> |
|[Télécharger l’état de la suppression](upload-delete-status-state.md) <br/> |Items  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |**[UPDEL](updel.md)** <br/> |
|[État de la hiérarchie du téléchargement](download-hierarchy-state.md) <br/> |Dossiers  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |**[DNHIER](dnhier.md)** <br/> |
|[Table état du téléchargement](download-table-state.md) <br/> |Items  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |**[DNTBL](dntbl.md)** <br/> |
|[Télécharger l’état d’en-tête de message](download-message-header-state.md) <br/> |En-tête de message  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
   
## <a name="state-transition-diagram"></a>Diagramme de Transition d’état

Le diagramme suivant illustre les transitions d’état qui se produisent lors du téléchargement ou effectuer une synchronisation complète (téléchargement suivi en les téléchargeant) de dossiers ou de contenu de dossiers (messagerie, calendrier, contacts, une note, tâche ou éléments de journal). 
  
@@@NEED À INSÉRER UNE IMAGE CLIPART ICI MANQUANT @@@
  
## <a name="example-uploading-a-folder-hierarchy"></a>Exemple : Téléchargement une hiérarchie de dossiers

 Lorsque vous transférez une hiérarchie de dossiers, la séquence d’étapes suivante a lieu : 
  
|||||
|:-----|:-----|:-----|:-----|
|**Étape** <br/> |**Opération** <br/> |**State** <br/> |**Structure de données connexes** <br/> |
|1.  <br/> |Le client envoie la hiérarchie de téléchargement **IOSTX::SyncBeg**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|2.  <br/> |Outlook 2013 ou Outlook 2010 remplit **UPHIER** avec des informations pour le client. Cela inclut l’initialisation des paramètres [out] : *iEnt* est défini sur 0 et *cEnt* au nombre de dossiers dans la hiérarchie qui a besoin de téléchargement.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|3.  <br/> |Le client effectue le téléchargement de la hiérarchie réel. Par exemple, si *cEnt* est 10, pour chacun des 10 dossiers, le client appelle **IOSTX::SyncBeg**, spécifiant la structure de données pour le téléchargement d’un dossier et l’identificateur de l’état approprié.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|4.  <br/> |Outlook 2013 ou Outlook 2010 remplit **UPFLD** par l’initialisation de ses paramètres [out], y compris la raison pour le téléchargement de dossier, le pointeur vers l’objet folder et l’identificateur d’entrée pour le dossier.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|5.  <br/> |Le client télécharge le dossier spécifié.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|6.  <br/> |Le client avertit le magasin local de la fin du téléchargement de dossier : en cas de réussite, le client définit le [in] paramètre *ulFlags* dans **UPFLD** avec **UPF_OK**, puis appelle **IOSTX::SetSyncResult (S_OK)** et **IOSTX::SyncEnd **. En cas d’échec, le client ne serait pas défini *ulFlags* avec l’indicateur **UPF_OK** . Elle appelle **IOSTX::SetSyncResult**, en passant la valeur **HRESULT** et **IOSTX::SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|7.  <br/> |Si **UPF_OK** est défini, Outlook 2013 ou Outlook 2010 efface la demande interne de téléchargement du dossier. Puis quel que soit l’état de *ulFlags* , elle nettoie les informations de suivi interne. Alors que les dossiers sont toujours dans la hiérarchie pour télécharger (*iEnt* est toujours inférieure à *cEnt*), répétez les étapes 3 à 7 client et Outlook 2013 ou Outlook 2010.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|8.  <br/> |Le client avertit le magasin local de la fin du téléchargement de hiérarchie : en cas de réussite, le client définit le [in] indicateur dans **UPHIER** avec **UPH_OK**et appelle ensuite **IOSTX::SetSyncResult (S_OK)** et **IOSTX::SyncEnd**. En cas d’échec, le client ne serait pas définir l’indicateur **UPH_OK** . Elle appelle **IOSTX::SetSyncResult**, en passant la valeur **HRESULT** et **IOSTX::SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|9.  <br/> |Si **UPH_OK** est défini, Outlook 2013 ou Outlook 2010 efface la demande interne de téléchargement de la hiérarchie. Puis quel que soit l’état de *ulFlags* , elle nettoie les informations de suivi interne.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
   
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[SYNCSTATE](syncstate.md)

