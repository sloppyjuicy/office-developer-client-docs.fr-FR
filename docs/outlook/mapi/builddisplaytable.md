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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3b5268f0b033126083a463f72e47c64957df07eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577687"
---
# <a name="builddisplaytable"></a><span data-ttu-id="267f6-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="267f6-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="267f6-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="267f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="267f6-105">Crée une table de l’affichage de données de la propriété page contenues dans une ou plusieurs structures [DTPAGE](dtpage.md) .</span><span class="sxs-lookup"><span data-stu-id="267f6-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="267f6-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="267f6-106">Header file:</span></span>  <br/> |<span data-ttu-id="267f6-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="267f6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="267f6-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="267f6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="267f6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="267f6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="267f6-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="267f6-110">Called by:</span></span>  <br/> |<span data-ttu-id="267f6-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="267f6-111">Service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="267f6-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="267f6-112">Parameters</span></span>

 <span data-ttu-id="267f6-113">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="267f6-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="267f6-114">[in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="267f6-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="267f6-115">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="267f6-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="267f6-116">[in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser pour allouer plus de mémoire.</span><span class="sxs-lookup"><span data-stu-id="267f6-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="267f6-117">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="267f6-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="267f6-118">[in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="267f6-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="267f6-119">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="267f6-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="267f6-120">Inutilisés ; doit être défini avec la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="267f6-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="267f6-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="267f6-121">_hInstance_</span></span>
  
> <span data-ttu-id="267f6-122">[in] Une instance d’un objet MAPI à partir de laquelle **BuildDisplayTable** récupère les ressources.</span><span class="sxs-lookup"><span data-stu-id="267f6-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="267f6-123">_cPages_</span><span class="sxs-lookup"><span data-stu-id="267f6-123">_cPages_</span></span>
  
> <span data-ttu-id="267f6-124">[in] Nombre de structures [DTPAGE](dtpage.md) dans le tableau indiqué par le paramètre _lpPage_ .</span><span class="sxs-lookup"><span data-stu-id="267f6-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="267f6-125">_lpPage_</span><span class="sxs-lookup"><span data-stu-id="267f6-125">_lpPage_</span></span>
  
> <span data-ttu-id="267f6-126">[in] Pointeur vers un tableau de structures **DTPAGE** qui contiennent des informations sur les pages de tableau d’affichage à générer.</span><span class="sxs-lookup"><span data-stu-id="267f6-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="267f6-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="267f6-127">_ulFlags_</span></span>
  
> <span data-ttu-id="267f6-128">[in] Masque de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="267f6-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="267f6-129">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="267f6-129">The following flag can be set:</span></span>
    
<span data-ttu-id="267f6-130">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="267f6-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="267f6-131">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="267f6-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="267f6-132">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="267f6-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="267f6-133">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="267f6-133">_lppTable_</span></span>
  
> <span data-ttu-id="267f6-134">[out] Pointeur vers un pointeur vers la table d’affichage, qui expose l’interface [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="267f6-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="267f6-135">_lppTblData_</span><span class="sxs-lookup"><span data-stu-id="267f6-135">_lppTblData_</span></span>
  
> <span data-ttu-id="267f6-136">[entrée, sortie] Pointeur vers un pointeur vers un objet de données de table exposant l’interface [ITableData](itabledataiunknown.md) sur la table renvoyée dans le paramètre _lppTable_ .</span><span class="sxs-lookup"><span data-stu-id="267f6-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="267f6-137">Si aucun objet de données de table n’est souhaitée, _lppTblData_ doit être défini sur NULL au lieu d’une valeur de pointeur.</span><span class="sxs-lookup"><span data-stu-id="267f6-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="267f6-138">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="267f6-138">Return value</span></span>

<span data-ttu-id="267f6-139">Aucune</span><span class="sxs-lookup"><span data-stu-id="267f6-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="267f6-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="267f6-140">Remarks</span></span>

<span data-ttu-id="267f6-141">MAPI utilise les fonctions désignées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart de l’allocation de mémoire et de désaffectation, en particulier pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel des interfaces de l’objet par exemple [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="267f6-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="267f6-142">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="267f6-142">Notes to callers</span></span>

<span data-ttu-id="267f6-143">Tout possible est lu à partir de la ressource de la boîte de dialogue, y compris :</span><span class="sxs-lookup"><span data-stu-id="267f6-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="267f6-144">Le titre de la page qui est, le membre _ulbLpszLabel_ de la structure [DTBLPAGE](dtblpage.md) lire le titre de la boîte de dialogue de la ressource.</span><span class="sxs-lookup"><span data-stu-id="267f6-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="267f6-145">Tous les titres de contrôle qui est, les membres _ulbLpszLabel_ d’autres structures de contrôle lire le texte du contrôle de la ressource.</span><span class="sxs-lookup"><span data-stu-id="267f6-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="267f6-146">**BuildDisplayTable** remplace tout élément transmis dans les structures de contrôle d’entrée avec des informations à partir de la ressource de boîte de dialogue, ce qui signifie que l’appelant de **BuildDisplayTable** ne peut pas spécifier dynamiquement des titres de page ou un contrôle.</span><span class="sxs-lookup"><span data-stu-id="267f6-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="267f6-147">Les appelants qui ont besoin de faire qui peuvent avoir **BuildDisplayTable** retourner l’objet de données de table _lppTableData_ et modifier des lignes ou qu’elles peuvent construire la table affichage manuellement dans un objet de données de table à la place.</span><span class="sxs-lookup"><span data-stu-id="267f6-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="267f6-148">Si _lppTableData_ n’est pas défini sur NULL, le fournisseur est chargé de libérer l’objet de données de table lorsqu’il a terminé l’affichage de la table.</span><span class="sxs-lookup"><span data-stu-id="267f6-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

