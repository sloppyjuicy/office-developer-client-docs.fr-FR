---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: eb91f4998f94ffafbc33b6024228945f7c91cf43
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564989"
---
# <a name="hrcompareabentryidswithexchangecontext"></a>HrCompareABEntryIDsWithExchangeContext

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux adresses livre **identificateurs d’entrée** en toute sécurité dans un profil Exchange plusieurs. Cette fonction est une fonction de remplacement pour [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
HRESULT HrCompareABEntryIDsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG * lpulResult
);
```

## <a name="parameters"></a>Paramètres

 _pmsess_
  
> [in] La session **IMAPISession**. Il ne peut pas être NULL.
    
 _pEmsmdbUID_
  
> [in] Pointeur vers un **emsmdbUID** qui identifie le Service Exchange qui contient le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher plus d’informations sur l’identificateur d’entrée. Si l’identificateur d’entrée entrant n’est pas un identificateur d’entrée de carnet d’adresses Exchange, ce paramètre est ignoré et l’appel de fonction se comporte comme [IAddrBook::Details](iaddrbook-details.md). Si ce paramètre est NULL ou un zéro MAPIUID, cette fonction se comporte comme [IAddrBook::Details](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] Le carnet d’adresses utilisée pour ouvrir l’identificateur d’entrée. Il ne peut pas être NULL.
    
 _cbEntryID1_
  
> [in] Nombre d’octets de la première identificateur d’entrée spécifié par le paramètre _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [in] Pointeur vers l’identificateur d’entrée première qui représente l’entrée du carnet d’adresses à comparer.
    
 _cbEntryID2_
  
> [in] Nombre d’octets de la deuxième identificateur d’entrée spécifié par le paramètre _lpEntryID2_ . 
    
 _lpEntryID2_
  
> [in] Pointeur vers l’identificateur d’entrée deuxième utilisé dans la comparaison qui représente l’entrée du carnet d’adresses à comparer.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulResult_
  
> [out] Pointeur vers l’emplacement qui contient les résultats de la comparaison. 
    

