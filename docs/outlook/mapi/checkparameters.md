---
title: CheckParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2161c68517e2f83e2f2388cf209d464116cac454
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567759"
---
# <a name="checkparameters"></a>CheckParameters

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Appelle une fonction interne pour valider les paramètres de débogage sur les méthodes de fournisseur de services appelées par MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
HRESULT CheckParameters(
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

La macro **CheckParameters** a été recalée par la macro [CheckParms.](checkparms.md) **CheckParms est** recommandé sur toutes les plateformes. 
  

