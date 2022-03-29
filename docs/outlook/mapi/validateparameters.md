---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: Appelle une fonction interne pour vérifier les paramètres que les applications clientes ont transmis aux fournisseurs de services pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: ea9a9c84dbc89c6f040c8a5926ff9cb0c1c0550e
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64456202"
---
# <a name="validateparameters"></a>ValidateParameters

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Appelle une fonction interne pour vérifier les paramètres que les applications clientes ont transmis aux fournisseurs de services. 
  
|Propriété |Valeur |
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
  
> [in] Spécifie, par l’éumération, la méthode à valider. 
    
 _First_
  
> [in] Pointeur vers le premier argument de la pile.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Tous les paramètres sont valides. 
    
MAPI_E_CALL_FAILED 
  
> Un ou plusieurs paramètres ne sont pas valides.
    
## <a name="remarks"></a>Remarques

La macro **ValidateParameters** a été recalée par la macro [ValidateParms](validateparms.md) . **ValidateParameters ne** fonctionne pas correctement sur les plateformes RISC et n’est plus en mesure de les compiler. Il est toujours compilé et fonctionne correctement sur les plateformes Intel, mais **ValidateParms** est recommandé sur toutes les plateformes. 
  

