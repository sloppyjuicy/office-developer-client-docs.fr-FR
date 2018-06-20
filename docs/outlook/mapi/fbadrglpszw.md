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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: da31da0ae0437e1578a681d9232b0693932b2aec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783282"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**S’applique à**: Outlook 
  
Valide toutes les chaînes dans un tableau de chaînes Unicode. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
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
    
## <a name="return-value"></a>Valeur renvoy�e

TRUE 
  
> Un ou plusieurs des chaînes dans le tableau spécifié ne sont pas valides. 
    
FALSE 
  
> Les chaînes dans le tableau spécifié sont valides.
    

