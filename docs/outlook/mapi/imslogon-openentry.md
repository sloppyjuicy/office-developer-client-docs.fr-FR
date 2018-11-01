---
title: IMSLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenEntry
api_type:
- COM
ms.assetid: 612cbab7-60cb-48bb-906e-18d9135e7a86
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 619357a608dd160cbe4811cc7db7ae3b392db858
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576889"
---
# <a name="imslogonopenentry"></a>IMSLogon::OpenEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un dossier ou un objet de message et retourne un pointeur vers l’objet pour fournir un accès plus. 
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulOpenFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> [in] La taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’adresse de l’identificateur d’entrée de l’objet de dossier ou un message à ouvrir. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’objet. Valeur null indique que l’objet est convertie à l’interface standard pour ce type d’objet. Le paramètre _lpInterface_ peut également être défini à un identificateur pour une interface appropriée pour l’objet. 
    
 _ulOpenFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert. Les indicateurs suivants peuvent être définis :
    
MAPI_BEST_ACCESS 
  
> L’objet doit être ouvert avec les autorisations maximales autorisées pour l’utilisateur et les autorisations d’application client maximale. Par exemple, si le client a l’autorisation de lecture/écriture, l’objet est ouvert avec l’autorisation de lecture/écriture ; Si le client dispose des autorisations en lecture seule, l’objet est ouvert avec l’autorisation en lecture seule. Le client peut extraire le niveau d’autorisation en obtenant la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_DEFERRED_ERRORS 
  
> L’appel est autorisé à fonctionne même si l’objet sous-jacent n’est pas disponible pour l’application appelante. Si l’objet n’est pas disponible, un appel à l’objet suivant renverra une erreur.
    
N' 
  
> Demandes d’autorisation de lecture/écriture. Par défaut, les objets sont créés avec l’autorisation en lecture seule, et les clients ne doivent pas fonctionner en supposant que bénéficie des autorisations en lecture/écriture. 
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppUnk_
  
> [out] Pointeur vers le pointeur vers l’objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

MAPI appelle la méthode **IMSLogon::OpenEntry** pour ouvrir un dossier ou un message dans une banque de messages. MAPI transmet l’identificateur d’entrée de l’objet à ouvrir. Le fournisseur de banque de message doit retourner un pointeur qui permet l’accès à l’objet spécifié dans le paramètre _lppUnk_ . 
  
Avant que les appels MAPI **IMSLogon::OpenEntry**, il détermine d’abord que le message donné ou l’identificateur d’entrée de dossier correspond à une enregistré par ce fournisseur de banque de messages. Pour plus d’informations sur comment enregistrent des fournisseurs de magasins d’identificateurs d’entrée, voir [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
  
 **IMSLogon::OpenEntry** est identique à la méthode [IMsgStore::OpenEntry](imsgstore-openentry.md) de l’objet store de message, sauf que le client n’appelle pas **IMSLogon::OpenEntry**; Les appels MAPI **IMSLogon::OpenEntry** lorsqu’il traite une méthode **IMAPISession::OpenEntry** . Objets ouverts à l’aide de **IMSLogon::OpenEntry** doivent être traités exactement comme objets ouverts en utilisant le message stockent l’objet ; en particulier, objets ouverts à l’aide de cet appel doivent être invalidés lors de l’objet de banque de messages. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

