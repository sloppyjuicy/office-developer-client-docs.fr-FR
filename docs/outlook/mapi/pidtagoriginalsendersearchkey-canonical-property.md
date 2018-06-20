---
title: Propriété canonique PidTagOriginalSenderSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderSearchKey
api_type:
- COM
ms.assetid: 164eb9dd-e553-459e-99c1-3da0284bb01f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2aa0a8601a72b6d4c40167ac55d3d643bf946708
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786327"
---
# <a name="pidtagoriginalsendersearchkey-canonical-property"></a>Propriété canonique PidTagOriginalSenderSearchKey

  
  
**S’applique à**: Outlook 
  
Contient la clé de recherche pour l’expéditeur de la première version d’un message, autrement dit, le message avant d’être transférés ou une réponse.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_SENDER_SEARCH_KEY  <br/> |
|Identificateur :  <br/> |0x005C  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une des propriétés d’adresse de l’expéditeur d’origine d’un message. Au premier envoi du message, l’application cliente doit définir cette propriété à la valeur de la propriété **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)). Il n’est jamais modifié lorsque le message est transféré ou d’une réponse.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

