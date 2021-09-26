---
title: Télécharger l’état d’en-tête de message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 27f9290c7a1059d66cfb7eda53bb9a3143c04611
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630970"
---
# <a name="download-message-header-state"></a>Télécharger l’état d’en-tête de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se produit pendant l’état d’en-tête du message de téléchargement de la machine à états de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
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

