---
title: GUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.GUID
api_type:
- COM
ms.assetid: e3608c47-06be-4476-a6ef-060fac252387
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8be044edc628143bc7f7a4a33caa1046f0a3e5e3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561739"
---
# <a name="guid"></a>GUID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un identificateur global unique (GUID). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiguid.h  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a>Members

 **Data1**
  
> Valeur de données long et non signée.
    
 **Data2**
  
> Valeur de données d’unteger court non signé.
    
 **Data3**
  
> Valeur de données d’unteger court non signé.
    
 **Data4**
  
> Tableau de caractères non signés.
    
## <a name="remarks"></a>Remarques

 **Les** structures GUID sont utilisées dans MAPI comme suit : 
  
- Dans les structures [MAPIUID](mapiuid.md) qui identifient de manière unique les fournisseurs de services. 
    
- Pour les identificateurs d’interface.
    
- Dans le jeu de propriétés, les noms des propriétés nommées. 
    
Les fournisseurs de magasins de messages et de carnets d’adresses génèrent une structure **GUID** à utiliser dans leur structure **MAPIUID.** En passant le **MAPIUID** résultant à [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), ces fournisseurs de services informent MAPI de leur identificateur unique.
  
En outre, ils sont utilisés dans l’implémentation de Microsoft Remote Procedure Call (RPC) et de l’ODL (Object Description Language). Pour plus d’informations sur ces utilisations, voir le Guide du programmeur  *Microsoft RPC* et la référence, *OLE Programmer’s Reference*  et Inside  *OLE*, *Second Edition*  . 
  
La structure **GUID** est définie dans le Guide de référence du *programmeur Win32.* Des valeurs spécifiques **pour les** structures GUID utilisées dans MAPI sont définies dans le fichier d’en-tête MAPI Mapiguid.h. 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)


[Structures MAPI](mapi-structures.md)

