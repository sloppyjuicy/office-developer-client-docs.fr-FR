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
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="7dc28-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="7dc28-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="7dc28-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dc28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7dc28-105">Compare deux entrées de carnet **d’adresses** en toute sécurité dans un profil Exchange multiples.</span><span class="sxs-lookup"><span data-stu-id="7dc28-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="7dc28-106">Cette fonction est une fonction de remplacement [pour IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span><span class="sxs-lookup"><span data-stu-id="7dc28-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7dc28-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7dc28-107">Header file:</span></span>  <br/> |<span data-ttu-id="7dc28-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="7dc28-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="7dc28-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="7dc28-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="7dc28-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="7dc28-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="7dc28-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="7dc28-111">Called by:</span></span>  <br/> |<span data-ttu-id="7dc28-112">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="7dc28-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="7dc28-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="7dc28-113">Parameters</span></span>

 <span data-ttu-id="7dc28-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="7dc28-114">_pmsess_</span></span>
  
> <span data-ttu-id="7dc28-115">[in] **L’IMAPISession** connecté.</span><span class="sxs-lookup"><span data-stu-id="7dc28-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="7dc28-116">Elle ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="7dc28-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="7dc28-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="7dc28-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="7dc28-118">[in] Pointeur vers **un élément emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher des détails sur l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7dc28-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="7dc28-119">Si l’identificateur d’entrée entrante n’est pas un identificateur d’entrée du fournisseur de carnet d’adresses Exchange, ce paramètre est ignoré et l’appel de fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="7dc28-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="7dc28-120">Si ce paramètre est NULL ou un MAPIUID zéro, cette fonction se comporte comme [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="7dc28-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="7dc28-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="7dc28-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="7dc28-122">[in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7dc28-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="7dc28-123">Elle ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="7dc28-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="7dc28-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="7dc28-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="7dc28-125">[in] Nombre d’bytes du premier identificateur d’entrée spécifié par _le paramètre lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="7dc28-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="7dc28-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="7dc28-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="7dc28-127">[in] Pointeur vers le premier identificateur d’entrée qui représente l’entrée de carnet d’adresses à comparer.</span><span class="sxs-lookup"><span data-stu-id="7dc28-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="7dc28-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="7dc28-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="7dc28-129">[in] Nombre d’bytes du deuxième identificateur d’entrée spécifié par _le paramètre lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="7dc28-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="7dc28-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="7dc28-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="7dc28-131">[in] Pointeur vers le deuxième identificateur d’entrée utilisé dans la comparaison qui représente l’entrée de carnet d’adresses à comparer.</span><span class="sxs-lookup"><span data-stu-id="7dc28-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="7dc28-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7dc28-132">_ulFlags_</span></span>
  
> <span data-ttu-id="7dc28-133">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="7dc28-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7dc28-134">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="7dc28-134">_lpulResult_</span></span>
  
> <span data-ttu-id="7dc28-135">[out] Pointeur vers l’emplacement qui contient les résultats de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="7dc28-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

