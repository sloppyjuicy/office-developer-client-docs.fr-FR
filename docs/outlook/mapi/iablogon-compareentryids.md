---
title: IABLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: cb4a38ff-2fdd-40ac-a613-12c3f11a1df9
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 48ddb5a7c4e013c03138b08d9dadcdc0991faeec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279607"
---
# <a name="iablogoncompareentryids"></a><span data-ttu-id="9336b-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="9336b-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="9336b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9336b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9336b-105">Compare deux identificateurs d'entrée pour déterminer s'ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="9336b-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulRet
);
```

## <a name="parameters"></a><span data-ttu-id="9336b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9336b-106">Parameters</span></span>

 <span data-ttu-id="9336b-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="9336b-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="9336b-108">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="9336b-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="9336b-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="9336b-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="9336b-110">dans Pointeur vers le premier identificateur d'entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="9336b-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="9336b-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="9336b-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="9336b-112">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="9336b-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="9336b-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="9336b-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="9336b-114">dans Pointeur vers le deuxième identificateur d'entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="9336b-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="9336b-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9336b-115">_ulFlags_</span></span>
  
> <span data-ttu-id="9336b-116">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="9336b-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9336b-117">_lpulRet_</span><span class="sxs-lookup"><span data-stu-id="9336b-117">_lpulRet_</span></span>
  
> <span data-ttu-id="9336b-118">remarquer Pointeur vers le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="9336b-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="9336b-119">TRUE pour indiquer que les deux identificateurs d'entrée font référence au même objet; Sinon, FALSe.</span><span class="sxs-lookup"><span data-stu-id="9336b-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9336b-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9336b-120">Return value</span></span>

<span data-ttu-id="9336b-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="9336b-121">S_OK</span></span> 
  
> <span data-ttu-id="9336b-122">Les identificateurs d'entrée ont été comparés avec succès.</span><span class="sxs-lookup"><span data-stu-id="9336b-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="9336b-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9336b-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="9336b-124">L'un des identificateurs d'entrée (ou les deux) n'appartient pas au fournisseur de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="9336b-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9336b-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="9336b-125">Remarks</span></span>

<span data-ttu-id="9336b-126">Les fournisseurs de carnets d'adresses implémentent la méthode **CompareEntryIDs** pour comparer deux identificateurs d'entrée afin de déterminer s'ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="9336b-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="9336b-127">**CompareEntryIDs** est utile, car un objet peut avoir plus d'un identificateur d'entrée valide; une telle situation peut se produire, par exemple, lorsque vous comparez un identificateur d'entrée à court terme à un identificateur d'entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="9336b-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="9336b-128">Pour plus d'informations sur la création d'identificateurs d'entrée, consultez la rubrique [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="9336b-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9336b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9336b-129">See also</span></span>



[<span data-ttu-id="9336b-130">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9336b-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

