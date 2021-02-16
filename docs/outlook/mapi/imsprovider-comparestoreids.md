---
title: IMSProviderCompareStoreIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 734e53c1e897c902c72319aa6f2d3d7af2d23fb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431707"
---
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="43260-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="43260-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="43260-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43260-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43260-105">Compare deux identificateurs d’entrée de magasin de messages pour déterminer s’ils font référence au même objet store.</span><span class="sxs-lookup"><span data-stu-id="43260-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
```cpp
HRESULT CompareStoreIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="43260-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43260-106">Parameters</span></span>

 <span data-ttu-id="43260-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="43260-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="43260-108">[in] Taille, en octets, de l’identificateur d’entrée pointé par  _le paramètre lpEntryID1_  _._</span><span class="sxs-lookup"><span data-stu-id="43260-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="43260-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="43260-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="43260-110">[in] Pointeur vers le premier identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="43260-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="43260-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="43260-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="43260-112">[in] Taille, en octets, de l’identificateur d’entrée pointé par  _le paramètre lpEntryID2_  _._</span><span class="sxs-lookup"><span data-stu-id="43260-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="43260-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="43260-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="43260-114">[in] Pointeur vers le deuxième identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="43260-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="43260-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="43260-115">_ulFlags_</span></span>
  
> <span data-ttu-id="43260-116">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="43260-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="43260-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="43260-117">_lpulResult_</span></span>
  
> <span data-ttu-id="43260-118">[out] Pointeur vers le résultat renvoyé de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="43260-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="43260-119">TRUE si les deux identificateurs d’entrée font référence au même objet ; sinon, FALSE.</span><span class="sxs-lookup"><span data-stu-id="43260-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="43260-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="43260-120">Return value</span></span>

<span data-ttu-id="43260-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="43260-121">S_OK</span></span> 
  
> <span data-ttu-id="43260-122">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="43260-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43260-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="43260-123">Remarks</span></span>

<span data-ttu-id="43260-124">MAPI appelle la méthode **IMSProvider::CompareStoreIDs** lorsqu’elle traite un appel à la méthode [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md)</span><span class="sxs-lookup"><span data-stu-id="43260-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="43260-125">**CompareStoreIDs** est appelée à ce stade pour déterminer la section de profil, le cas cas, est associée à la magasin de messages en cours d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="43260-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="43260-126">Un **appel CompareStoreIDs peut** être effectué lorsqu’aucune boutique de messages n’est ouverte pour un fournisseur de magasins particulier.</span><span class="sxs-lookup"><span data-stu-id="43260-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="43260-127">En outre, MAPI appelle **également CompareStoreIDs** lorsqu’il traite un appel de fournisseur de magasin à la méthode [IMAPISupport::OpenProfileSection.](imapisupport-openprofilesection.md)</span><span class="sxs-lookup"><span data-stu-id="43260-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="43260-128">Les identificateurs d’entrée comparés par **compares CompareStoreID** sont tous deux pour la bibliothèque de liens dynamiques (DLL) du fournisseur de magasins actuel et sont tous deux des identificateurs d’entrée de magasin non veloppés.</span><span class="sxs-lookup"><span data-stu-id="43260-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="43260-129">Pour plus d’informations sur l’habillage des identificateurs d’entrée de magasin, voir [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span><span class="sxs-lookup"><span data-stu-id="43260-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="43260-130">La comparaison des identificateurs d’entrée est utile, car un objet peut avoir plusieurs identificateurs d’entrée valides.</span><span class="sxs-lookup"><span data-stu-id="43260-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="43260-131">Cela peut se produire, par exemple, après l’installation d’une nouvelle version d’un fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="43260-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="43260-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43260-132">See also</span></span>



[<span data-ttu-id="43260-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="43260-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="43260-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="43260-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="43260-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="43260-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="43260-136">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="43260-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

