---
title: BuildDisplayTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BuildDisplayTable
api_type:
- HeaderDef
ms.assetid: 0846415b-6fe1-4504-8620-108af6719015
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8c5e6078be05ff846b7737ff53e9a6338fcb2141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431595"
---
# <a name="builddisplaytable"></a><span data-ttu-id="e2d49-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="e2d49-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="e2d49-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2d49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2d49-105">Crée un tableau d’affichage à partir des données de page de propriétés contenues dans une ou plusieurs structures [DTPAGE.](dtpage.md)</span><span class="sxs-lookup"><span data-stu-id="e2d49-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2d49-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e2d49-106">Header file:</span></span>  <br/> |<span data-ttu-id="e2d49-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e2d49-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e2d49-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e2d49-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e2d49-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e2d49-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e2d49-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e2d49-110">Called by:</span></span>  <br/> |<span data-ttu-id="e2d49-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="e2d49-111">Service providers</span></span>  <br/> |
   
```cpp
STDAPI BuildDisplayTable(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpMalloc,
  HINSTANCE hInstance,
  UINT cPages,
  LPDTPAGE lpPage,
  ULONG ulFlags,
  LPMAPITABLE * lppTable,
  LPTABLEDATA * lppTblData
);
```

## <a name="parameters"></a><span data-ttu-id="e2d49-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2d49-112">Parameters</span></span>

 <span data-ttu-id="e2d49-113">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="e2d49-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="e2d49-114">[in] Pointeur vers la [fonction MAPIAllocateBuffer,](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e2d49-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="e2d49-115">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="e2d49-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="e2d49-116">[in] Pointeur vers la [fonction MAPIAllocateMore,](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="e2d49-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="e2d49-117">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="e2d49-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="e2d49-118">[in] Pointeur vers la [fonction MAPIFreeBuffer,](mapifreebuffer.md) à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e2d49-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="e2d49-119">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="e2d49-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="e2d49-120">Inutilisé ; doit être définie sur NULL.</span><span class="sxs-lookup"><span data-stu-id="e2d49-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="e2d49-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="e2d49-121">_hInstance_</span></span>
  
> <span data-ttu-id="e2d49-122">[in] Instance d’un objet MAPI à partir duquel **BuildDisplayTable** récupère des ressources.</span><span class="sxs-lookup"><span data-stu-id="e2d49-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="e2d49-123">_cPages_</span><span class="sxs-lookup"><span data-stu-id="e2d49-123">_cPages_</span></span>
  
> <span data-ttu-id="e2d49-124">[in] Nombre de structures [DTPAGE](dtpage.md) dans le tableau pointées par _le paramètre lpPage._</span><span class="sxs-lookup"><span data-stu-id="e2d49-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="e2d49-125">_lpPage_</span><span class="sxs-lookup"><span data-stu-id="e2d49-125">_lpPage_</span></span>
  
> <span data-ttu-id="e2d49-126">[in] Pointeur vers un tableau de structures **DTPAGE** qui contiennent des informations sur les pages du tableau d’affichage à construire.</span><span class="sxs-lookup"><span data-stu-id="e2d49-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="e2d49-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e2d49-127">_ulFlags_</span></span>
  
> <span data-ttu-id="e2d49-128">[in] Masque de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="e2d49-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="e2d49-129">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="e2d49-129">The following flag can be set:</span></span>
    
<span data-ttu-id="e2d49-130">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e2d49-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e2d49-131">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="e2d49-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="e2d49-132">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="e2d49-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="e2d49-133">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="e2d49-133">_lppTable_</span></span>
  
> <span data-ttu-id="e2d49-134">[out] Pointeur vers un pointeur vers le tableau d’affichage, qui expose l’interface [IMAPITable.](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="e2d49-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="e2d49-135">_lppTblData_</span><span class="sxs-lookup"><span data-stu-id="e2d49-135">_lppTblData_</span></span>
  
> <span data-ttu-id="e2d49-136">[in, out] Pointeur vers un pointeur vers un objet de données de table exposant [l’interface ITableData](itabledataiunknown.md) sur la table renvoyée dans _le paramètre lppTable._</span><span class="sxs-lookup"><span data-stu-id="e2d49-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="e2d49-137">Si aucun objet de données de table n’est souhaité,  _lppTblData_ doit être définie sur NULL au lieu d’une valeur de pointeur.</span><span class="sxs-lookup"><span data-stu-id="e2d49-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e2d49-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e2d49-138">Return value</span></span>

<span data-ttu-id="e2d49-139">Aucun</span><span class="sxs-lookup"><span data-stu-id="e2d49-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e2d49-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="e2d49-140">Remarks</span></span>

<span data-ttu-id="e2d49-141">MAPI utilise les fonctions pointées par  _lpAllocateBuffer_,  _lpAllocateMore_ et  _lpFreeBuffer_ pour la plupart de l’allocation et de la déallocation de la mémoire, en particulier pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel d’interfaces d’objets telles que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="e2d49-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e2d49-142">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="e2d49-142">Notes to callers</span></span>

<span data-ttu-id="e2d49-143">Tout ce qui est possible est lu à partir de la ressource de boîte de dialogue, notamment :</span><span class="sxs-lookup"><span data-stu-id="e2d49-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="e2d49-144">Titre de la page, le membre  _ulbLpszLabel_ de la structure [DTBLPAGE](dtblpage.md) lu à partir du titre de la boîte de dialogue dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="e2d49-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="e2d49-145">Tous les titres de contrôle, c’est-à-dire, les membres  _ulbLpszLabel_ des autres structures de contrôle lisent le texte du contrôle dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="e2d49-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="e2d49-146">**BuildDisplayTable** overwres anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span><span class="sxs-lookup"><span data-stu-id="e2d49-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="e2d49-147">Les appelants qui doivent le faire peuvent avoir **BuildDisplayTable** renvoyer l’objet de données de table  _dans lppTableData_ et y modifier des lignes ; ou ils peuvent créer la table d’affichage à la place dans un objet de données de table.</span><span class="sxs-lookup"><span data-stu-id="e2d49-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="e2d49-148">Si  _lppTableData_ n’est pas définie sur NULL, le fournisseur est chargé de libérer l’objet de données de table lorsqu’il a terminé avec le tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e2d49-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

