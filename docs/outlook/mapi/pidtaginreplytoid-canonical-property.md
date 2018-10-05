---
title: Propriété canonique PidTagInReplyToId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInReplyToId
api_type:
- HeaderDef
ms.assetid: d435a65a-de01-4fb0-bc54-a87a2c4462ac
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 036f38c1228e08cfc9a2093c027195a802904f19
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392171"
---
# <a name="pidtaginreplytoid-canonical-property"></a>Propriété canonique PidTagInReplyToId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur de la propriété **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) du message d’origine.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W  <br/> |
|Identificateur :  <br/> |0x1042  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés doivent être définies sur tous les messages de réponse.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

