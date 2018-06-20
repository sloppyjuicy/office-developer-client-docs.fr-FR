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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 37d0ce65e125b2420af775d61ead51db189758ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784462"
---
# <a name="itabledatahrdeleterow"></a><span data-ttu-id="9748b-103">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="9748b-103">ITableData::HrDeleteRow</span></span>

  
  
<span data-ttu-id="9748b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9748b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9748b-105">Supprime une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="9748b-105">Deletes a table row.</span></span>
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="9748b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9748b-106">Parameters</span></span>

 <span data-ttu-id="9748b-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="9748b-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="9748b-108">[in] Pointeur vers une structure de valeur de propriété qui décrit la colonne d’index de la ligne à supprimer.</span><span class="sxs-lookup"><span data-stu-id="9748b-108">[in] A pointer to a property value structure that describes the index column for the row to be deleted.</span></span> <span data-ttu-id="9748b-109">Le membre **ulPropTag** de la structure de valeur de propriété doit contenir la même balise de propriété en tant que paramètre _ulPropTagIndexColumn_ de l’appel à la fonction [Create table](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="9748b-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9748b-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="9748b-110">Return value</span></span>

<span data-ttu-id="9748b-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="9748b-111">S_OK</span></span> 
  
> <span data-ttu-id="9748b-112">La ligne a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="9748b-112">The row was successfully deleted.</span></span>
    
<span data-ttu-id="9748b-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9748b-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="9748b-114">La propriété désignée par le paramètre _lpSPropValue_ n’identifie pas une ligne dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="9748b-114">The property pointed to by the  _lpSPropValue_ parameter does not identify a row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9748b-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="9748b-115">Remarks</span></span>

<span data-ttu-id="9748b-116">La méthode **ITableData::HrDeleteRow** supprime la ligne de tableau qui contient la colonne qui correspond à la propriété désignée par le paramètre _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="9748b-116">The **ITableData::HrDeleteRow** method removes the table row that contains the column that matches the property pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="9748b-117">Les données de la ligne sont supprimées et la ligne est supprimée de toutes les vues ouvertes.</span><span class="sxs-lookup"><span data-stu-id="9748b-117">The data for the row is deleted and the row is removed from all open views.</span></span> 
  
<span data-ttu-id="9748b-118">Une fois que la ligne est supprimée, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode la table [IMAPITable::Advise](imapitable-advise.md) pour inscrire les notifications.</span><span class="sxs-lookup"><span data-stu-id="9748b-118">After the row is deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="9748b-119">Suppression d’une ligne ne réduit pas l’ensemble de colonnes qui est disponible pour les vues existantes ou ouvert par la suite les affichages, même si la ligne supprimée est la dernière ligne ayant une valeur d’une colonne spécifique.</span><span class="sxs-lookup"><span data-stu-id="9748b-119">Deleting a row does not reduce the column set that is available to existing views or subsequently opened views, even if the deleted row is the last row that has a value for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9748b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9748b-120">See also</span></span>



[<span data-ttu-id="9748b-121">Create table</span><span class="sxs-lookup"><span data-stu-id="9748b-121">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="9748b-122">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="9748b-122">ITableData::HrDeleteRows</span></span>](itabledata-hrdeleterows.md)
  
[<span data-ttu-id="9748b-123">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="9748b-123">ITableData::HrModifyRow</span></span>](itabledata-hrmodifyrow.md)
  
[<span data-ttu-id="9748b-124">SPropValue</span><span class="sxs-lookup"><span data-stu-id="9748b-124">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="9748b-125">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9748b-125">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="9748b-126">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9748b-126">ITableData : IUnknown</span></span>](itabledataiunknown.md)

