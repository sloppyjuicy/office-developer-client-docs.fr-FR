---
title: IABLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ba7dce26ac7791f5cfb8f5361c552be1883839ca
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62463816"
---
# <a name="iablogonopenentry"></a>IABLogon::OpenEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un conteneur, un utilisateur de messagerie ou une liste de distribution et renvoie un pointeur vers une implémentation d’interface pour fournir un accès supplémentaire.
  
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
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du conteneur, de l’utilisateur de messagerie ou de la liste de distribution à ouvrir.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet ouvert. La transmission null renvoie l’identificateur de l’interface standard de l’objet. Pour les conteneurs, l’interface standard [est IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Les interfaces standard pour les objets de carnet d’adresses sont [IDistList : IMAPIContainer](idistlistimapicontainer.md) pour une liste de distribution et [IMailUser : IMAPIProp](imailuserimapiprop.md) pour un utilisateur de messagerie. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert. Les indicateurs suivants peuvent être définies :
    
MAPI_BEST_ACCESS 
  
> Demande l’ouverture de l’objet avec les autorisations réseau maximales autorisées pour l’utilisateur et l’accès maximal à l’application cliente. Par exemple, si le client dispose d’une autorisation de lecture/écriture, l’objet doit être ouvert avec une autorisation de lecture/écriture . Si le client dispose d’une autorisation en lecture seule, l’objet doit être ouvert avec une autorisation en lecture seule.
    
MAPI_DEFERRED_ERRORS 
  
> Permet à la **méthode OpenEntry** de renvoyer correctement, éventuellement avant que le client appelant ait accédé entièrement à l’objet. Si l’objet n’est pas accessible, effectuer un appel d’objet ultérieur peut occasioner une erreur. 
    
MAPI_MODIFY 
  
> Demande une autorisation de lecture/écriture. Par défaut, les objets sont ouverts avec un accès en lecture seule et les clients ne doivent pas supposer que l’autorisation lecture/écriture a été accordée.
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppUnk_
  
> [out] Pointeur vers un pointeur vers l’objet ouvert.
    
## <a name="remarks"></a>Remarques

S_OK 
  
> L’objet a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> Soit l’utilisateur ne dispose pas des autorisations suffisantes pour ouvrir l’objet, soit une tentative d’ouverture d’un objet en lecture seule avec une autorisation de lecture/écriture a été tentée.
    
MAPI_E_NOT_FOUND 
  
> L’identificateur d’entrée spécifié  _par lpEntryID_ ne représente pas un objet. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’identificateur d’entrée dans _le paramètre lpEntryID_ n’est pas d’un format reconnu par le fournisseur de carnet d’adresses. 
    
## <a name="remarks"></a>Remarques

MAPI appelle la **méthode OpenEntry** pour ouvrir un conteneur, un utilisateur de messagerie ou une liste de distribution. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Avant que MAPI appelle **votre méthode OpenEntry** , il détermine que l’identificateur d’entrée dans le paramètre _lpEntryID_ vous appartient et non à un autre fournisseur. POUR ce faire, MAPI fait correspondre la structure [MAPIUID](mapiuid.md) dans l’identificateur d’entrée avec le **MAPIUID** que vous avez enregistré en appelant la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) au démarrage. 
  
Ouvrez l’objet en lecture seule, sauf si l’MAPI_MODIFY ou MAPI_BEST_ACCESS est définie dans le _paramètre ulFlags_ . Si vous n’autorisez pas la modification de l’objet demandé, n’ouvrez pas l’objet et ne renvoyez aucune MAPI_E_NO_ACCESS. 
  
Si MAPI transmet la valeur NULL pour  _lpEntryID_, ouvrez le conteneur racine dans votre hiérarchie de conteneur.
  
L’objet que vous êtes invité à ouvrir peut être un objet copié à partir d’un autre fournisseur. Dans ce cas, il prendra en charge la **propriété PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Si l’objet prend en charge cette propriété, appelez la méthode [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) pour établir une liaison avec le code de cette entrée dans le fournisseur étranger, en passant **PR_TEMPLATEID** dans le paramètre _lpTemplateID_ et 0 dans le paramètre _ulTemplateFlags_ . **IMAPISupport::OpenTemplateID** transmet ces informations au fournisseur étranger dans un appel à la méthode [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) du fournisseur étranger. Si **IMAPISupport::OpenTemplateID** lève une erreur, généralement parce que le fournisseur étranger n’est pas disponible ou n’est pas inclus dans le profil, essayez de continuer en traitant l’entrée indépendant comme étant en lecture seule. Pour plus d’informations sur l’ouverture d’entrées de carnet d’adresses étrangères, voir [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).
  
## <a name="see-also"></a>Voir aussi



[IABLogon : IUnknown](iablogoniunknown.md)

