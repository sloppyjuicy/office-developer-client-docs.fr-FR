---
title: IMAPISupportCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompareEntryIDs
api_type:
- COM
ms.assetid: be6991d9-6353-4838-bc6b-39de51a94d8d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6c79943792c8c17ee007c39b5c5c215a6fbc0699
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331569"
---
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="1ff35-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="1ff35-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="1ff35-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ff35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ff35-105">Compare deux identificateurs d'entrée pour déterminer s'ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="1ff35-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="1ff35-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ff35-106">Parameters</span></span>

 <span data-ttu-id="1ff35-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="1ff35-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="1ff35-108">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="1ff35-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="1ff35-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="1ff35-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="1ff35-110">dans Pointeur vers le premier identificateur d'entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="1ff35-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="1ff35-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="1ff35-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="1ff35-112">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="1ff35-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="1ff35-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="1ff35-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="1ff35-114">dans Pointeur vers le deuxième identificateur d'entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="1ff35-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="1ff35-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1ff35-115">_ulFlags_</span></span>
  
> <span data-ttu-id="1ff35-116">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="1ff35-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1ff35-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="1ff35-117">_lpulResult_</span></span>
  
> <span data-ttu-id="1ff35-118">remarquer Pointeur vers le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="1ff35-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="1ff35-119">TRUE si les deux identificateurs d'entrée font référence au même objet; Sinon, FALSe.</span><span class="sxs-lookup"><span data-stu-id="1ff35-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1ff35-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1ff35-120">Return value</span></span>

<span data-ttu-id="1ff35-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ff35-121">S_OK</span></span> 
  
> <span data-ttu-id="1ff35-122">La comparaison a réussi.</span><span class="sxs-lookup"><span data-stu-id="1ff35-122">The comparison was successful.</span></span>
    
<span data-ttu-id="1ff35-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1ff35-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="1ff35-124">L'un des identificateurs d'entrée spécifiés en tant que paramètres ne fait pas référence à des objets valides, car ils ne sont pas actuellement ouverts et indisponibles.</span><span class="sxs-lookup"><span data-stu-id="1ff35-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ff35-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="1ff35-125">Remarks</span></span>

<span data-ttu-id="1ff35-126">La méthode **IMAPISupport:: CompareEntryIDs** est implémentée pour les objets de prise en charge du carnet d'adresses et du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="1ff35-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="1ff35-127">**CompareEntryIDs** compare deux identificateurs d'entrée qui appartiennent à un seul fournisseur de services pour déterminer s'ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="1ff35-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="1ff35-128">MAPI extrait la partie [MAPIUID](mapiuid.md) des identificateurs d'entrée afin de déterminer le fournisseur de services responsable des objets.</span><span class="sxs-lookup"><span data-stu-id="1ff35-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="1ff35-129">MAPI appelle ensuite la méthode **CompareEntryIDs** de l'objet Logon pour effectuer la comparaison.</span><span class="sxs-lookup"><span data-stu-id="1ff35-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1ff35-130">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="1ff35-130">Notes to callers</span></span>

 <span data-ttu-id="1ff35-131">**CompareEntryIDs** est utile, car un objet peut avoir plus d'un identificateur d'entrée valide.</span><span class="sxs-lookup"><span data-stu-id="1ff35-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="1ff35-132">Cette situation peut se produire, par exemple, après l'installation d'une nouvelle version d'un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="1ff35-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="1ff35-133">Si **CompareEntryIDs** renvoie une erreur, n'effectuez aucune action en fonction du résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="1ff35-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="1ff35-134">Au lieu de cela, adoptez l'approche la plus conservatrice possible.</span><span class="sxs-lookup"><span data-stu-id="1ff35-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="1ff35-135">**CompareEntryIDs** peut échouer si, par exemple, un ou les deux identificateurs d'entrée contiennent une structure **MAPIUID** incorrecte.</span><span class="sxs-lookup"><span data-stu-id="1ff35-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ff35-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ff35-136">See also</span></span>



[<span data-ttu-id="1ff35-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="1ff35-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="1ff35-138">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1ff35-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

