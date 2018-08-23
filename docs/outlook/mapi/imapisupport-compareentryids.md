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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9dbf02fc94519d40431fb6bd493ef8e68df59d11
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566543"
---
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="79acf-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="79acf-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="79acf-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79acf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79acf-105">Compare deux identificateurs d’entrée pour déterminer si elles font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="79acf-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="79acf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79acf-106">Parameters</span></span>

 <span data-ttu-id="79acf-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="79acf-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="79acf-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="79acf-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="79acf-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="79acf-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="79acf-110">[in] Pointeur vers le premier identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="79acf-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="79acf-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="79acf-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="79acf-112">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="79acf-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="79acf-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="79acf-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="79acf-114">[in] Pointeur vers le deuxième identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="79acf-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="79acf-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="79acf-115">_ulFlags_</span></span>
  
> <span data-ttu-id="79acf-116">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="79acf-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="79acf-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="79acf-117">_lpulResult_</span></span>
  
> <span data-ttu-id="79acf-118">[out] Pointeur vers le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="79acf-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="79acf-119">TRUE si les identificateurs de deux entrée font référence au même objet ; Sinon, FALSE.</span><span class="sxs-lookup"><span data-stu-id="79acf-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="79acf-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="79acf-120">Return value</span></span>

<span data-ttu-id="79acf-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="79acf-121">S_OK</span></span> 
  
> <span data-ttu-id="79acf-122">La comparaison a réussi.</span><span class="sxs-lookup"><span data-stu-id="79acf-122">The comparison was successful.</span></span>
    
<span data-ttu-id="79acf-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="79acf-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="79acf-124">Une ou les deux les identificateurs d’entrée spécifiés en tant que paramètres ne font pas référencent aux objets valides, éventuellement, car ils sont en cours non ouverts et non disponible.</span><span class="sxs-lookup"><span data-stu-id="79acf-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="79acf-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="79acf-125">Remarks</span></span>

<span data-ttu-id="79acf-126">La méthode **IMAPISupport::CompareEntryIDs** est implémentée pour adresse livre et message fournisseur prise en charge des objets store.</span><span class="sxs-lookup"><span data-stu-id="79acf-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="79acf-127">**CompareEntryIDs** compare deux identificateurs d’entrée qui appartiennent à un fournisseur de service unique pour déterminer si elles font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="79acf-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="79acf-128">MAPI extrait la partie [MAPIUID](mapiuid.md) les identificateurs d’entrée pour déterminer le fournisseur de services responsable pour les objets.</span><span class="sxs-lookup"><span data-stu-id="79acf-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="79acf-129">MAPI appelle ensuite la méthode **CompareEntryIDs** de l’objet de son ouverture de session pour effectuer la comparaison.</span><span class="sxs-lookup"><span data-stu-id="79acf-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="79acf-130">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="79acf-130">Notes to callers</span></span>

 <span data-ttu-id="79acf-131">**CompareEntryIDs** est utile car un objet peut avoir plusieurs identificateurs d’entrée valide.</span><span class="sxs-lookup"><span data-stu-id="79acf-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="79acf-132">Cette situation peut se produire, par exemple, après avoir installé une nouvelle version d’un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="79acf-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="79acf-133">Si **CompareEntryIDs** renvoie une erreur, ne prend aucune action basée sur le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="79acf-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="79acf-134">Au lieu de cela, adoptez une approche plus prudente possible.</span><span class="sxs-lookup"><span data-stu-id="79acf-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="79acf-135">**CompareEntryIDs** peut échouer si, par exemple, un ou les deux les identificateurs d’entrée contient une structure **MAPIUID** non valide.</span><span class="sxs-lookup"><span data-stu-id="79acf-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79acf-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79acf-136">See also</span></span>



[<span data-ttu-id="79acf-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="79acf-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="79acf-138">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="79acf-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

