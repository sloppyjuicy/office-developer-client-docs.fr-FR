---
title: SRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SRow
api_type:
- COM
ms.assetid: 369c2d5c-8c2b-4314-9cb2-aaa89580aa2b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c88cb2425e44844de4fc127a1b97ad5dc9ed851a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566492"
---
# <a name="srow"></a>SRow

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une ligne d’un tableau qui contient les propriétés sélectionnées pour un objet spécifique. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a>Members

**ulAdrEntryPad**
  
> Remplissage d’octets pour aligner correctement les valeurs de propriété pointées par le **membre lpProps.** 
    
**cValues**
  
> Nombre de valeurs de propriétés pointées par **lpProps**. 
    
**lpProps**
  
> Pointeur vers un tableau de structures [SPropValue](spropvalue.md) qui décrivent les valeurs de propriété pour les colonnes de la ligne. 
    
## <a name="remarks"></a>Remarques

Une **structure SRow** décrit une ligne dans un tableau. Il est inclus dans la structure [TABLE_NOTIFICATION](table_notification.md) qui accompagne une notification de tableau. 
  
Les structures **SRow** sont utilisées dans les méthodes suivantes : 
  
- [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
    
- [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [ITableData : IUnknown](itabledataiunknown.md) (nombreuses méthodes) 
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Lorsque plusieurs lignes doivent être décrites, une structure [SRowSet](srowset.md) est utilisée. Une structure **SRowSet** contient un tableau de structures **SRow** et un nombre de structures dans le tableau. 
  
L’illustration suivante montre la relation entre une structure de données **SRow** et une structure **de données SRowSet.** 
  
**Relation entre SRow et SRowSet**
  
![Relation entre SRow et SRowSet](media/amapi_17.gif "Relation entre SRow et SRowSet")
  
Les structures **SRow** sont définies de la même manière que les structures [ADRENTRY.](adrentry.md) Par conséquent, une ligne d’une table des destinataires et une entrée dans une liste d’adresses peuvent être traitées de la même manière. 
  
Pour plus d’informations sur la façon dont la mémoire des structures **SRow** doit être allouée, voir [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Voir aussi

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [Structures MAPI](mapi-structures.md)
- [Gestion de la mémoire pour les structures ADRLIST et SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

