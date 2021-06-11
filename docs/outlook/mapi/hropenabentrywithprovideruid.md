---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 20344185ffcbd90017fa3c3493218bd9b3ddfd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408893"
---
# <a name="hropenabentrywithprovideruid"></a>HrOpenABEntryWithProviderUID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre **l’entryID à** l’aide Exchange carnet d’adresses identifié par _pEmsabpUID_. Cette fonction fonctionne de la même manière que [IAddrBook::OpenEntry,](iaddrbook-openentry.md) sauf que l’utilisation de cette fonction garantit que [IAddrBook::OpenEntry](iaddrbook-openentry.md) est ouvert à l’aide du fournisseur de carnet d’adresses Exchange attendu. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUID(
  const MAPIUID *pEmsabpUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameters

 _pEmsmdbUID_
  
> [in] Pointeur vers **un élément emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher des détails sur l’identificateur d’entrée. Si l’identificateur d’entrée entrante n’est pas un identificateur d’entrée du fournisseur de carnet d’adresses Exchange, ce paramètre est ignoré et l’appel de fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md). Si ce paramètre est NULL ou un MAPIUID zéro, cette fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée. Elle ne peut pas être NULL.
    
 _cbEntryID_
  
> [in] Nombre d’bytes de l’identificateur d’entrée spécifié par _le paramètre lpEntryID._ 
    
 _lpEntryID_
  
>  [in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’interface utilisée pour accéder à l’entrée ouverte. La transmission NULL renvoie l’interface standard de l’objet. Pour les utilisateurs de messagerie, l’interface standard [est IMailUser : IMAPIProp](imailuserimapiprop.md). Pour les listes de distribution, il s’agit de [IDistList : IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs, il s’agit de [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Les appelants peuvent définir  _lpInterface_ sur l’interface standard appropriée ou une interface dans la hiérarchie d’héritage. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouverte, les indicateurs suivants peuvent être définies :
    
MAPI_BEST_ACCESS
  
> Demande l’ouverture de l’entrée avec le nombre maximal d’autorisations réseau et client autorisées. Par exemple, si le client dispose d’autorisations de lecture et d’écriture, le fournisseur de carnet d’adresses tente d’ouvrir l’entrée avec des autorisations de lecture et d’écriture. Le client peut récupérer le niveau d’accès accordé en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’entrée ouverte et en récupérant la propriété PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Utilisez uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d’ouvrir la liste d’adresses globale (LAL) en mode Exchange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le Exchange de carnet d’adresses.
    
MAPI_DEFERRED_ERRORS
  
> Permet de réussir l’appel, éventuellement avant que l’entrée soit entièrement ouverte et disponible, ce qui signifie que les appels ultérieurs à l’entrée peuvent renvoyer une erreur.
    
MAPI_GAL_ONLY
  
> Utilisez uniquement la LA GAL pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le Exchange de carnet d’adresses.
    
MAPI_MODIFY
  
> Demande l’ouverture de l’entrée avec une autorisation de lecture et d’écriture. Étant donné que les entrées sont ouvertes avec un accès en lecture seule par défaut, les clients ne doivent pas supposer que l’autorisation de lecture et d’écriture a été accordée, qu’MAPI_MODIFY soit définie ou non.
    
MAPI_NO_CACHE
  
> N’utilisez pas le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le Exchange de carnet d’adresses.
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’entrée ouverte.
    
 _lppUnk_
  
> [out] Pointeur vers un pointeur de l’entrée ouverte.
    

