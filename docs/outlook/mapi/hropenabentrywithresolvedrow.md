---
title: HrOpenABEntryWithResolvedRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3a583c-16a9-4268-9476-926d2780eae5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2eb643e0002e2159e3197d66e021aba0bb8c126f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347774"
---
# <a name="hropenabentrywithresolvedrow"></a>HrOpenABEntryWithResolvedRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Effectue la même fonction que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , sauf qu'il obtient automatiquement **emsabpUID** à partir de la ligne résolue et ouvre la propriété **entryID**.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithResolvedRow(
  LPSRow prwResolved,
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

 _prwResolved_
  
> dans Pointeur vers la ligne résolue utilisée pour obtenir le **emsabpUID** et ouvrir la propriété **entryID**.
    
 _pAddrBook_
  
> dans Carnet d'adresses utilisé pour ouvrir l'identificateur d'entrée. Il ne peut pas être NULL.
    
 _cbEntryID_
  
> dans Nombre d'octets de l'identificateur d'entrée spécifié par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
>  dans Pointeur vers l'identificateur d'entrée qui représente l'entrée de carnet d'adresses à ouvrir. 
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) de l'interface qui est utilisé pour accéder à l'entrée ouverte. Le passage de la valeur NULL renvoie l'interface standard de l'objet. Pour les utilisateurs de messagerie, l'interface standard est [IMailUser: IMAPIProp](imailuserimapiprop.md). Pour les listes de distribution, il s'agit de [IDistList: IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs, il s'agit de [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Les appelants peuvent définir _lpInterface_ sur l'interface standard appropriée ou une interface dans la hiérarchie d'héritage. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'entrée. Les indicateurs suivants peuvent être définis:
    
MAPI_BEST_ACCESS
  
> Demande que l'entrée soit ouverte avec les autorisations réseau et client maximales autorisées. Par exemple, si le client dispose d'une autorisation en lecture et en écriture, le fournisseur de carnet d'adresses tente d'ouvrir l'entrée avec une autorisation en lecture et en écriture. Le client peut récupérer le niveau d'accès qui a été accordé en appelant la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de l'entrée ouverte et en récupérant la propriété PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Utilise uniquement le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d'ouvrir la liste d'adresses globale (LAG) en mode Exchange mis en cache et d'accéder à une entrée de ce carnet d'adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.
    
MAPI_DEFERRED_ERRORS
  
> Permet à l'appel de réussir, éventuellement avant que l'entrée soit entièrement ouverte et disponible, ce qui implique que des appels ultérieurs à l'entrée renvoient une erreur.
    
MAPI_GAL_ONLY
  
> Utilise uniquement la liste d'adresses globale pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.
    
MAPI_MODIFY
  
> Demande que l'entrée soit ouverte avec une autorisation en lecture et en écriture. Étant donné que les entrées sont ouvertes avec un accès en lecture seule par défaut, les clients ne doivent pas supposer que l'autorisation de lecture et d'écriture a été accordée, que MAPI_MODIFY soit défini ou non.
    
MAPI_NO_CACHE
  
> N'utilise pas le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.
    
 _lpulObjType_
  
> remarquer Pointeur vers le type de l'entrée ouverte.
    
 _lppUnk_
  
> remarquer Pointeur vers un pointeur de l'entrée ouverte.
    

