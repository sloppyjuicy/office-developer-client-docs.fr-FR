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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: cda3de1719ec1b7cfca1a9ecdad7bc3b59a8b17d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571149"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="16394-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="16394-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="16394-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16394-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16394-105">Renvoie l’état et le type de la table.</span><span class="sxs-lookup"><span data-stu-id="16394-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="16394-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16394-106">Parameters</span></span>

 <span data-ttu-id="16394-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="16394-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="16394-108">[out] Pointeur vers une valeur indiquant l’état de la table.</span><span class="sxs-lookup"><span data-stu-id="16394-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="16394-109">Une des valeurs suivantes peut être renvoyée :</span><span class="sxs-lookup"><span data-stu-id="16394-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="16394-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="16394-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="16394-111">Aucune opération n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="16394-111">No operations are in progress.</span></span>
    
<span data-ttu-id="16394-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="16394-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="16394-113">Le contenu de la table ont changé expectantly.</span><span class="sxs-lookup"><span data-stu-id="16394-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="16394-114">Cette valeur d’état n’est pas retournée pour que les modifications qui résultent des opérations de tri ou de restriction.</span><span class="sxs-lookup"><span data-stu-id="16394-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="16394-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="16394-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="16394-116">Une erreur s’est produite pendant une opération [IMAPITable](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="16394-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="16394-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="16394-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="16394-118">Une opération **IMAPITable** est en cours.</span><span class="sxs-lookup"><span data-stu-id="16394-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="16394-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="16394-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="16394-120">Une erreur s’est produite pendant une opération [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="16394-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="16394-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="16394-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="16394-122">Une opération **IMAPITable::SetColumns** est en cours.</span><span class="sxs-lookup"><span data-stu-id="16394-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="16394-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="16394-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="16394-124">Une erreur s’est produite pendant une opération [IMAPITable::SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="16394-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="16394-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="16394-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="16394-126">Une opération **IMAPITable::SortTable** est en cours.</span><span class="sxs-lookup"><span data-stu-id="16394-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="16394-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="16394-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="16394-128">[out] Pointeur vers une valeur qui indique le type de la table.</span><span class="sxs-lookup"><span data-stu-id="16394-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="16394-129">Un des types de trois tableau suivantes peut être renvoyé :</span><span class="sxs-lookup"><span data-stu-id="16394-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="16394-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="16394-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="16394-131">Le contenu de la table est dynamique ; les lignes et les valeurs de colonne peuvent changer en tant que les modifications de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="16394-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="16394-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="16394-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="16394-133">Les lignes dans le tableau sont fixe, mais les valeurs de colonnes dans les lignes sont dynamiques et peuvent changer lorsque les modifications de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="16394-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="16394-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="16394-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="16394-135">Le tableau est statique et son contenu n’est pas modifié lorsque les données sous-jacentes changent.</span><span class="sxs-lookup"><span data-stu-id="16394-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="16394-136">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="16394-136">Return value</span></span>

<span data-ttu-id="16394-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="16394-137">S_OK</span></span> 
  
> <span data-ttu-id="16394-138">L’état de la table a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="16394-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16394-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="16394-139">Remarks</span></span>

<span data-ttu-id="16394-140">La méthode **IMAPTable::GetStatus** récupère des informations sur le type et l’état actuel d’une table.</span><span class="sxs-lookup"><span data-stu-id="16394-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="16394-141">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="16394-141">Notes to callers</span></span>

<span data-ttu-id="16394-142">Vous pouvez utiliser **GetStatus** conjointement avec les trois autres méthodes **IMAPITable** pour surveiller l’état de ces opérations et de déterminer l’incidence sur le tableau.</span><span class="sxs-lookup"><span data-stu-id="16394-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="16394-143">Appelez **GetStatus** après avoir effectué une des appels **IMAPITable** suivants :</span><span class="sxs-lookup"><span data-stu-id="16394-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="16394-144">[IMAPITable](imapitable-restrict.md) pour définir une restriction.</span><span class="sxs-lookup"><span data-stu-id="16394-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="16394-145">[IMAPITable::SortTable](imapitable-sorttable.md) pour établir un ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="16394-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="16394-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) pour définir un ensemble de colonnes.</span><span class="sxs-lookup"><span data-stu-id="16394-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="16394-147">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="16394-147">MFCMAPI reference</span></span>

<span data-ttu-id="16394-148">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="16394-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="16394-149">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="16394-149">**File**</span></span>|<span data-ttu-id="16394-150">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="16394-150">**Function**</span></span>|<span data-ttu-id="16394-151">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="16394-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="16394-152">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="16394-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="16394-153">CContentsTableListCtrl::GetStatus</span><span class="sxs-lookup"><span data-stu-id="16394-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="16394-154">MFCMAPI utilise la méthode **IMAPITable::GetStatus** pour indiquer l’état d’une table.</span><span class="sxs-lookup"><span data-stu-id="16394-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="16394-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16394-155">See also</span></span>



[<span data-ttu-id="16394-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="16394-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="16394-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="16394-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="16394-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="16394-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="16394-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="16394-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="16394-160">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="16394-160">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

