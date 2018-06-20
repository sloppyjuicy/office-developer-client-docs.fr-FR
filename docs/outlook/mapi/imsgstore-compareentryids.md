---
title: IMsgStoreCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.CompareEntryIDs
api_type:
- COM
ms.assetid: 33d70748-0d3f-4be4-bcb5-7ec048887944
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a1c5cdc67bc64f20dd8ba0a5e8682c5e2f97294f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784243"
---
# <a name="imsgstorecompareentryids"></a><span data-ttu-id="1cc15-103">IMsgStore::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="1cc15-103">IMsgStore::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="1cc15-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1cc15-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1cc15-105">Compare deux identificateurs d’entrée pour déterminer si elles font référence à la même entrée dans une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="1cc15-105">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span> <span data-ttu-id="1cc15-106">MAPI passe cet appel à un fournisseur de services uniquement si les identificateurs uniques (UID) dans les deux identificateurs d’entrée à comparer sont gérés par ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1cc15-106">MAPI passes this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="1cc15-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cc15-107">Parameters</span></span>

 <span data-ttu-id="1cc15-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="1cc15-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="1cc15-109">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="1cc15-109">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="1cc15-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="1cc15-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="1cc15-111">[in] Pointeur vers le premier identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="1cc15-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="1cc15-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="1cc15-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="1cc15-113">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="1cc15-113">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="1cc15-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="1cc15-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="1cc15-115">[in] Pointeur vers le deuxième identificateur d’entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="1cc15-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="1cc15-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1cc15-116">_ulFlags_</span></span>
  
> <span data-ttu-id="1cc15-117">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="1cc15-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1cc15-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="1cc15-118">_lpulResult_</span></span>
  
> <span data-ttu-id="1cc15-119">[out] Pointeur vers le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="1cc15-119">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="1cc15-120">TRUE si les identificateurs de deux entrée font référence au même objet ; Sinon, FALSE.</span><span class="sxs-lookup"><span data-stu-id="1cc15-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1cc15-121">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="1cc15-121">Return value</span></span>

<span data-ttu-id="1cc15-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="1cc15-122">S_OK</span></span> 
  
> <span data-ttu-id="1cc15-123">La comparaison a réussi.</span><span class="sxs-lookup"><span data-stu-id="1cc15-123">The comparison was successful.</span></span>
    
<span data-ttu-id="1cc15-124">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1cc15-124">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="1cc15-125">Un ou les deux les identificateurs d’entrée spécifiés comme paramètres ne font pas référence aux objets, éventuellement, car les objets correspondants sont non ouverts et non à présentent.</span><span class="sxs-lookup"><span data-stu-id="1cc15-125">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because the corresponding objects are unopened and unavailable at present.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1cc15-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="1cc15-126">Remarks</span></span>

<span data-ttu-id="1cc15-127">La méthode **IMsgStore::CompareEntryIDs** compare deux identificateurs d’entrée qui appartiennent à la banque de messages pour déterminer si elles font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="1cc15-127">The **IMsgStore::CompareEntryIDs** method compares two entry identifiers that belong to the message store to determine whether they refer to the same object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1cc15-128">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="1cc15-128">Notes to callers</span></span>

 <span data-ttu-id="1cc15-129">**CompareEntryIDs** est utile car un objet peut avoir plusieurs identificateurs d’entrée valide (par exemple, après avoir installé une nouvelle version d’un fournisseur de magasin de message).</span><span class="sxs-lookup"><span data-stu-id="1cc15-129">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier (for example, after a new version of a message store provider is installed).</span></span> 
  
<span data-ttu-id="1cc15-130">Si **CompareEntryIDs** renvoie une erreur, ne prend aucune action basée sur le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="1cc15-130">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="1cc15-131">Au lieu de cela, adoptez une approche plus prudente possible.</span><span class="sxs-lookup"><span data-stu-id="1cc15-131">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="1cc15-132">**CompareEntryIDs** peut échouer si, par exemple, un ou les deux les identificateurs d’entrée contient un non valide **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="1cc15-132">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contains an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1cc15-133">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1cc15-133">MFCMAPI reference</span></span>

<span data-ttu-id="1cc15-134">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1cc15-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1cc15-135">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="1cc15-135">**File**</span></span>|<span data-ttu-id="1cc15-136">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="1cc15-136">**Function**</span></span>|<span data-ttu-id="1cc15-137">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="1cc15-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1cc15-138">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="1cc15-138">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="1cc15-139">CBaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="1cc15-139">CBaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="1cc15-140">MFCMAPI utilise la méthode **IMsgStore::CompareEntryIDs** pour comparer les identificateurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1cc15-140">MFCMAPI uses the **IMsgStore::CompareEntryIDs** method to compare entry IDs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1cc15-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cc15-141">See also</span></span>



[<span data-ttu-id="1cc15-142">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="1cc15-142">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="1cc15-143">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1cc15-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="1cc15-144">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="1cc15-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

