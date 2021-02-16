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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b187cccc4505256b7ab4d580c30eeb2e15ebf574
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421675"
---
# <a name="itabledatahrdeleterow"></a><span data-ttu-id="17773-103">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="17773-103">ITableData::HrDeleteRow</span></span>

  
  
<span data-ttu-id="17773-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17773-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17773-105">Supprime une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="17773-105">Deletes a table row.</span></span>
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="17773-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17773-106">Parameters</span></span>

 <span data-ttu-id="17773-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="17773-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="17773-108">[in] Pointeur vers une structure de valeurs de propriété qui décrit la colonne d’index de la ligne à supprimer.</span><span class="sxs-lookup"><span data-stu-id="17773-108">[in] A pointer to a property value structure that describes the index column for the row to be deleted.</span></span> <span data-ttu-id="17773-109">Le **membre ulPropTag** de la structure de valeurs de propriété doit contenir la même balise de propriété que le paramètre _ulPropTagIndexColumn_ de l’appel à la [fonction CreateTable.](createtable.md)</span><span class="sxs-lookup"><span data-stu-id="17773-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="17773-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="17773-110">Return value</span></span>

<span data-ttu-id="17773-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="17773-111">S_OK</span></span> 
  
> <span data-ttu-id="17773-112">La ligne a été supprimée avec succès.</span><span class="sxs-lookup"><span data-stu-id="17773-112">The row was successfully deleted.</span></span>
    
<span data-ttu-id="17773-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="17773-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="17773-114">La propriété pointée par  _le paramètre lpSPropValue_ n’identifie pas une ligne dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="17773-114">The property pointed to by the  _lpSPropValue_ parameter does not identify a row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="17773-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="17773-115">Remarks</span></span>

<span data-ttu-id="17773-116">La **méthode ITableData::HrDeleteRow** supprime la ligne de tableau qui contient la colonne qui correspond à la propriété pointée par le paramètre _lpSPropValue._</span><span class="sxs-lookup"><span data-stu-id="17773-116">The **ITableData::HrDeleteRow** method removes the table row that contains the column that matches the property pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="17773-117">Les données de la ligne sont supprimées et la ligne est supprimée de tous les affichages ouverts.</span><span class="sxs-lookup"><span data-stu-id="17773-117">The data for the row is deleted and the row is removed from all open views.</span></span> 
  
<span data-ttu-id="17773-118">Une fois la ligne supprimée, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable::Advise](imapitable-advise.md) de la table pour s’inscrire aux notifications.</span><span class="sxs-lookup"><span data-stu-id="17773-118">After the row is deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="17773-119">La suppression d’une ligne ne réduit pas le jeu de colonnes disponible pour les affichages existants ou les affichages ouverts par la suite, même si la ligne supprimée est la dernière ligne qui a une valeur pour une colonne spécifique.</span><span class="sxs-lookup"><span data-stu-id="17773-119">Deleting a row does not reduce the column set that is available to existing views or subsequently opened views, even if the deleted row is the last row that has a value for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="17773-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17773-120">See also</span></span>



[<span data-ttu-id="17773-121">CreateTable</span><span class="sxs-lookup"><span data-stu-id="17773-121">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="17773-122">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="17773-122">ITableData::HrDeleteRows</span></span>](itabledata-hrdeleterows.md)
  
[<span data-ttu-id="17773-123">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="17773-123">ITableData::HrModifyRow</span></span>](itabledata-hrmodifyrow.md)
  
[<span data-ttu-id="17773-124">SPropValue</span><span class="sxs-lookup"><span data-stu-id="17773-124">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="17773-125">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="17773-125">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="17773-126">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="17773-126">ITableData : IUnknown</span></span>](itabledataiunknown.md)

