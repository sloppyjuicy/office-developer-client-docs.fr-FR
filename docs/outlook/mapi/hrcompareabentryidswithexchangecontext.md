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
ms.openlocfilehash: 4bada5913623e2eb463a9e72347bd31eb22c414b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436432"
---
# <a name="hrcompareabentryidswithexchangecontext"></a>HrCompareABEntryIDsWithExchangeContext

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux entrées de carnet **d’adresses** en toute sécurité dans un profil Exchange multiple. Cette fonction est une fonction de remplacement [pour IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |abhelp.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
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
  
> [in] **L’IMAPISession** connecté. Elle ne peut pas être NULL.
    
 _pEmsmdbUID_
  
> [in] Pointeur vers **un emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher des détails sur l’identificateur d’entrée. Si l’identificateur d’entrée entrante n’est pas un identificateur d’entrée du fournisseur de carnet d’adresses Exchange, ce paramètre est ignoré et l’appel de fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md). Si ce paramètre est NULL ou un MAPIUID zéro, cette fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée. Elle ne peut pas être NULL.
    
 _cbEntryID1_
  
> [in] Nombre d’bytes du premier identificateur d’entrée spécifié par _le paramètre lpEntryID1._ 
    
 _lpEntryID1_
  
> [in] Pointeur vers le premier identificateur d’entrée qui représente l’entrée de carnet d’adresses à comparer.
    
 _cbEntryID2_
  
> [in] Nombre d’bytes du deuxième identificateur d’entrée spécifié par _le paramètre lpEntryID2._ 
    
 _lpEntryID2_
  
> [in] Pointeur vers le deuxième identificateur d’entrée utilisé dans la comparaison qui représente l’entrée de carnet d’adresses à comparer.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulResult_
  
> [out] Pointeur vers l’emplacement qui contient les résultats de la comparaison. 
    

