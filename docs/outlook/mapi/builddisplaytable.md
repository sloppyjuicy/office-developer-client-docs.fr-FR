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
# <a name="builddisplaytable"></a><span data-ttu-id="70321-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="70321-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="70321-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70321-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70321-105">Crée une table d'affichage à partir des données de la page de propriétés contenues dans une ou plusieurs structures [DTPAGE](dtpage.md) .</span><span class="sxs-lookup"><span data-stu-id="70321-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="70321-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="70321-106">Header file:</span></span>  <br/> |<span data-ttu-id="70321-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="70321-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="70321-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="70321-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="70321-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="70321-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="70321-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="70321-110">Called by:</span></span>  <br/> |<span data-ttu-id="70321-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="70321-111">Service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="70321-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70321-112">Parameters</span></span>

 <span data-ttu-id="70321-113">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="70321-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="70321-114">dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="70321-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="70321-115">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="70321-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="70321-116">dans Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="70321-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="70321-117">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="70321-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="70321-118">dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="70321-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="70321-119">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="70321-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="70321-120">Inutilisés doit être défini sur NULL.</span><span class="sxs-lookup"><span data-stu-id="70321-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="70321-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="70321-121">_hInstance_</span></span>
  
> <span data-ttu-id="70321-122">dans Instance d'un objet MAPI à partir de laquelle **BuildDisplayTable** récupère des ressources.</span><span class="sxs-lookup"><span data-stu-id="70321-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="70321-123">_cPages_</span><span class="sxs-lookup"><span data-stu-id="70321-123">_cPages_</span></span>
  
> <span data-ttu-id="70321-124">dans Nombre de structures [DTPAGE](dtpage.md) dans le tableau vers lequel pointe le paramètre _lpPage_ .</span><span class="sxs-lookup"><span data-stu-id="70321-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="70321-125">_lpPage_</span><span class="sxs-lookup"><span data-stu-id="70321-125">_lpPage_</span></span>
  
> <span data-ttu-id="70321-126">dans Pointeur vers un tableau de structures **DTPAGE** qui contiennent des informations sur les pages de table d'affichage à créer.</span><span class="sxs-lookup"><span data-stu-id="70321-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="70321-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="70321-127">_ulFlags_</span></span>
  
> <span data-ttu-id="70321-128">dans Masque de réindicateur des indicateurs.</span><span class="sxs-lookup"><span data-stu-id="70321-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="70321-129">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="70321-129">The following flag can be set:</span></span>
    
<span data-ttu-id="70321-130">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="70321-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="70321-131">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="70321-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="70321-132">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="70321-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="70321-133">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="70321-133">_lppTable_</span></span>
  
> <span data-ttu-id="70321-134">remarquer Pointeur vers un pointeur vers la table d'affichage, qui expose l'interface [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="70321-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="70321-135">_lppTblData_</span><span class="sxs-lookup"><span data-stu-id="70321-135">_lppTblData_</span></span>
  
> <span data-ttu-id="70321-136">[in, out] Pointeur vers un pointeur vers un objet de données de tableau exposant l'interface [ITableData](itabledataiunknown.md) sur le tableau renvoyé dans le paramètre _lppTable_ .</span><span class="sxs-lookup"><span data-stu-id="70321-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="70321-137">Si aucun objet de données de table n'est souhaité, _lppTblData_ doit être défini sur null au lieu d'une valeur de pointeur.</span><span class="sxs-lookup"><span data-stu-id="70321-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="70321-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="70321-138">Return value</span></span>

<span data-ttu-id="70321-139">Aucun</span><span class="sxs-lookup"><span data-stu-id="70321-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70321-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="70321-140">Remarks</span></span>

<span data-ttu-id="70321-141">MAPI utilise les fonctions pointées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart de l'allocation et de la libération de mémoire, notamment pour allouer de la mémoire aux applications clientes lors de l'appel d'interfaces d'objets comme [IMAPIProp:: GetProps](imapiprop-getprops.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="70321-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="70321-142">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="70321-142">Notes to callers</span></span>

<span data-ttu-id="70321-143">Tout ce qu'il est possible de lire à partir de la ressource Dialog, y compris:</span><span class="sxs-lookup"><span data-stu-id="70321-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="70321-144">Le titre de la page, qui est le membre _ulbLpszLabel_ de la structure [DTBLPAGE](dtblpage.md) , qui est lu à partir du titre de la boîte de dialogue dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="70321-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="70321-145">Tous les titres de contrôle qui sont les membres _ulbLpszLabel_ d'autres structures de contrôle lues à partir du texte du contrôle de la ressource.</span><span class="sxs-lookup"><span data-stu-id="70321-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="70321-146">**BuildDisplayTable** remplace tous les éléments transmis dans les structures de contrôle d'entrée par les informations de la ressource Dialog, ce qui signifie que l'appelant de **BuildDisplayTable** ne peut pas spécifier dynamiquement des titres de page ou de contrôle.</span><span class="sxs-lookup"><span data-stu-id="70321-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="70321-147">Les appelants qui doivent effectuer cette opération peuvent avoir **BuildDisplayTable** renvoyer l'objet de données de tableau dans _lppTableData_ et modifier des lignes dans celui-ci; ou ils peuvent créer la table d'affichage manuellement dans un objet de données de table.</span><span class="sxs-lookup"><span data-stu-id="70321-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="70321-148">Si _lppTableData_ n'est pas défini sur null, le fournisseur est responsable de la libération de l'objet de données de table lorsqu'il est terminé avec la table d'affichage.</span><span class="sxs-lookup"><span data-stu-id="70321-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

