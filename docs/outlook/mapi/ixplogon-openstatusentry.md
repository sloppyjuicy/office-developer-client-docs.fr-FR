---
title: IXPLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 261d5f7c-bb61-4e1d-aa41-cca224c63f8e
ms.openlocfilehash: 3f37e2d3b5580e7375ea1248d11b52a31f29e2c3
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376216"
---
# <a name="ixplogonopenstatusentry"></a>IXPLogon::OpenStatusEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre l’objet d’état du fournisseur de transport.
  
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
  
> [in] Pointeur vers un identificateur d’interface (IID) pour l’objet d’identification de transport. La transmission null renvoie [l’interface IMAPIStatus](imapistatusimapiprop.md) . Le  _paramètre lpInterface_ peut également être définie sur un identificateur pour une interface pour l’objet. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet d’état est ouvert. L’indicateur suivant peut être définie :
    
MAPI_MODIFY 
  
> Demande une autorisation de lecture/écriture. L’interface par défaut est en lecture seule. 
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppEntry_
  
> [out] Pointeur vers le pointeur vers l’objet d’état ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Lepooler MAPI appelle la méthode **IXPLogon::OpenStatusEntry** lorsqu’une application cliente appelle une méthode **OpenEntry** pour l’identificateur d’entrée dans la ligne de table d’état du fournisseur de transport. **OpenStatusEntry ouvre** un objet avec l’interface **IMAPIStatus** associée à ce fournisseur de transport particulier. Cet objet est ensuite utilisé pour permettre aux applications clientes d’appeler des méthodes **IMAPIStatus** (par exemple, pour reconfigurer la session d’ouverture de session à l’aide de la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) , ou pour valider l’état de la session d’ouverture de session à l’aide de la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) ). 
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

