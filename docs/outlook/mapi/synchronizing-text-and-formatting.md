---
title: Synchronisation du texte et de la mise en forme
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2c4d72e556724a78734790771835a7abe6a9103b
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62782527"
---
# <a name="synchronizing-text-and-formatting"></a>Synchronisation du texte et de la mise en forme

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le principal défi lors de l’envoi de messages au format RTF (Rich Text Format) est de conserver le texte synchronisé avec la mise en forme. Pour s’assurer que lorsque les messages arrivent à destination, ils sont comme prévu par leurs créateurs et que le texte et la mise en forme sont synchronisés, MAPI fournit la [fonction RTFSync](rtfsync.md) . **RtFSync** est généralement appelé par les clients rtF avant d’afficher les messages entrants et par lepooler MAPI lorsqu’il télécharge les messages vers un fournisseur de transport. Les appelants spécifient la zone de différences possible en passant un ou deux indicateurs à **RTFSync** :
  
- RTF_SYNC_BODY_CHANGED pour indiquer une modification dans le texte du message.
    
- RTF_SYNC_RTF_CHANGED pour indiquer une modification dans la mise en forme des messages.
    
Le processus de synchronisation qui se produit dans **RTFSync** est une vérification sophistiquée de la redondance cyclique (CRC) du texte du message qui ignore certains caractères et en convertit d’autres. Les caractères qui ont probablement été ajoutés par les fournisseurs de transport sont ignorés. MAPI définit plusieurs propriétés pour travailler avec rtf comme décrit dans le tableau suivant. 
  
|**RtF, propriété**|**Description**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |Indique le début du texte du message réel. |
|**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |Contient le résultat de la vérification de redondance cyclique du texte du message. |
|**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |Contient le nombre de caractères dans **PR_RTF_SYNC_BODY_CRC**. |
|**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))  <br/> |Valeur TRUE lorsque le texte et la mise en forme du message ont été synchronisés. |
|**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |Contient le nombre de caractères nonwhitespace qui ont précédé le texte du message. |
|**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |Contient le nombre de caractères nonwhitespace qui s’ajoutent au texte du message. |
   

