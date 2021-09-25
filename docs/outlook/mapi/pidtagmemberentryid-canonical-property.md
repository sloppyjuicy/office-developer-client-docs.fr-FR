---
title: Propriété canonique PidTagMemberEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 851c08abcb1d75d6649bb9b5f46618ffa4500d0c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609858"
---
# <a name="pidtagmemberentryid-canonical-property"></a>Propriété canonique PidTagMemberEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée d’objet d’annuaire d’un membre de la table liste de contrôle d’accès système (SACL).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MEMBER_ENTRYID  <br/> |
|Identificateur :  <br/> |0x0FFF  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée par l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) pour identifier de manière unique une personne ou un rôle auquel la SACL s’applique. Une fois qu’un membre est créé dans la table SACL, **l’ENTRYID** ne peut pas être modifié. Pour le modifier, vous devez supprimer le membre de la table et le créer à nouveau avec un **autre ENTRYID**.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

