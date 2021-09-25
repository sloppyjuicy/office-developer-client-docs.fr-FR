---
title: CheckParms
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2c7fc3875abc26e642b6ae1e5bf4c96c3c017aad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556860"
---
# <a name="checkparms"></a>CheckParms

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Appelle une fonction interne pour valider les paramètres de débogage sur les méthodes de fournisseur de services appelées par MAPI. 
  
|||
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
  
> [in] Spécifie, par l’éumération, la méthode à valider. 
    
 _First_
  
> [in] Pointeur vers le premier argument de la pile.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi.
    
## <a name="remarks"></a>Remarques

Contrairement aux [macros ValidateParms](validateparms.md) et [UlValidateParms,](ulvalidateparms.md) la macro **CheckParms** n’effectue pas de validation de paramètre complète. Les paramètres transmis entre MAPI et les fournisseurs de services sont supposés être corrects, de sorte que **CheckParms** effectue une validation de débogage uniquement. 
  

