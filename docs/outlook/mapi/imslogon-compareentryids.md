---
title: IMSLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: 481812d6-8e94-4510-b288-55501dd5757c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4196ed8b949ecb9e23c4bd34380db9cc5a369e23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410132"
---
# <a name="imslogoncompareentryids"></a><span data-ttu-id="f0cea-103">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="f0cea-103">IMSLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="f0cea-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0cea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0cea-105">Compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="f0cea-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="f0cea-106">MAPI fait référence à cet appel à un fournisseur de services uniquement si les identificateurs uniques (IUD) des deux identificateurs d’entrée à comparer sont gérés par ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f0cea-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="f0cea-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="f0cea-107">Parameters</span></span>

 <span data-ttu-id="f0cea-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="f0cea-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="f0cea-109">[in] Taille, en octets, de l’identificateur d’entrée pointé par  _le paramètre lpEntryID1_  _._</span><span class="sxs-lookup"><span data-stu-id="f0cea-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="f0cea-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="f0cea-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="f0cea-111">[in] Pointeur vers le premier identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="f0cea-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="f0cea-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="f0cea-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="f0cea-113">[in] Taille, en octets, de l’identificateur d’entrée pointé par  _le paramètre lpEntryID2_  _._</span><span class="sxs-lookup"><span data-stu-id="f0cea-113">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="f0cea-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="f0cea-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="f0cea-115">[in] Pointeur vers le deuxième identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="f0cea-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="f0cea-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f0cea-116">_ulFlags_</span></span>
  
> <span data-ttu-id="f0cea-117">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="f0cea-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f0cea-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="f0cea-118">_lpulResult_</span></span>
  
> <span data-ttu-id="f0cea-119">[out] Pointeur vers le résultat renvoyé de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="f0cea-119">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="f0cea-120">TRUE si les deux identificateurs d’entrée font référence au même objet ; sinon, FALSE.</span><span class="sxs-lookup"><span data-stu-id="f0cea-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f0cea-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f0cea-121">Return value</span></span>

<span data-ttu-id="f0cea-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="f0cea-122">S_OK</span></span> 
  
> <span data-ttu-id="f0cea-123">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f0cea-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f0cea-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="f0cea-124">Remarks</span></span>

<span data-ttu-id="f0cea-125">Les fournisseurs de magasins de messages implémentent la méthode **IMSLogon::CompareEntryIDs** pour comparer deux identificateurs d’entrée pour une entrée donnée dans une magasin de messages afin de déterminer s’ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="f0cea-125">Message store providers implement the **IMSLogon::CompareEntryIDs** method to compare two entry identifiers for a given entry in a message store to determine whether they refer to the same object.</span></span> <span data-ttu-id="f0cea-126">Si les deux identificateurs d’entrée font référence au même objet, **CompareEntryIDs** définit le paramètre  _lpulResult_ sur TRUE ; S’ils font référence à différents objets, **CompareEntryIDs** définit  _lpulResult_ sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="f0cea-126">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets  _lpulResult_ to FALSE.</span></span> 
  
 <span data-ttu-id="f0cea-127">**CompareEntryIDs est utile** car un objet peut avoir plusieurs identificateurs d’entrée valides.</span><span class="sxs-lookup"><span data-stu-id="f0cea-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="f0cea-128">Cela peut se produire, par exemple, après l’installation d’une nouvelle version d’un fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="f0cea-128">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f0cea-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0cea-129">See also</span></span>



[<span data-ttu-id="f0cea-130">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f0cea-130">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

