---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: acb42aa4fedf0cdd006553cbeb9a5a5be96f61b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620673"
---
# <a name="imslogonopenstatusentry"></a>IMSLogon::OpenStatusEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un objet status.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a>Paramètres

 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’objet d’état à ouvrir. La transmission null indique que l’interface standard de l’objet est renvoyée (dans ce cas, l’interface [IMAPIStatus).](imapistatusimapiprop.md) Le  _paramètre lpInterface_ peut également être définie sur un identificateur pour une interface appropriée pour l’objet. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet d’état est ouvert. L’indicateur suivant peut être définie :
    
MAPI_MODIFY 
  
> Demande une autorisation de lecture/écriture. Par défaut, les objets sont créés avec une autorisation en lecture seule et les applications clientes ne doivent pas fonctionner sur l’hypothèse que l’autorisation lecture/écriture a été accordée. 
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppEntry_
  
> [out] Pointeur vers le pointeur vers l’objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de magasins de messages implémentent la méthode **IMSLogon::OpenStatusEntry** pour ouvrir un objet d’état. Cet objet d’état est ensuite utilisé pour permettre aux clients d’appeler des [méthodes IMAPIStatus.](imapistatusimapiprop.md) Par exemple, les clients peuvent utiliser la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) pour reconfigurer la session d’ouverture de session de la boutique de messages ou la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) pour valider l’état de la session d’ouverture de session de la boutique de messages. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

