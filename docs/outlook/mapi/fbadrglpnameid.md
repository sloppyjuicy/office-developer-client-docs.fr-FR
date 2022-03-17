---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: Valide un tableau de structures qui décrivent les propriétés nommées et vérifie leur allocation.
ms.openlocfilehash: 84d03b7c0d05de445c5fdd9123817d66b2232502
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63519894"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

**S’applique à** : Outlook 2013 | Outlook 2016
  
Valide un tableau de structures qui décrivent les propriétés nommées et vérifie leur allocation.
  
|**Propriété**|**Valeur**|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |

```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a>Paramètres

 _lppNameId_
  
> [in] Pointeur vers un tableau de structures [MAPINAMEID](mapinameid.md) décrivant les propriétés nommées.

 _cNames_
  
> [in] Nombre de structures de propriétés nommées dans le tableau pointés par _le paramètre lppNameId_ .

## <a name="return-value"></a>Valeur renvoyée

TRUE
  
> Une ou plusieurs des structures de noms de propriété spécifiées ne sont pas valides.

FALSE
  
> Les structures de noms de propriété spécifiées sont toutes valides.

## <a name="remarks"></a>Remarques

La **fonction FBadRglpNameID** peut être utilisée lors de la configuration d’un appel à [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) ou [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).
  