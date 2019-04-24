---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e0cdcb92238dd4dffbcd6514e698e5511b05bf45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360493"
---
# <a name="ulvalidateparms"></a>UlValidateParms

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Appelle une fonction interne pour vérifier les paramètres que les applications clientes ont transmises aux fournisseurs de services et MAPI. 
  
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
  
> dans Spécifie, par énumération, la méthode à valider. 
    
 _First_
  
> dans Pointeur vers le premier argument de la pile.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur a empêché l'exécution de l'opération.
    
## <a name="remarks"></a>Remarques

Les paramètres transmis entre MAPI et les fournisseurs de services sont supposés être corrects et soumis à la validation de débogage uniquement avec la macro [CheckParms](checkparms.md) . Les fournisseurs doivent vérifier tous les paramètres transmis par les applications clientes, mais les clients doivent supposer que les paramètres MAPI et de fournisseur sont corrects. Utilisez la macro **HR_FAILED** pour tester les valeurs renvoyées. 
  
La macro **UlValidateParms** est appelée différemment selon que le code appelant est C ou C++. Cette macro permet de valider les paramètres pour les méthodes **IUnknown** et MAPI qui renvoient ulong au lieu de valeurs HRESULT; la macro [ValidateParms](validateparms.md) fonctionne pour tous les autres. 
  

