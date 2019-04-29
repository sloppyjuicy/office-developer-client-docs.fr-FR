---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ec305fc872d1bf1718592dabdd230617d50d3f54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434332"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="7b71f-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="7b71f-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="7b71f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b71f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b71f-105">Renvoie l'État et le type de la table.</span><span class="sxs-lookup"><span data-stu-id="7b71f-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="7b71f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b71f-106">Parameters</span></span>

 <span data-ttu-id="7b71f-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="7b71f-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="7b71f-108">remarquer Pointeur vers une valeur indiquant l'état de la table.</span><span class="sxs-lookup"><span data-stu-id="7b71f-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="7b71f-109">L'une des valeurs suivantes peut être renvoyée:</span><span class="sxs-lookup"><span data-stu-id="7b71f-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="7b71f-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="7b71f-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="7b71f-111">Aucune opération n'est en cours.</span><span class="sxs-lookup"><span data-stu-id="7b71f-111">No operations are in progress.</span></span>
    
<span data-ttu-id="7b71f-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="7b71f-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="7b71f-113">Le contenu de la table a expectantly modifié.</span><span class="sxs-lookup"><span data-stu-id="7b71f-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="7b71f-114">Cette valeur d'État n'est pas renvoyée pour les modifications résultant des opérations de tri ou de restriction.</span><span class="sxs-lookup"><span data-stu-id="7b71f-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="7b71f-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="7b71f-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="7b71f-116">Une erreur s'est produite lors d'une opération [IMAPITable:: Restrict](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="7b71f-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="7b71f-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="7b71f-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="7b71f-118">Une opération **IMAPITable:: Restrict** est en cours.</span><span class="sxs-lookup"><span data-stu-id="7b71f-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="7b71f-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="7b71f-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="7b71f-120">Une erreur s'est produite lors d'une opération [IMAPITable:: SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="7b71f-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="7b71f-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="7b71f-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="7b71f-122">Une opération **IMAPITable:: SetColumns** est en cours.</span><span class="sxs-lookup"><span data-stu-id="7b71f-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="7b71f-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="7b71f-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="7b71f-124">Une erreur s'est produite lors d'une opération [IMAPITable:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="7b71f-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="7b71f-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="7b71f-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="7b71f-126">Une opération **IMAPITable:: SortTable** est en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="7b71f-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="7b71f-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="7b71f-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="7b71f-128">remarquer Pointeur vers une valeur qui indique le type de la table.</span><span class="sxs-lookup"><span data-stu-id="7b71f-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="7b71f-129">L'un des trois types de tableau suivants peut être renvoyé:</span><span class="sxs-lookup"><span data-stu-id="7b71f-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="7b71f-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="7b71f-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="7b71f-131">Le contenu de la table est dynamique; les lignes et les valeurs de colonne peuvent changer lorsque les données sous-jacentes sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="7b71f-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="7b71f-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="7b71f-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="7b71f-133">Les lignes du tableau sont fixes, mais les valeurs des colonnes de ces lignes sont dynamiques et peuvent changer à mesure que les données sous-jacentes sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="7b71f-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="7b71f-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="7b71f-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="7b71f-135">Le tableau est statique et son contenu ne change pas lorsque les données sous-jacentes sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="7b71f-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7b71f-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7b71f-136">Return value</span></span>

<span data-ttu-id="7b71f-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="7b71f-137">S_OK</span></span> 
  
> <span data-ttu-id="7b71f-138">L'état de la table a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="7b71f-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7b71f-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="7b71f-139">Remarks</span></span>

<span data-ttu-id="7b71f-140">La méthode **IMAPTable:: GetStatus** récupère des informations sur le type et l'état actuel d'une table.</span><span class="sxs-lookup"><span data-stu-id="7b71f-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7b71f-141">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="7b71f-141">Notes to callers</span></span>

<span data-ttu-id="7b71f-142">Vous pouvez utiliser **GetStatus** conjointement avec trois autres méthodes **IMAPITable** pour surveiller l'état de ces opérations et déterminer l'effet sur le tableau.</span><span class="sxs-lookup"><span data-stu-id="7b71f-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="7b71f-143">Appelez **GetStatus** après avoir effectué l'un des appels de **IMAPITable** suivants:</span><span class="sxs-lookup"><span data-stu-id="7b71f-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="7b71f-144">[IMAPITable:: restreindre](imapitable-restrict.md) pour définir une restriction.</span><span class="sxs-lookup"><span data-stu-id="7b71f-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="7b71f-145">[IMAPITable:: SortTable](imapitable-sorttable.md) pour établir un ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="7b71f-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="7b71f-146">[IMAPITable:: SetColumns](imapitable-setcolumns.md) pour définir un jeu de colonnes.</span><span class="sxs-lookup"><span data-stu-id="7b71f-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="7b71f-147">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7b71f-147">MFCMAPI reference</span></span>

<span data-ttu-id="7b71f-148">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7b71f-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7b71f-149">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="7b71f-149">**File**</span></span>|<span data-ttu-id="7b71f-150">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="7b71f-150">**Function**</span></span>|<span data-ttu-id="7b71f-151">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="7b71f-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7b71f-152">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="7b71f-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="7b71f-153">CContentsTableListCtrl:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="7b71f-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="7b71f-154">MFCMAPI utilise la méthode **IMAPITable:: GetStatus** pour signaler l'état d'un tableau.</span><span class="sxs-lookup"><span data-stu-id="7b71f-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b71f-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b71f-155">See also</span></span>



[<span data-ttu-id="7b71f-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="7b71f-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="7b71f-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="7b71f-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="7b71f-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="7b71f-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="7b71f-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b71f-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="7b71f-160">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="7b71f-160">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

