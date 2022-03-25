---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: Appelle une fonction interne pour vérifier les paramètres des applications clientes qui ont été transmises aux fournisseurs de services et MAPI.
ms.openlocfilehash: 809ad4fec36f8ad55ca6431da09aa811afa3dbf6
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63781893"
---
# <a name="ulvalidateparms"></a>UlValidateParms

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Appelle une fonction interne pour vérifier les paramètres que les applications clientes ont transmis aux fournisseurs de services et MAPI. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
HRESULT UlValidateParms(
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
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur a empêché l’exécution de l’opération.
    
## <a name="remarks"></a>Remarques

Les paramètres transmis entre MAPI et les fournisseurs de services sont supposés être corrects et ne subissent une validation de débogage qu’avec la macro [CheckParms](checkparms.md) . Les fournisseurs doivent vérifier tous les paramètres transmis par les applications clientes, mais les clients doivent supposer que les paramètres MAPI et fournisseur sont corrects. Utilisez la macro **HR_FAILED** pour tester les valeurs de retour. 
  
La macro **UlValidateParms est** appelée différemment selon que le code appelant est C ou C++. Cette macro est utilisée pour valider les paramètres des quelques méthodes **IUnknown** et MAPI qui retournent ULONG au lieu de valeurs HRESULT ; La macro [ValidateParms fonctionne](validateparms.md) pour tous les autres. 
  

