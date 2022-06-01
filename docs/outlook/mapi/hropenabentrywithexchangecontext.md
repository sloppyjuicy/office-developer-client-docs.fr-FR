---
title: HrOpenABEntryWithExchangeContext
description: Cet article décrit HrOpenABEntryWithExchangeContext qui ouvre l’entryID à l’aide du carnet d’adresses Exchange identifié par pEmsmdbUID.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
ms.openlocfilehash: a97799fbfe656bbea3bde7df7cc7afbb290df5aa
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816219"
---
# <a name="hropenabentrywithexchangecontext"></a>HrOpenABEntryWithExchangeContext

**S’applique à** : Outlook 2013 | Outlook 2016
 
Ouvre **l’entryID** à l’aide du carnet d’adresses Exchange identifié par **pEmsmdbUID**. Cette fonction fonctionne de la même façon que [IAddrBook::D etails](iaddrbook-details.md), sauf que l’utilisation de cette fonction garantit que [IAddrBook::OpenEntry](iaddrbook-openentry.md) est ouvert à l’aide du fournisseur de carnet d’adresses Exchange attendu.
 
|Propriété|Valeur|
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
  
> [in] Session **IMAPISession**. Il ne peut pas être NULL.

 _pEmsmdbUID_
  
> [in] Pointeur vers un **emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher des détails sur l’identificateur d’entrée. Si l’identificateur d’entrée entrante n’est pas un identificateur d’entrée de fournisseur de carnet d’adresses Exchange, ce paramètre est ignoré et l’appel de fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md). Si ce paramètre est NULL ou mapIUID zéro, cette fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).

 _pAddrBook_
  
> [in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée. Il ne peut pas être NULL.

 _cbEntryID_
  
> [in] Nombre d’octets de l’identificateur d’entrée spécifié par le paramètre _lpEntryID_ .

 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la façon dont l’entrée est ouverte. Les indicateurs suivants peuvent être définis :

MAPI_BEST_ACCESS
  
> Demande que l’entrée soit ouverte avec les autorisations maximales autorisées sur le réseau et le client. Par exemple, si le client dispose d’autorisations de lecture et d’écriture, le fournisseur de carnet d’adresses tente d’ouvrir l’entrée avec l’autorisation de lecture et d’écriture. Le client peut récupérer le niveau d’accès qui a été accordé en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’entrée ouverte et en récupérant la propriété PR_ACCESS_LEVEL (PidTagAccessLevel).

MAPI_CACHE_ONLY
  
> Utilise uniquement le carnet d’adresses hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d’ouvrir la liste d’adresses globale (GAL) en mode d’échange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur de carnets d’adresses Exchange.

MAPI_DEFERRED_ERRORS
  
> Permet à l’appel de réussir, potentiellement avant que l’entrée soit entièrement ouverte et disponible, ce qui implique que les appels suivants à l’entrée peuvent retourner une erreur.

MAPI_GAL_ONLY
  
> Utilise uniquement la gal pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur de carnets d’adresses Exchange.

MAPI_MODIFY
  
> Demande que l’entrée soit ouverte avec l’autorisation de lecture et d’écriture. Étant donné que les entrées sont ouvertes avec un accès en lecture seule par défaut, les clients ne doivent pas supposer que l’autorisation de lecture et d’écriture a été accordée, que MAPI_MODIFY soit défini ou non.

MAPI_NO_CACHE
  
> N’utilise pas le carnet d’adresses hors connexion pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur de carnets d’adresses Exchange.
