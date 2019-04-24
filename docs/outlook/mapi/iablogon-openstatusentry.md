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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 22f98e52444b17c383737bffd1685df0fb7ba8bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349020"
---
# <a name="iablogonopenstatusentry"></a>IABLogon::OpenStatusEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre l'objet d'État du fournisseur.
  
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
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface qui doit être utilisée pour accéder à l'objet d'État. La transmission de la valeur NULL renvoie l'interface standard de l'objet, [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'objet d'État. L'indicateur suivant peut être défini:
    
MAPI_MODIFY 
  
> Demande une autorisation en lecture/écriture. Par défaut, les objets sont ouverts avec un accès en lecture seule, et les appelants ne doivent pas supposer que l'autorisation de lecture/écriture a été octroyée.
    
 _lpulObjType_
  
> remarquer Pointeur vers le type de l'objet ouvert.
    
 _lppEntry_
  
> remarquer Pointeur vers un pointeur vers l'objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et l'objet d'État a été ouvert.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de carnets d'adresses implémentent la méthode **OpenStatusEntry** pour accorder l'accès à leur objet d'État. Tous les fournisseurs de carnets d'adresses sont requis pour implémenter un objet Status qui prend en charge, au minimum, la méthode [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) . Pour plus d'informations, voir état de l' [objet](status-object-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

