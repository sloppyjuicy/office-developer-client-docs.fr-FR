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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 00662d7a5bf1c2addc5c4e0b39d657abd7073753
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784458"
---
# <a name="itabledatahrdeleterows"></a><span data-ttu-id="38412-103">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="38412-103">ITableData::HrDeleteRows</span></span>

  
  
<span data-ttu-id="38412-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38412-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38412-105">Supprime plusieurs lignes de tableau.</span><span class="sxs-lookup"><span data-stu-id="38412-105">Deletes multiple table rows.</span></span>
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a><span data-ttu-id="38412-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="38412-106">Parameters</span></span>

 <span data-ttu-id="38412-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="38412-107">_ulFlags_</span></span>
  
> <span data-ttu-id="38412-108">[in] Masque de bits d’indicateurs qui contrôle la suppression.</span><span class="sxs-lookup"><span data-stu-id="38412-108">[in] A bitmask of flags that controls the deletion.</span></span> <span data-ttu-id="38412-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="38412-109">The following flag can be set:</span></span>
    
<span data-ttu-id="38412-110">TAD_ALL_ROWS</span><span class="sxs-lookup"><span data-stu-id="38412-110">TAD_ALL_ROWS</span></span> 
  
> <span data-ttu-id="38412-111">Supprime toutes les lignes de la table et toutes les vues correspondants, l’envoi d’une notification TABLE_RELOAD unique.</span><span class="sxs-lookup"><span data-stu-id="38412-111">Deletes all rows from the table and all corresponding views, sending a single TABLE_RELOAD notification.</span></span>
    
 <span data-ttu-id="38412-112">_lprowsetToDelete_</span><span class="sxs-lookup"><span data-stu-id="38412-112">_lprowsetToDelete_</span></span>
  
> <span data-ttu-id="38412-113">[in] Pointeur vers un ensemble de lignes qui décrit les lignes à supprimer.</span><span class="sxs-lookup"><span data-stu-id="38412-113">[in] A pointer to a row set that describes the rows to be deleted.</span></span> <span data-ttu-id="38412-114">Le paramètre _lprowsetToDelete_ peut être NULL si l’indicateur TAD_ALL_ROWS est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="38412-114">The  _lprowsetToDelete_ parameter can be NULL if the TAD_ALL_ROWS flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="38412-115">_cRowsDeleted_</span><span class="sxs-lookup"><span data-stu-id="38412-115">_cRowsDeleted_</span></span>
  
> <span data-ttu-id="38412-116">[out] Le nombre de lignes supprimées.</span><span class="sxs-lookup"><span data-stu-id="38412-116">[out] The count of the deleted rows.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="38412-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="38412-117">Return value</span></span>

<span data-ttu-id="38412-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="38412-118">S_OK</span></span> 
  
> <span data-ttu-id="38412-119">Les lignes de table ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="38412-119">The table rows were successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38412-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="38412-120">Remarks</span></span>

<span data-ttu-id="38412-121">La méthode **ITableData::HrDeleteRows** localise et supprime les lignes de la table contenant les colonnes qui correspondent à la propriété pointée pour définir les par le membre **lpProps** de chaque entrée **: UGAL** dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="38412-121">The **ITableData::HrDeleteRows** method locates and removes the table rows that contain the columns that match the property pointed to by the **lpProps** member of each **aRow** entry in the row set.</span></span> <span data-ttu-id="38412-122">Une colonne d’index est utilisée pour identifier chaque ligne ; Cette colonne doit avoir la même balise de propriété en tant que la balise de propriété passée dans le paramètre _ulPropTagIndexColumn_ dans l’appel à la fonction [Create table](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="38412-122">An index column is used to identify each row; this column must have the same property tag as the property tag passed in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
  
<span data-ttu-id="38412-123">Le nombre de lignes qui ont été supprimées réellement est retourné dans _cRowsDeleted_.</span><span class="sxs-lookup"><span data-stu-id="38412-123">The number of rows that were actually deleted is returned in  _cRowsDeleted_.</span></span> <span data-ttu-id="38412-124">Aucune erreur n’est renvoyée si une ou plusieurs lignes est introuvable.</span><span class="sxs-lookup"><span data-stu-id="38412-124">No error is returned if one or more rows could not be found.</span></span> 
  
<span data-ttu-id="38412-125">Une fois que les lignes sont supprimées, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode la table [IMAPITable::Advise](imapitable-advise.md) pour inscrire les notifications.</span><span class="sxs-lookup"><span data-stu-id="38412-125">After the rows are deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="38412-126">Suppression de lignes ne réduit pas les colonnes aux tableaux existants ou ouvert par la suite des affichages tableau, même si les lignes supprimées sont la dernière ayant des valeurs d’une colonne spécifique.</span><span class="sxs-lookup"><span data-stu-id="38412-126">Deleting rows does not reduce the columns available to existing table views or subsequently opened table views, even if the deleted rows are the last that have values for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="38412-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38412-127">See also</span></span>



[<span data-ttu-id="38412-128">Create table</span><span class="sxs-lookup"><span data-stu-id="38412-128">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="38412-129">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="38412-129">ITableData::HrDeleteRow</span></span>](itabledata-hrdeleterow.md)
  
[<span data-ttu-id="38412-130">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="38412-130">ITableData::HrModifyRows</span></span>](itabledata-hrmodifyrows.md)
  
[<span data-ttu-id="38412-131">SRowSet</span><span class="sxs-lookup"><span data-stu-id="38412-131">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="38412-132">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="38412-132">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="38412-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38412-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

