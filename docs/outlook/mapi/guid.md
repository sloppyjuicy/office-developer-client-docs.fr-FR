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
description: Décrit un identificateur global unique (GUID). Les fournisseurs de magasins de messages et de carnets d’adresses génèrent un GUID à utiliser dans leur structure MAPIUID.
ms.openlocfilehash: f2fd8b9ab69a1ff1972a7a91c0c7cc2c4292de0d
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763389"
---
# <a name="guid"></a>GUID

**S’applique à** : Outlook 2013 | Outlook 2016
  
Décrit un identificateur global unique (GUID).
  
|Propriété |Valeur |
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

 **Les structures GUID** sont utilisées dans MAPI comme suit :
  
- Dans les structures [MAPIUID](mapiuid.md) qui identifient de manière unique les fournisseurs de services.

- Pour les identificateurs d’interface.

- Dans le jeu de propriétés, les noms des propriétés nommées.

Les fournisseurs de magasins de messages et de carnets d’adresses génèrent une structure **GUID** à utiliser dans leur structure **MAPIUID** . En passant le **MAPIUID** résultant à [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), ces fournisseurs de services informent MAPI de leur identificateur unique.
  
Ils sont également utilisés dans l’implémentation de l’appel de procédure distante Microsoft (RPC) et du langage ODL (Object Description Language). Pour plus d’informations sur ces utilisations, voir guide et référence du programmeur  *Microsoft RPC*, *OLE Programmer’s Reference* et  *Inside OLE*, *Second Edition*.

La structure **GUID** est définie dans le Guide de référence du *programmeur Win32*. Des valeurs spécifiques pour **les structures GUID** utilisées dans MAPI sont définies dans le fichier d’en-tête MAPI Mapiguid.h.
  
## <a name="see-also"></a>Voir aussi

[MAPIUID](mapiuid.md)
 [Structures MAPI](mapi-structures.md)
