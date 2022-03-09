---
title: IMAPIOfflineSetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOffline.SetCurrentState
api_type:
- COM
ms.assetid: c0aa0df2-79f9-2558-7eb6-accae9bef4b2
ms.openlocfilehash: 3cf4584fe223d45ed30bb5a4303efe9806504227
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374704"
---
# <a name="imapiofflinesetcurrentstate"></a>IMAPIOffline::SetCurrentState

**S’applique à** : Outlook 2013 | Outlook 2016
  
Définit l’état actuel d’un objet hors connexion sur en ligne ou hors connexion.
  
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
  
> [in] Modifie le comportement de cet appel. Les valeurs prises en charge sont les suivantes :

MAPIOFFLINE_FLAG_BLOCK
  
> Si _vous définissez ulFlags_ sur cette valeur, l’appel **SetCurrentState** est bloqué jusqu’à ce que le changement d’état soit terminé. Par défaut, la transition a lieu de manière asynchrone. Lorsque la transition se produit de manière asynchrone, tous les appels **SetCurrentState** sont **E_PENDING jusqu’à** ce que la modification soit terminée.

MAPIOFFLINE_FLAG_DEFAULT
  
> Définit l’état actuel sans blocage.

 _ulMask_
  
> [in] Partie de l’état à modifier. La seule valeur prise en charge est MAPIOFFLINE_STATE_OFFLINE_MASK.

 _ulState_
  
> [in] État à modifier. Elle doit être l’une des deux valeurs ci-après :

MAPIOFFLINE_STATE_ONLINE
  
>

MAPIOFFLINE_STATE_OFFLINE
  
>

 _pReserved_
  
> Ce paramètre est réservé à un Outlook interne et n’est pas pris en charge.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L’état de l’objet hors connexion a été modifié avec succès.

E_PENDING
  
> Cela indique que l’état de l’objet hors connexion change de manière asynchrone. Cela se produit lorsque _ulFlags_ est définie sur MAPIOFFLINE_FLAG_BLOCK dans un appel **SetCurrentState** précédent et que tout appel **SetCurrentState** ultérieur retourne cette valeur jusqu’à ce que la modification de l’état asynchrone soit terminée.

## <a name="see-also"></a>Voir aussi

[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)  
[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
 [Constantes MAPI](mapi-constants.md)
