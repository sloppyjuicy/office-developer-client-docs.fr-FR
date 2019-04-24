---
title: IXPLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 261d5f7c-bb61-4e1d-aa41-cca224c63f8e
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: d9e09de1064a0ae034bb3618f0e5b3719a82c163
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356027"
---
# <a name="ixplogonopenstatusentry"></a>IXPLogon::OpenStatusEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre l'objet d'État du fournisseur de transport.
  
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
  
> dans Pointeur vers un identificateur d'interface (IID) pour l'objet de connexion de transport. Le passage de NULL renvoie l'interface [IMAPIStatus](imapistatusimapiprop.md) . Le paramètre _lpInterface_ peut également être défini sur un identificateur pour une interface pour l'objet. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'objet d'État. L'indicateur suivant peut être défini:
    
MAPI_MODIFY 
  
> Demande une autorisation en lecture/écriture. L'interface par défaut est en lecture seule. 
    
 _lpulObjType_
  
> remarquer Pointeur vers le type de l'objet ouvert.
    
 _lppEntry_
  
> remarquer Pointeur vers le pointeur vers l'objet d'état ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPLogon:: OpenStatusEntry** lorsqu'une application cliente appelle une méthode **OpenEntry** pour l'identificateur d'entrée dans la ligne de la table d'État du fournisseur de transport. **OpenStatusEntry** ouvre un objet avec l'interface **IMAPIStatus** associée à cette ouverture de session de fournisseur de transport particulier. Cet objet est ensuite utilisé pour permettre aux applications clientes d'appeler des méthodes **IMAPIStatus** (par exemple, pour reconfigurer la session de connexion à l'aide de la méthode [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) , ou pour valider l'état de la session de connexion à l'aide du [ IMAPIStatus:: ValidateState](imapistatus-validatestate.md) , méthode). 
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

