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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a471b66709d2109bfd3894eed80168ea1b8d5140
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571555"
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
  
> [in] Pointeur vers un identificateur d’interface (IID) pour l’objet d’identification de transport. La transmission null renvoie [l’interface IMAPIStatus.](imapistatusimapiprop.md) Le  _paramètre lpInterface peut_ également être définie sur un identificateur pour une interface pour l’objet. 
    
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

Lepooler MAPI appelle la méthode **IXPLogon::OpenStatusEntry** lorsqu’une application cliente appelle une méthode **OpenEntry** pour l’identificateur d’entrée dans la ligne de table d’état du fournisseur de transport. **OpenStatusEntry ouvre** un objet avec l’interface **IMAPIStatus** associée à ce fournisseur de transport particulier. Cet objet est ensuite utilisé pour permettre aux applications clientes d’appeler des méthodes **IMAPIStatus** (par exemple, pour reconfigurer la session d’ouverture de session à l’aide de la méthode [IMAPIStatus::SettingsDialog,](imapistatus-settingsdialog.md) ou pour valider l’état de la session d’ouverture de session à l’aide de la méthode [IMAPIStatus::ValidateState).](imapistatus-validatestate.md) 
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

