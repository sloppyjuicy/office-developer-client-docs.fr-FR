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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 734e53c1e897c902c72319aa6f2d3d7af2d23fb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317268"
---
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="0c2bc-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="0c2bc-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="0c2bc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c2bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c2bc-105">Compare deux identificateurs d'entrée de banque de messages pour déterminer s'ils font référence au même objet Store.</span><span class="sxs-lookup"><span data-stu-id="0c2bc-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="0c2bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c2bc-106">Parameters</span></span>

 <span data-ttu-id="0c2bc-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="0c2bc-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="0c2bc-108">dans Taille, en octets, de l'identificateur d'entrée pointé par le paramètre _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="0c2bc-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="0c2bc-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="0c2bc-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="0c2bc-110">dans Pointeur vers le premier identificateur d'entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="0c2bc-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="0c2bc-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="0c2bc-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="0c2bc-112">dans Taille, en octets, de l'identificateur d'entrée pointé par le paramètre _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="0c2bc-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="0c2bc-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="0c2bc-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="0c2bc-114">dans Pointeur vers le deuxième identificateur d'entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="0c2bc-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="0c2bc-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0c2bc-115">_ulFlags_</span></span>
  
> <span data-ttu-id="0c2bc-116">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="0c2bc-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0c2bc-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="0c2bc-117">_lpulResult_</span></span>
  
> <span data-ttu-id="0c2bc-118">remarquer Pointeur vers le résultat renvoyé de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="0c2bc-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="0c2bc-119">TRUE si les deux identificateurs d'entrée font référence au même objet; Sinon, FALSe.</span><span class="sxs-lookup"><span data-stu-id="0c2bc-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c2bc-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0c2bc-120">Return value</span></span>

<span data-ttu-id="0c2bc-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c2bc-121">S_OK</span></span> 
  
> <span data-ttu-id="0c2bc-122">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="0c2bc-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c2bc-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c2bc-123">Remarks</span></span>

<span data-ttu-id="0c2bc-124">MAPI appelle la méthode **IMSProvider:: CompareStoreIDs** lorsqu'il traite un appel à la méthode [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="0c2bc-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="0c2bc-125">**CompareStoreIDs** est appelé à ce stade pour déterminer quelle section de profil, le cas échéant, est associée à la Banque de messages en cours d'ouverture.</span><span class="sxs-lookup"><span data-stu-id="0c2bc-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="0c2bc-126">Un appel **CompareStoreIDs** peut être effectué lorsqu'aucun magasin de messages n'est ouvert pour un fournisseur de banque particulier.</span><span class="sxs-lookup"><span data-stu-id="0c2bc-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="0c2bc-127">De plus, MAPI appelle également **CompareStoreIDs** lorsqu'il traite un appel de fournisseur de banque à la méthode [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="0c2bc-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="0c2bc-128">Les identificateurs d'entrée comparés par **CompareStoreIDs** sont tous deux pour la bibliothèque de liens dynamiques (dll) du fournisseur de magasin actuel et sont tous deux des identificateurs d'entrée de magasin non enveloppés.</span><span class="sxs-lookup"><span data-stu-id="0c2bc-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="0c2bc-129">Pour plus d'informations sur les identificateurs d'entrée de magasin de contenu, voir [IMAPISupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span><span class="sxs-lookup"><span data-stu-id="0c2bc-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="0c2bc-130">La comparaison des identificateurs d'entrée est utile, car un objet peut avoir plusieurs identificateurs d'entrée valides.</span><span class="sxs-lookup"><span data-stu-id="0c2bc-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="0c2bc-131">Cela peut se produire, par exemple, après l'installation d'une nouvelle version d'un fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="0c2bc-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c2bc-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c2bc-132">See also</span></span>



[<span data-ttu-id="0c2bc-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="0c2bc-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="0c2bc-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="0c2bc-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="0c2bc-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="0c2bc-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="0c2bc-136">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c2bc-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

