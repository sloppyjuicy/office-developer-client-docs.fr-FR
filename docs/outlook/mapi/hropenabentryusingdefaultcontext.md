---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: Effectue la même fonction que HrOpenABEntryWithExchangeContext, sauf qu’elle utilise l’interface emsmdbUID héritée comme paramètre _pEmsmdbUID_ .
ms.openlocfilehash: ae7c1c71165a7ead2a821a95d9363d779bc31292
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64406420"
---
# <a name="hropenabentryusingdefaultcontext"></a>HrOpenABEntryUsingDefaultContext

**S’applique à** : Outlook 2013 | Outlook 2016
  
Effectue la même fonction que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , sauf qu’elle utilise **l’interface emsmdbUID** héritée comme paramètre _pEmsmdbUID_ . N’utilisez pas cette fonction, sauf si vous ne pouvez pas obtenir le bon **emsmdbUID** pour l’appel à [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |

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

> [in] **IMAPISession** connecté. Elle ne peut pas être NULL.

 _pAddrBook_

> [in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée. Elle ne peut pas être NULL.

 _cbEntryID_

> [in] Nombre d’bytes de l’identificateur d’entrée spécifié par _le paramètre lpEntryID_ .

 _lpEntryID_

> [in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.

 _lpInterface_

> [in] Pointeur vers l’identificateur d’interface (IID) de l’interface utilisée pour accéder à l’entrée ouverte. La transmission NULL renvoie l’interface standard de l’objet. Pour les utilisateurs de messagerie, l’interface standard [est IMailUser : IMAPIProp](imailuserimapiprop.md). Pour les listes de distribution, il s’agit de [IDistList : IMAPIContainer](idistlistimapicontainer.md), et pour les conteneurs [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Les appelants peuvent définir _lpInterface_ sur l’interface standard appropriée ou une interface dans la hiérarchie d’héritage.

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

 _lpulObjType_

> [out] Pointeur vers le type de l’entrée ouverte.

 _lppUnk_

> [out] Pointeur vers un pointeur de l’entrée ouverte.
