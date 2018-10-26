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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7cb77308ebc7229adcab290fc8e1f9e11ce45065
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587018"
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
  
> [in] Pointeur vers un identificateur d’interface (IID) de l’objet d’ouverture de session de transport. Passage de NULL renvoie l’interface [IMAPIStatus](imapistatusimapiprop.md) . Le paramètre _lpInterface_ peut également avoir un identificateur pour une interface pour l’objet. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet d’état est ouvert. Vous pouvez définir l’indicateur suivant :
    
N' 
  
> Demandes d’autorisation de lecture/écriture. L’interface par défaut est en lecture seule. 
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppEntry_
  
> [out] Pointeur vers le pointeur vers l’objet de l’état ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPLogon::OpenStatusEntry** lorsqu’une application cliente appelle une méthode **OpenEntry** pour l’identificateur d’entrée dans la ligne de tableau de statut du fournisseur de transport. **OpenStatusEntry** ouvre un objet avec l’interface **IMAPIStatus** associé à cette connexion au fournisseur du transport particulier. Cet objet est ensuite utilisé pour permettre aux applications clientes d’appeler des méthodes **IMAPIStatus** (par exemple, pour reconfigurer l’ouverture de session à l’aide de la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) ou pour valider l’état de l’ouverture de session à l’aide de la [ IMAPIStatus::ValidateState](imapistatus-validatestate.md) méthode). 
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

