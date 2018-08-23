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
ms.openlocfilehash: d6f983e49132e7ab6ea402a8e32bb5ec56d1efba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564849"
---
# <a name="iaddrbookcompareentryids"></a><span data-ttu-id="f7f94-103">IAddrBook::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="f7f94-103">IAddrBook::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="f7f94-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7f94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7f94-105">Compare deux identificateurs d’entrée qui appartiennent à un fournisseur de carnet d’adresse spécifique afin de déterminer si elles font référence à l’objet de carnet d’adresses même.</span><span class="sxs-lookup"><span data-stu-id="f7f94-105">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="f7f94-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7f94-106">Parameters</span></span>

 <span data-ttu-id="f7f94-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="f7f94-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="f7f94-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="f7f94-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="f7f94-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="f7f94-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="f7f94-110">[in] Pointeur vers le premier identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="f7f94-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="f7f94-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="f7f94-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="f7f94-112">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="f7f94-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="f7f94-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="f7f94-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="f7f94-114">[in] Pointeur vers le deuxième identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="f7f94-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="f7f94-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f7f94-115">_ulFlags_</span></span>
  
> <span data-ttu-id="f7f94-116">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="f7f94-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f7f94-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="f7f94-117">_lpulResult_</span></span>
  
> <span data-ttu-id="f7f94-118">[out] Pointeur vers le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="f7f94-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="f7f94-119">Le contenu de _lpulResult_ est défini à TRUE si les identificateurs de deux entrée font référence au même objet ; Sinon, le contenu est défini sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="f7f94-119">The contents of  _lpulResult_ are set to TRUE if the two entry identifiers refer to the same object; otherwise, the contents are set to FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f7f94-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f7f94-120">Return value</span></span>

<span data-ttu-id="f7f94-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="f7f94-121">S_OK</span></span> 
  
> <span data-ttu-id="f7f94-122">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f7f94-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f7f94-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f7f94-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="f7f94-124">Une ou les deux les identificateurs d’entrée passés avec les paramètres _lpEntryID1_ ou _lpEntryID2_ ne sont pas reconnus par n’importe quel fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f7f94-124">One or both of the entry identifiers passed in with the  _lpEntryID1_ or  _lpEntryID2_ parameters are not recognized by any address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f7f94-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="f7f94-125">Remarks</span></span>

<span data-ttu-id="f7f94-126">Applications clientes et fournisseurs appel au service la méthode **CompareEntryIDs** pour comparer deux identificateurs d’entrée qui appartient à un fournisseur de carnet d’adresses unique pour déterminer si elles font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="f7f94-126">Client applications and service providers call the **CompareEntryIDs** method to compare two entry identifiers that belongs to a single address book provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="f7f94-127">**CompareEntryIDs** est utile car un objet peut avoir plusieurs identificateurs d’entrée valide.</span><span class="sxs-lookup"><span data-stu-id="f7f94-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="f7f94-128">Cette situation peut se produire, par exemple, après avoir installé une nouvelle version d’un fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f7f94-128">This situation can occur, for example, after a new version of an address book provider is installed.</span></span> 
  
<span data-ttu-id="f7f94-129">MAPI passe cet appel vers le fournisseur de carnet d’adresses qui est chargé des identificateurs d’entrée, en déterminant le fournisseur approprié en faisant correspondre la structure [MAPIUID](mapiuid.md) dans les identificateurs d’entrée avec la structure **MAPIUID** enregistrée par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="f7f94-129">MAPI passes this call to the address book provider that is responsible for the entry identifiers, determining the appropriate provider by matching the [MAPIUID](mapiuid.md) structure in the entry identifiers with the **MAPIUID** structure registered by the provider.</span></span> 
  
<span data-ttu-id="f7f94-130">Si les identificateurs de deux entrée font référence au même objet, **CompareEntryIDs** définit le contenu du paramètre _lpulResult_ sur TRUE ; s’ils font référence à des objets différents, **CompareEntryIDs** définit la valeur sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="f7f94-130">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the contents of the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets the contents to FALSE.</span></span> <span data-ttu-id="f7f94-131">Dans les deux cas, **CompareEntryIDs** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="f7f94-131">In either case, **CompareEntryIDs** returns S_OK.</span></span> <span data-ttu-id="f7f94-132">Si **CompareEntryIDs** renvoie une erreur qui peut se produire si aucun fournisseur de carnet d’adresses n’a inscrit une structure **MAPIUID** qui correspond à celui dans les identificateurs d’entrée, fournisseurs et clients ne doivent pas aucune action en fonction des résultats de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="f7f94-132">If **CompareEntryIDs** returns an error, which can occur if no address book provider has registered a **MAPIUID** structure that matches the one in the entry identifiers, clients and providers should not take any action based on the result of the comparison.</span></span> <span data-ttu-id="f7f94-133">Au lieu de cela, ils adopter l’approche la plus traditionnelle à l’action en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f7f94-133">They should instead take the most conservative approach to the action being performed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f7f94-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7f94-134">See also</span></span>



[<span data-ttu-id="f7f94-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f7f94-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

