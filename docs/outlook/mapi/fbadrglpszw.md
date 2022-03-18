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
ms.openlocfilehash: 894ba2618458c0c0adf812aad0742972db4bad5f
ms.sourcegitcommit: 2d91bac3a93af3f1f73098f484000ba2a6377cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2022
ms.locfileid: "63558760"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

**S’applique à** : Outlook 2013 | Outlook 2016
  
Valide toutes les chaînes d’un tableau de chaînes Unicode.
  
|**Informations**|**Valeur**|
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
