---
title: HrCompareABEntryIDsWithExchangeContext
description: La fonction HrCompareABEntryIDsWithExchangeContext compare deux entryID de carnet d’adresses en toute sécurité dans un profil à plusieurs Exchange.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
ms.openlocfilehash: d0f06131da67211f508c1393e66f29abb563ba75
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816912"
---
# <a name="hrcompareabentryidswithexchangecontext"></a>HrCompareABEntryIDsWithExchangeContext

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux **entryID de** carnet d’adresses en toute sécurité dans un profil à plusieurs Exchange. Cette fonction est une fonction de remplacement pour [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).
  
|Propriété |Valeur |
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
  
> [in] Session **IMAPISession**. Il ne peut pas être NULL.
    
 _pEmsmdbUID_
  
> [in] Pointeur vers un **emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher des détails sur l’identificateur d’entrée. Si l’identificateur d’entrée entrante n’est pas un identificateur d’entrée de fournisseur de carnet d’adresses Exchange, ce paramètre est ignoré et l’appel de fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md). Si ce paramètre est NULL ou mapIUID zéro, cette fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée. Il ne peut pas être NULL.
    
 _cbEntryID1_
  
> [in] Nombre d’octets du premier identificateur d’entrée spécifié par le paramètre  _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [in] Pointeur vers le premier identificateur d’entrée qui représente l’entrée de carnet d’adresses à comparer.
    
 _cbEntryID2_
  
> [in] Nombre d’octets du deuxième identificateur d’entrée spécifié par le paramètre  _lpEntryID2_ . 
    
 _lpEntryID2_
  
> [in] Pointeur vers le deuxième identificateur d’entrée utilisé dans la comparaison qui représente l’entrée de carnet d’adresses à comparer.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulResult_
  
> [out] Pointeur vers l’emplacement qui contient les résultats de la comparaison. 
    

