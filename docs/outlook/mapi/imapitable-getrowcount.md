---
title: IMAPITableGetRowCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetRowCount
api_type:
- COM
ms.assetid: 44a12c92-7462-4acf-9520-5d4c2d7f1d47
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b13bf3bdd8392efc42ad189e48dffad8636f0708
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425602"
---
# <a name="imapitablegetrowcount"></a><span data-ttu-id="38445-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="38445-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="38445-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38445-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38445-105">Renvoie le nombre total de lignes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="38445-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="38445-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38445-106">Parameters</span></span>

 <span data-ttu-id="38445-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="38445-107">_ulFlags_</span></span>
  
> <span data-ttu-id="38445-108">MSR doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="38445-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="38445-109">_lpulCount_</span><span class="sxs-lookup"><span data-stu-id="38445-109">_lpulCount_</span></span>
  
> <span data-ttu-id="38445-110">remarquer Pointeur vers le nombre de lignes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="38445-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="38445-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="38445-111">Return value</span></span>

<span data-ttu-id="38445-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="38445-112">S_OK</span></span> 
  
> <span data-ttu-id="38445-113">Le nombre de lignes a été correctement renvoyé.</span><span class="sxs-lookup"><span data-stu-id="38445-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="38445-114">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="38445-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="38445-115">Une autre opération est en cours, ce qui empêche le démarrage de l'opération de récupération du nombre de lignes.</span><span class="sxs-lookup"><span data-stu-id="38445-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="38445-116">L'opération en cours doit être autorisée ou elle doit être arrêtée.</span><span class="sxs-lookup"><span data-stu-id="38445-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="38445-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="38445-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="38445-118">Le tableau ne peut pas calculer le nombre de lignes.</span><span class="sxs-lookup"><span data-stu-id="38445-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="38445-119">MAPI_W_APPROX_COUNT</span><span class="sxs-lookup"><span data-stu-id="38445-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="38445-120">L'appel a réussi, mais un nombre approximatif de lignes a été renvoyé, car le nombre exact de lignes n'a pas pu être déterminé en raison de contraintes de mémoire.</span><span class="sxs-lookup"><span data-stu-id="38445-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="38445-121">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="38445-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="38445-122">Consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="38445-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38445-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="38445-123">Remarks</span></span>

<span data-ttu-id="38445-124">La méthode **IMAPITable:: GetRowCount** récupère le nombre total de lignes dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="38445-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="38445-125">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="38445-125">Notes to implementers</span></span>

<span data-ttu-id="38445-126">Si vous ne pouvez pas déterminer le nombre exact de lignes de la table, renvoyez MAPI_W_APPROX_COUNT et un nombre approximatif de lignes dans le contenu du paramètre _lpulCount_ .</span><span class="sxs-lookup"><span data-stu-id="38445-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="38445-127">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="38445-127">Notes to callers</span></span>

<span data-ttu-id="38445-128">Utilisez **GetRowCount** pour déterminer le nombre de lignes qu'une table contient avant d'appeler la méthode [IMAPITable:: QueryRows](imapitable-queryrows.md) pour extraire les données.</span><span class="sxs-lookup"><span data-stu-id="38445-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="38445-129">S'il y a moins de vingt lignes dans le tableau, il est possible d'appeler **QueryPosition** pour récupérer le tableau entier.</span><span class="sxs-lookup"><span data-stu-id="38445-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="38445-130">S'il y a plus de vingt lignes dans le tableau, envisagez d'effectuer plusieurs appels à **QueryPosition** et limitez le nombre de lignes extraites dans chaque appel.</span><span class="sxs-lookup"><span data-stu-id="38445-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="38445-131">Certaines tables ne prennent pas en charge **GetRowCount** et renvoient MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="38445-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="38445-132">Si **GetRowCount** n'est pas pris en charge, vous pouvez également appeler la méthode [IMAPITable:: QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="38445-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="38445-133">Avec les résultats d' **QueryPosition**, vous pouvez déterminer la relation entre la ligne active et la dernière ligne.</span><span class="sxs-lookup"><span data-stu-id="38445-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="38445-134">Lorsque **GetRowCount** renvoie MAPI_E_BUSY parce qu'il est temporairement incapable de récupérer un nombre de lignes, appelez la méthode [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md) .</span><span class="sxs-lookup"><span data-stu-id="38445-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="38445-135">Lorsque **WaitForCompletion** renvoie, essayez à nouveau l'appel à **GetRowCount**.</span><span class="sxs-lookup"><span data-stu-id="38445-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="38445-136">Pour détecter si une opération asynchrone est en cours, vous pouvez également appeler la méthode [IMAPITable:: GetStatus](imapitable-getstatus.md) et vérifier le contenu du paramètre _lpulTableState_ .</span><span class="sxs-lookup"><span data-stu-id="38445-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="38445-137">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="38445-137">MFCMAPI reference</span></span>

<span data-ttu-id="38445-138">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="38445-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="38445-139">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="38445-139">**File**</span></span>|<span data-ttu-id="38445-140">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="38445-140">**Function**</span></span>|<span data-ttu-id="38445-141">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="38445-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="38445-142">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="38445-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="38445-143">CopyFolderContents</span><span class="sxs-lookup"><span data-stu-id="38445-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="38445-144">MFCMAPI utilise la méthode **IMAPITable:: GetRowCount** pour déterminer le nombre de lignes contenues dans la table source de sorte que la mémoire puisse être allouée à l'exécution de la copie.</span><span class="sxs-lookup"><span data-stu-id="38445-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38445-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38445-145">See also</span></span>



[<span data-ttu-id="38445-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="38445-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="38445-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="38445-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="38445-148">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="38445-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="38445-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="38445-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="38445-150">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38445-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="38445-151">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="38445-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

