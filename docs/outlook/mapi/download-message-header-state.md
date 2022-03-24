---
title: Télécharger l’état d’en-tête de message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: de3dc880a78a895b11f22a8432555e8891c3c38a
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63725862"
---
# <a name="download-message-header-state"></a>Télécharger l’état d’en-tête de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se produit pendant l’état d’en-tête du message de téléchargement de la machine à états de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|Structure de données associée :  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|À partir de cet état :  <br/> |[État inactif](idle-state.md) <br/> |
|À cet état :  <br/> |État inactif  <br/> |
   
> [!NOTE]
> La machine à états de réplication est une machine à états déterministe. Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second. 
  
## <a name="description"></a>Description

Pendant cet état, le client met à jour l’en-tête d’un message dans un magasin local. Le magasin local entre cet état sur **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** et se quitte lorsque **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** est appelé. Au cours de cet état, Outlook initialise les membres de la structure de données **HDRSYNC** associée avec des informations sur l’en-tête d’un message. Le client télécharge d’abord l’élément de message complet à partir du serveur, puis met à jour l’en-tête de l’élément de message localement. 
  
Lorsque la synchronisation se termine, le client définit les résultats du téléchargement. Le magasin local revient à l’état inactif.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

