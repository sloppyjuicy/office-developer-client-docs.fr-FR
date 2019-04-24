---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b187cccc4505256b7ab4d580c30eeb2e15ebf574
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278858"
---
# <a name="itabledatahrdeleterow"></a><span data-ttu-id="146b9-103">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="146b9-103">ITableData::HrDeleteRow</span></span>

  
  
<span data-ttu-id="146b9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="146b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="146b9-105">Supprime une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="146b9-105">Deletes a table row.</span></span>
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="146b9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="146b9-106">Parameters</span></span>

 <span data-ttu-id="146b9-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="146b9-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="146b9-108">dans Pointeur vers une structure de valeur de propriété qui décrit la colonne d'index de la ligne à supprimer.</span><span class="sxs-lookup"><span data-stu-id="146b9-108">[in] A pointer to a property value structure that describes the index column for the row to be deleted.</span></span> <span data-ttu-id="146b9-109">Le membre **ulPropTag** de la structure de la valeur de la propriété doit contenir la même balise property que le paramètre _ulPropTagIndexColumn_ de l'appel à la fonction [CreateTable](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="146b9-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="146b9-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="146b9-110">Return value</span></span>

<span data-ttu-id="146b9-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="146b9-111">S_OK</span></span> 
  
> <span data-ttu-id="146b9-112">La ligne a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="146b9-112">The row was successfully deleted.</span></span>
    
<span data-ttu-id="146b9-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="146b9-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="146b9-114">La propriété désignée par le paramètre _lpSPropValue_ n'identifie pas une ligne dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="146b9-114">The property pointed to by the  _lpSPropValue_ parameter does not identify a row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="146b9-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="146b9-115">Remarks</span></span>

<span data-ttu-id="146b9-116">La méthode **ITableData:: HrDeleteRow** supprime la ligne de tableau qui contient la colonne qui correspond à la propriété désignée par le paramètre _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="146b9-116">The **ITableData::HrDeleteRow** method removes the table row that contains the column that matches the property pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="146b9-117">Les données de la ligne sont supprimées et la ligne est supprimée de toutes les vues ouvertes.</span><span class="sxs-lookup"><span data-stu-id="146b9-117">The data for the row is deleted and the row is removed from all open views.</span></span> 
  
<span data-ttu-id="146b9-118">Une fois la ligne supprimée, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable:: Advise](imapitable-advise.md) pour s'inscrire aux notifications.</span><span class="sxs-lookup"><span data-stu-id="146b9-118">After the row is deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="146b9-119">La suppression d'une ligne ne réduit pas le jeu de colonnes disponible pour les affichages existants ou les vues ouvertes par la suite, même si la ligne supprimée est la dernière ligne contenant une valeur pour une colonne spécifique.</span><span class="sxs-lookup"><span data-stu-id="146b9-119">Deleting a row does not reduce the column set that is available to existing views or subsequently opened views, even if the deleted row is the last row that has a value for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="146b9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="146b9-120">See also</span></span>



[<span data-ttu-id="146b9-121">CreateTable</span><span class="sxs-lookup"><span data-stu-id="146b9-121">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="146b9-122">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="146b9-122">ITableData::HrDeleteRows</span></span>](itabledata-hrdeleterows.md)
  
[<span data-ttu-id="146b9-123">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="146b9-123">ITableData::HrModifyRow</span></span>](itabledata-hrmodifyrow.md)
  
[<span data-ttu-id="146b9-124">SPropValue</span><span class="sxs-lookup"><span data-stu-id="146b9-124">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="146b9-125">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="146b9-125">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="146b9-126">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="146b9-126">ITableData : IUnknown</span></span>](itabledataiunknown.md)

