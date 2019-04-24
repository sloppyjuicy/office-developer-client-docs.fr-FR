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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 0b6837b51b09ecd9a60630c613e1806cb10c1d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321209"
---
# <a name="imapiofflinesetcurrentstate"></a>IMAPIOffline::SetCurrentState

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit l'état actuel d'un objet hors connexion sur en ligne ou hors connexion.
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Modifie le comportement de cet appel. Les valeurs prises en charge sont les suivantes :
    
MAPIOFFLINE_FLAG_BLOCK
  
> Le fait de définir _ulFlags_ sur cette valeur bloque l'appel **SetCurrentState** jusqu'à ce que le changement d'État soit terminé. Par défaut, la transition a lieu de manière asynchrone. Lorsque la transition se produit de manière asynchrone, tous les appels **SetCurrentState** renvoient **E_PENDING** jusqu'à la fin de la modification. 
    
MAPIOFFLINE_FLAG_DEFAULT
  
> Définit l'état actuel sans blocage.
    
 _ulMask_
  
> dans Partie de l'État à modifier. La seule valeur prise en charge est MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulState_
  
> dans État à modifier. Il doit s'agir de l'une des deux valeurs suivantes:
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
 _Disparition_
  
> Ce paramètre est réservé à un usage interne d'Outlook et n'est pas pris en charge. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'état de l'objet hors connexion a été modifié.
    
E_PENDING
  
> Cela indique que l'état de l'objet hors connexion est modifié de manière asynchrone. Cela se produit lorsque _ulFlags_ est défini sur MAPIOFFLINE_FLAG_BLOCK dans un appel de **SetCurrentState** précédent et que tout appel ultérieur de **SetCurrentState** renverra cette valeur jusqu'à ce que le changement d'état asynchrone soit terminé. 
    
## <a name="see-also"></a>Voir aussi



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)


[Constantes MAPI](mapi-constants.md)

