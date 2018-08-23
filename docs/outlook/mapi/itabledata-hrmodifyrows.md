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
ms.openlocfilehash: 06356d60b43d7e5be61d944c07001570bdd5c678
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571107"
---
# <a name="itabledatahrmodifyrows"></a><span data-ttu-id="1a158-103">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="1a158-103">ITableData::HrModifyRows</span></span>

  
  
<span data-ttu-id="1a158-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a158-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a158-105">Insère plusieurs lignes de tableau, remplaçant éventuellement les lignes existantes.</span><span class="sxs-lookup"><span data-stu-id="1a158-105">Inserts multiple table rows, possibly replacing existing rows.</span></span>
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="1a158-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="1a158-106">Parameters</span></span>

 <span data-ttu-id="1a158-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1a158-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1a158-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="1a158-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1a158-109">_lpSRowSet_</span><span class="sxs-lookup"><span data-stu-id="1a158-109">_lpSRowSet_</span></span>
  
> <span data-ttu-id="1a158-110">[in] Un pointeur vers une structure [SRowSet](srowset.md) qui contient l’ensemble de lignes à ajouter, en remplaçant les lignes existantes, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1a158-110">[in] A pointer to an [SRowSet](srowset.md) structure that contains the set of rows to be added, replacing existing rows if necessary.</span></span> <span data-ttu-id="1a158-111">Une des structures de valeur de propriété pointés pour définir les par le membre **lpProps** de chaque structure [SRow](srow.md) dans la ligne doit contenir la colonne d’index, la même valeur que celle qui a été spécifiée dans le paramètre _ulPropTagIndexColumn_ dans l’appel à la [ CREATE TABLE](createtable.md) fonction.</span><span class="sxs-lookup"><span data-stu-id="1a158-111">One of the property value structures pointed to by the **lpProps** member of each [SRow](srow.md) structure in the row set should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1a158-112">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="1a158-112">Return value</span></span>

<span data-ttu-id="1a158-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1a158-113">S_OK</span></span> 
  
> <span data-ttu-id="1a158-114">Les lignes insérées ou modifiées avec succès.</span><span class="sxs-lookup"><span data-stu-id="1a158-114">The rows were successfully inserted or modified.</span></span>
    
<span data-ttu-id="1a158-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1a158-115">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="1a158-116">Un ou plusieurs des lignes dans le passé ne dispose pas d’une colonne d’index.</span><span class="sxs-lookup"><span data-stu-id="1a158-116">One or more of the passed-in rows does not have an index column.</span></span> <span data-ttu-id="1a158-117">Si cette erreur est renvoyée, aucune ligne n’est modifiés.</span><span class="sxs-lookup"><span data-stu-id="1a158-117">If this error is returned, no rows are changed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a158-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a158-118">Remarks</span></span>

<span data-ttu-id="1a158-119">La méthode **ITableData::HrModifyRows** insère les lignes décrites par la structure [SRowSet](srowset.md) désignée par le paramètre _lpSRowSet_ .</span><span class="sxs-lookup"><span data-stu-id="1a158-119">The **ITableData::HrModifyRows** method inserts the rows described by the [SRowSet](srowset.md) structure pointed to by the  _lpSRowSet_ parameter.</span></span> <span data-ttu-id="1a158-120">Si la valeur de colonne d’index d’une ligne dans le jeu de lignes correspond à la valeur d’une ligne existante dans le tableau, la ligne existante est remplacée.</span><span class="sxs-lookup"><span data-stu-id="1a158-120">If the index column value of a row in the row set matches the value for an existing row in the table, the existing row is replaced.</span></span> <span data-ttu-id="1a158-121">Si aucune ligne n’existe qui correspond à celui qui est inclus dans la structure **SRowSet** , **HrModifyRows** ajoute la ligne à la fin de la table.</span><span class="sxs-lookup"><span data-stu-id="1a158-121">If no row exists that matches the one included in the **SRowSet** structure, **HrModifyRows** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="1a158-122">Toutes les vues de la table sont modifiées pour inclure les lignes désignés par _lpSRowSet_.</span><span class="sxs-lookup"><span data-stu-id="1a158-122">All views of the table are modified to include the rows pointed to by  _lpSRowSet_.</span></span> <span data-ttu-id="1a158-123">Toutefois, si un affichage a une restriction place excluant une ligne, il peut être pas visible à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1a158-123">However, if a view has a restriction in place that excludes a row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="1a158-124">Les colonnes dans les lignes désignés par _lpSRowSet_ n’ont pas à se trouver dans le même ordre que les colonnes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="1a158-124">The columns in the rows pointed to by  _lpSRowSet_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="1a158-125">L’appelant peut également inclure en tant que propriétés de colonnes qui ne sont pas actuellement dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="1a158-125">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="1a158-126">Pour des vues existantes, **HrModifyRows** rend ces nouvelles colonnes disponibles, mais n’inclut pas les dans la colonne en cours.</span><span class="sxs-lookup"><span data-stu-id="1a158-126">For existing views, **HrModifyRows** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="1a158-127">Pour les affichages futures, **HrModifyRows** inclut les nouvelles colonnes dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="1a158-127">For future views, **HrModifyRows** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="1a158-128">Une fois que **HrModifyRows** a ajouté les lignes, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode la table [IMAPITable::Advise](imapitable-advise.md) pour inscrire les notifications.</span><span class="sxs-lookup"><span data-stu-id="1a158-128">After **HrModifyRows** has added the rows, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="1a158-129">MAPI envoie des notifications TABLE_ROW_ADDED ou TABLE_ROW_MODIFIED pour chaque ligne, jusqu'à huit lignes.</span><span class="sxs-lookup"><span data-stu-id="1a158-129">MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows.</span></span> <span data-ttu-id="1a158-130">Si plus de huit lignes sont affectées par l’appel **HrModifyRows** , MAPI envoie une notification TABLE_CHANGED unique à la place.</span><span class="sxs-lookup"><span data-stu-id="1a158-130">If more than eight rows are affected by the **HrModifyRows** call, MAPI sends a single TABLE_CHANGED notification instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a158-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a158-131">See also</span></span>



[<span data-ttu-id="1a158-132">SRowSet</span><span class="sxs-lookup"><span data-stu-id="1a158-132">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="1a158-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a158-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

