---
title: SRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRow
api_type:
- COM
ms.assetid: 369c2d5c-8c2b-4314-9cb2-aaa89580aa2b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 56bf1366cdd44fac185277280d2e8ab80c644c45
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579122"
---
# <a name="srow"></a>SRow

**S’applique à**: Outlook 2013 | Outlook 2016 
  
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
  
> Octets pour aligner correctement les valeurs des propriétés de remplissage vers laquelle pointe le membre **lpProps** . 
    
**cValues**
  
> Nombre de valeurs de propriété désignés par **lpProps**. 
    
**lpProps**
  
> Pointeur vers un tableau de structures [SPropValue](spropvalue.md) qui décrivent les valeurs de propriété pour les colonnes de la ligne. 
    
## <a name="remarks"></a>Remarques

Une structure **SRow** décrit une ligne dans une table. Il est inclus dans la structure [TABLE_NOTIFICATION](table_notification.md) qui accompagne une notification de la table. 
  
Structures **SRow** sont utilisés dans les méthodes suivantes : 
  
- [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
    
- [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [ITableData : IUnknown](itabledataiunknown.md) (de nombreuses méthodes) 
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Lorsque plusieurs lignes doit être indiqué, une structure [SRowSet](srowset.md) est utilisée. Une structure **SRowSet** contient un tableau de structures **SRow** et le nombre de structures dans le tableau. 
  
L’illustration suivante montre la relation entre un **SRow** et une structure de données **SRowSet** . 
  
**Relation entre SRow et SRowSet**
  
![Relation entre SRow et SRowSet] (media/amapi_17.gif "Relation entre SRow et SRowSet")
  
Structures **SRow** sont définies les mêmes en tant que structures [ADRENTRY](adrentry.md) . Par conséquent, une ligne d’une table de destinataires et une entrée dans une liste d’adresses peut être traité. 
  
Pour plus d’informations sur comment d’allouer de la mémoire pour les structures **SRow** , voir [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Voir aussi

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [Structures MAPI](mapi-structures.md)
- [Gestion de la mémoire pour les structures ADRLIST et SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

