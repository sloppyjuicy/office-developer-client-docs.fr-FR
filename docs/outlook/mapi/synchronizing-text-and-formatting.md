---
title: Synchronisation du texte et de la mise en forme
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d797932a9fd22944f1cfd78e7fb67cd3ddbf8632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588817"
---
# <a name="synchronizing-text-and-formatting"></a>Synchronisation du texte et de la mise en forme

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Le défi principal de l’envoi de messages RTF (RICH Text Format) consiste à maintenir la synchronisation avec la mise en forme du texte. Pour garantir que lorsque les messages arrivent à destination qu’ils sont en tant que leurs auteurs prévus et que le texte et la mise en forme sont synchronisées, MAPI fournit la fonction [RTFSync](rtfsync.md) . **RTFSync** est généralement appelée par les clients prenant en charge les RTF avant d’afficher les messages entrants et par le spouleur MAPI lorsqu’il télécharge des messages à un fournisseur de transport. Les appelants spécifier la zone d’incohérence possible en transmettant un ou deux indicateurs à **RTFSync**:
  
- RTF_SYNC_BODY_CHANGED pour indiquer une modification dans le texte du message.
    
- RTF_SYNC_RTF_CHANGED pour indiquer une modification dans la mise en forme du message.
    
Le processus de synchronisation qui se produit dans **RTFSync** est un contrôle de redondance cyclique sophistiquées (CRC) du texte des messages qui ignore certains caractères et convertit d’autres personnes. Caractères probablement ont été ajoutés par les fournisseurs de transport sont ignorés. MAPI définit plusieurs propriétés pour travailler avec le format RTF comme décrit dans le tableau suivant. 
  
|**Propriété RTF**|**Description**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |Indique le début du texte du message réel.  <br/> |
|**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |Contient le résultat de la vérification de redondance cyclique du texte du message.  <br/> |
|**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |Contient le nombre de caractères dans **PR_RTF_SYNC_BODY_CRC**.  <br/> |
|**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))  <br/> |Valeur TRUE lorsque le message texte et la mise en forme ont été synchronisés.  <br/> |
|**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |Contient le nombre de caractères nonwhitespace que précédez le texte du message.  <br/> |
|**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |Contient le nombre de caractères nonwhitespace qui trace le texte du message.  <br/> |
   

