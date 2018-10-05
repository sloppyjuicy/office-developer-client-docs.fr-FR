---
title: Propriété canonique PidTagEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmailAddress
api_type:
- HeaderDef
ms.assetid: bbd1e187-172e-4612-9efe-7c8e52967dfe
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: efcb72d872836adce544f3a90cf093de1f3713a7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393879"
---
# <a name="pidtagemailaddress-canonical-property"></a>Propriété canonique PidTagEmailAddress

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’adresse de messagerie de l’utilisateur de messagerie. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |ADRESSE_EMAIL_PR, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W  <br/> |
|Identificateur :  <br/> |0x3003  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |MAPI courantes  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont des exemples de propriétés d’adresse de base pour tous les utilisateurs de messagerie. Il est une chaîne dont le format a de signification seulement pour le système de messagerie sous-jacent. 
  
Ces propriétés sont utilisées conjointement avec les propriétés **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) dans les messages d’adressage **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)). Le format de chaîne est qualifié par **TYPEADR_PR**. 
  
Les valeurs valides pour cette propriété sont les suivantes : 
  
```cpp
network/postoffice/user 
Bruce@XYZZY.COM 
/c=US/a=att/p=Microsoft/o=Finance/ou=Purchasing/s=Furthur/g=Joe 
 
```

## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
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

