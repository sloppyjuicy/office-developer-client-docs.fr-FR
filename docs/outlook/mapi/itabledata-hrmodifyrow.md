---
title: ITableDataHrModifyRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRow
api_type:
- COM
ms.assetid: 9e255b3e-dd17-4528-ba4e-c3a1aef32b04
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 44ecf095ad24dd266dc5f603ace9c7b9f21c1b41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348663"
---
# <a name="itabledatahrmodifyrow"></a><span data-ttu-id="0862f-103">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="0862f-103">ITableData::HrModifyRow</span></span>

  
  
<span data-ttu-id="0862f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0862f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0862f-105">Insère une nouvelle ligne de tableau, éventuellement en remplaçant une ligne existante.</span><span class="sxs-lookup"><span data-stu-id="0862f-105">Inserts a new table row, possibly replacing an existing row.</span></span>
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="0862f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0862f-106">Parameters</span></span>

 <span data-ttu-id="0862f-107">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="0862f-107">_lpSRow_</span></span>
  
> <span data-ttu-id="0862f-108">dans Pointeur vers une structure [SRow](srow.md) qui décrit la ligne à ajouter ou pour remplacer une ligne existante.</span><span class="sxs-lookup"><span data-stu-id="0862f-108">[in] A pointer to an [SRow](srow.md) structure that describes the row to be added or to replace an existing row.</span></span> <span data-ttu-id="0862f-109">L'une des structures de valeurs de propriété vers lesquelles pointe le membre **lpProps** de la structure **SRow** doit contenir la colonne d'index, la valeur qui a été spécifiée dans le paramètre _ulPropTagIndexColumn_ dans l'appel à la [CreateTable ](createtable.md)fonction.</span><span class="sxs-lookup"><span data-stu-id="0862f-109">One of the property value structures pointed to by the **lpProps** member of the **SRow** structure should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0862f-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0862f-110">Return value</span></span>

<span data-ttu-id="0862f-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="0862f-111">S_OK</span></span> 
  
> <span data-ttu-id="0862f-112">La ligne a été insérée ou modifiée.</span><span class="sxs-lookup"><span data-stu-id="0862f-112">The row was successfully inserted or modified.</span></span>
    
<span data-ttu-id="0862f-113">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0862f-113">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="0862f-114">La ligne passée ne possède pas de colonne d'index.</span><span class="sxs-lookup"><span data-stu-id="0862f-114">The passed-in row does not have an index column.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0862f-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="0862f-115">Remarks</span></span>

<span data-ttu-id="0862f-116">La méthode **ITableData:: HrModifyRow** insère la ligne décrite par la structure **SRow** vers laquelle pointe le paramètre _lpSRow_ .</span><span class="sxs-lookup"><span data-stu-id="0862f-116">The **ITableData::HrModifyRow** method inserts the row described by the **SRow** structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="0862f-117">Si une ligne qui a la même valeur pour sa colonne d'index que la ligne sur laquelle pointe _lpSRow_ existe déjà dans le tableau, la ligne existante est remplacée.</span><span class="sxs-lookup"><span data-stu-id="0862f-117">If a row that has the same value for its index column as the row that  _lpSRow_ points to already exists in the table, the existing row is replaced.</span></span> <span data-ttu-id="0862f-118">S'il n'existe aucune ligne correspondant à celle incluse dans la structure **SRow** , **HrModifyRow** ajoute la ligne à la fin du tableau.</span><span class="sxs-lookup"><span data-stu-id="0862f-118">If no row exists that matches the one included in the **SRow** structure, **HrModifyRow** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="0862f-119">Toutes les vues de la table sont modifiées de façon à inclure la ligne sur laquelle pointe _lpSRow_.</span><span class="sxs-lookup"><span data-stu-id="0862f-119">All views of the table are modified to include the row pointed to by  _lpSRow_.</span></span> <span data-ttu-id="0862f-120">Toutefois, si une vue a une restriction en place qui exclut la ligne, elle peut ne pas être visible par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0862f-120">However, if a view has a restriction in place that excludes the row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="0862f-121">Les colonnes de la ligne sur lesquelles pointe _lpSRow_ n'ont pas besoin d'être dans le même ordre que les colonnes du tableau.</span><span class="sxs-lookup"><span data-stu-id="0862f-121">The columns in the row pointed to by  _lpSRow_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="0862f-122">L'appelant peut également inclure en tant que propriétés de colonnes qui ne se trouvent pas actuellement dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="0862f-122">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="0862f-123">Pour les affichages existants, **HrModifyRow** rend ces nouvelles colonnes disponibles, mais ne les inclut pas dans le jeu de colonnes actuel.</span><span class="sxs-lookup"><span data-stu-id="0862f-123">For existing views, **HrModifyRow** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="0862f-124">Pour les futures vues, **HrModifyRow** inclut les nouvelles colonnes dans l'ensemble de colonnes.</span><span class="sxs-lookup"><span data-stu-id="0862f-124">For future views, **HrModifyRow** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="0862f-125">Une fois que **HrModifyRow** a ajouté la ligne, des notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable:: Advise](imapitable-advise.md) pour s'inscrire aux notifications.</span><span class="sxs-lookup"><span data-stu-id="0862f-125">After **HrModifyRow** adds the row, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0862f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0862f-126">See also</span></span>



[<span data-ttu-id="0862f-127">SRow</span><span class="sxs-lookup"><span data-stu-id="0862f-127">SRow</span></span>](srow.md)
  
[<span data-ttu-id="0862f-128">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0862f-128">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="0862f-129">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0862f-129">ITableData : IUnknown</span></span>](itabledataiunknown.md)

