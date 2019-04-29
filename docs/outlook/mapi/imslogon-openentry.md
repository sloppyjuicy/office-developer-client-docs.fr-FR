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
ms.openlocfilehash: 544aaaace18a9d26972e6484803b63a1ee7060fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416299"
---
# <a name="imslogonopenentry"></a>IMSLogon::OpenEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un objet Folder ou message et renvoie un pointeur vers l'objet pour fournir un accès supplémentaire. 
  
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
  
> dans Taille, en octets, de l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'adresse de l'identificateur d'entrée du dossier ou de l'objet de message à ouvrir. 
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) de l'objet. La transmission de la valeur NULL indique que l'objet est casté en interface standard pour ce type d'objet. Le paramètre _lpInterface_ peut également être défini sur un identificateur pour une interface appropriée pour l'objet. 
    
 _ulOpenFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'objet. Les indicateurs suivants peuvent être définis:
    
MAPI_BEST_ACCESS 
  
> L'objet doit être ouvert avec les autorisations maximales accordées à l'utilisateur et les autorisations d'application client maximales. Par exemple, si le client dispose d'une autorisation en lecture/écriture, l'objet est ouvert avec une autorisation en lecture/écriture; Si le client dispose d'une autorisation en lecture seule, l'objet est ouvert en lecture seule. Le client peut récupérer le niveau d'autorisation en obtenant la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_DEFERRED_ERRORS 
  
> L'appel est autorisé même si l'objet sous-jacent n'est pas disponible pour l'application appelante. Si l'objet n'est pas disponible, un appel ultérieur à l'objet peut renvoyer une erreur.
    
MAPI_MODIFY 
  
> Demande une autorisation en lecture/écriture. Par défaut, les objets sont créés avec l'autorisation lecture seule, et les clients ne doivent pas travailler en supposant que l'autorisation de lecture/écriture a été octroyée. 
    
 _lpulObjType_
  
> remarquer Pointeur vers le type de l'objet ouvert.
    
 _lppUnk_
  
> remarquer Pointeur vers le pointeur vers l'objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

MAPI appelle la méthode **IMSLogon:: OpenEntry** pour ouvrir un dossier ou un message dans une banque de messages. MAPI transmet l'identificateur d'entrée de l'objet à ouvrir. Le fournisseur de banque de messages doit renvoyer un pointeur qui permet un accès supplémentaire à l'objet spécifié dans le paramètre _lppUnk_ . 
  
Avant que MAPI appelle **IMSLogon:: OpenEntry**, il détermine d'abord que l'identificateur d'entrée de dossier ou de message donné correspond à l'un des éléments inscrits par ce fournisseur de banque de messages. Pour plus d'informations sur la façon dont les fournisseurs de magasins inscrivent les identificateurs d'entrée, voir [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md).
  
 **IMSLogon:: OpenEntry** est identique à la méthode [IMsgStore:: OpenEntry](imsgstore-openentry.md) de l'objet de banque de messages, sauf que le client n'appelle pas **IMSLogon:: OpenEntry**; MAPI appelle **IMSLogon:: OpenEntry** lorsqu'il traite une méthode **IMAPISession:: OpenEntry** . Les objets ouverts à l'aide de **IMSLogon:: OpenEntry** doivent être traités exactement de la même façon que les objets ouverts à l'aide de l'objet de banque de messages; en particulier, les objets ouverts à l'aide de cet appel doivent être invalidés lors de la publication de l'objet de banque de messages. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

