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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b161c8c0da78b5ca872b87cad9a297169426d4cd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565003"
---
# <a name="iablogoncompareentryids"></a><span data-ttu-id="963ce-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="963ce-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="963ce-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="963ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="963ce-105">Compare deux identificateurs d’entrée pour déterminer si elles font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="963ce-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="963ce-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="963ce-106">Parameters</span></span>

 <span data-ttu-id="963ce-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="963ce-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="963ce-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="963ce-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="963ce-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="963ce-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="963ce-110">[in] Pointeur vers le premier identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="963ce-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="963ce-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="963ce-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="963ce-112">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="963ce-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="963ce-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="963ce-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="963ce-114">[in] Pointeur vers le deuxième identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="963ce-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="963ce-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="963ce-115">_ulFlags_</span></span>
  
> <span data-ttu-id="963ce-116">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="963ce-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="963ce-117">_lpulRet_</span><span class="sxs-lookup"><span data-stu-id="963ce-117">_lpulRet_</span></span>
  
> <span data-ttu-id="963ce-118">[out] Pointeur vers le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="963ce-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="963ce-119">TRUE pour indiquer que les identificateurs de deux entrée font référence au même objet ; Sinon, FALSE.</span><span class="sxs-lookup"><span data-stu-id="963ce-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="963ce-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="963ce-120">Return value</span></span>

<span data-ttu-id="963ce-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="963ce-121">S_OK</span></span> 
  
> <span data-ttu-id="963ce-122">Les identificateurs d’entrée ont été comparées avec succès.</span><span class="sxs-lookup"><span data-stu-id="963ce-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="963ce-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="963ce-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="963ce-124">Une ou les deux les identificateurs d’entrée n’appartiennent pas au fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="963ce-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="963ce-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="963ce-125">Remarks</span></span>

<span data-ttu-id="963ce-126">Fournisseurs de carnet d’adresses implémentent la méthode **CompareEntryIDs** pour comparer deux identificateurs d’entrée pour déterminer si elles font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="963ce-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="963ce-127">**CompareEntryIDs** est utile car un objet peut avoir plusieurs identificateurs d’entrée valide ; Cette situation peut se produire, par exemple, lorsque vous comparez un identificateur d’entrée à court terme avec un identificateur d’entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="963ce-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="963ce-128">Pour plus d’informations sur la création d’identificateurs d’entrée, voir [Identificateurs d’entrée MAPI](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="963ce-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="963ce-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="963ce-129">See also</span></span>



[<span data-ttu-id="963ce-130">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="963ce-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

