---
title: Propriété canonique PidTagMemberName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberName
api_type:
- HeaderDef
ms.assetid: e19129bf-d07c-4d2e-9d4d-edbfda088ea7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a119cf1446600153e433c4aae99037d9810015c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390890"
---
# <a name="pidtagmembername-canonical-property"></a>Propriété canonique PidTagMemberName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom complet d’un membre de la table de liste (ACL) du contrôle access.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W  <br/> |
|Identificateur :  <br/> |0x6672  <br/> |
|Type de données :  <br/> |PT_STRING8  <br/> |
|Domaine :  <br/> |Contrôle d’accès  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont utilisées par le [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface pour afficher le nom d’un membre d’une table ACL, qui est une personne ou un rôle disposant de droits explicites sur un dossier ou d’une boîte aux lettres. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Gère la récupération des listes d’autorisations de dossier sont stockés sur le serveur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

