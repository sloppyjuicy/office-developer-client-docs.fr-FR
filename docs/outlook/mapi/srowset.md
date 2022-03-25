---
title: SRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SRowSet
api_type:
- COM
ms.assetid: 7e3761be-afd6-46cb-9a08-25e9016c1241
description: Contient un tableau de structures SRow. Chaque structure SRow décrit une ligne d’un tableau.
ms.openlocfilehash: a1453e86ba831cd9ca7a04ded65c4eb1168f6eb9
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405383"
---
# <a name="srowset"></a>SRowSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [SRow](srow.md) . Chaque **structure SRow** décrit une ligne d’un tableau. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros associées :  <br/> |[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md) <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a>Members

 **cRows**
  
> Nombre de structures **SRow** dans le **membre aRow** . 
    
 **aRow**
  
> Tableau de structures **SRow** . Il existe une structure pour chaque ligne du tableau. 
    
## <a name="remarks"></a>Remarques

Une **structure SRowSet** est utilisée pour décrire plusieurs lignes de données à partir d’une table. **Les structures SRowSet** sont utilisées dans les méthodes d’interface [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md) et [IMAPITable](imapitableiunknown.md) , en plus des fonctions suivantes : 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 **Les structures SRowSet** sont définies de la même manière que les structures [ADRLIST](adrlist.md) pour que les lignes d’une table de destinataires et les entrées d’une liste d’adresses soient traitées de la même manière. Les structures **SRowSet** et **ADRLIST** peuvent être transmises à des méthodes telles que [IMessage::ModifyRecipients](imessage-modifyrecipients.md) et [IAddrBook::Address](iaddrbook-address.md). 
  
En outre, les règles d’allocation de mémoire pour les structures **SRowSet** sont les mêmes que pour les structures **ADRLIST** . Pour résumer, chaque structure [SPropValue](spropvalue.md) du tableau pointée par le membre **lpProps** de chaque ligne du jeu de lignes doit être allouée séparément à l’aide de [MAPIAllocateBuffer](mapiallocatebuffer.md). Chaque structure de valeur de propriété doit également être désattribuée à l’aide de [MAPIFreeBuffer](mapifreebuffer.md) avant la désallocation de sa structure **SRowSet** afin que les pointeurs vers les structures **SPropValue** allouées ne soient pas perdus. La mémoire allouée d’une ligne peut ensuite être conservée et réutilisée en dehors du contexte de la structure **SRowSet** . 
  
Pour plus d’informations sur la façon dont la mémoire des structures **SRowSet** doit être allouée, voir [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Voir aussi



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Structures MAPI](mapi-structures.md)

