---
title: Synchronisation du texte et de la mise en forme
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435102"
---
# <a name="synchronizing-text-and-formatting"></a>Synchronisation du texte et de la mise en forme

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le principal défi à relever lors de l'envoi de messages RTF (Rich Text Format) est le maintien de la synchronisation du texte avec la mise en forme. Pour vous assurer que lorsque les messages arrivent à leur destination, ils sont en tant que leurs expéditeurs et que le texte et la mise en forme sont synchronisés, MAPI fournit la fonction [RTFSync](rtfsync.md) . **RTFSync** est généralement appelé par les clients compatibles RTF avant l'affichage des messages entrants et par le spouleur MAPI lorsqu'il télécharge des messages vers un fournisseur de transport. Les appelants spécifient la zone de divergence possible en passant un ou deux indicateurs à **RTFSync**:
  
- RTF_SYNC_BODY_CHANGED pour indiquer une modification dans le texte d'un message.
    
- RTF_SYNC_RTF_CHANGED pour indiquer une modification dans la mise en forme du message.
    
Le processus de synchronisation qui se produit dans **RTFSync** est un contrôle de redondance cyclique (CRC) sophistiqué du texte du message qui ignore certains caractères et en convertit d'autres. Les caractères qui ont le plus de chances d'être ajoutés par les fournisseurs de transport sont ignorés. MAPI définit plusieurs propriétés pour utiliser le format RTF, comme décrit dans le tableau suivant. 
  
|**Propriété RTF**|**Description**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |Indique le début du texte du message réel.  <br/> |
|**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |Contient le résultat de la vérification de redondance cyclique du texte du message.  <br/> |
|**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |Contient le nombre de caractères dans **PR_RTF_SYNC_BODY_CRC**.  <br/> |
|**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))  <br/> |Affectez à cet argument la valeur TRUE lorsque le texte et la mise en forme du message ont été synchronisés.  <br/> |
|**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |Contient le nombre de caractères autres que le texte du message.  <br/> |
|**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |Contient le nombre de caractères autres que le texte du message.  <br/> |
   

