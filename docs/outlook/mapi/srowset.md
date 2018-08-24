---
title: SRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRowSet
api_type:
- COM
ms.assetid: 7e3761be-afd6-46cb-9a08-25e9016c1241
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 82fa1b0af504cc4774b1dc077a6ef48378740d26
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580676"
---
# <a name="srowset"></a>SRowSet

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [SRow](srow.md) . Chaque structure **SRow** décrit une ligne d’une table. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros connexes :  <br/> |[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md) <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a>Members

 **cRows**
  
> Nombre de structures **SRow** dans le membre **: UGAL** . 
    
 **: UGAL**
  
> Tableau de structures **SRow** . Il existe une structure pour chaque ligne du tableau. 
    
## <a name="remarks"></a>Remarques

Une structure **SRowSet** est utilisée pour décrire plusieurs lignes de données d’une table. Structures **SRowSet** sont utilisés dans les méthodes d’interface [IMAPITable](imapitableiunknown.md) [IAddrBook](iaddrbookimapiprop.md)et [ITableData](itabledataiunknown.md), outre les fonctions suivantes : 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 Les structures **SRowSet** sont définis la même que celle des structures [ADRLIST](adrlist.md) pour autoriser les lignes d’une table de destinataires et les entrées dans une liste d’adresses pour être traités de la même. Les structures **SRowSet** et **ADRLIST** peuvent être transmis aux méthodes telles que [IMessage::ModifyRecipients](imessage-modifyrecipients.md) et [IAddrBook::Address](iaddrbook-address.md). 
  
En outre, les règles pour l’allocation de mémoire pour les structures **SRowSet** sont les mêmes que pour les structures **ADRLIST** . Pour résumer, chaque structure [SPropValue](spropvalue.md) dans le tableau de pointe pour définir les par le membre **lpProps** de chaque ligne dans la ligne doit être alloué séparément à l’aide de [MAPIAllocateBuffer](mapiallocatebuffer.md). Chaque structure de valeur de propriété doit également être libérée à l’aide de [MAPIFreeBuffer](mapifreebuffer.md) avant la libération de sa structure **SRowSet** afin que des pointeurs vers les structures **SPropValue** alloués ne sont pas perdues. Une ligne d’allouée mémoire peuvent être conservée puis réutilisée en dehors du contexte de la structure **SRowSet** . 
  
Pour plus d’informations sur comment d’allouer de la mémoire pour les structures **SRowSet** , voir [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Voir aussi



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Structures MAPI](mapi-structures.md)

