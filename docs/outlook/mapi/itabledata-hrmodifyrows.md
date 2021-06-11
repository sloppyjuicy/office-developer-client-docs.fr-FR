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
# <a name="itabledatahrmodifyrows"></a><span data-ttu-id="9a49c-103">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="9a49c-103">ITableData::HrModifyRows</span></span>

  
  
<span data-ttu-id="9a49c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a49c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a49c-105">Insère plusieurs lignes de tableau, en remplaçant éventuellement les lignes existantes.</span><span class="sxs-lookup"><span data-stu-id="9a49c-105">Inserts multiple table rows, possibly replacing existing rows.</span></span>
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="9a49c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9a49c-106">Parameters</span></span>

 <span data-ttu-id="9a49c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9a49c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9a49c-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="9a49c-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9a49c-109">_lpSRowSet_</span><span class="sxs-lookup"><span data-stu-id="9a49c-109">_lpSRowSet_</span></span>
  
> <span data-ttu-id="9a49c-110">[in] Pointeur vers une structure [SRowSet](srowset.md) qui contient l’ensemble de lignes à ajouter, en remplaçant les lignes existantes si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9a49c-110">[in] A pointer to an [SRowSet](srowset.md) structure that contains the set of rows to be added, replacing existing rows if necessary.</span></span> <span data-ttu-id="9a49c-111">L’une des structures de valeurs de propriétés pointées par le membre **lpProps** de chaque structure [SRow](srow.md) dans le jeu de lignes doit contenir la colonne d’index, la même valeur spécifiée dans le paramètre _ulPropTagIndexColumn_ dans l’appel à la fonction [CreateTable.](createtable.md)</span><span class="sxs-lookup"><span data-stu-id="9a49c-111">One of the property value structures pointed to by the **lpProps** member of each [SRow](srow.md) structure in the row set should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9a49c-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9a49c-112">Return value</span></span>

<span data-ttu-id="9a49c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="9a49c-113">S_OK</span></span> 
  
> <span data-ttu-id="9a49c-114">Les lignes ont été insérées ou modifiées avec succès.</span><span class="sxs-lookup"><span data-stu-id="9a49c-114">The rows were successfully inserted or modified.</span></span>
    
<span data-ttu-id="9a49c-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9a49c-115">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="9a49c-116">Une ou plusieurs lignes transmises n’ont pas de colonne d’index.</span><span class="sxs-lookup"><span data-stu-id="9a49c-116">One or more of the passed-in rows does not have an index column.</span></span> <span data-ttu-id="9a49c-117">Si cette erreur est renvoyée, aucune ligne n’est modifiée.</span><span class="sxs-lookup"><span data-stu-id="9a49c-117">If this error is returned, no rows are changed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a49c-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="9a49c-118">Remarks</span></span>

<span data-ttu-id="9a49c-119">La **méthode ITableData::HrModifyRows insère** les lignes décrites par la structure [SRowSet](srowset.md) pointée vers le _paramètre lpSRowSet._</span><span class="sxs-lookup"><span data-stu-id="9a49c-119">The **ITableData::HrModifyRows** method inserts the rows described by the [SRowSet](srowset.md) structure pointed to by the  _lpSRowSet_ parameter.</span></span> <span data-ttu-id="9a49c-120">Si la valeur de colonne d’index d’une ligne du jeu de lignes correspond à la valeur d’une ligne existante du tableau, la ligne existante est remplacée.</span><span class="sxs-lookup"><span data-stu-id="9a49c-120">If the index column value of a row in the row set matches the value for an existing row in the table, the existing row is replaced.</span></span> <span data-ttu-id="9a49c-121">S’il n’existe aucune ligne qui corresponde à celle incluse dans la structure **SRowSet,** **HrModifyRows** ajoute la ligne à la fin du tableau.</span><span class="sxs-lookup"><span data-stu-id="9a49c-121">If no row exists that matches the one included in the **SRowSet** structure, **HrModifyRows** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="9a49c-122">Tous les affichages de la table sont modifiés pour inclure les lignes pointées par  _lpSRowSet_.</span><span class="sxs-lookup"><span data-stu-id="9a49c-122">All views of the table are modified to include the rows pointed to by  _lpSRowSet_.</span></span> <span data-ttu-id="9a49c-123">Toutefois, si une restriction est en place sur un affichage qui exclut une ligne, il se peut qu’elle ne soit pas visible pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9a49c-123">However, if a view has a restriction in place that excludes a row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="9a49c-124">Les colonnes des lignes pointées par  _lpSRowSet_ ne doivent pas être dans le même ordre que les colonnes du tableau.</span><span class="sxs-lookup"><span data-stu-id="9a49c-124">The columns in the rows pointed to by  _lpSRowSet_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="9a49c-125">L’appelant peut également inclure en tant que propriétés de colonnes qui ne figurent pas actuellement dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="9a49c-125">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="9a49c-126">Pour les affichages **existants, HrModifyRows** rend ces nouvelles colonnes disponibles, mais ne les inclut pas dans le jeu de colonnes actuel.</span><span class="sxs-lookup"><span data-stu-id="9a49c-126">For existing views, **HrModifyRows** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="9a49c-127">Pour les affichages futurs, **HrModifyRows** inclut les nouvelles colonnes dans le jeu de colonnes.</span><span class="sxs-lookup"><span data-stu-id="9a49c-127">For future views, **HrModifyRows** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="9a49c-128">Une fois **que HrModifyRows** a ajouté les lignes, des notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable::Advise](imapitable-advise.md) de la table pour s’inscrire aux notifications.</span><span class="sxs-lookup"><span data-stu-id="9a49c-128">After **HrModifyRows** has added the rows, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="9a49c-129">MAPI envoie TABLE_ROW_ADDED ou TABLE_ROW_MODIFIED notifications pour chaque ligne, jusqu’à huit lignes.</span><span class="sxs-lookup"><span data-stu-id="9a49c-129">MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows.</span></span> <span data-ttu-id="9a49c-130">Si plus de huit lignes sont affectées par l’appel **HrModifyRows,** MAPI envoie une seule notification TABLE_CHANGED à la place.</span><span class="sxs-lookup"><span data-stu-id="9a49c-130">If more than eight rows are affected by the **HrModifyRows** call, MAPI sends a single TABLE_CHANGED notification instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9a49c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a49c-131">See also</span></span>



[<span data-ttu-id="9a49c-132">SRowSet</span><span class="sxs-lookup"><span data-stu-id="9a49c-132">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="9a49c-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a49c-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

