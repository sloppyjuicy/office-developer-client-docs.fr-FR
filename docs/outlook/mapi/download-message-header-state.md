---
title: Télécharger l'état de l'en-tête du message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417118"
---
# <a name="download-message-header-state"></a>Télécharger l'état de l'en-tête du message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe pendant l'état de l'en-tête du message de téléchargement de la machine à États de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d'État:  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|Structure de données associée:  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|À partir de cet État:  <br/> |[État inactif](idle-state.md) <br/> |
|À cet État:  <br/> |État inactif  <br/> |
   
> [!NOTE]
> L'ordinateur d'état de réplication est un ordinateur d'État déterministe. Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier. 
  
## <a name="description"></a>Description

Dans cet État, le client met à jour l'en-tête d'un message dans un magasin local. Le magasin local passe dans cet État sur **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)** et quitte lorsque **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)** est appelé. Dans cet État, Outlook initialise les membres de la structure de données **HDRSYNC** associée avec des informations sur l'en-tête d'un message. Le client télécharge d'abord l'élément de message complet à partir du serveur, puis met à jour l'en-tête de l'élément de message localement. 
  
Lorsque synchronisation se termine, le client définit les résultats du téléchargement. Le magasin local revient à l'état inactif.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

