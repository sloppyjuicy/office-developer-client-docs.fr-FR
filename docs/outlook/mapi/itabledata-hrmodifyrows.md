---
title: ITableDataHrModifyRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRows
api_type:
- COM
ms.assetid: d295c896-9882-4d6f-9689-5cf40db208c0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d0074dd006fda6d44252011d0b979169e0c3d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405358"
---
# <a name="itabledatahrmodifyrows"></a><span data-ttu-id="b0077-103">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="b0077-103">ITableData::HrModifyRows</span></span>

  
  
<span data-ttu-id="b0077-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0077-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0077-105">Insère plusieurs lignes de tableau, susceptibles de remplacer des lignes existantes.</span><span class="sxs-lookup"><span data-stu-id="b0077-105">Inserts multiple table rows, possibly replacing existing rows.</span></span>
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="b0077-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0077-106">Parameters</span></span>

 <span data-ttu-id="b0077-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b0077-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b0077-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="b0077-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b0077-109">_lpSRowSet_</span><span class="sxs-lookup"><span data-stu-id="b0077-109">_lpSRowSet_</span></span>
  
> <span data-ttu-id="b0077-110">dans Pointeur vers une structure [SRowSet](srowset.md) qui contient l'ensemble de lignes à ajouter, en remplaçant les lignes existantes si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b0077-110">[in] A pointer to an [SRowSet](srowset.md) structure that contains the set of rows to be added, replacing existing rows if necessary.</span></span> <span data-ttu-id="b0077-111">L'une des structures de valeur de propriété auxquelles pointe le membre **lpProps** de chaque structure [SRow](srow.md) dans l'ensemble de lignes doit contenir la colonne d'index, la valeur qui a été spécifiée dans le paramètre _ulPropTagIndexColumn_ dans l'appel à la [ Fonction CreateTable](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="b0077-111">One of the property value structures pointed to by the **lpProps** member of each [SRow](srow.md) structure in the row set should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b0077-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b0077-112">Return value</span></span>

<span data-ttu-id="b0077-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0077-113">S_OK</span></span> 
  
> <span data-ttu-id="b0077-114">Les lignes ont été correctement insérées ou modifiées.</span><span class="sxs-lookup"><span data-stu-id="b0077-114">The rows were successfully inserted or modified.</span></span>
    
<span data-ttu-id="b0077-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b0077-115">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="b0077-116">Une ou plusieurs lignes transmises ne possèdent pas de colonne d'index.</span><span class="sxs-lookup"><span data-stu-id="b0077-116">One or more of the passed-in rows does not have an index column.</span></span> <span data-ttu-id="b0077-117">Si cette erreur est renvoyée, aucune ligne n'est modifiée.</span><span class="sxs-lookup"><span data-stu-id="b0077-117">If this error is returned, no rows are changed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0077-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="b0077-118">Remarks</span></span>

<span data-ttu-id="b0077-119">La méthode **ITableData:: HrModifyRows** insère les lignes décrites par la structure [SRowSet](srowset.md) vers laquelle pointe le paramètre _lpSRowSet_ .</span><span class="sxs-lookup"><span data-stu-id="b0077-119">The **ITableData::HrModifyRows** method inserts the rows described by the [SRowSet](srowset.md) structure pointed to by the  _lpSRowSet_ parameter.</span></span> <span data-ttu-id="b0077-120">Si la valeur de la colonne d'index d'une ligne dans l'ensemble de lignes correspond à la valeur d'une ligne existante dans le tableau, la ligne existante est remplacée.</span><span class="sxs-lookup"><span data-stu-id="b0077-120">If the index column value of a row in the row set matches the value for an existing row in the table, the existing row is replaced.</span></span> <span data-ttu-id="b0077-121">S'il n'existe aucune ligne correspondant à celle incluse dans la structure **SRowSet** , **HrModifyRows** ajoute la ligne à la fin du tableau.</span><span class="sxs-lookup"><span data-stu-id="b0077-121">If no row exists that matches the one included in the **SRowSet** structure, **HrModifyRows** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="b0077-122">Toutes les vues de la table sont modifiées de façon à inclure les lignes vers lesquelles pointe _lpSRowSet_.</span><span class="sxs-lookup"><span data-stu-id="b0077-122">All views of the table are modified to include the rows pointed to by  _lpSRowSet_.</span></span> <span data-ttu-id="b0077-123">Toutefois, si une vue a une restriction en place qui exclut une ligne, elle peut ne pas être visible par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b0077-123">However, if a view has a restriction in place that excludes a row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="b0077-124">Les colonnes des lignes vers lesquelles pointe _lpSRowSet_ n'ont pas besoin d'être dans le même ordre que les colonnes du tableau.</span><span class="sxs-lookup"><span data-stu-id="b0077-124">The columns in the rows pointed to by  _lpSRowSet_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="b0077-125">L'appelant peut également inclure en tant que propriétés de colonnes qui ne se trouvent pas actuellement dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="b0077-125">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="b0077-126">Pour les affichages existants, **HrModifyRows** rend ces nouvelles colonnes disponibles, mais ne les inclut pas dans le jeu de colonnes actuel.</span><span class="sxs-lookup"><span data-stu-id="b0077-126">For existing views, **HrModifyRows** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="b0077-127">Pour les futures vues, **HrModifyRows** inclut les nouvelles colonnes dans l'ensemble de colonnes.</span><span class="sxs-lookup"><span data-stu-id="b0077-127">For future views, **HrModifyRows** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="b0077-128">Une fois que **HrModifyRows** a ajouté les lignes, des notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable:: Advise](imapitable-advise.md) pour s'inscrire aux notifications.</span><span class="sxs-lookup"><span data-stu-id="b0077-128">After **HrModifyRows** has added the rows, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="b0077-129">MAPI envoie des notifications TABLE_ROW_ADDED ou TABLE_ROW_MODIFIED pour chaque ligne, jusqu'à huit lignes.</span><span class="sxs-lookup"><span data-stu-id="b0077-129">MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows.</span></span> <span data-ttu-id="b0077-130">Si plus de huit lignes sont affectées par l'appel **HrModifyRows** , MAPI envoie à la place une seule notification TABLE_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="b0077-130">If more than eight rows are affected by the **HrModifyRows** call, MAPI sends a single TABLE_CHANGED notification instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b0077-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0077-131">See also</span></span>



[<span data-ttu-id="b0077-132">SRowSet</span><span class="sxs-lookup"><span data-stu-id="b0077-132">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="b0077-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0077-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

