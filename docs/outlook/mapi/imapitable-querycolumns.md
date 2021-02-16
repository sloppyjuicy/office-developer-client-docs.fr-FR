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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d142e19fc4721cec4dde0df7fc030a001121da63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410104"
---
# <a name="imapitablequerycolumns"></a><span data-ttu-id="c5628-103">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="c5628-103">IMAPITable::QueryColumns</span></span>

  
  
<span data-ttu-id="c5628-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5628-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5628-105">Renvoie une liste de colonnes pour le tableau.</span><span class="sxs-lookup"><span data-stu-id="c5628-105">Returns a list of columns for the table.</span></span>
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="c5628-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5628-106">Parameters</span></span>

 <span data-ttu-id="c5628-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c5628-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c5628-108">[in] Masque de bits d’indicateurs qui indique quel jeu de colonnes doit être renvoyé.</span><span class="sxs-lookup"><span data-stu-id="c5628-108">[in] Bitmask of flags that indicates which column set should be returned.</span></span> <span data-ttu-id="c5628-109">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="c5628-109">The following flag can be set:</span></span>
    
<span data-ttu-id="c5628-110">TBL_ALL_COLUMNS</span><span class="sxs-lookup"><span data-stu-id="c5628-110">TBL_ALL_COLUMNS</span></span> 
  
> <span data-ttu-id="c5628-111">Le tableau doit renvoyer toutes les colonnes disponibles.</span><span class="sxs-lookup"><span data-stu-id="c5628-111">The table should return all available columns.</span></span>
    
 <span data-ttu-id="c5628-112">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="c5628-112">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="c5628-113">[out] Pointeur vers une structure [SPropTagArray](sproptagarray.md) contenant les balises de propriété pour le jeu de colonnes.</span><span class="sxs-lookup"><span data-stu-id="c5628-113">[out] Pointer to an [SPropTagArray](sproptagarray.md) structure containing the property tags for the column set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c5628-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c5628-114">Return value</span></span>

<span data-ttu-id="c5628-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="c5628-115">S_OK</span></span> 
  
> <span data-ttu-id="c5628-116">Le jeu de colonnes a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="c5628-116">The column set was successfully returned.</span></span>
    
<span data-ttu-id="c5628-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="c5628-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="c5628-118">Une autre opération est en cours qui empêche le démarrage de l’opération de récupération du jeu de colonnes.</span><span class="sxs-lookup"><span data-stu-id="c5628-118">Another operation is in progress that prevents the column set retrieval operation from starting.</span></span> <span data-ttu-id="c5628-119">L’opération en cours doit être autorisée ou arrêtée.</span><span class="sxs-lookup"><span data-stu-id="c5628-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c5628-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5628-120">Remarks</span></span>

<span data-ttu-id="c5628-121">La **méthode IMAPITable::QueryColumns** peut être appelée pour récupérer :</span><span class="sxs-lookup"><span data-stu-id="c5628-121">The **IMAPITable::QueryColumns** method can be called to retrieve:</span></span> 
  
- <span data-ttu-id="c5628-122">Colonne par défaut définie pour un tableau.</span><span class="sxs-lookup"><span data-stu-id="c5628-122">The default column set for a table.</span></span>
    
- <span data-ttu-id="c5628-123">Colonne actuelle définie pour une table, tel qu’établi par un appel à la méthode [IMAPITable::SetColumns.](imapitable-setcolumns.md)</span><span class="sxs-lookup"><span data-stu-id="c5628-123">The current column set for a table, as established by a call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="c5628-124">Ensemble de colonnes complet d’un tableau, colonnes disponibles, mais pas nécessairement partie de l’ensemble actuel.</span><span class="sxs-lookup"><span data-stu-id="c5628-124">The complete column set for a table, the columns that are available, but not necessarily part of the current set.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="c5628-125">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="c5628-125">Notes to callers</span></span>

<span data-ttu-id="c5628-126">Si vous ne définissez pas l’indicateur TBL_ALL_COLUMNS, **IMAPITable::QueryColumns** renvoie l’ensemble de colonnes par défaut ou actuel d’une table, selon que la table a été affectée par un appel à **IMAPITable::SetColumns**.</span><span class="sxs-lookup"><span data-stu-id="c5628-126">If you do not set the TBL_ALL_COLUMNS flag, **IMAPITable::QueryColumns** returns either a table's default or current column set, depending on whether the table has been affected by a call to **IMAPITable::SetColumns**.</span></span> <span data-ttu-id="c5628-127">**SetColumns** modifie l’ordre et la sélection des colonnes dans le jeu de colonnes d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="c5628-127">**SetColumns** changes the order and selection of columns in a table's column set.</span></span> 
  
<span data-ttu-id="c5628-128">Si vous définissez l’TBL_ALL_COLUMNS, **QueryColumns** renvoie toutes les colonnes pouvant être dans le jeu de colonnes de la table.</span><span class="sxs-lookup"><span data-stu-id="c5628-128">If you set the TBL_ALL_COLUMNS flag, **QueryColumns** returns all of the columns that are capable of being in the table's column set.</span></span> 
  
<span data-ttu-id="c5628-129">Libérez la mémoire du tableau de balises de propriétés pointé par le paramètre _lpPropTagArray_ en appelant la [fonction MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="c5628-129">Free the memory for the property tag array pointed to by the  _lpPropTagArray_ parameter by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c5628-130">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c5628-130">MFCMAPI reference</span></span>

<span data-ttu-id="c5628-131">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c5628-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c5628-132">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="c5628-132">**File**</span></span>|<span data-ttu-id="c5628-133">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="c5628-133">**Function**</span></span>|<span data-ttu-id="c5628-134">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="c5628-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c5628-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="c5628-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="c5628-136">CContentsTableListCtrl::D oSetColumns</span><span class="sxs-lookup"><span data-stu-id="c5628-136">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="c5628-137">MFCMAPI utilise la méthode **IMAPITable::QueryColumns** pour récupérer le jeu de colonnes actuel d’une table afin que l’utilisateur puisse la modifier.</span><span class="sxs-lookup"><span data-stu-id="c5628-137">MFCMAPI uses the **IMAPITable::QueryColumns** method to retrieve the current column set for a table so the user can edit it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5628-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5628-138">See also</span></span>



[<span data-ttu-id="c5628-139">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="c5628-139">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="c5628-140">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c5628-140">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c5628-141">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="c5628-141">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="c5628-142">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c5628-142">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="c5628-143">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="c5628-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

