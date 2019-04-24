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
ms.openlocfilehash: 2a2439bae79b497f018391983e2c4b03a35eee70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348789"
---
# <a name="imsgstorecompareentryids"></a><span data-ttu-id="23aa9-103">IMsgStore::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="23aa9-103">IMsgStore::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="23aa9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23aa9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23aa9-105">Compare deux identificateurs d'entrée pour déterminer s'ils font référence à la même entrée dans une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="23aa9-105">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span> <span data-ttu-id="23aa9-106">MAPI transmet cet appel à un fournisseur de services uniquement si les identificateurs uniques (UID) dans les deux identificateurs d'entrée à comparer sont gérés par ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="23aa9-106">MAPI passes this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="23aa9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23aa9-107">Parameters</span></span>

 <span data-ttu-id="23aa9-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="23aa9-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="23aa9-109">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="23aa9-109">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="23aa9-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="23aa9-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="23aa9-111">dans Pointeur vers le premier identificateur d'entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="23aa9-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="23aa9-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="23aa9-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="23aa9-113">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="23aa9-113">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="23aa9-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="23aa9-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="23aa9-115">dans Pointeur vers le deuxième identificateur d'entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="23aa9-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="23aa9-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="23aa9-116">_ulFlags_</span></span>
  
> <span data-ttu-id="23aa9-117">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="23aa9-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="23aa9-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="23aa9-118">_lpulResult_</span></span>
  
> <span data-ttu-id="23aa9-119">remarquer Pointeur vers le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="23aa9-119">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="23aa9-120">TRUE si les deux identificateurs d'entrée font référence au même objet; Sinon, FALSe.</span><span class="sxs-lookup"><span data-stu-id="23aa9-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="23aa9-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="23aa9-121">Return value</span></span>

<span data-ttu-id="23aa9-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="23aa9-122">S_OK</span></span> 
  
> <span data-ttu-id="23aa9-123">La comparaison a réussi.</span><span class="sxs-lookup"><span data-stu-id="23aa9-123">The comparison was successful.</span></span>
    
<span data-ttu-id="23aa9-124">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="23aa9-124">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="23aa9-125">L'un des identificateurs d'entrée spécifiés comme paramètres ne fait pas référence aux objets, probablement parce que les objets correspondants ne sont pas ouverts et ne sont pas disponibles pour le moment.</span><span class="sxs-lookup"><span data-stu-id="23aa9-125">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because the corresponding objects are unopened and unavailable at present.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="23aa9-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="23aa9-126">Remarks</span></span>

<span data-ttu-id="23aa9-127">La méthode **IMsgStore:: CompareEntryIDs** compare deux identificateurs d'entrée qui appartiennent à la Banque de messages pour déterminer s'ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="23aa9-127">The **IMsgStore::CompareEntryIDs** method compares two entry identifiers that belong to the message store to determine whether they refer to the same object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="23aa9-128">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="23aa9-128">Notes to callers</span></span>

 <span data-ttu-id="23aa9-129">**CompareEntryIDs** est utile, car un objet peut avoir plusieurs identificateurs d'entrée valides (par exemple, après l'installation d'une nouvelle version d'un fournisseur de banque de messages).</span><span class="sxs-lookup"><span data-stu-id="23aa9-129">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier (for example, after a new version of a message store provider is installed).</span></span> 
  
<span data-ttu-id="23aa9-130">Si **CompareEntryIDs** renvoie une erreur, n'effectuez aucune action en fonction du résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="23aa9-130">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="23aa9-131">Au lieu de cela, adoptez l'approche la plus conservatrice possible.</span><span class="sxs-lookup"><span data-stu-id="23aa9-131">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="23aa9-132">**CompareEntryIDs** peut échouer si, par exemple, un ou les deux identificateurs d'entrée contiennent un **MAPIUID**non valide.</span><span class="sxs-lookup"><span data-stu-id="23aa9-132">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contains an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="23aa9-133">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="23aa9-133">MFCMAPI reference</span></span>

<span data-ttu-id="23aa9-134">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="23aa9-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="23aa9-135">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="23aa9-135">**File**</span></span>|<span data-ttu-id="23aa9-136">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="23aa9-136">**Function**</span></span>|<span data-ttu-id="23aa9-137">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="23aa9-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="23aa9-138">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="23aa9-138">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="23aa9-139">CBaseDialog:: OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="23aa9-139">CBaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="23aa9-140">MFCMAPI utilise la méthode **IMsgStore:: CompareEntryIDs** pour comparer les ID d'entrée.</span><span class="sxs-lookup"><span data-stu-id="23aa9-140">MFCMAPI uses the **IMsgStore::CompareEntryIDs** method to compare entry IDs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23aa9-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23aa9-141">See also</span></span>



[<span data-ttu-id="23aa9-142">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="23aa9-142">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="23aa9-143">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="23aa9-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="23aa9-144">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="23aa9-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

