---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: fdd6f40b4d7aa7f65bf1a46d3d9a4f18472b19f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278946"
---
# <a name="itabledatahrdeleterows"></a><span data-ttu-id="0d930-103">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="0d930-103">ITableData::HrDeleteRows</span></span>

  
  
<span data-ttu-id="0d930-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d930-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d930-105">Supprime plusieurs lignes de tableau.</span><span class="sxs-lookup"><span data-stu-id="0d930-105">Deletes multiple table rows.</span></span>
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a><span data-ttu-id="0d930-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d930-106">Parameters</span></span>

 <span data-ttu-id="0d930-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0d930-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0d930-108">dans Masque de des indicateurs qui contrôle la suppression.</span><span class="sxs-lookup"><span data-stu-id="0d930-108">[in] A bitmask of flags that controls the deletion.</span></span> <span data-ttu-id="0d930-109">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="0d930-109">The following flag can be set:</span></span>
    
<span data-ttu-id="0d930-110">TAD_ALL_ROWS</span><span class="sxs-lookup"><span data-stu-id="0d930-110">TAD_ALL_ROWS</span></span> 
  
> <span data-ttu-id="0d930-111">Supprime toutes les lignes de la table et de toutes les vues correspondantes, en envoyant une seule notification TABLE_RELOAD.</span><span class="sxs-lookup"><span data-stu-id="0d930-111">Deletes all rows from the table and all corresponding views, sending a single TABLE_RELOAD notification.</span></span>
    
 <span data-ttu-id="0d930-112">_lprowsetToDelete_</span><span class="sxs-lookup"><span data-stu-id="0d930-112">_lprowsetToDelete_</span></span>
  
> <span data-ttu-id="0d930-113">dans Pointeur vers un jeu de lignes qui décrit les lignes à supprimer.</span><span class="sxs-lookup"><span data-stu-id="0d930-113">[in] A pointer to a row set that describes the rows to be deleted.</span></span> <span data-ttu-id="0d930-114">Le paramètre _lprowsetToDelete_ peut être null si l'indicateur TAD_ALL_ROWS est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="0d930-114">The  _lprowsetToDelete_ parameter can be NULL if the TAD_ALL_ROWS flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="0d930-115">_cRowsDeleted_</span><span class="sxs-lookup"><span data-stu-id="0d930-115">_cRowsDeleted_</span></span>
  
> <span data-ttu-id="0d930-116">remarquer Nombre de lignes supprimées.</span><span class="sxs-lookup"><span data-stu-id="0d930-116">[out] The count of the deleted rows.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0d930-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0d930-117">Return value</span></span>

<span data-ttu-id="0d930-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d930-118">S_OK</span></span> 
  
> <span data-ttu-id="0d930-119">Les lignes de tableau ont été supprimées avec succès.</span><span class="sxs-lookup"><span data-stu-id="0d930-119">The table rows were successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d930-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="0d930-120">Remarks</span></span>

<span data-ttu-id="0d930-121">La méthode **ITableData:: HrDeleteRows** localise et supprime les lignes de table qui contiennent les colonnes qui correspondent à la propriété sur laquelle pointe le membre **LpProps** de chaque **aRow** entrée du jeu de lignes.</span><span class="sxs-lookup"><span data-stu-id="0d930-121">The **ITableData::HrDeleteRows** method locates and removes the table rows that contain the columns that match the property pointed to by the **lpProps** member of each **aRow** entry in the row set.</span></span> <span data-ttu-id="0d930-122">Une colonne d'index est utilisée pour identifier chaque ligne; Cette colonne doit avoir la même balise de propriété que la balise de propriété passée dans le paramètre _ulPropTagIndexColumn_ dans l'appel à la fonction [CreateTable](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="0d930-122">An index column is used to identify each row; this column must have the same property tag as the property tag passed in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
  
<span data-ttu-id="0d930-123">Le nombre de lignes réellement supprimées est renvoyé dans _cRowsDeleted_.</span><span class="sxs-lookup"><span data-stu-id="0d930-123">The number of rows that were actually deleted is returned in  _cRowsDeleted_.</span></span> <span data-ttu-id="0d930-124">Aucune erreur n'est renvoyée si une ou plusieurs lignes sont introuvables.</span><span class="sxs-lookup"><span data-stu-id="0d930-124">No error is returned if one or more rows could not be found.</span></span> 
  
<span data-ttu-id="0d930-125">Une fois les lignes supprimées, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable:: Advise](imapitable-advise.md) pour s'inscrire aux notifications.</span><span class="sxs-lookup"><span data-stu-id="0d930-125">After the rows are deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="0d930-126">La suppression de lignes ne réduit pas les colonnes disponibles pour les affichages de tableau existants ou les vues de table ouvertes par la suite, même si les lignes supprimées sont les dernières qui contiennent des valeurs pour une colonne spécifique.</span><span class="sxs-lookup"><span data-stu-id="0d930-126">Deleting rows does not reduce the columns available to existing table views or subsequently opened table views, even if the deleted rows are the last that have values for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0d930-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d930-127">See also</span></span>



[<span data-ttu-id="0d930-128">CreateTable</span><span class="sxs-lookup"><span data-stu-id="0d930-128">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="0d930-129">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="0d930-129">ITableData::HrDeleteRow</span></span>](itabledata-hrdeleterow.md)
  
[<span data-ttu-id="0d930-130">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="0d930-130">ITableData::HrModifyRows</span></span>](itabledata-hrmodifyrows.md)
  
[<span data-ttu-id="0d930-131">SRowSet</span><span class="sxs-lookup"><span data-stu-id="0d930-131">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="0d930-132">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0d930-132">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="0d930-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d930-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

