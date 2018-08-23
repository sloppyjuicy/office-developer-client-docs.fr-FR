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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5ef210aedc884e5c09eca6335199e2ef284b901c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574831"
---
# <a name="itabledatahrmodifyrow"></a><span data-ttu-id="12b18-103">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="12b18-103">ITableData::HrModifyRow</span></span>

  
  
<span data-ttu-id="12b18-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12b18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12b18-105">Insérer une nouvelle ligne de tableau, en remplaçant éventuellement une ligne existante.</span><span class="sxs-lookup"><span data-stu-id="12b18-105">Inserts a new table row, possibly replacing an existing row.</span></span>
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="12b18-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12b18-106">Parameters</span></span>

 <span data-ttu-id="12b18-107">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="12b18-107">_lpSRow_</span></span>
  
> <span data-ttu-id="12b18-108">[in] Pointeur vers une structure [SRow](srow.md) qui décrit la ligne à ajouter ou pour remplacer une ligne existante.</span><span class="sxs-lookup"><span data-stu-id="12b18-108">[in] A pointer to an [SRow](srow.md) structure that describes the row to be added or to replace an existing row.</span></span> <span data-ttu-id="12b18-109">Une des structures de valeur de propriété vers laquelle pointés le membre **lpProps** de la structure **SRow** doit contenir la colonne d’index, la même valeur que celle qui a été spécifiée dans le paramètre _ulPropTagIndexColumn_ dans l’appel à la [Create table ](createtable.md)fonction.</span><span class="sxs-lookup"><span data-stu-id="12b18-109">One of the property value structures pointed to by the **lpProps** member of the **SRow** structure should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="12b18-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="12b18-110">Return value</span></span>

<span data-ttu-id="12b18-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="12b18-111">S_OK</span></span> 
  
> <span data-ttu-id="12b18-112">La ligne a été correctement insérée ou modifiée.</span><span class="sxs-lookup"><span data-stu-id="12b18-112">The row was successfully inserted or modified.</span></span>
    
<span data-ttu-id="12b18-113">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="12b18-113">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="12b18-114">La ligne dans le passé ne dispose pas d’une colonne d’index.</span><span class="sxs-lookup"><span data-stu-id="12b18-114">The passed-in row does not have an index column.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="12b18-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="12b18-115">Remarks</span></span>

<span data-ttu-id="12b18-116">La méthode **ITableData::HrModifyRow** insère la ligne décrite par la structure **SRow** désignée par le paramètre _lpSRow_ .</span><span class="sxs-lookup"><span data-stu-id="12b18-116">The **ITableData::HrModifyRow** method inserts the row described by the **SRow** structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="12b18-117">Si une ligne qui possède la même valeur pour la colonne d’index en tant que la ligne qui pointe _lpSRow_ existe déjà dans le tableau, la ligne existante est remplacée.</span><span class="sxs-lookup"><span data-stu-id="12b18-117">If a row that has the same value for its index column as the row that  _lpSRow_ points to already exists in the table, the existing row is replaced.</span></span> <span data-ttu-id="12b18-118">Si aucune ligne n’existe qui correspond à celui qui est inclus dans la structure **SRow** , **HrModifyRow** ajoute la ligne à la fin de la table.</span><span class="sxs-lookup"><span data-stu-id="12b18-118">If no row exists that matches the one included in the **SRow** structure, **HrModifyRow** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="12b18-119">Toutes les vues de la table sont modifiées pour inclure la ligne désignée par _lpSRow_.</span><span class="sxs-lookup"><span data-stu-id="12b18-119">All views of the table are modified to include the row pointed to by  _lpSRow_.</span></span> <span data-ttu-id="12b18-120">Toutefois, si un affichage a une restriction en place qui exclut de la ligne, il peut être pas visible à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="12b18-120">However, if a view has a restriction in place that excludes the row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="12b18-121">Les colonnes de la ligne désignés par _lpSRow_ n’ont pas à inclure dans le même ordre que les colonnes de la table.</span><span class="sxs-lookup"><span data-stu-id="12b18-121">The columns in the row pointed to by  _lpSRow_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="12b18-122">L’appelant peut également inclure en tant que propriétés de colonnes qui ne sont pas actuellement dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="12b18-122">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="12b18-123">Pour des vues existantes, **HrModifyRow** rend ces nouvelles colonnes disponibles, mais n’inclut pas les dans la colonne en cours.</span><span class="sxs-lookup"><span data-stu-id="12b18-123">For existing views, **HrModifyRow** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="12b18-124">Pour les affichages futures, **HrModifyRow** inclut les nouvelles colonnes dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="12b18-124">For future views, **HrModifyRow** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="12b18-125">Une fois que **HrModifyRow** ajoute la ligne, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode la table [IMAPITable::Advise](imapitable-advise.md) pour inscrire les notifications.</span><span class="sxs-lookup"><span data-stu-id="12b18-125">After **HrModifyRow** adds the row, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="12b18-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12b18-126">See also</span></span>



[<span data-ttu-id="12b18-127">SRow</span><span class="sxs-lookup"><span data-stu-id="12b18-127">SRow</span></span>](srow.md)
  
[<span data-ttu-id="12b18-128">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="12b18-128">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="12b18-129">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="12b18-129">ITableData : IUnknown</span></span>](itabledataiunknown.md)

