---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3b3b6b5ca0b06fc55a60e035ffd9118391cab8f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565913"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide toutes les chaînes dans un tableau de chaînes Unicode. 
  
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
  
> [in] Pointeur vers un tableau de chaînes Unicode. 
    
 _cStrings_
  
> [in] Nombre de chaînes dans le tableau indiqué par le paramètre _lppszW_ . 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Un ou plusieurs des chaînes dans le tableau spécifié ne sont pas valides. 
    
FALSE 
  
> Les chaînes dans le tableau spécifié sont valides.
    

