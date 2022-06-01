---
title: DTBLDDLBX
description: DTBLDDLBX décrit un contrôle de liste déroulante qui sera utilisé dans une boîte de dialogue créée à partir d’une table d’affichage.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLDDLBX
api_type:
- COM
ms.assetid: cf60584c-4357-44c7-9d51-f30f7e510c0c
ms.openlocfilehash: 5bcf36b336c1b60046e3bbfe533af8ad84716b95
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817556"
---
# <a name="dtblddlbx"></a>DTBLDDLBX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un contrôle de liste déroulante qui sera utilisé dans une boîte de dialogue créée à partir d’une table d’affichage.
  
|Propriété|Valeur|
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
  
> Balise de propriété pour une propriété de type PT_TSTRING. Cette propriété est l’une des colonnes de la table identifiées par le membre **ulPRTableName** . Les valeurs de cette propriété sont affichées dans la liste. 
    
 **ulPRSetProperty**
  
> Balise de propriété pour une propriété de n’importe quel type. Cette propriété est l’une des colonnes de la table identifiées par le membre **ulPRTableName** . Lorsque l’utilisateur de la liste sélectionne une valeur de propriété pour le membre **ulPRDisplayProperty** dans les lignes de la table identifiées par le membre **ulPRTableName** , le membre **ulPRSetProperty** correspondant est défini. 
    
 **ulPRTableName**
  
> Balise de propriété pour une propriété de table de type PT_OBJECT qui peut être ouverte à l’aide d’un appel **OpenProperty** . La table doit avoir deux colonnes : **ulPRDisplayProperty** et **ulPRSetProperty**. Les lignes de la table doivent correspondre aux éléments de la liste.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLDDLBX** décrit un contrôle de liste déroulante qui s’affiche en tant qu’élément unique jusqu’à ce que l’utilisateur choisisse de le développer. 
  
Les trois propriétés identifiées par les balises de propriété fonctionnent ensemble pour afficher les informations dans la liste et définir une propriété associée. Le membre **ulPRTableName** est un objet de table accessible via un appel à [IMAPIProp::OpenProperty](imapiprop-openproperty.md). La table a deux colonnes : une colonne pour la propriété identifiée par le membre **ulPRDisplayProperty** et l’autre pour la propriété identifiée par le membre **ulPRSetProperty** . 
  
La propriété **ulPRDisplayProperty** pilote l’affichage de la liste. Lorsqu’un utilisateur sélectionne l’une des valeurs dans l’affichage, MAPI appelle [IMAPIProp::SetProps](imapiprop-setprops.md) pour définir la propriété correspondante telle qu’identifiée par le membre **ulPRSetProperty** . Cela signifie que la propriété dans la même ligne que la propriété d’affichage sélectionnée. Le membre **ulPRSetProperty** ne peut pas être défini sur **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
  
Une valeur initiale s’affiche dans la liste si MAPI a récupéré la propriété représentée par le membre **ulPRSetProperty** via un appel à [IMAPIProp::GetProps](imapiprop-getprops.md) et a localisé une ligne dans la table avec la valeur du membre **ulPRSetProperty** . La valeur initiale affichée est le contenu de la colonne **ulPRDisplayProperty** de cette ligne qui correspond à la propriété dans le membre **ulPRDisplayProperty** de la structure. La valeur retournée par **GetProps** pour la propriété identifiée par le membre **ulPRDisplayProperty** devient la valeur initiale affichée lors de la première affichage de la liste. 
  
Pour obtenir une vue d’ensemble des tables d’affichage, consultez [Tables d’affichage](display-tables.md). Pour plus d’informations sur l’implémentation d’une table d’affichage, consultez [Implémentation d’une table d’affichage](display-table-implementation.md). Pour plus d’informations sur les types de propriétés, consultez [vue d’ensemble du type de propriété MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[Structures MAPI](mapi-structures.md)
  
[Implémentation de table d’affichage](display-table-implementation.md)
  
[Afficher les tables](display-tables.md)
  
[Vue d’ensemble du type de propriété MAPI](mapi-property-type-overview.md)

