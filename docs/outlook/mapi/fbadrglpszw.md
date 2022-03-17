---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: Valide toutes les chaînes d’un tableau de chaînes Unicode.
ms.openlocfilehash: 43b85f3d15b5409e22dd2f64d2d59aaf560fdf93
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63519985"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

**S’applique à** : Outlook 2013 | Outlook 2016
  
Valide toutes les chaînes d’un tableau de chaînes Unicode.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |

```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a>Paramètres

 _lppszW_
  
> [in] Pointeur vers un tableau de chaînes Unicode terminées par null.

 _cStrings_
  
> [in] Nombre de chaînes dans le tableau pointées par _le paramètre lppszW_ .

## <a name="return-value"></a>Valeur renvoyée

TRUE
  
> Une ou plusieurs des chaînes du tableau spécifié ne sont pas valides.

FALSE
  
> Les chaînes du tableau spécifié sont valides.
