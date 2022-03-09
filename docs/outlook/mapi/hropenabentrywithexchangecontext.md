---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e0133c537ecf572865c0927f0102166fd3f2bca9
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374452"
---
# <a name="hropenabentrywithexchangecontext"></a>HrOpenABEntryWithExchangeContext

**S’applique à** : Outlook 2013 | Outlook 2016
 
Ouvre **l’entryID à** l’aide Exchange carnet d’adresses identifié **par pEmsmdbUID**. Cette fonction fonctionne de la même manière que [IAddrBook::D etails](iaddrbook-details.md), sauf que l’utilisation de cette fonction garantit que [l’IAddrBook::OpenEntry](iaddrbook-openentry.md) est ouvert à l’aide du fournisseur de carnet d’adresses Exchange attendu.
 
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |

```cpp
HRESULT HrDoABDetailsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _pmsess_
  
> [in] **IMAPISession** connecté. Elle ne peut pas être NULL.

 _pEmsmdbUID_
  
> [in] Pointeur vers **un emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher des détails sur l’identificateur d’entrée. Si l’identificateur d’entrée entrante n’est pas un identificateur d’entrée du fournisseur de carnet d’adresses Exchange, ce paramètre est ignoré et l’appel de fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md). Si ce paramètre est NULL ou un MAPIUID zéro, cette fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).

 _pAddrBook_
  
> [in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée. Elle ne peut pas être NULL.

 _cbEntryID_
  
> [in] Nombre d’bytes de l’identificateur d’entrée spécifié par _le paramètre lpEntryID_ .

 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouverte. Les indicateurs suivants peuvent être définies :

MAPI_BEST_ACCESS
  
> Demande l’ouverture de l’entrée avec le nombre maximal d’autorisations réseau et client autorisées. Par exemple, si le client dispose d’autorisations de lecture et d’écriture, le fournisseur de carnet d’adresses tente d’ouvrir l’entrée avec des autorisations de lecture et d’écriture. Le client peut récupérer le niveau d’accès accordé en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’entrée ouverte et en récupérant la propriété PR_ACCESS_LEVEL (PidTagAccessLevel).

MAPI_CACHE_ONLY
  
> Utilise uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d’ouvrir la liste d’adresses globale (LAL) en mode Exchange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur Exchange carnet d’adresses.

MAPI_DEFERRED_ERRORS
  
> Permet à l’appel de réussir, potentiellement avant que l’entrée soit entièrement ouverte et disponible, ce qui signifie que les appels ultérieurs à l’entrée peuvent renvoyer une erreur.

MAPI_GAL_ONLY
  
> Utilise uniquement la LA GAL pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur Exchange carnet d’adresses.

MAPI_MODIFY
  
> Demande l’ouverture de l’entrée avec une autorisation de lecture et d’écriture. Étant donné que les entrées sont ouvertes avec un accès en lecture seule par défaut, les clients ne doivent pas supposer que les autorisations de lecture et d’écriture ont été accordées, qu’MAPI_MODIFY soit définie ou non.

MAPI_NO_CACHE
  
> N’utilise pas le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur Exchange carnet d’adresses.
