---
title: HrOpenABEntryWithResolvedRow
description: HrOpenABEntryWithResolvedRow obtient automatiquement l’emsabpUID à partir de la ligne résolue et ouvre l’entryID.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ce3a583c-16a9-4268-9476-926d2780eae5
ms.openlocfilehash: 884cea0f3d073dcd4f815ea1447b6bf5273fe117
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65818221"
---
# <a name="hropenabentrywithresolvedrow"></a>HrOpenABEntryWithResolvedRow

**S’applique à** : Outlook 2013 | Outlook 2016
  
Exécute la même fonction que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , sauf qu’il obtient automatiquement **l’emsabpUID** à partir de la ligne résolue et ouvre **l’entryID**.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp.h  <br/> |
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
  
> [in] Pointeur vers la ligne résolue utilisée pour obtenir **l’emsabpUID** et ouvrir **l’entryID**.

 _pAddrBook_
  
> [in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée. Il ne peut pas être NULL.

 _cbEntryID_
  
> [in] Nombre d’octets de l’identificateur d’entrée spécifié par le paramètre _lpEntryID_ .

 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.

 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’interface utilisée pour accéder à l’entrée ouverte. Le passage de NULL retourne l’interface standard de l’objet. Pour les utilisateurs de messagerie, l’interface standard est [IMailUser : IMAPIProp](imailuserimapiprop.md). Pour les listes de distribution, il s’agit [d’IDistList : IMAPIContainer](idistlistimapicontainer.md)et pour les conteneurs, il s’agit [d’IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Les appelants peuvent définir _lpInterface_ sur l’interface standard appropriée ou une interface dans la hiérarchie d’héritage.

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

 _lpulObjType_
  
> [out] Pointeur vers le type de l’entrée ouverte.

 _lppUnk_
  
> [out] Pointeur vers un pointeur de l’entrée ouverte.
