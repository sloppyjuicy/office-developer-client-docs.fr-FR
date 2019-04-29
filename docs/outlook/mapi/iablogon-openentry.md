---
title: IABLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 70f61ef553350f08eed96c1ee4e9ab790359d1fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409229"
---
# <a name="iablogonopenentry"></a>IABLogon::OpenEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un conteneur, un utilisateur de messagerie ou une liste de distribution, et renvoie un pointeur vers une implémentation d'interface pour fournir un accès supplémentaire.
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée du conteneur, de l'utilisateur de messagerie ou de la liste de distribution à ouvrir.
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à l'objet ouvert. Le fait de transmettre NULL renvoie l'identificateur pour l'interface standard de l'objet. Pour les conteneurs, l'interface standard est [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Les interfaces standard pour les objets de carnet d'adresses sont [IDistList: IMAPIContainer](idistlistimapicontainer.md) pour une liste de distribution et [IMailUser: IMAPIProp](imailuserimapiprop.md) pour un utilisateur de messagerie. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'objet. Les indicateurs suivants peuvent être définis:
    
MAPI_BEST_ACCESS 
  
> Demande l'ouverture de l'objet avec les autorisations réseau maximales accordées à l'utilisateur et l'accès maximal de l'application cliente. Par exemple, si le client dispose d'une autorisation en lecture/écriture, l'objet doit être ouvert avec une autorisation en lecture/écriture; Si le client dispose d'une autorisation en lecture seule, l'objet doit être ouvert en lecture seule.
    
MAPI_DEFERRED_ERRORS 
  
> Permet à la méthode **OpenEntry** de renvoyer correctement, éventuellement avant que le client appelant ait accédé à l'objet. Si l'objet n'est pas accessible, un appel d'objet ultérieur peut déclencher une erreur. 
    
MAPI_MODIFY 
  
> Demande une autorisation en lecture/écriture. Par défaut, les objets sont ouverts avec un accès en lecture seule et les clients ne doivent pas supposer que l'autorisation de lecture/écriture a été octroyée.
    
 _lpulObjType_
  
> remarquer Pointeur vers le type de l'objet ouvert.
    
 _lppUnk_
  
> remarquer Pointeur vers un pointeur vers l'objet ouvert.
    
## <a name="remarks"></a>Remarques

S_OK 
  
> L'objet a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> Soit l'utilisateur ne dispose pas des autorisations suffisantes pour ouvrir l'objet, soit une tentative d'ouverture d'un objet en lecture seule avec une autorisation en lecture/écriture est effectuée.
    
MAPI_E_NOT_FOUND 
  
> L'identificateur d'entrée spécifié par _lpEntryID_ ne représente pas un objet. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L'identificateur d'entrée dans le paramètre _lpEntryID_ n'est pas un format reconnu par le fournisseur de carnet d'adresses. 
    
## <a name="remarks"></a>Remarques

MAPI appelle la méthode **OpenEntry** pour ouvrir un conteneur, un utilisateur de messagerie ou une liste de distribution. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Avant que MAPI appelle votre méthode **OpenEntry** , il détermine que l'identificateur d'entrée dans le paramètre _lpEntryID_ appartient à vous et non à un autre fournisseur. MAPI effectue cette opération en faisant correspondre la structure [MAPIUID](mapiuid.md) dans l'identificateur d'entrée avec le **MAPIUID** que vous avez enregistré en appelant la méthode [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) au démarrage. 
  
Ouvrez l'objet en lecture seule, sauf si l'indicateur MAPI_MODIFY ou MAPI_BEST_ACCESS est défini dans le paramètre _ulFlags_ . Si vous n'autorisez pas la modification de l'objet demandé, n'ouvrez pas l'objet et retournez MAPI_E_NO_ACCESS. 
  
Si MAPI transmet NULL pour _lpEntryID_, ouvrez le conteneur racine dans votre hiérarchie de conteneurs.
  
L'objet que vous êtes invité à ouvrir peut être un objet copié à partir d'un autre fournisseur. Dans ce cas, elle prend en charge la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Si l'objet prend en charge cette propriété, appelez la méthode [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) pour établir une liaison avec le code pour cette entrée dans le fournisseur étranger, en passant **PR_TEMPLATEID** dans le paramètre _LpTemplateID_ et 0 dans le _ulTemplateFlags _paramètre. **IMAPISupport:: OpenTemplateID** transmet ces informations au fournisseur étranger dans un appel à la méthode [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) du fournisseur étranger. Si **IMAPISupport:: OpenTemplateID** génère une erreur, généralement parce que le fournisseur étranger n'est pas disponible ou n'est pas inclus dans le profil, essayez de continuer en traitant l'entrée indépendante en lecture seule. Pour plus d'informations sur l'ouverture des entrées de carnet d'adresses étranger, consultez [la rubrique agir en tant que fournisseur de carnets d'adresses hôte](acting-as-a-host-address-book-provider.md).
  
## <a name="see-also"></a>Voir aussi



[IABLogon : IUnknown](iablogoniunknown.md)

