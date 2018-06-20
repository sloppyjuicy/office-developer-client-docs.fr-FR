---
title: DTBLDDLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLDDLBX
api_type:
- COM
ms.assetid: cf60584c-4357-44c7-9d51-f30f7e510c0c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2db95697cd98e66da9fb3d0cd0180b238c0a8dff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783217"
---
# <a name="dtblddlbx"></a>DTBLDDLBX

  
  
**S’applique à**: Outlook 
  
Décrit un contrôle de liste déroulante qui sera utilisé dans une boîte de dialogue établie à partir d’un tableau d’affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a>Membres

 **ulFlags**
  
> Réservé, doit être égal à zéro. 
    
 **ulPRDisplayProperty**
  
> Balise de propriété pour une propriété de type PT_TSTRING. Cette propriété est une des colonnes de la table identifiée par le membre **ulPRTableName** . Les valeurs de cette propriété sont affichent dans la liste. 
    
 **ulPRSetProperty**
  
> Balise de propriété pour une propriété d’un type quelconque. Cette propriété est une des colonnes de la table identifiée par le membre **ulPRTableName** . Lorsque l’utilisateur de la liste sélectionne une valeur de propriété pour le membre **ulPRDisplayProperty** à partir des lignes de la table identifiée par le membre **ulPRTableName** , le membre **ulPRSetProperty** correspondant est défini. 
    
 **ulPRTableName**
  
> Balise de propriété pour une propriété de tableau de type PT_OBJECT qui peuvent être ouverts à l’aide d’un **OpenProperty** appeler. Le tableau doit avoir deux colonnes : **ulPRDisplayProperty** et **ulPRSetProperty**. Les lignes du tableau doivent correspondre aux éléments de la liste.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLDDLBX** décrit un contrôle de liste déroulante qui s’affiche sous la forme d’un seul élément jusqu'à ce que l’utilisateur choisit pour le développer. 
  
Les trois propriétés identifiées par les balises de propriété fonctionnent ensemble pour afficher les informations dans la liste et définir une propriété connexe. Le membre **ulPRTableName** est un objet table qui est accessible via un appel à [IMAPIProp::OpenProperty](imapiprop-openproperty.md). La table contient deux colonnes : une colonne pour la propriété identifiée par le membre **ulPRDisplayProperty** et l’autre pour la propriété identifiée par le membre **ulPRSetProperty** . 
  
La propriété **ulPRDisplayProperty** gère l’affichage de liste. Lorsqu’un utilisateur sélectionne une des valeurs de l’affichage, [IMAPIProp::SetProps](imapiprop-setprops.md) pour définir la propriété correspondante tels qu’identifiés par le membre **ulPRSetProperty** appels MAPI. Cela signifie que la propriété dans la même ligne que la propriété affichage sélectionné. Le membre **ulPRSetProperty** ne peut pas être défini sur **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
  
Une valeur initiale s’affiche dans la liste si MAPI a récupéré de la propriété représentée par le membre **ulPRSetProperty** via un appel à [IMAPIProp::GetProps](imapiprop-getprops.md) et trouve une ligne dans la table avec la valeur du membre **ulPRSetProperty** . La valeur affichée initiale est le contenu de la colonne **ulPRDisplayProperty** à partir de la ligne qui correspond à la propriété dans le membre **ulPRDisplayProperty** de la structure. La valeur renvoyée par **GetProps** pour la propriété identifiée par le membre **ulPRDisplayProperty** devient la valeur initiale qui s’affiche lors du premier affichage de la liste. 
  
Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md). Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md). Pour plus d’informations sur les types de propriété, voir [Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[Structures MAPI](mapi-structures.md)
  
[Affichage tableau implémentation](display-table-implementation.md)
  
[Afficher les Tables](display-tables.md)
  
[Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md)

