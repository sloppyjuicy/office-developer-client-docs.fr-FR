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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 4196ed8b949ecb9e23c4bd34380db9cc5a369e23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348726"
---
# <a name="imslogoncompareentryids"></a><span data-ttu-id="abcf4-103">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="abcf4-103">IMSLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="abcf4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abcf4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abcf4-105">Compare deux identificateurs d'entrée pour déterminer s'ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="abcf4-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="abcf4-106">MAPI renvoie cet appel à un fournisseur de services uniquement si les identificateurs uniques (UID) dans les deux identificateurs d'entrée à comparer sont gérés par ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="abcf4-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="abcf4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abcf4-107">Parameters</span></span>

 <span data-ttu-id="abcf4-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="abcf4-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="abcf4-109">dans Taille, en octets, de l'identificateur d'entrée pointé par le paramètre _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="abcf4-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="abcf4-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="abcf4-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="abcf4-111">dans Pointeur vers le premier identificateur d'entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="abcf4-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="abcf4-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="abcf4-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="abcf4-113">dans Taille, en octets, de l'identificateur d'entrée pointé par le paramètre _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="abcf4-113">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="abcf4-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="abcf4-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="abcf4-115">dans Pointeur vers le deuxième identificateur d'entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="abcf4-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="abcf4-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="abcf4-116">_ulFlags_</span></span>
  
> <span data-ttu-id="abcf4-117">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="abcf4-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="abcf4-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="abcf4-118">_lpulResult_</span></span>
  
> <span data-ttu-id="abcf4-119">remarquer Pointeur vers le résultat renvoyé de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="abcf4-119">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="abcf4-120">TRUE si les deux identificateurs d'entrée font référence au même objet; Sinon, FALSe.</span><span class="sxs-lookup"><span data-stu-id="abcf4-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="abcf4-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="abcf4-121">Return value</span></span>

<span data-ttu-id="abcf4-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="abcf4-122">S_OK</span></span> 
  
> <span data-ttu-id="abcf4-123">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="abcf4-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="abcf4-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="abcf4-124">Remarks</span></span>

<span data-ttu-id="abcf4-125">Les fournisseurs de banque de messages implémentent la méthode **IMSLogon:: CompareEntryIDs** pour comparer deux identificateurs d'entrée pour une entrée donnée dans une banque de messages afin de déterminer s'ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="abcf4-125">Message store providers implement the **IMSLogon::CompareEntryIDs** method to compare two entry identifiers for a given entry in a message store to determine whether they refer to the same object.</span></span> <span data-ttu-id="abcf4-126">Si les deux identificateurs d'entrée font référence au même objet, **CompareEntryIDs** définit le paramètre _lpulResult_ sur true; s'ils font référence à des objets différents, **CompareEntryIDs** définit _lpulResult_ sur false.</span><span class="sxs-lookup"><span data-stu-id="abcf4-126">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets  _lpulResult_ to FALSE.</span></span> 
  
 <span data-ttu-id="abcf4-127">**CompareEntryIDs** est utile, car un objet peut avoir plus d'un identificateur d'entrée valide.</span><span class="sxs-lookup"><span data-stu-id="abcf4-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="abcf4-128">Cela peut se produire, par exemple, après l'installation d'une nouvelle version d'un fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="abcf4-128">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="abcf4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abcf4-129">See also</span></span>



[<span data-ttu-id="abcf4-130">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="abcf4-130">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

