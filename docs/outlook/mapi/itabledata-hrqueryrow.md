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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 92540159386e6f37d93684aff037b235071010f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784477"
---
# <a name="itabledatahrqueryrow"></a><span data-ttu-id="8a613-103">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="8a613-103">ITableData::HrQueryRow</span></span>

  
  
<span data-ttu-id="8a613-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8a613-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8a613-105">Récupère une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="8a613-105">Retrieves a table row.</span></span>
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a><span data-ttu-id="8a613-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a613-106">Parameters</span></span>

 <span data-ttu-id="8a613-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="8a613-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="8a613-108">[in] Pointeur vers une structure de valeur de propriété qui décrit la colonne d’index de la ligne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="8a613-108">[in] A pointer to a property value structure that describes the index column for the row to be retrieved.</span></span> <span data-ttu-id="8a613-109">Le membre **ulPropTag** de la structure de valeur de propriété doit contenir la même balise de propriété en tant que paramètre de l’appel à la fonction [Create table](createtable.md) , qui accède à l’implémentation [ITableData](itabledataiunknown.md) _ulPropTagIndexColumn_ .</span><span class="sxs-lookup"><span data-stu-id="8a613-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function, which accesses the [ITableData](itabledataiunknown.md) implementation.</span></span> 
    
 <span data-ttu-id="8a613-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="8a613-110">_lppSRow_</span></span>
  
> <span data-ttu-id="8a613-111">[out] Pointeur vers un pointeur vers la ligne récupérée.</span><span class="sxs-lookup"><span data-stu-id="8a613-111">[out] A pointer to a pointer to the retrieved row.</span></span> 
    
 <span data-ttu-id="8a613-112">_lpuliRow_</span><span class="sxs-lookup"><span data-stu-id="8a613-112">_lpuliRow_</span></span>
  
> <span data-ttu-id="8a613-113">[entrée, sortie] Sur entrée, un pointeur valide ou valeur NULL, ce qui indique qu’aucune information ne doit être renvoyé.</span><span class="sxs-lookup"><span data-stu-id="8a613-113">[in, out] On input, a valid pointer or NULL, which indicates that no information needs to be returned.</span></span> <span data-ttu-id="8a613-114">Sur la sortie, un pointeur valid qui pointe vers le numéro de la ligne de la ligne, un numéro qui identifie la position de la ligne dans la table.</span><span class="sxs-lookup"><span data-stu-id="8a613-114">On output, a valid pointer that points to the row's row number, a sequential number that identifies the row's position in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8a613-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8a613-115">Return value</span></span>

<span data-ttu-id="8a613-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a613-116">S_OK</span></span> 
  
> <span data-ttu-id="8a613-117">La ligne a été récupérée correctement.</span><span class="sxs-lookup"><span data-stu-id="8a613-117">The row was successfully retrieved.</span></span>
    
<span data-ttu-id="8a613-118">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8a613-118">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="8a613-119">Le [SPropValue](spropvalue.md) structure _lpSPropValue_ pointant vers ne contient ne pas la propriété de colonne d’index.</span><span class="sxs-lookup"><span data-stu-id="8a613-119">The [SPropValue](spropvalue.md) structure that  _lpSPropValue_ points to does not contain the index column property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8a613-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="8a613-120">Remarks</span></span>

<span data-ttu-id="8a613-121">La méthode **ITableData::HrQueryRow** récupère toutes les propriétés de la ligne qui a une colonne d’index qui correspond à la valeur de la colonne d’index incluse dans la structure de propriété désignée par _lpSPropValue_.</span><span class="sxs-lookup"><span data-stu-id="8a613-121">The **ITableData::HrQueryRow** method retrieves all of the properties for the row that has an index column that matches the value of the index column included in the property structure pointed to by  _lpSPropValue_.</span></span> <span data-ttu-id="8a613-122">**HrQueryRow** renvoie également le numéro de ligne, si l’appelant demande, qui identifie la position de la ligne dans la table.</span><span class="sxs-lookup"><span data-stu-id="8a613-122">**HrQueryRow** also returns the row number, if the caller requests it, that identifies the row's position in the table.</span></span> 
  
<span data-ttu-id="8a613-123">Étant donné que **HrQueryRow** ne modifie pas la structure **SPropValue** désignée par _lpSPropValue_, les appelants doivent libérer la structure lorsque **HrQueryRow** renvoie.</span><span class="sxs-lookup"><span data-stu-id="8a613-123">Because **HrQueryRow** does not modify the **SPropValue** structure pointed to by  _lpSPropValue_, callers must free the structure when **HrQueryRow** returns.</span></span> <span data-ttu-id="8a613-124">Les appelants doivent également libérer la structure **SRow** qui contient la ligne récupérée.</span><span class="sxs-lookup"><span data-stu-id="8a613-124">Callers must also free the **SRow** structure that contains the retrieved row.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8a613-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a613-125">See also</span></span>



[<span data-ttu-id="8a613-126">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="8a613-126">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="8a613-127">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8a613-127">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8a613-128">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8a613-128">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="8a613-129">SRow</span><span class="sxs-lookup"><span data-stu-id="8a613-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="8a613-130">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a613-130">ITableData : IUnknown</span></span>](itabledataiunknown.md)

