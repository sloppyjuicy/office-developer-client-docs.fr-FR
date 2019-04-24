---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b3862ea539907bb0570a0e845b09a15e7bed0507
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329567"
---
# <a name="validateparameters"></a>ValidateParameters

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Appelle une fonction interne pour vérifier les paramètres que les applications clientes ont transmises aux fournisseurs de services. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Paramètres

 _eMethod_
  
> dans Spécifie, par énumération, la méthode à valider. 
    
 _First_
  
> dans Pointeur vers le premier argument de la pile.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Tous les paramètres sont valides. 
    
MAPI_E_CALL_FAILED 
  
> Un ou plusieurs paramètres ne sont pas valides.
    
## <a name="remarks"></a>Remarques

La macro **ValidateParameters** a été remplacée par la macro [ValidateParms](validateparms.md) . **ValidateParameters** ne fonctionne pas correctement sur les plateformes RISC et ne peut plus être compilé sur ces plateformes. Il se compile et fonctionne correctement sur les plateformes Intel, mais **ValidateParms** est recommandé sur toutes les plateformes. 
  

