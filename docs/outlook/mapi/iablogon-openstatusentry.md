---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cb9a2ba72ee9fd9c45aefe9d0797930a4871404a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579283"
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
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface qui doit être utilisé pour accéder à l’objet d’état. Passage de NULL renvoie l’interface standard de l’objet, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet d’état est ouvert. Vous pouvez définir l’indicateur suivant :
    
N' 
  
> Demandes d’autorisation de lecture/écriture. Par défaut, les objets sont ouverts avec accès en lecture seule, et les appelants ne doivent pas supposer bénéficie des autorisations en lecture/écriture.
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppEntry_
  
> [out] Pointeur vers un pointeur vers l’objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et que l’objet de l’état a été ouvert.
    
## <a name="remarks"></a>Remarques

Fournisseurs de carnet d’adresses implémentent la méthode **OpenStatusEntry** pour accorder l’accès à l’objet d’état. Tous les fournisseurs de carnet d’adresses sont requis pour implémenter un objet état qui prend en charge, au minimum, la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . Pour plus d’informations, voir [Implémentation d’objet état](status-object-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

