---
title: CheckParms
description: CheckParms appelle une fonction interne pour valider les paramètres de débogage sur les méthodes de fournisseur de services appelées par MAPI.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
ms.openlocfilehash: 8a8fd55abff39b944d163bf481dbdd0fb076db53
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817570"
---
# <a name="checkparms"></a>CheckParms

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Appelle une fonction interne pour valider les paramètres de débogage sur les méthodes de fournisseur de services appelées par MAPI. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Paramètres

 _eMethod_
  
> [in] Spécifie, par énumération, la méthode à valider. 
    
 _First_
  
> [in] Pointeur vers le premier argument de la pile.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi.
    
## <a name="remarks"></a>Remarques

Contrairement aux [macros ValidateParms](validateparms.md) et [UlValidateParms](ulvalidateparms.md) , la macro **CheckParms** n’effectue pas de validation de paramètre complète. Les paramètres passés entre MAPI et les fournisseurs de services étant supposés corrects, **CheckParms** effectue une validation de débogage uniquement. 
  

