---
title: Propriété canonique PidTagReadReceiptSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptSearchKey
api_type:
- COM
ms.assetid: a0ea5628-1393-4ab8-bc34-a58cf130db51
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: aa92e224f10fd652078b965c8e3a0b5ab59cc388
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398730"
---
# <a name="pidtagreadreceiptsearchkey-canonical-property"></a>Propriété canonique PidTagReadReceiptSearchKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une clé de recherche pour l’utilisateur de messagerie à laquelle le système de messagerie doit diriger un rapport de lecture d’un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_READ_RECEIPT_SEARCH_KEY  <br/> |
|Identificateur :  <br/> |0x0053  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est ignorée sauf si la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) est définie sur TRUE.
  
Si une application cliente doit recevoir une lu reports lui-même, il peut laisser cette propriété non définie ou affectez-lui la clé de recherche contenue dans la propriété **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) au moment d’envoi de message.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidef.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

