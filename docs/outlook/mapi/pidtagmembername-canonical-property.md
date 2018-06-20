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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 694cc4e4626fb9070927232bb72252f716eb458e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786207"
---
# <a name="pidtagmembername-canonical-property"></a>Propriété canonique PidTagMemberName

  
  
**S’applique à**: Outlook 
  
Contient le nom complet d’un membre de la table de liste (ACL) du contrôle access.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W  <br/> |
|Identificateur :  <br/> |0x6672  <br/> |
|Type de données :  <br/> |PT_STRING8  <br/> |
|Zone :  <br/> |Contrôle d’accès  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont utilisées par le [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface pour afficher le nom d’un membre d’une table ACL, qui est une personne ou un rôle disposant de droits explicites sur un dossier ou d’une boîte aux lettres. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
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
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

