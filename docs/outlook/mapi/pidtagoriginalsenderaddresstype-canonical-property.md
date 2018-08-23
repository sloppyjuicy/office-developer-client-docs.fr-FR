---
title: Propriété canonique PidTagOriginalSenderAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderAddressType
api_type:
- COM
ms.assetid: bd777f19-cbb1-4497-8a0b-e05b491c6957
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ba0d68482c06a1f6d9ccdae95f63e980a1fd23e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563743"
---
# <a name="pidtagoriginalsenderaddresstype-canonical-property"></a>Propriété canonique PidTagOriginalSenderAddressType

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient le type d’adresse de l’expéditeur de la première version d’un message, autrement dit, le message avant d’être transférés ou une réponse.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W  <br/> |
|Identificateur :  <br/> |0x0066  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont des exemples de propriétés d’adresse de l’expéditeur d’origine d’un message. Au premier envoi du message, l’application cliente doit définir ces propriétés à la valeur de **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)). Il n’est jamais modifié lorsque le message est transféré ou d’une réponse.
  
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
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

