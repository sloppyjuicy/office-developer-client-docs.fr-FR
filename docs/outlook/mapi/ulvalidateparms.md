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
ms.openlocfilehash: 12b1655b1e6786d2ebc985e834b635679e59f7d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787412"
---
# <a name="ulvalidateparms"></a>UlValidateParms

  
  
**S’applique à**: Outlook 
  
Appelle une fonction interne pour vérifier que les applications clientes de paramètres transmis à MAPI et les fournisseurs de services. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Paramètres

 _eMethod_
  
> [in] Spécifie, par l’énumération, la méthode à valider. 
    
 _Premier_
  
> [in] Pointeur vers le premier argument dans la pile.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur a empêché l’opération de se terminer.
    
## <a name="remarks"></a>Remarques

Paramètres passés entre MAPI et service fournisseurs sont supposés être correct et sont soumis à la validation de débogage uniquement avec la macro [CheckParms](checkparms.md) . Fournisseurs doivent vérifier tous les paramètres passés par les applications clientes, mais les clients doivent supposer que MAPI et le fournisseur de paramètres sont corrects. Utilisez la macro **HR_FAILED** pour tester les valeurs de retour. 
  
La macro **UlValidateParms** est appelée différemment selon que le code appelant est C ou C++. Cette macro est utilisée pour valider les paramètres pour les quelques méthodes **IUnknown** et MAPI qui renvoient ULONG au lieu des valeurs HRESULT ; la macro [ValidateParms](validateparms.md) fonctionne pour tous les autres. 
  

