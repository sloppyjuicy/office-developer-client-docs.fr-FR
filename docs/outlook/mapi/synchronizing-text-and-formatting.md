---
title: Synchronisation du texte et de la mise en forme
description: Décrit les solutions au principal défi lié à l’envoi de messages RTF (Rich Text Format), en conservant le texte synchronisé avec la mise en forme.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
ms.openlocfilehash: 436a244f4591dc08458f01cf72b6b31b20e0ba2e
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893934"
---
# <a name="synchronizing-text-and-formatting"></a>Synchronisation du texte et de la mise en forme

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le principal défi dans l’envoi de messages RTF (Rich Text Format) consiste à maintenir le texte synchronisé avec la mise en forme. Pour s’assurer que lorsque les messages arrivent à destination, ils sont comme leurs initiateurs prévus et que le texte et la mise en forme sont synchronisés, MAPI fournit la fonction [RTFSync](rtfsync.md) . **RTFSync** est généralement appelé par les clients prenant en compte RTF avant d’afficher les messages entrants et par le spouleur MAPI lorsqu’il télécharge les messages vers un fournisseur de transport. Les appelants spécifient la zone de différence possible en passant un ou deux indicateurs à **RTFSync** :
  
- RTF_SYNC_BODY_CHANGED pour indiquer une modification dans le texte du message.
    
- RTF_SYNC_RTF_CHANGED pour indiquer une modification dans la mise en forme des messages.
    
Le processus de synchronisation qui se produit dans **RTFSync** est une vérification de redondance cyclique sophistiquée (CRC) du texte du message qui ignore certains caractères et convertit d’autres caractères. Les caractères qui ont probablement été ajoutés par les fournisseurs de transport sont ignorés. MAPI définit plusieurs propriétés pour l’utilisation de RTF, comme décrit dans le tableau suivant. 
  
|**RTF, propriété**|**Description**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |Indique le début du texte réel du message. |
|**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |Contient le résultat de la vérification de redondance cyclique du texte du message. |
|**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |Contient le nombre de caractères dans **PR_RTF_SYNC_BODY_CRC**. |
|**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))  <br/> |Défini sur TRUE lorsque le texte et la mise en forme du message ont été synchronisés. |
|**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |Contient le nombre de caractères non vides qui ont précédé le texte du message. |
|**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |Contient le nombre de caractères nonwhitespace qui s’y retrouvent à la fin du texte du message. |
   

