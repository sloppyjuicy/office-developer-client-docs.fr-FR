---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1082e3680ed9a53894c5fd810be91b42eac22cee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596455"
---
# <a name="iablogonopenstatusentry"></a>IABLogon::OpenStatusEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre l’objet d’état du fournisseur.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a>Paramètres

 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface qui doit être utilisée pour accéder à l’objet d’état. La transmission null renvoie l’interface standard de l’objet, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet d’état est ouvert. L’indicateur suivant peut être définie :
    
MAPI_MODIFY 
  
> Demande une autorisation de lecture/écriture. Par défaut, les objets sont ouverts avec un accès en lecture seule et les appelants ne doivent pas supposer que l’autorisation lecture/écriture a été accordée.
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppEntry_
  
> [out] Pointeur vers un pointeur vers l’objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et l’objet d’état a été ouvert.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de carnets d’adresses **implémentent la méthode OpenStatusEntry** pour accorder l’accès à leur objet d’état. Tous les fournisseurs de carnet d’adresses sont requis pour implémenter un objet d’état qui prend en charge, au minimum, la méthode [IMAPIStatus::ValidateState.](imapistatus-validatestate.md) Pour plus d’informations, voir [Status Object Implementation](status-object-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

