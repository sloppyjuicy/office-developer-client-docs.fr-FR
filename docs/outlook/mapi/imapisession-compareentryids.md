---
title: IMAPISessionCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: df6347298aab5404ec69bd9ac876863e31b741d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783944"
---
# <a name="imapisessioncompareentryids"></a><span data-ttu-id="4b9f2-103">IMAPISession::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="4b9f2-103">IMAPISession::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="4b9f2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4b9f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4b9f2-105">Compare deux identificateurs d’entrée pour déterminer si elles font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="4b9f2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b9f2-106">Parameters</span></span>

 <span data-ttu-id="4b9f2-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="4b9f2-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="4b9f2-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="4b9f2-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="4b9f2-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="4b9f2-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="4b9f2-110">[in] Pointeur vers le premier identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="4b9f2-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="4b9f2-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="4b9f2-112">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="4b9f2-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="4b9f2-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="4b9f2-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="4b9f2-114">[in] Pointeur vers le deuxième identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="4b9f2-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4b9f2-115">_ulFlags_</span></span>
  
> <span data-ttu-id="4b9f2-116">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4b9f2-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="4b9f2-117">_lpulResult_</span></span>
  
> <span data-ttu-id="4b9f2-118">[out] Pointeur vers le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="4b9f2-119">TRUE si les identificateurs de deux entrée font référence au même objet ; Sinon, FALSE.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4b9f2-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="4b9f2-120">Return value</span></span>

<span data-ttu-id="4b9f2-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="4b9f2-121">S_OK</span></span> 
  
> <span data-ttu-id="4b9f2-122">La comparaison a réussi.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-122">The comparison was successful.</span></span>
    
<span data-ttu-id="4b9f2-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4b9f2-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="4b9f2-124">Une ou les deux les identificateurs d’entrée spécifiés en tant que paramètres ne font pas référencent aux objets, éventuellement, car ces objets sont actuellement non ouverts et non disponible.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-124">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because these objects are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b9f2-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="4b9f2-125">Remarks</span></span>

<span data-ttu-id="4b9f2-126">La méthode **IMAPISession::CompareEntryIDs** compare deux identificateurs d’entrée qui appartiennent à un fournisseur de service unique pour déterminer si elles font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-126">The **IMAPISession::CompareEntryIDs** method compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="4b9f2-127">MAPI extrait la partie [MAPIUID](mapiuid.md) les identificateurs d’entrée pour déterminer le fournisseur de services responsable pour les objets et appelle ensuite la méthode **CompareEntryIDs** de l’objet de son ouverture de session pour effectuer la comparaison.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-127">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects and then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4b9f2-128">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="4b9f2-128">Notes to callers</span></span>

<span data-ttu-id="4b9f2-129">La méthode **CompareEntryIDs** est utile car un objet peut avoir plusieurs identificateurs d’entrée valide.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-129">The **CompareEntryIDs** method is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="4b9f2-130">Cette situation peut se produire, par exemple, après avoir installé une nouvelle version d’un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-130">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="4b9f2-131">Si **CompareEntryIDs** renvoie une erreur, ne prend aucune action basée sur le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-131">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="4b9f2-132">Au lieu de cela, adoptez une approche plus prudente possible.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-132">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="4b9f2-133">**CompareEntryIDs** peut échouer si, par exemple, un ou les deux les identificateurs d’entrée contient un non valide **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-133">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4b9f2-134">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4b9f2-134">MFCMAPI reference</span></span>

<span data-ttu-id="4b9f2-135">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4b9f2-136">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="4b9f2-136">**File**</span></span>|<span data-ttu-id="4b9f2-137">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="4b9f2-137">**Function**</span></span>|<span data-ttu-id="4b9f2-138">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="4b9f2-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4b9f2-139">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="4b9f2-139">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="4b9f2-140">CbaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="4b9f2-140">CbaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="4b9f2-141">MFCMAPI utilise la méthode **IMAPISession::CompareEntryIDs** pour comparer deux identificateurs d’entrée par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4b9f2-141">MFCMAPI uses the **IMAPISession::CompareEntryIDs** method to compare two entry IDs that a user enters.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b9f2-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b9f2-142">See also</span></span>



[<span data-ttu-id="4b9f2-143">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="4b9f2-143">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="4b9f2-144">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4b9f2-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="4b9f2-145">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="4b9f2-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

