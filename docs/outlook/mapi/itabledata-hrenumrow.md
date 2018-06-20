---
title: ITableDataHrEnumRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrEnumRow
api_type:
- COM
ms.assetid: b25d9f2b-9454-4983-98f7-6a051a3b8a04
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6c149a215a048b96408025e08df55972fa989f46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784461"
---
# <a name="itabledatahrenumrow"></a><span data-ttu-id="8ac2e-103">ITableData::HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="8ac2e-103">ITableData::HrEnumRow</span></span>

  
  
<span data-ttu-id="8ac2e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8ac2e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8ac2e-105">Récupère une ligne en fonction de sa position dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8ac2e-105">Retrieves a row based on its position in the table.</span></span> 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a><span data-ttu-id="8ac2e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ac2e-106">Parameters</span></span>

 <span data-ttu-id="8ac2e-107">_ulRowNumber_</span><span class="sxs-lookup"><span data-stu-id="8ac2e-107">_ulRowNumber_</span></span>
  
> <span data-ttu-id="8ac2e-108">[in] Le numéro de la ligne pour laquelle retourner les propriétés.</span><span class="sxs-lookup"><span data-stu-id="8ac2e-108">[in] The number of the row for which to return properties.</span></span> <span data-ttu-id="8ac2e-109">La valeur dans le paramètre _ulRowNumber_ peut être n’importe quelle valeur comprise entre 0, ce qui indique la première ligne dans le tableau, à n - 1, ce qui indique la dernière ligne dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8ac2e-109">The value in the  _ulRowNumber_ parameter can be any value from 0, which indicates the first row in the table, through n - 1, which indicates the last row in the table.</span></span> 
    
 <span data-ttu-id="8ac2e-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="8ac2e-110">_lppSRow_</span></span>
  
> <span data-ttu-id="8ac2e-111">[out] Pointeur vers un pointeur vers une structure [SRow](srow.md) qui décrit la ligne cible.</span><span class="sxs-lookup"><span data-stu-id="8ac2e-111">[out] A pointer to a pointer to an [SRow](srow.md) structure that describes the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8ac2e-112">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8ac2e-112">Return value</span></span>

<span data-ttu-id="8ac2e-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="8ac2e-113">S_OK</span></span> 
  
> <span data-ttu-id="8ac2e-114">La ligne a été récupérée avec succès, ou une ligne pour le numéro de la ligne spécifiée par le paramètre _ulRowNumber_ n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="8ac2e-114">The row was retrieved successfully, or a row for the row number specified by the  _ulRowNumber_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8ac2e-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="8ac2e-115">Remarks</span></span>

<span data-ttu-id="8ac2e-116">La méthode **ITableData::HrEnumRow** récupère une ligne basée sur un numéro séquentiel.</span><span class="sxs-lookup"><span data-stu-id="8ac2e-116">The **ITableData::HrEnumRow** method retrieves a row based on a sequential number.</span></span> <span data-ttu-id="8ac2e-117">Ce nombre représente l’ordre d’insertion (0 indique que la première ligne et le nombre de lignes moins 1 indique la dernière ligne).</span><span class="sxs-lookup"><span data-stu-id="8ac2e-117">This number represents the order of insertion (0 indicates the first row, and the number of rows minus 1 indicates the last row).</span></span> <span data-ttu-id="8ac2e-118">MAPI gère cet ordre chronologique d’insertion de ligne pour la durée de vie de l’objet de données de table.</span><span class="sxs-lookup"><span data-stu-id="8ac2e-118">MAPI maintains this chronological order of row insertion for the lifetime of the table data object.</span></span> 
  
<span data-ttu-id="8ac2e-119">Si le numéro spécifié dans _ulRowNumber_ ne correspond pas à une ligne dans le tableau, **HrEnumRow** renvoie S_OK et définit le paramètre _lppSRow_ sur NULL.</span><span class="sxs-lookup"><span data-stu-id="8ac2e-119">If the number specified in  _ulRowNumber_ does not correspond to a row in the table, **HrEnumRow** returns S_OK and sets the  _lppSRow_ parameter to NULL.</span></span> 
  
<span data-ttu-id="8ac2e-120">MAPI alloue de la mémoire pour la structure **SRow** retournée à l’aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) lors de la création de l’objet de données de table.</span><span class="sxs-lookup"><span data-stu-id="8ac2e-120">MAPI allocates memory for the returned **SRow** structure by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function when the table data object is created.</span></span> <span data-ttu-id="8ac2e-121">L’appelant doit libérer cette mémoire en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8ac2e-121">The caller must release this memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="8ac2e-122">Pour récupérer des lignes d’une table dans l’ordre qu’ils ont été insérés, les utilisateurs de tableau données objet appeler la méthode **HrEnumRow** .</span><span class="sxs-lookup"><span data-stu-id="8ac2e-122">To retrieve rows from a table in the order that they were inserted, table data object users call the **HrEnumRow** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8ac2e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ac2e-123">See also</span></span>



[<span data-ttu-id="8ac2e-124">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="8ac2e-124">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="8ac2e-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8ac2e-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8ac2e-126">SRow</span><span class="sxs-lookup"><span data-stu-id="8ac2e-126">SRow</span></span>](srow.md)
  
[<span data-ttu-id="8ac2e-127">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8ac2e-127">ITableData : IUnknown</span></span>](itabledataiunknown.md)

