---
title: IAddrBookOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: Dernière modification le 1er février 2013
ms.openlocfilehash: 4ef48009f95d7cca6e9f4a4500494e032b712aa5
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62461932"
---
# <a name="iaddrbookopenentry"></a>IAddrBook::OpenEntry

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une entrée de carnet d’adresses et renvoie un pointeur vers une interface qui peut être utilisée pour accéder à l’entrée.
  
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
  
> [in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.
    
_lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’interface à utiliser pour accéder à l’entrée ouverte. La transmission NULL renvoie l’interface standard de l’objet. Pour les utilisateurs de messagerie, l’interface standard [est IMailUser : IMAPIProp](imailuserimapiprop.md). Pour les listes de distribution, il s’agit [d’IDistList : IMAPIContainer](idistlistimapicontainer.md) et pour les conteneurs, il s’agit de [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Les appelants peuvent définir  _lpInterface_ sur l’interface standard appropriée ou une interface dans la hiérarchie d’héritage. 
    
_ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouverte. Les indicateurs suivants peuvent être définies.
    
MAPI_BEST_ACCESS 
  
> Demande l’ouverture de l’entrée avec le nombre maximal d’autorisations réseau et client autorisées. Par exemple, si le client dispose d’une autorisation de lecture/écriture, le fournisseur de carnet d’adresses doit tenter d’ouvrir l’entrée avec une autorisation de lecture/écriture. Le client peut récupérer le niveau d’accès accordé en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’entrée ouverte et en récupérant la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_CACHE_ONLY
  
> Ouvre une entrée de carnet d’adresses et y accède uniquement à partir du cache. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d’ouvrir la liste d’adresses globale (LAL) en mode Exchange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur Exchange carnet d’adresses.
    
MAPI_DEFERRED_ERRORS 
  
> Permet de réussir l’appel, éventuellement avant que l’entrée soit entièrement ouverte et disponible, ce qui signifie que les appels ultérieurs à l’entrée peuvent renvoyer une erreur.
    
MAPI_GAL_ONLY
  
> Utilisez uniquement la LA GAL pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le Exchange de carnet d’adresses.
    
  > [!NOTE]
  > Les  _MAPI_GAL_ONLY ulFlags_ peuvent ne pas être définis dans le fichier d’en-tête téléchargeable dont vous disposez actuellement, auquel cas vous pouvez l’ajouter à votre code à l’aide de la valeur suivante : >  `#define MAPI_GAL_ONLY (0x00000080)`
  
MAPI_MODIFY 
  
> Demande l’ouverture de l’entrée avec une autorisation de lecture/écriture. Étant donné que les entrées sont ouvertes avec un accès en lecture seule par défaut, les clients ne doivent pas supposer que l’autorisation de lecture/écriture a été accordée, que l’autorisation MAPI_MODIFY soit définie ou non.
    
MAPI_NO_CACHE
  
> N’utilisez pas le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le Exchange de carnet d’adresses.
    
_lpulObjType_
  
> [out] Pointeur vers le type de l’entrée ouverte.
    
_lppUnk_
  
> [out] Pointeur vers un pointeur vers l’entrée ouverte.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’entrée a été ouverte avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative d’ouverture d’une entrée pour laquelle l’utilisateur dispose d’autorisations insuffisantes a été tentée.
    
MAPI_E_NOT_FOUND 
  
> L’entrée représentée par  _lpEntryID_ n’existe pas. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’identificateur d’entrée spécifié  _dans lpEntryID_ n’est pas reconnu. Cette valeur est généralement renvoyée si le fournisseur de carnet d’adresses responsable de l’entrée correspondante n’est pas ouvert. 
    
## <a name="remarks"></a>Remarques

Les clients et les fournisseurs de services appellent **la méthode IAddrBook::OpenEntry** pour ouvrir une entrée de carnet d’adresses. MAPI forwards the call to the appropriate address book provider, based on the [MAPIUID](mapiuid.md) structure included in the entry identifier passed in the _lpEntryID_ parameter. Le fournisseur de carnet d’adresses ouvre l’entrée en lecture seule, sauf si l’indicateur MAPI_MODIFY ou MAPI_BEST_ACCESS dans le paramètre _ulFlags_ est définie. Toutefois, ces indicateurs sont des suggestions. Si le fournisseur de carnet d’adresses n’autorise pas la modification de l’entrée demandée, il renvoie MAPI_E_NO_ACCESS. 
  
Le  _paramètre lpInterface_ indique l’interface à utiliser pour accéder à l’entrée ouverte. La transmission null dans  _lpInterface_ indique que l’interface MAPI standard pour ce type d’entrée doit être utilisée. Étant donné que le fournisseur de carnet d’adresses peut renvoyer une interface différente de celle suggérée par le paramètre  _lpInterface_ , l’appelant doit vérifier la valeur renvoyée dans le paramètre _lpulObjType_ pour déterminer si le type d’objet renvoyé est ce qui était attendu. Si le type d’objet n’est pas du type attendu, l’appelant peut caster le paramètre  _lppUnk_ vers un type plus approprié. 
  
## <a name="see-also"></a>Voir aussi

- [IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

