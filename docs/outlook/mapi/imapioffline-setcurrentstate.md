---
title: IMAPIOfflineSetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.SetCurrentState
api_type:
- COM
ms.assetid: c0aa0df2-79f9-2558-7eb6-accae9bef4b2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 13a4cf401cf51241a52401668eef008d65aa5459
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567138"
---
# <a name="imapiofflinesetcurrentstate"></a>IMAPIOffline::SetCurrentState

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit l’état actuel d’un objet en mode hors connexion en ligne ou hors connexion.
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Modifie le comportement de cet appel. Les valeurs prises en charge sont :
    
MAPIOFFLINE_FLAG_BLOCK
  
> Définition de _ulFlags_ sur cette valeur empêchera l’appel **SetCurrentState** jusqu'à ce que le changement d’état est terminé. Par défaut la transition s’effectue de manière asynchrone. Lors de la transition se produit de manière asynchrone, tous les appels **SetCurrentState** retournera **E_PENDING** jusqu'à ce que la modification est terminée. 
    
MAPIOFFLINE_FLAG_DEFAULT
  
> Définit l’état actuel sans blocage.
    
 _ulMask_
  
> [in] La partie de l’état à modifier. La seule valeur pris en charge est MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulState_
  
> [in] L’état à convertir. Il doit être une de ces deux valeurs :
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
 _Conservés_
  
> Ce paramètre est réservé à un usage interne Outlook et n’est pas pris en charge. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L’état de l’objet en mode hors connexion a été modifié correctement.
    
E_PENDING
  
> Cela indique que la modification de l’état de l’objet en mode hors connexion est en mode asynchrone. Cela se produit lorsque _ulFlags_ est défini sur MAPIOFFLINE_FLAG_BLOCK dans un appel **SetCurrentState** précédent, tous les appels suivants **SetCurrentState** renverra cette valeur jusqu'à ce que le changement d’état asynchrone est terminé. 
    
## <a name="see-also"></a>Voir aussi



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)


[Constantes MAPI](mapi-constants.md)

