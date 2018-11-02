---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a48d8248878c64de827bb09030073e6becba3024
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571198"
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
  
> [in] Pointeur vers l’identificateur d’interface (IID) pour l’objet d’état à ouvrir. Valeur null indique l’interface standard pour l’objet est retournée (dans ce cas, l’interface [IMAPIStatus](imapistatusimapiprop.md) ). Le paramètre _lpInterface_ peut également être défini à un identificateur pour une interface appropriée pour l’objet. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet d’état est ouvert. Vous pouvez définir l’indicateur suivant :
    
N' 
  
> Demandes d’autorisation de lecture/écriture. Par défaut, les objets sont créés avec l’autorisation en lecture seule, et les applications clientes ne doivent pas fonctionner sur l’hypothèse que bénéficie des autorisations en lecture/écriture. 
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppEntry_
  
> [out] Pointeur vers le pointeur vers l’objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Fournisseurs de magasins message implémentent la méthode **IMSLogon::OpenStatusEntry** pour ouvrir un objet d’état. Cet objet état sert ensuite pour permettre aux clients d’appeler des méthodes [IMAPIStatus](imapistatusimapiprop.md) . Par exemple, les clients peuvent utiliser la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) pour reconfigurer la session d’ouverture de session du magasin de message ou la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) pour valider l’état de la session d’ouverture de session du magasin de message. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

