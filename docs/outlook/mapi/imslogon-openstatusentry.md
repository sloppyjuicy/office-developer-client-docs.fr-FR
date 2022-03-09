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
ms.openlocfilehash: 4c06df6eb5d2e3917a1347996b42fa7399178dcc
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372555"
---
# <a name="imslogonopenstatusentry"></a>IMSLogon::OpenStatusEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un objet d’état.
  
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
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’objet d’état à ouvrir. La transmission de la valeur NULL indique que l’interface standard de l’objet est renvoyée (dans ce cas, l’interface [IMAPIStatus](imapistatusimapiprop.md) ). Le  _paramètre lpInterface peut_ également être définie sur un identificateur pour une interface appropriée pour l’objet. 
    
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

Les fournisseurs de magasins de messages implémentent **la méthode IMSLogon::OpenStatusEntry** pour ouvrir un objet d’état. Cet objet d’état est ensuite utilisé pour permettre aux clients d’appeler des [méthodes IMAPIStatus](imapistatusimapiprop.md) . Par exemple, les clients peuvent utiliser la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) pour reconfigurer la session d’ouverture de session de la boutique de messages ou la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) pour valider l’état de la session d’ouverture de session de la boutique de messages. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

