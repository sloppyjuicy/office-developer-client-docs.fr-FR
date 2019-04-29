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
ms.openlocfilehash: 63cef6ef2bb26e8b723c60fe01dd6771aa070ae8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407255"
---
# <a name="srowset"></a>SRowSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [SRow](srow.md) . Chaque structure **SRow** décrit une ligne d'une table. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macros connexes:  <br/> |[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md) <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a>Members

 **Pattes**
  
> Nombre de structures **SRow** dans le membre **aRow** . 
    
 **aRow**
  
> Tableau de structures **SRow** . Il existe une structure pour chaque ligne dans le tableau. 
    
## <a name="remarks"></a>Remarques

Une structure **SRowSet** est utilisée pour décrire plusieurs lignes de données d'un tableau. Les structures **SRowSet** sont utilisées dans les méthodes d'interface [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md)et [IMAPITable](imapitableiunknown.md) , en plus des fonctions suivantes: 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 Les structures **SRowSet** sont définies de la même façon que les structures [ADRLIST](adrlist.md) pour permettre aux lignes d'une table de destinataires et aux entrées d'une liste d'adresses d'être traitées de la même manière. Les structures **SRowSet** et **ADRLIST** peuvent être transmises à des méthodes telles que [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) et [IAddrBook:: Address](iaddrbook-address.md). 
  
En outre, les règles d'allocation de mémoire pour les structures **SRowSet** sont les mêmes que pour les structures **ADRLIST** . Pour résumer, chaque structure [SPropValue](spropvalue.md) dans le tableau vers lequel pointe le membre **lpProps** de chaque ligne du jeu de lignes doit être allouée séparément à l'aide de [MAPIAllocateBuffer](mapiallocatebuffer.md). Chaque structure de valeur de propriété doit également être désallouée à l'aide de [MAPIFreeBuffer](mapifreebuffer.md) avant la désaffectation de sa structure **SRowSet** afin que les pointeurs vers les structures **SPropValue** allouées ne soient pas perdues. La mémoire allouée d'une ligne peut ensuite être conservée et réutilisée en dehors du contexte de la structure **SRowSet** . 
  
Pour plus d'informations sur la façon dont la mémoire des structures **SRowSet** doit être allouée, consultez la rubrique [Managing Memory for ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Voir aussi



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Structures MAPI](mapi-structures.md)

