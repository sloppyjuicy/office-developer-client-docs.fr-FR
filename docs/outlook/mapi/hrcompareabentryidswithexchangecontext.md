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
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="19aec-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="19aec-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="19aec-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19aec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19aec-105">Compare deux adresses livre **identificateurs d’entrée** en toute sécurité dans un profil Exchange plusieurs.</span><span class="sxs-lookup"><span data-stu-id="19aec-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="19aec-106">Cette fonction est une fonction de remplacement pour [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span><span class="sxs-lookup"><span data-stu-id="19aec-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19aec-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="19aec-107">Header file:</span></span>  <br/> |<span data-ttu-id="19aec-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="19aec-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="19aec-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="19aec-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="19aec-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="19aec-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="19aec-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="19aec-111">Called by:</span></span>  <br/> |<span data-ttu-id="19aec-112">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="19aec-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="19aec-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19aec-113">Parameters</span></span>

 <span data-ttu-id="19aec-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="19aec-114">_pmsess_</span></span>
  
> <span data-ttu-id="19aec-115">[in] La session **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="19aec-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="19aec-116">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="19aec-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="19aec-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="19aec-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="19aec-118">[in] Pointeur vers un **emsmdbUID** qui identifie le Service Exchange qui contient le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher plus d’informations sur l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="19aec-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="19aec-119">Si l’identificateur d’entrée entrant n’est pas un identificateur d’entrée de carnet d’adresses Exchange, ce paramètre est ignoré et l’appel de fonction se comporte comme [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="19aec-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="19aec-120">Si ce paramètre est NULL ou un zéro MAPIUID, cette fonction se comporte comme [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="19aec-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="19aec-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="19aec-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="19aec-122">[in] Le carnet d’adresses utilisée pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="19aec-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="19aec-123">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="19aec-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="19aec-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="19aec-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="19aec-125">[in] Nombre d’octets de la première identificateur d’entrée spécifié par le paramètre _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="19aec-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="19aec-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="19aec-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="19aec-127">[in] Pointeur vers l’identificateur d’entrée première qui représente l’entrée du carnet d’adresses à comparer.</span><span class="sxs-lookup"><span data-stu-id="19aec-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="19aec-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="19aec-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="19aec-129">[in] Nombre d’octets de la deuxième identificateur d’entrée spécifié par le paramètre _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="19aec-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="19aec-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="19aec-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="19aec-131">[in] Pointeur vers l’identificateur d’entrée deuxième utilisé dans la comparaison qui représente l’entrée du carnet d’adresses à comparer.</span><span class="sxs-lookup"><span data-stu-id="19aec-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="19aec-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="19aec-132">_ulFlags_</span></span>
  
> <span data-ttu-id="19aec-133">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="19aec-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="19aec-134">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="19aec-134">_lpulResult_</span></span>
  
> <span data-ttu-id="19aec-135">[out] Pointeur vers l’emplacement qui contient les résultats de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="19aec-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

