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
ms.openlocfilehash: bf6386ae3a7d835c8748e332235d8737c7a502e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589468"
---
# <a name="iablogonopenentry"></a>IABLogon::OpenEntry

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ouvre un conteneur, utilisateur ou les listes de distribution, de messagerie et retourne un pointeur vers une implémentation d’interface pour fournir un accès plus.
  
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
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du conteneur, utilisateur ou liste de distribution pour ouvrir la messagerie.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet ouvert. Passage de NULL renvoie l’identificateur de l’interface standard de l’objet. Pour les conteneurs, l’interface standard est [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Pour les objets de carnet d’adresses sont des interfaces de la norme [IDistList : IMAPIContainer](idistlistimapicontainer.md) pour une liste de distribution et [IMailUser : IMAPIProp](imailuserimapiprop.md) pour un utilisateur de messagerie. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert. Les indicateurs suivants peuvent être définis :
    
MAPI_BEST_ACCESS 
  
> Demande que l’objet s’ouvre avec les autorisations de réseau maximale autorisées pour l’accès des utilisateurs et le nombre maximal de clients application. Par exemple, si le client a l’autorisation de lecture/écriture, l’objet doit être ouvert avec l’autorisation de lecture/écriture ; Si le client dispose des autorisations en lecture seule, l’objet doit être ouvert avec l’autorisation en lecture seule.
    
MAPI_DEFERRED_ERRORS 
  
> Permet à la méthode **OpenEntry** renvoyer avec succès, éventuellement avant le client appelant entièrement a accédé à l’objet. Si l’objet n’est pas accessible, l’émission d’un appel d’objet suivantes peut déclencher une erreur. 
    
N' 
  
> Demandes d’autorisation de lecture/écriture. Par défaut, les objets sont ouverts avec accès en lecture seule et clients ne doivent pas supposer bénéficie des autorisations en lecture-écriture.
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppUnk_
  
> [out] Pointeur vers un pointeur vers l’objet ouvert.
    
## <a name="remarks"></a>Remarques

S_OK 
  
> L’objet a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> L’utilisateur dispose des autorisations suffisantes pour ouvrir l’objet, soit une tentative a été effectuée pour ouvrir un objet en lecture seule avec l’autorisation de lecture/écriture.
    
MAPI_E_NOT_FOUND 
  
> L’identificateur d’entrée spécifié par _lpEntryID_ ne représente pas un objet. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’identificateur d’entrée dans le paramètre _lpEntryID_ n’est pas un format reconnu par le fournisseur de carnet d’adresses. 
    
## <a name="remarks"></a>Remarques

MAPI appelle la méthode **OpenEntry** pour ouvrir un conteneur, utilisateur ou liste de distribution de messagerie. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Avant votre méthode **OpenEntry** appels MAPI, il détermine que l’identificateur d’entrée dans le paramètre _lpEntryID_ appartient à vous et non à un autre fournisseur. Pour cela, MAPI correspondant à la structure [MAPIUID](mapiuid.md) est l’identificateur d’entrée avec la **MAPIUID** que vous avez enregistré en appelant la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) au démarrage. 
  
Ouvrez l’objet en lecture seule, sauf si l’indicateur n’ou MAPI_BEST_ACCESS est défini dans le paramètre _ulFlags_ . Si vous n’autorisez pas la modification de l’objet demandé, ne pas ouvrir l’objet tout et retourner MAPI_E_NO_ACCESS. 
  
Si MAPI passe NULL pour _lpEntryID_, ouvrez le conteneur racine dans votre hiérarchie de conteneur.
  
L’objet que vous êtes invité à ouvrir peut être un objet copié à partir d’un autre fournisseur. Dans ce cas, il prendra en charge la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Si l’objet ne prend pas en charge cette propriété, appelez la méthode [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) pour lier au code de cette entrée dans le fournisseur étranger, en transmettant **PR_TEMPLATEID** dans le paramètre _lpTemplateID_ et 0 dans l’ulTemplateFlags _ _paramètre. **IMAPISupport::OpenTemplateID** passe ces informations au fournisseur étrangère dans un appel de méthode de [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) du fournisseur étranger. Si **IMAPISupport::OpenTemplateID** génère une erreur, généralement car le fournisseur étranger est indisponible ou non inclus dans le profil, essayez de continuer à traiter l’entrée indépendante en lecture seule. Pour plus d’informations sur l’ouverture des entrées de carnet d’adresse étrangère, voir [agit comme fournisseur de carnet d’adresses hôte](acting-as-a-host-address-book-provider.md).
  
## <a name="see-also"></a>Voir aussi



[IABLogon : IUnknown](iablogoniunknown.md)

