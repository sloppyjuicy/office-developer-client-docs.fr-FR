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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4dfde82aa843072168288f4e0b0084dfccd5cd2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427814"
---
# <a name="imapisessioncompareentryids"></a><span data-ttu-id="ee901-103">IMAPISession::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="ee901-103">IMAPISession::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="ee901-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee901-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee901-105">Compare deux identificateurs d'entrée pour déterminer s'ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="ee901-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="ee901-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee901-106">Parameters</span></span>

 <span data-ttu-id="ee901-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="ee901-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="ee901-108">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="ee901-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="ee901-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="ee901-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="ee901-110">dans Pointeur vers le premier identificateur d'entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="ee901-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="ee901-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="ee901-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="ee901-112">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="ee901-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="ee901-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="ee901-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="ee901-114">dans Pointeur vers le deuxième identificateur d'entrée à comparer.</span><span class="sxs-lookup"><span data-stu-id="ee901-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="ee901-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee901-115">_ulFlags_</span></span>
  
> <span data-ttu-id="ee901-116">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="ee901-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ee901-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="ee901-117">_lpulResult_</span></span>
  
> <span data-ttu-id="ee901-118">remarquer Pointeur vers le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="ee901-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="ee901-119">TRUE si les deux identificateurs d'entrée font référence au même objet; Sinon, FALSe.</span><span class="sxs-lookup"><span data-stu-id="ee901-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ee901-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ee901-120">Return value</span></span>

<span data-ttu-id="ee901-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee901-121">S_OK</span></span> 
  
> <span data-ttu-id="ee901-122">La comparaison a réussi.</span><span class="sxs-lookup"><span data-stu-id="ee901-122">The comparison was successful.</span></span>
    
<span data-ttu-id="ee901-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ee901-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="ee901-124">L'un des identificateurs d'entrée spécifiés comme paramètres ne fait pas référence à des objets, probablement parce que ces objets ne sont pas ouverts et ne sont pas disponibles actuellement.</span><span class="sxs-lookup"><span data-stu-id="ee901-124">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because these objects are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee901-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="ee901-125">Remarks</span></span>

<span data-ttu-id="ee901-126">La méthode **IMAPISession:: CompareEntryIDs** compare deux identificateurs d'entrée qui appartiennent à un seul fournisseur de services pour déterminer s'ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="ee901-126">The **IMAPISession::CompareEntryIDs** method compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="ee901-127">MAPI extrait la partie [MAPIUID](mapiuid.md) des identificateurs d'entrée afin de déterminer le fournisseur de services responsable des objets, puis appelle la méthode **CompareEntryIDs** de l'objet Logon pour effectuer la comparaison.</span><span class="sxs-lookup"><span data-stu-id="ee901-127">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects and then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ee901-128">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="ee901-128">Notes to callers</span></span>

<span data-ttu-id="ee901-129">La méthode **CompareEntryIDs** est utile, car un objet peut avoir plusieurs identificateurs d'entrée valides.</span><span class="sxs-lookup"><span data-stu-id="ee901-129">The **CompareEntryIDs** method is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="ee901-130">Cette situation peut se produire, par exemple, après l'installation d'une nouvelle version d'un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="ee901-130">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="ee901-131">Si **CompareEntryIDs** renvoie une erreur, n'effectuez aucune action en fonction du résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="ee901-131">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="ee901-132">Au lieu de cela, adoptez l'approche la plus conservatrice possible.</span><span class="sxs-lookup"><span data-stu-id="ee901-132">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="ee901-133">**CompareEntryIDs** peut échouer si, par exemple, un ou les deux identificateurs d'entrée contiennent un **MAPIUID**non valide.</span><span class="sxs-lookup"><span data-stu-id="ee901-133">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ee901-134">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ee901-134">MFCMAPI reference</span></span>

<span data-ttu-id="ee901-135">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ee901-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ee901-136">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="ee901-136">**File**</span></span>|<span data-ttu-id="ee901-137">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="ee901-137">**Function**</span></span>|<span data-ttu-id="ee901-138">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="ee901-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ee901-139">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="ee901-139">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="ee901-140">CbaseDialog:: OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="ee901-140">CbaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="ee901-141">MFCMAPI utilise la méthode **IMAPISession:: CompareEntryIDs** pour comparer deux ID d'entrée entrés par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ee901-141">MFCMAPI uses the **IMAPISession::CompareEntryIDs** method to compare two entry IDs that a user enters.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee901-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee901-142">See also</span></span>



[<span data-ttu-id="ee901-143">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ee901-143">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ee901-144">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee901-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="ee901-145">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="ee901-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

