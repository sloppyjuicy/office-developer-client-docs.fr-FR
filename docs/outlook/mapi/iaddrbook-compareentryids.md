---
title: IAddrBookCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b6abecc298df7a86afff9338752a15615c73b3a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424258"
---
# <a name="iaddrbookcompareentryids"></a><span data-ttu-id="07eb0-103">IAddrBook::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="07eb0-103">IAddrBook::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="07eb0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07eb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07eb0-105">Compare deux identificateurs d’entrée appartenant à un fournisseur de carnet d’adresses particulier pour déterminer s’ils font référence au même objet de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="07eb0-105">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span> 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="07eb0-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="07eb0-106">Parameters</span></span>

 <span data-ttu-id="07eb0-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="07eb0-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="07eb0-108">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="07eb0-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="07eb0-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="07eb0-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="07eb0-110">[in] Pointeur vers le premier identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="07eb0-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="07eb0-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="07eb0-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="07eb0-112">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="07eb0-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="07eb0-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="07eb0-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="07eb0-114">[in] Pointeur vers le deuxième identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="07eb0-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="07eb0-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="07eb0-115">_ulFlags_</span></span>
  
> <span data-ttu-id="07eb0-116">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="07eb0-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="07eb0-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="07eb0-117">_lpulResult_</span></span>
  
> <span data-ttu-id="07eb0-118">[out] Pointeur vers le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="07eb0-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="07eb0-119">Le contenu de  _lpulResult_ est définie sur TRUE si les deux identificateurs d’entrée font référence au même objet ; Dans le cas contraire, le contenu est définie sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="07eb0-119">The contents of  _lpulResult_ are set to TRUE if the two entry identifiers refer to the same object; otherwise, the contents are set to FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="07eb0-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="07eb0-120">Return value</span></span>

<span data-ttu-id="07eb0-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="07eb0-121">S_OK</span></span> 
  
> <span data-ttu-id="07eb0-122">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="07eb0-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="07eb0-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="07eb0-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="07eb0-124">L’un ou les deux identificateurs d’entrée transmis avec les paramètres  _lpEntryID1_ ou  _lpEntryID2_ ne sont reconnus par aucun fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="07eb0-124">One or both of the entry identifiers passed in with the  _lpEntryID1_ or  _lpEntryID2_ parameters are not recognized by any address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="07eb0-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="07eb0-125">Remarks</span></span>

<span data-ttu-id="07eb0-126">Les applications clientes et les fournisseurs de services appellent la méthode **CompareEntryIDs** pour comparer deux identificateurs d’entrée appartenant à un seul fournisseur de carnet d’adresses afin de déterminer s’ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="07eb0-126">Client applications and service providers call the **CompareEntryIDs** method to compare two entry identifiers that belongs to a single address book provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="07eb0-127">**CompareEntryIDs est utile** car un objet peut avoir plusieurs identificateurs d’entrée valides.</span><span class="sxs-lookup"><span data-stu-id="07eb0-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="07eb0-128">Cette situation peut se produire, par exemple, après l’installation d’une nouvelle version d’un fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="07eb0-128">This situation can occur, for example, after a new version of an address book provider is installed.</span></span> 
  
<span data-ttu-id="07eb0-129">MAPI transmet cet appel au fournisseur de carnet d’adresses responsable des identificateurs d’entrée, en déterminant le fournisseur approprié en faisant correspondre la structure [MAPIUID](mapiuid.md) dans les identificateurs d’entrée avec la structure **MAPIUID** inscrite par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="07eb0-129">MAPI passes this call to the address book provider that is responsible for the entry identifiers, determining the appropriate provider by matching the [MAPIUID](mapiuid.md) structure in the entry identifiers with the **MAPIUID** structure registered by the provider.</span></span> 
  
<span data-ttu-id="07eb0-130">Si les deux identificateurs d’entrée font référence au même objet, **CompareEntryIDs** définit le contenu du paramètre  _lpulResult_ sur TRUE ; S’ils font référence à différents objets, **CompareEntryIDs** définit le contenu sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="07eb0-130">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the contents of the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets the contents to FALSE.</span></span> <span data-ttu-id="07eb0-131">Dans les deux cas, **CompareEntryIDs** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="07eb0-131">In either case, **CompareEntryIDs** returns S_OK.</span></span> <span data-ttu-id="07eb0-132">Si **CompareEntryIDs** renvoie une erreur, qui peut se produire si aucun fournisseur de carnet d’adresses n’a inscrit une structure **MAPIUID** qui correspond à celle des identificateurs d’entrée, les clients et les fournisseurs ne doivent pas prendre d’action en fonction du résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="07eb0-132">If **CompareEntryIDs** returns an error, which can occur if no address book provider has registered a **MAPIUID** structure that matches the one in the entry identifiers, clients and providers should not take any action based on the result of the comparison.</span></span> <span data-ttu-id="07eb0-133">Au lieu de cela, ils doivent prendre l’approche la plus prudent de l’action en cours.</span><span class="sxs-lookup"><span data-stu-id="07eb0-133">They should instead take the most conservative approach to the action being performed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="07eb0-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07eb0-134">See also</span></span>



[<span data-ttu-id="07eb0-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="07eb0-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

