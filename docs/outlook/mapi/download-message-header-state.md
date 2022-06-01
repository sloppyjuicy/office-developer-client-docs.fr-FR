---
title: Télécharger l’état de l’en-tête de message
description: Cette rubrique décrit ce qui se passe pendant l’état d’en-tête du message de téléchargement de l’ordinateur d’état de réplication.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
ms.openlocfilehash: 39f88a47e17c53e5b3f6c1b62554866c8ca58161
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817955"
---
# <a name="download-message-header-state"></a>Télécharger l’état de l’en-tête de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe pendant l’état d’en-tête du message de téléchargement de l’ordinateur d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|Structure de données associée :  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|À partir de cet état :  <br/> |[État inactif](idle-state.md) <br/> |
|À cet état :  <br/> |État inactif  <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est un ordinateur d’état déterministe. Un client qui part d’un état à un autre doit finalement revenir au premier d’un autre état. 
  
## <a name="description"></a>Description

Pendant cet état, le client met à jour l’en-tête d’un message sur un magasin local. Le magasin local entre dans cet état sur **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** et se ferme quand **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** est appelé. Pendant cet état, Outlook initialise les membres de la structure de données **HDRSYNC** associée avec des informations sur l’en-tête d’un message. Le client télécharge d’abord l’élément de message complet à partir du serveur, puis met à jour l’en-tête de l’élément de message localement. 
  
À la fin de la synchronisation, le client définit les résultats du téléchargement. Le magasin local revient à l’état d’inactivité.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

