---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 879ba4afe85e1f6db31bd829411689b2dad58ed9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565465"
---
# <a name="hropenabentryusingdefaultcontext"></a>HrOpenABEntryUsingDefaultContext

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Effectue la même fonction que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) sauf qu’il utilise hérité **emsmdbUID** en tant que paramètre _pEmsmdbUID_ . N’utilisez pas cette fonction, sauf si vous ne peut pas obtenir correct **emsmdbUID** pour l’appel à [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
HRESULT HrOpenABEntryUsingDefaultContext(
  LPMAPISESSION pmsess,
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

 _pmsess_
  
> [in] La session **IMAPISession**. Il ne peut pas être NULL.
    
 _pAddrBook_
  
> [in] Le carnet d’adresses utilisée pour ouvrir l’identificateur d’entrée. Il ne peut pas être NULL.
    
 _cbEntryID_
  
> [in] Nombre d’octets de l’identificateur d’entrée spécifié par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
>  [in] Pointeur vers l’identificateur d’entrée qui représente l’entrée du carnet d’adresses à ouvrir. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’interface qui est utilisée pour accéder à l’entrée open. Passage de NULL renvoie l’interface standard de l’objet. Pour les utilisateurs de messagerie, l’interface standard est [IMailUser : IMAPIProp](imailuserimapiprop.md). Pour les listes de distribution, il est [IDistList : IMAPIContainer](idistlistimapicontainer.md)et il s’agit de conteneurs [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Les appelants peuvent définir _lpInterface_ à l’interface standard ou d’une interface dans la hiérarchie d’héritage. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouvert. Les indicateurs suivants peuvent être définis :
    
MAPI_BEST_ACCESS
  
> Demandes que l’entrée s’ouvre avec les autorisations maximales autorisées réseau et le client. Par exemple, si le client dispose de lecture et l’autorisation d’écriture, le fournisseur de carnet d’adresses essaie ouvrir l’entrée en lecture et l’autorisation d’écriture. Le client peut extraire le niveau d’accès qui a été accordé en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’écriture ouverte et de récupération de la propriété PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Utilise uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour autoriser une application cliente ouvrir la liste d’adresses globale (LAG) en mode exchange mis en cache et accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer le trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.
    
MAPI_DEFERRED_ERRORS
  
> Permet l’appel aboutisse, potentiellement avant que l’entrée est entièrement ouverte et disponible, ce qui implique que les appels suivants à l’entrée renverra une erreur.
    
MAPI_GAL_ONLY
  
> Utilise uniquement la liste d’adresses globale pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.
    
N'
  
> Demandes ouvrir avec l’entrée de lire et écrire des autorisations. Étant donné que les entrées sont ouvertes avec accès en lecture seule par défaut, les clients ne doivent pas supposer que lire et écrire l’autorisation a été accordée même si n’est définie.
    
MAPI_NO_CACHE
  
> N’utilise pas le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’entrée ouvert.
    
 _lppUnk_
  
> [out] Pointeur vers un pointeur de l’entrée ouvert.
    

