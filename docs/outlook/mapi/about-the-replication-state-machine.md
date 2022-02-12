---
title: À propos de la machine à états de réplication
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: cf36c6cb-57b4-7b2b-e23d-e0bc8696de96
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 708a38b6f3e5789389febbf08750c16278a3b637
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770828"
---
# <a name="about-the-replication-state-machine"></a>À propos de la machine à états de réplication
 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique contient une vue d’ensemble de la machine à états pour Microsoft Outlook 2013 et Microsoft Outlook 2010 réplication des données.
  
> [!NOTE]
> L’API de réplication doit être entièrement implémentée conformément aux instructions de cette rubrique afin d’être utile ou prise en charge. L’API de réplication est disponible exclusivement pour répliquer Outlook 2013 ou Outlook 2010 vers et à partir d’un serveur. 
  
## <a name="iostx-and-the-state-machine"></a>IOSTX et la machine à états

Un client appelle **[IOSTX::SyncBeg](iostx-syncbeg.md)**, **[IOSTX::SyncEnd](iostx-syncend.md)**, **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** et **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** dans une séquence pour synchroniser les dossiers et éléments Outlook 2013 ou Outlook 2010 entre un magasin local et un serveur. La séquence d’appels réelle dépend des données qui doivent être répliquées (par exemple, une hiérarchie de dossiers Outlook 2013 ou Outlook 2010, un dossier Outlook 2013 ou Outlook 2010, des éléments de courrier, des éléments de calendrier, et ainsi de suite) et le sens de la synchronisation (que ce soit le téléchargement à partir du magasin local vers le serveur ou le téléchargement du serveur vers le magasin local). Voici une séquence d’appels classique : 
  
1. Le client appelle **IOSTX::SyncBeg** pour commencer la réplication, en spécifiant un identificateur d’état et un pointeur vers une adresse d’une structure de données correspondante. 
    
2. Outlook 2013 ou Outlook 2010 alloue la structure de données et initialise la structure de données avec les informations nécessaires pour le client. 
    
3. Le client effectue la réplication, en mettant à jour la structure de données pour transmettre au magasin local les informations nécessaires sur la réplication.
    
4. Après avoir effectué la réplication, le client appelle **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** et **IOSTX::SyncEnd** pour informer le magasin local de la fin de la réplication spécifique. 
    
> [!NOTE]
> Le client appelle toujours **IOSTX::SyncEnd** pour mettre fin à une réplication que le client a commencée pour un certain état. Selon les données globales que le client doit synchroniser, il peut appeler la paire d’appels **IOSTX::SyncBeg** et **IOSTX::SyncEnd** plusieurs fois. 
  
## <a name="state-table"></a>State Table

> [!NOTE]
> Le tableau suivant répertorie tous les états valides de la machine à états de réplication, ainsi que les identificateurs d’état et les structures de données correspondants. Dans la **colonne Répliquée des** données, le terme « éléments » inclut les éléments courrier, calendrier, contact, note, journal et tâche. Lors de la réplication des modifications du magasin local vers le serveur, utilisez des identificateurs d’état spécifiant « UPLOAD » et des structures de données avec le préfixe « UP » (par exemple, **LR_SYNC_UPLOAD_HIERARCHY** et **[UPHIER](uphier.md)** ). Lors de la réplication des modifications du serveur vers le magasin local, utilisez des identificateurs d’état spécifiant « DOWNLOAD » et des structures de données avec le préfixe « DN » (par exemple, **LR_SYNC_DOWNLOAD_HIERARCHY** et **[DNHIER](dnhier.md)** ). 
  
|||||
|:-----|:-----|:-----|:-----|
|**État** <br/> |**Données répliquées** <br/> |**Identificateur d’état** <br/> |**Structure des données** <br/> |
|[État inactif](idle-state.md) <br/> | *Aucune*  <br/> |**LR_SYNC_IDLE** <br/> | *Aucune*  <br/> |
|[Synchronisation de l’état](synchronize-state.md) <br/> |Dossiers ou éléments  <br/> |**LR_SYNC** <br/> |**[SYNC](sync.md)** <br/> |
|[Télécharger hiérarchie](upload-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**[UPHIER](uphier.md)** <br/> |
|[Télécharger dossier](upload-folder-state.md) <br/> |Folder  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**[UPFLD](upfld.md)** <br/> |
|[Synchroniser l’état du contenu](synchronize-contents-state.md) <br/> |Éléments  <br/> |**LR_SYNC_CONTENTS** <br/> |**[SYNCCONT](synccont.md)** <br/> |
|[Télécharger table](upload-table-state.md) <br/> |Éléments  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |**[UPTBL](uptbl.md)** <br/> |
|[Télécharger message](upload-message-state.md) <br/> |Item  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |**[UPMSG](upmsg.md)** <br/> |
|[Télécharger statut de lecture](upload-read-status-state.md) <br/> |Éléments  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |**[UPREAD](upread.md)** <br/> |
|[Télécharger l’état de suppression](upload-delete-status-state.md) <br/> |Éléments  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |**[UPDEL](updel.md)** <br/> |
|[Télécharger l’état de la hiérarchie](download-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |**[DNHIER](dnhier.md)** <br/> |
|[Télécharger l’état de la table](download-table-state.md) <br/> |Éléments  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |**[DNTBL](dntbl.md)** <br/> |
|[Télécharger l’état d’en-tête du message](download-message-header-state.md) <br/> |En-tête de message  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |**[HDRSYNC](hdrsync.md)** <br/> |

  
## <a name="example-uploading-a-folder-hierarchy"></a>Exemple : téléchargement d’une hiérarchie de dossiers

 Lors du chargement d’une hiérarchie de dossiers, la séquence d’étapes suivante a lieu : 
  
|||||
|:-----|:-----|:-----|:-----|
|**Étape** <br/> |**Action** <br/> |**État** <br/> |**Structure de données associée** <br/> |
|1. |Le client lance le chargement de la hiérarchie avec **IOSTX::SyncBeg**. |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|2. |Outlook 2013 ou Outlook 2010 remplit **UPHIER** avec des informations pour le client. Cela inclut l’initialisation des paramètres [out] :  *iEnt*  est définie sur 0 et  *cEnt*  sur le nombre de dossiers dans la hiérarchie qui doivent être téléchargés. |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|3. |Le client charge la hiérarchie réelle. Par exemple, si  *cEnt*  est 10, pour chacun des 10 dossiers, le client appelle **IOSTX::SyncBeg**, en spécifiant l’identificateur d’état et la structure de données appropriés pour le téléchargement d’un dossier. |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|4. |Outlook 2013 ou Outlook 2010 remplit **UPFLD** en initialisant ses paramètres [out], y compris la raison du chargement du dossier, le pointeur vers l’objet dossier et l’ID d’entrée du dossier. |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|5. |Le client charge le dossier spécifié. |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|6. |Le client avertit le magasin local de la fin du chargement du dossier : en cas de réussite, le client définit le paramètre [in]  *ulFlags*  dans **UPFLD** avec **UPF_OK**, puis appelle **IOSTX::SetSyncResult (S_OK)** et **IOSTX::SyncEnd**. En cas d’échec, le client ne définirait pas  *ulFlags*  avec **l’UPF_OK** défaut. Il appelle **IOSTX::SetSyncResult**, en passant la valeur **HRESULT** et **IOSTX::SyncEnd**. |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|7. |Si **UPF_OK** est définie, Outlook 2013 ou Outlook 2010 effacera la demande interne de téléchargement du dossier. Ensuite, quel que soit l’état *des ulFlags*, il nettoie toutes les informations de comptabilité internes. Bien qu’il existe encore des dossiers dans la hiérarchie à télécharger (*iEnt* est toujours inférieur à *cEnt*), le client et Outlook 2013 ou Outlook 2010 répètent les étapes 3 à 7. |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|8. |Le client **avertit** le magasin local de la fin du chargement de la hiérarchie : en cas de réussite, le client définit l’indicateur [in] dans **UPHIER** avec UPH_OK, puis appelle **IOSTX::SetSyncResult (S_OK)** et **IOSTX::SyncEnd**. En cas d’échec, le client ne définirait pas **l’UPH_OK** défaut. Il appelle **IOSTX::SetSyncResult**, en passant la valeur **HRESULT** et **IOSTX::SyncEnd**. |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|9. |Si **UPH_OK** est définie, Outlook 2013 ou Outlook 2010 effacera la demande interne de téléchargement de la hiérarchie. Ensuite, quel que soit l’état *des ulFlags*, il nettoie toutes les informations de comptabilité internes. |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
   
## <a name="see-also"></a>Voir aussi

[À propos de l’API de réplication](about-the-replication-api.md)  
[Constantes MAPI](mapi-constants.md)  
[SYNCSTATE](syncstate.md)
