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
ms.openlocfilehash: c5b2d7db745cc270c0be7ee2184e86c6a4f97aad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594298"
---
# <a name="imslogoncompareentryids"></a><span data-ttu-id="1daea-103">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="1daea-103">IMSLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="1daea-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1daea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1daea-105">Compare deux identificateurs d’entrée pour déterminer si elles font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="1daea-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="1daea-106">MAPI fait référence à cet appel à un fournisseur de services uniquement si les identificateurs uniques (UID) dans les deux identificateurs d’entrée à comparer sont gérés par ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1daea-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="1daea-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1daea-107">Parameters</span></span>

 <span data-ttu-id="1daea-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="1daea-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="1daea-109">[in] La taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="1daea-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="1daea-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="1daea-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="1daea-111">[in] Pointeur vers le premier identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="1daea-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="1daea-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="1daea-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="1daea-113">[in] La taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="1daea-113">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="1daea-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="1daea-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="1daea-115">[in] Pointeur vers le deuxième identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="1daea-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="1daea-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1daea-116">_ulFlags_</span></span>
  
> <span data-ttu-id="1daea-117">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="1daea-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1daea-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="1daea-118">_lpulResult_</span></span>
  
> <span data-ttu-id="1daea-119">[out] Pointeur vers le résultat de la comparaison retourné.</span><span class="sxs-lookup"><span data-stu-id="1daea-119">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="1daea-120">TRUE si les identificateurs de deux entrée font référence au même objet ; Sinon, FALSE.</span><span class="sxs-lookup"><span data-stu-id="1daea-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1daea-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1daea-121">Return value</span></span>

<span data-ttu-id="1daea-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="1daea-122">S_OK</span></span> 
  
> <span data-ttu-id="1daea-123">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="1daea-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1daea-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="1daea-124">Remarks</span></span>

<span data-ttu-id="1daea-125">Fournisseurs de magasins de message implémentent la méthode **IMSLogon::CompareEntryIDs** pour comparer deux identificateurs d’entrée pour une entrée de donnée dans une banque de messages pour déterminer si elles font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="1daea-125">Message store providers implement the **IMSLogon::CompareEntryIDs** method to compare two entry identifiers for a given entry in a message store to determine whether they refer to the same object.</span></span> <span data-ttu-id="1daea-126">Si les identificateurs de deux entrée font référence au même objet, **CompareEntryIDs** définit le paramètre _lpulResult_ sur TRUE. s’ils font référence à des objets différents, **CompareEntryIDs** définit _lpulResult_ sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="1daea-126">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets  _lpulResult_ to FALSE.</span></span> 
  
 <span data-ttu-id="1daea-127">**CompareEntryIDs** est utile car un objet peut avoir plusieurs identificateurs d’entrée valide.</span><span class="sxs-lookup"><span data-stu-id="1daea-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="1daea-128">Par exemple, cela peut se produire après l’installation d’une nouvelle version d’un fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="1daea-128">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1daea-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1daea-129">See also</span></span>



[<span data-ttu-id="1daea-130">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1daea-130">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

