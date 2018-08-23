---
title: IMAPITableQueryColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 86dfaa8fbc9ff24d38472f1339a22534086d890b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593745"
---
# <a name="imapitablequerycolumns"></a><span data-ttu-id="534c3-103">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="534c3-103">IMAPITable::QueryColumns</span></span>

  
  
<span data-ttu-id="534c3-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="534c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="534c3-105">Renvoie une liste de colonnes pour la table.</span><span class="sxs-lookup"><span data-stu-id="534c3-105">Returns a list of columns for the table.</span></span>
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="534c3-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="534c3-106">Parameters</span></span>

 <span data-ttu-id="534c3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="534c3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="534c3-108">[in] Masque de bits d’indicateurs qui indique la colonne dans laquelle la valeur doit être retournée.</span><span class="sxs-lookup"><span data-stu-id="534c3-108">[in] Bitmask of flags that indicates which column set should be returned.</span></span> <span data-ttu-id="534c3-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="534c3-109">The following flag can be set:</span></span>
    
<span data-ttu-id="534c3-110">TBL_ALL_COLUMNS</span><span class="sxs-lookup"><span data-stu-id="534c3-110">TBL_ALL_COLUMNS</span></span> 
  
> <span data-ttu-id="534c3-111">Le tableau doit renvoyer toutes les colonnes disponibles.</span><span class="sxs-lookup"><span data-stu-id="534c3-111">The table should return all available columns.</span></span>
    
 <span data-ttu-id="534c3-112">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="534c3-112">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="534c3-113">[out] Pointeur vers une structure [SPropTagArray](sproptagarray.md) contenant les balises de propriété pour la colonne valeur.</span><span class="sxs-lookup"><span data-stu-id="534c3-113">[out] Pointer to an [SPropTagArray](sproptagarray.md) structure containing the property tags for the column set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="534c3-114">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="534c3-114">Return value</span></span>

<span data-ttu-id="534c3-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="534c3-115">S_OK</span></span> 
  
> <span data-ttu-id="534c3-116">L’ensemble de la colonne a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="534c3-116">The column set was successfully returned.</span></span>
    
<span data-ttu-id="534c3-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="534c3-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="534c3-118">Une autre opération est en cours qui empêche la colonne définie opération de récupération de démarrage.</span><span class="sxs-lookup"><span data-stu-id="534c3-118">Another operation is in progress that prevents the column set retrieval operation from starting.</span></span> <span data-ttu-id="534c3-119">L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="534c3-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="534c3-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="534c3-120">Remarks</span></span>

<span data-ttu-id="534c3-121">La méthode **IMAPITable::QueryColumns** peut être appelée pour récupérer :</span><span class="sxs-lookup"><span data-stu-id="534c3-121">The **IMAPITable::QueryColumns** method can be called to retrieve:</span></span> 
  
- <span data-ttu-id="534c3-122">La colonne par défaut d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="534c3-122">The default column set for a table.</span></span>
    
- <span data-ttu-id="534c3-123">La colonne en cours défini pour une table, comme ouverte par un appel à la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="534c3-123">The current column set for a table, as established by a call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="534c3-124">La colonne complète d’une table, les colonnes qui sont disponibles, mais pas nécessairement partie de l’ensemble actuel.</span><span class="sxs-lookup"><span data-stu-id="534c3-124">The complete column set for a table, the columns that are available, but not necessarily part of the current set.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="534c3-125">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="534c3-125">Notes to callers</span></span>

<span data-ttu-id="534c3-126">Si vous ne définissez pas l’indicateur TBL_ALL_COLUMNS, **IMAPITable::QueryColumns** renvoie d’une table par défaut ou ensemble de colonnes en cours, selon que le tableau a été affecté par un appel à **IMAPITable::SetColumns**.</span><span class="sxs-lookup"><span data-stu-id="534c3-126">If you do not set the TBL_ALL_COLUMNS flag, **IMAPITable::QueryColumns** returns either a table's default or current column set, depending on whether the table has been affected by a call to **IMAPITable::SetColumns**.</span></span> <span data-ttu-id="534c3-127">**SetColumns** modifie l’ordre et la sélection des colonnes dans un ensemble de colonnes d’une table.</span><span class="sxs-lookup"><span data-stu-id="534c3-127">**SetColumns** changes the order and selection of columns in a table's column set.</span></span> 
  
<span data-ttu-id="534c3-128">Si vous définissez l’indicateur TBL_ALL_COLUMNS, **QueryColumns** renvoie toutes les colonnes qui sont susceptibles d’être dans l’ensemble de colonnes de la table.</span><span class="sxs-lookup"><span data-stu-id="534c3-128">If you set the TBL_ALL_COLUMNS flag, **QueryColumns** returns all of the columns that are capable of being in the table's column set.</span></span> 
  
<span data-ttu-id="534c3-129">Libérer de la mémoire pour le tableau de balise de propriété indiqué par le paramètre _lpPropTagArray_ en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="534c3-129">Free the memory for the property tag array pointed to by the  _lpPropTagArray_ parameter by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="534c3-130">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="534c3-130">MFCMAPI reference</span></span>

<span data-ttu-id="534c3-131">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="534c3-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="534c3-132">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="534c3-132">**File**</span></span>|<span data-ttu-id="534c3-133">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="534c3-133">**Function**</span></span>|<span data-ttu-id="534c3-134">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="534c3-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="534c3-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="534c3-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="534c3-136">CContentsTableListCtrl::DoSetColumns</span><span class="sxs-lookup"><span data-stu-id="534c3-136">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="534c3-137">MFCMAPI utilise la méthode **IMAPITable::QueryColumns** pour récupérer la colonne en cours d’une table afin que l’utilisateur peut le modifier.</span><span class="sxs-lookup"><span data-stu-id="534c3-137">MFCMAPI uses the **IMAPITable::QueryColumns** method to retrieve the current column set for a table so the user can edit it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="534c3-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="534c3-138">See also</span></span>



[<span data-ttu-id="534c3-139">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="534c3-139">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="534c3-140">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="534c3-140">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="534c3-141">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="534c3-141">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="534c3-142">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="534c3-142">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="534c3-143">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="534c3-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

