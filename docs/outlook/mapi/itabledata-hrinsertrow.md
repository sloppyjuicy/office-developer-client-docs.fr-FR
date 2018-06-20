---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 29fdbf060576ee9309473fddf8740b06229dae9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784457"
---
# <a name="itabledatahrinsertrow"></a><span data-ttu-id="8dc3e-103">ITableData::HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="8dc3e-103">ITableData::HrInsertRow</span></span>

  
  
<span data-ttu-id="8dc3e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8dc3e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8dc3e-105">Insère une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-105">Inserts a table row.</span></span> 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="8dc3e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8dc3e-106">Parameters</span></span>

 <span data-ttu-id="8dc3e-107">_uliRow_</span><span class="sxs-lookup"><span data-stu-id="8dc3e-107">_uliRow_</span></span>
  
> <span data-ttu-id="8dc3e-108">[in] Un numéro de ligne séquentiel qui représente une ligne spécifique.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-108">[in] A sequential row number that represents a specific row.</span></span> <span data-ttu-id="8dc3e-109">La nouvelle ligne est placée après la ligne qui indique le nombre.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-109">The new row will be placed after the row that the number indicates.</span></span> <span data-ttu-id="8dc3e-110">Le paramètre _uliRow_ peut contenir des numéros de ligne de n à 0, où n est le nombre total de lignes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-110">The  _uliRow_ parameter can contains row numbers from 0 through n, where n is the total number of rows in the table.</span></span> <span data-ttu-id="8dc3e-111">En passant n _uliRow_ ajoute la ligne à la fin de la table.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-111">Passing n in  _uliRow_ appends the row to the end of the table.</span></span> 
    
 <span data-ttu-id="8dc3e-112">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="8dc3e-112">_lpSRow_</span></span>
  
> <span data-ttu-id="8dc3e-113">[in] Pointeur vers une structure [SRow](srow.md) qui décrit la ligne doit être inséré.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-113">[in] A pointer to an [SRow](srow.md) structure that describes the row to be inserted.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8dc3e-114">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8dc3e-114">Return value</span></span>

<span data-ttu-id="8dc3e-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="8dc3e-115">S_OK</span></span> 
  
> <span data-ttu-id="8dc3e-116">La ligne a été insérée correctement.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-116">The row was successfully inserted.</span></span>
    
<span data-ttu-id="8dc3e-117">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8dc3e-117">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="8dc3e-118">Une ligne qui possède la même valeur pour la colonne d’index que la ligne doit être inséré déjà existe dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-118">A row that has the same value for its index column as the row to be inserted already exists in the table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8dc3e-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="8dc3e-119">Remarks</span></span>

<span data-ttu-id="8dc3e-120">La méthode **ITableData::HrInsertRow** insère une ligne dans une table à un emplacement particulier.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-120">The **ITableData::HrInsertRow** method inserts a row into a table at a particular position.</span></span> <span data-ttu-id="8dc3e-121">La nouvelle ligne est insérée après la ligne qui se trouve dans la position spécifiée par le paramètre _uliRow_ .</span><span class="sxs-lookup"><span data-stu-id="8dc3e-121">The new row is inserted after the row that is in the position specified by the  _uliRow_ parameter.</span></span> 
  
<span data-ttu-id="8dc3e-122">Si _uliRow_ est défini sur le nombre de lignes dans le tableau, la nouvelle ligne est ajoutée à la fin de la table.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-122">If  _uliRow_ is set to the number of rows in the table, the new row is appended to the end of the table.</span></span> 
  
<span data-ttu-id="8dc3e-123">La propriété agit en tant que la colonne d’index pour la table doit être incluse dans le membre **lpProps** de la structure [SRow](srow.md) désigné par le paramètre _lpSRow_ .</span><span class="sxs-lookup"><span data-stu-id="8dc3e-123">The property that acts as the index column for the table must be included in the **lpProps** member of the [SRow](srow.md) structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="8dc3e-124">Cette propriété index, généralement **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), sert à identifier de manière unique la ligne pour les tâches de maintenance future.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-124">This index property, typically **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), is used to uniquely identify the row for future maintenance tasks.</span></span>
  
<span data-ttu-id="8dc3e-125">Les colonnes de propriétés dans la structure **SRow** n’ont pas à se trouver dans le même ordre que les colonnes de propriétés dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-125">The property columns in the **SRow** structure do not have to be in the same order as the property columns in the table.</span></span> 
  
<span data-ttu-id="8dc3e-126">Une fois que la ligne est insérée, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode la table [IMAPITable::Advise](imapitable-advise.md) pour inscrire les notifications.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-126">After the row is inserted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="8dc3e-127">Aucune notification n’est envoyée si la ligne insérée n’est pas incluse dans l’affichage en raison d’une restriction.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-127">No notification is sent if the inserted row is not included in the view due to a restriction.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8dc3e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dc3e-128">See also</span></span>



[<span data-ttu-id="8dc3e-129">SRow</span><span class="sxs-lookup"><span data-stu-id="8dc3e-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="8dc3e-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8dc3e-130">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="8dc3e-131">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8dc3e-131">ITableData : IUnknown</span></span>](itabledataiunknown.md)

