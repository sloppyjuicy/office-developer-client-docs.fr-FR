---
title: Télécharger l’état de l’en-tête de message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c9d1745d25e7f7a5052d767350ade6723067d1b8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578842"
---
# <a name="download-message-header-state"></a>Télécharger l’état de l’en-tête de message

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit le déroulement de l’état d’en-tête de message téléchargement de l’ordinateur d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|Structure de données associées :  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|À partir de cet état :  <br/> |[État inactif](idle-state.md) <br/> |
|Avec cet état :  <br/> |État inactif  <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est une machine à états déterministe. Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier. 
  
## <a name="description"></a>Description

Au cours de cet état, le client met à jour l’en-tête d’un message sur un magasin local. Le magasin local passe à cet état lors de **[l’IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** et quitte lorsque **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** est appelée. Au cours de cet état, Outlook initialise les membres de la structure de données **HDRSYNC** associée avec des informations sur l’en-tête d’un message. Le client télécharge d’abord l’élément de message complet à partir du serveur, puis met à jour l’en-tête de l’élément de message localement. 
  
Lors de la synchronisation se termine, le client définit les résultats de téléchargement. Le magasin local renvoie l’état inactif.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

