---
title: Propriété canonique PidTagMemberEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 83a645b49e5bb48051bbaedb26058d2da053348b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342496"
---
# <a name="pidtagmemberentryid-canonical-property"></a>Propriété canonique PidTagMemberEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l'identificateur d'entrée d'objet d'annuaire d'un membre de la liste de contrôle d'accès système (SACL).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MEMBER_ENTRYID  <br/> |
|Identificateur :  <br/> |0x0FFF  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée par l'interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) pour identifier de manière unique une personne ou un rôle auxquels s'applique la liste SACL. Après la création d'un membre dans la table SACL, la propriété **EntryID** ne peut pas être modifiée. Pour le modifier, vous devez supprimer le membre de la table et le recréer avec un **EntryID**différent.
  
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

