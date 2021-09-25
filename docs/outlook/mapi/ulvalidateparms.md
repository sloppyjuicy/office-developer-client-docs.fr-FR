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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d111c6a0e51f3487014a411b6b7ebf4e3d588744
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578416"
---
# <a name="ulvalidateparms"></a>UlValidateParms

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Appelle une fonction interne pour vérifier les paramètres que les applications clientes ont transmis aux fournisseurs de services et MAPI. 
  
|||
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

Les paramètres transmis entre MAPI et les fournisseurs de services sont supposés corrects et ne subissent une validation de débogage qu’avec la macro [CheckParms.](checkparms.md) Les fournisseurs doivent vérifier tous les paramètres transmis par les applications clientes, mais les clients doivent supposer que les paramètres MAPI et fournisseur sont corrects. Utilisez la macro **HR_FAILED** pour tester les valeurs de retour. 
  
La macro **UlValidateParms est** appelée différemment selon que le code appelant est C ou C++. Cette macro est utilisée pour valider les paramètres des quelques méthodes **IUnknown** et MAPI qui retournent ULONG au lieu de valeurs HRESULT ; La macro [ValidateParms fonctionne](validateparms.md) pour tous les autres. 
  

