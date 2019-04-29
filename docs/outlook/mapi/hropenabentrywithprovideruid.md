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
  
Ouvre la propriété **entryID** à l'aide du carnet d'adresses Exchange identifié par _pEmsabpUID_. Cette fonction fonctionne de la même manière que [IAddrBook:: OpenEntry](iaddrbook-openentry.md) à l'exception du fait que l'utilisation de cette fonction garantit l'ouverture de [IAddrBook:: OpenEntry](iaddrbook-openentry.md) à l'aide du fournisseur de carnet d'adresses Exchange attendu. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp. h  <br/> |
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

## <a name="parameters"></a>Paramètres

 _pEmsmdbUID_
  
> dans Pointeur vers un **emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnets d'adresses Exchange que cette fonction doit utiliser pour afficher les détails sur l'identificateur d'entrée. Si l'identificateur d'entrée entrante n'est pas un identificateur d'entrée de fournisseur de carnet d'adresses Exchange, ce paramètre est ignoré et l'appel de fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md). Si ce paramètre est NULL ou un zéro MAPIUID, cette fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> dans Carnet d'adresses utilisé pour ouvrir l'identificateur d'entrée. Il ne peut pas être NULL.
    
 _cbEntryID_
  
> dans Nombre d'octets de l'identificateur d'entrée spécifié par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
>  dans Pointeur vers l'identificateur d'entrée qui représente l'entrée de carnet d'adresses à ouvrir. 
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) de l'interface qui est utilisé pour accéder à l'entrée ouverte. Le passage de la valeur NULL renvoie l'interface standard de l'objet. Pour les utilisateurs de messagerie, l'interface standard est [IMailUser: IMAPIProp](imailuserimapiprop.md). Pour les listes de distribution, il s'agit de [IDistList: IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs, il s'agit de [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Les appelants peuvent définir _lpInterface_ sur l'interface standard appropriée ou une interface dans la hiérarchie d'héritage. 
    
 _ulFlags_
  
> dans Un masque de réindicateur des indicateurs qui contrôle le mode d'ouverture de l'entrée, les indicateurs suivants peuvent être définis:
    
MAPI_BEST_ACCESS
  
> Demande que l'entrée soit ouverte avec les autorisations réseau et client maximales autorisées. Par exemple, si le client dispose d'une autorisation en lecture et en écriture, le fournisseur de carnet d'adresses tente d'ouvrir l'entrée avec une autorisation en lecture et en écriture. Le client peut récupérer le niveau d'accès qui a été accordé en appelant la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de l'entrée ouverte et en récupérant la propriété PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Utilisez uniquement le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d'ouvrir la liste d'adresses globale (LAG) en mode Exchange mis en cache et d'accéder à une entrée de ce carnet d'adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.
    
MAPI_DEFERRED_ERRORS
  
> Permet à l'appel de réussir, éventuellement avant que l'entrée soit entièrement ouverte et disponible, ce qui implique que des appels ultérieurs à l'entrée renvoient une erreur.
    
MAPI_GAL_ONLY
  
> Utilisez uniquement la liste d'adresses globale pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.
    
MAPI_MODIFY
  
> Demande que l'entrée soit ouverte avec une autorisation en lecture et en écriture. Étant donné que les entrées sont ouvertes avec un accès en lecture seule par défaut, les clients ne doivent pas supposer que l'autorisation de lecture et d'écriture a été accordée, que MAPI_MODIFY soit défini ou non.
    
MAPI_NO_CACHE
  
> N'utilisez pas le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.
    
 _lpulObjType_
  
> remarquer Pointeur vers le type de l'entrée ouverte.
    
 _lppUnk_
  
> remarquer Pointeur vers un pointeur de l'entrée ouverte.
    

