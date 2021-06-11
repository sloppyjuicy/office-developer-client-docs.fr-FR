---
title: ITableDataHrQueryRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrQueryRow
api_type:
- COM
ms.assetid: 66ce8f36-2b2b-4a8e-b9b2-43782d8357a1
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: da41fadc9a71a410dd115e28ce2cf9c81442b104
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434766"
---
# <a name="itabledatahrqueryrow"></a><span data-ttu-id="f49ef-103">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="f49ef-103">ITableData::HrQueryRow</span></span>

  
  
<span data-ttu-id="f49ef-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f49ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f49ef-105">Récupère une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="f49ef-105">Retrieves a table row.</span></span>
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a><span data-ttu-id="f49ef-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f49ef-106">Parameters</span></span>

 <span data-ttu-id="f49ef-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="f49ef-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="f49ef-108">[in] Pointeur vers une structure de valeurs de propriété qui décrit la colonne d’index de la ligne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="f49ef-108">[in] A pointer to a property value structure that describes the index column for the row to be retrieved.</span></span> <span data-ttu-id="f49ef-109">Le **membre ulPropTag** de la structure de valeurs de propriété doit contenir la même balise de propriété que le paramètre _ulPropTagIndexColumn_ de l’appel à la fonction [CreateTable,](createtable.md) qui accède à l’implémentation [ITableData.](itabledataiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="f49ef-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function, which accesses the [ITableData](itabledataiunknown.md) implementation.</span></span> 
    
 <span data-ttu-id="f49ef-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="f49ef-110">_lppSRow_</span></span>
  
> <span data-ttu-id="f49ef-111">[out] Pointeur vers un pointeur vers la ligne récupérée.</span><span class="sxs-lookup"><span data-stu-id="f49ef-111">[out] A pointer to a pointer to the retrieved row.</span></span> 
    
 <span data-ttu-id="f49ef-112">_lpuliRow_</span><span class="sxs-lookup"><span data-stu-id="f49ef-112">_lpuliRow_</span></span>
  
> <span data-ttu-id="f49ef-113">[in, out] Lors de l’entrée, un pointeur valide ou NULL, qui indique qu’aucune information ne doit être renvoyée.</span><span class="sxs-lookup"><span data-stu-id="f49ef-113">[in, out] On input, a valid pointer or NULL, which indicates that no information needs to be returned.</span></span> <span data-ttu-id="f49ef-114">En sortie, un pointeur valide qui pointe vers le numéro de ligne de la ligne, un numéro séquentiel qui identifie la position de la ligne dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f49ef-114">On output, a valid pointer that points to the row's row number, a sequential number that identifies the row's position in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f49ef-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f49ef-115">Return value</span></span>

<span data-ttu-id="f49ef-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f49ef-116">S_OK</span></span> 
  
> <span data-ttu-id="f49ef-117">La ligne a été récupérée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f49ef-117">The row was successfully retrieved.</span></span>
    
<span data-ttu-id="f49ef-118">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f49ef-118">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="f49ef-119">La structure [SPropValue](spropvalue.md) vers qui  _pointe lpSPropValue_ ne contient pas la propriété de colonne d’index.</span><span class="sxs-lookup"><span data-stu-id="f49ef-119">The [SPropValue](spropvalue.md) structure that  _lpSPropValue_ points to does not contain the index column property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f49ef-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="f49ef-120">Remarks</span></span>

<span data-ttu-id="f49ef-121">La **méthode ITableData::HrQueryRow** récupère toutes les propriétés de la ligne qui possède une colonne d’index qui correspond à la valeur de la colonne d’index incluse dans la structure de propriétés pointée par  _lpSPropValue_.</span><span class="sxs-lookup"><span data-stu-id="f49ef-121">The **ITableData::HrQueryRow** method retrieves all of the properties for the row that has an index column that matches the value of the index column included in the property structure pointed to by  _lpSPropValue_.</span></span> <span data-ttu-id="f49ef-122">**HrQueryRow renvoie** également le numéro de ligne, si l’appelant le demande, qui identifie la position de la ligne dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f49ef-122">**HrQueryRow** also returns the row number, if the caller requests it, that identifies the row's position in the table.</span></span> 
  
<span data-ttu-id="f49ef-123">Étant donné que **HrQueryRow** ne modifie pas la structure **SPropValue** pointée par _lpSPropValue_, les appelants doivent libérer la structure lorsque **HrQueryRow renvoie.**</span><span class="sxs-lookup"><span data-stu-id="f49ef-123">Because **HrQueryRow** does not modify the **SPropValue** structure pointed to by  _lpSPropValue_, callers must free the structure when **HrQueryRow** returns.</span></span> <span data-ttu-id="f49ef-124">Les appelants doivent également libérer la structure **SRow** qui contient la ligne récupérée.</span><span class="sxs-lookup"><span data-stu-id="f49ef-124">Callers must also free the **SRow** structure that contains the retrieved row.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f49ef-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f49ef-125">See also</span></span>



[<span data-ttu-id="f49ef-126">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="f49ef-126">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="f49ef-127">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f49ef-127">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f49ef-128">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f49ef-128">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="f49ef-129">SRow</span><span class="sxs-lookup"><span data-stu-id="f49ef-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="f49ef-130">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f49ef-130">ITableData : IUnknown</span></span>](itabledataiunknown.md)

