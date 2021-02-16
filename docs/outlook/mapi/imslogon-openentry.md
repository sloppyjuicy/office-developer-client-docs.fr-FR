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
  
Ouvre un dossier ou un objet message et renvoie un pointeur vers l’objet pour fournir un accès supplémentaire. 
  
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
  
> [in] Taille, en octets, de l’identificateur d’entrée pointé par _le paramètre lpEntryID._ 
    
 _lpEntryID_
  
> [in] Pointeur vers l’adresse de l’identificateur d’entrée du dossier ou de l’objet message à ouvrir. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’objet. Le passage de null indique que l’objet est casté vers l’interface standard pour un tel objet. Le  _paramètre lpInterface peut_ également être définie sur un identificateur pour une interface appropriée pour l’objet. 
    
 _ulOpenFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert. Les indicateurs suivants peuvent être définies :
    
MAPI_BEST_ACCESS 
  
> L’objet doit être ouvert avec les autorisations maximales autorisées pour l’utilisateur et le nombre maximal d’autorisations d’application cliente. Par exemple, si le client dispose d’une autorisation de lecture/écriture, l’objet est ouvert avec une autorisation de lecture/écriture . Si le client dispose d’une autorisation en lecture seule, l’objet est ouvert avec une autorisation en lecture seule. Le client peut récupérer le niveau d’autorisation en obtenant **la propriété PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_DEFERRED_ERRORS 
  
> L’appel est autorisé à réussir même si l’objet sous-jacent n’est pas disponible pour l’application à l’origine de l’appel. Si l’objet n’est pas disponible, un appel ultérieur à l’objet peut renvoyer une erreur.
    
MAPI_MODIFY 
  
> Demande une autorisation de lecture/écriture. Par défaut, les objets sont créés avec une autorisation en lecture seule et les clients ne doivent pas fonctionner sur l’hypothèse que l’autorisation lecture/écriture a été accordée. 
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppUnk_
  
> [out] Pointeur vers le pointeur vers l’objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

MAPI appelle la **méthode IMSLogon::OpenEntry** pour ouvrir un dossier ou un message dans une magasin de messages. MAPI transmet l’identificateur d’entrée de l’objet à ouvrir. Le fournisseur de la boutique de messages doit renvoyer un pointeur qui permet un accès supplémentaire à l’objet spécifié dans _le paramètre lppUnk._ 
  
Avant que MAPI appelle **IMSLogon::OpenEntry,** il détermine d’abord que l’identificateur d’entrée de message ou de dossier donné correspond à un identificateur enregistré par ce fournisseur de magasin de messages. Pour plus d’informations sur la façon dont les fournisseurs de magasins enregistrent les identificateurs d’entrée, voir [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
  
 **IMSLogon::OpenEntry** est identique à la méthode [IMsgStore::OpenEntry](imsgstore-openentry.md) de l’objet de magasin de messages, sauf que le client n’appelle pas **IMSLogon::OpenEntry**; MAPI appelle **IMSLogon::OpenEntry** lorsqu’il traite une **méthode IMAPISession::OpenEntry.** Les objets ouverts à l’aide **d’IMSLogon::OpenEntry** doivent être traités exactement de la même manière que les objets ouverts à l’aide de l’objet de la boutique de messages . en particulier, les objets ouverts à l’aide de cet appel doivent être invalidés lorsque l’objet de la boutique de messages est libéré. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

