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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 244aaea4902d6be8eda4cdca176436af9b002ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438847"
---
# <a name="dtblddlbx"></a>DTBLDDLBX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un contrôle de liste déroulante qui sera utilisé dans une boîte de dialogue construite à partir d'une table d'affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
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
  
> Balise de propriété pour une propriété de type PT_TSTRING. Cette propriété est une des colonnes du tableau identifié par le membre **ulPRTableName** . Les valeurs de cette propriété sont affichées dans la liste. 
    
 **ulPRSetProperty**
  
> Balise de propriété pour une propriété de n'importe quel type. Cette propriété est une des colonnes du tableau identifié par le membre **ulPRTableName** . Lorsque l'utilisateur de la liste sélectionne une valeur de propriété pour le membre **ulPRDisplayProperty** à partir des lignes du tableau identifié par le membre **ulPRTableName** , le membre **ulPRSetProperty** correspondant est défini. 
    
 **ulPRTableName**
  
> Balise de propriété pour une propriété de table de type PT_OBJECT qui peut être ouverte à l'aide d'un appel **OpenProperty** . Le tableau doit contenir deux colonnes: **ulPRDisplayProperty** et **ulPRSetProperty**. Les lignes du tableau doivent correspondre à des éléments de la liste.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLDDLBX** décrit un contrôle de liste déroulante qui s'affiche sous la forme d'un élément unique jusqu'à ce que l'utilisateur choisisse de le développer. 
  
Les trois propriétés identifiées par les balises Property s'emploient ensemble pour afficher les informations de la liste et définir une propriété associée. Le membre **ulPRTableName** est un objet table accessible via un appel à [IMAPIProp:: OpenProperty](imapiprop-openproperty.md). Le tableau comporte deux colonnes: une colonne pour la propriété identifiée par le membre **ulPRDisplayProperty** et l'autre pour la propriété identifiée par le membre **ulPRSetProperty** . 
  
La propriété **ulPRDisplayProperty** pilote l'affichage de la liste. Lorsqu'un utilisateur sélectionne une des valeurs dans l'affichage, MAPI appelle [IMAPIProp:: SetProps](imapiprop-setprops.md) pour définir la propriété correspondante identifiée par le membre **ulPRSetProperty** . Cela signifie que la propriété est dans la même ligne que la propriété Display sélectionnée. Le membre **ulPRSetProperty** ne peut pas être défini sur **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
  
Une valeur initiale s'affiche dans la liste si MAPI a récupéré la propriété représentée par le membre **ulPRSetProperty** via un appel à [IMAPIProp:: GetProps](imapiprop-getprops.md) et a localisé une ligne dans le tableau avec la valeur du membre **ulPRSetProperty** . La valeur initiale affichée est le contenu de la colonne **ulPRDisplayProperty** de cette ligne qui correspond à la propriété dans le membre **ulPRDisplayProperty** de la structure. La valeur renvoyée par **GetProps** pour la propriété identifiée par le membre de **ulPRDisplayProperty** devient la valeur initiale qui apparaît lorsque la liste est d'abord affichée. 
  
Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md). Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md). Pour plus d'informations sur les types de propriétés, voir [MAPI Property type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[Structures MAPI](mapi-structures.md)
  
[Implémentation des tables d'affichage](display-table-implementation.md)
  
[Tables d'affichage](display-tables.md)
  
[Vue d'ensemble du type de propriété MAPI](mapi-property-type-overview.md)

