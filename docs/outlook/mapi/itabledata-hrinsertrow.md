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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2709ac612fc9e2edaa57b280d52c0a5229ee9978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435438"
---
# <a name="itabledatahrinsertrow"></a><span data-ttu-id="12631-103">ITableData::HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="12631-103">ITableData::HrInsertRow</span></span>

  
  
<span data-ttu-id="12631-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12631-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12631-105">Insère une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="12631-105">Inserts a table row.</span></span> 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="12631-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12631-106">Parameters</span></span>

 <span data-ttu-id="12631-107">_uliRow_</span><span class="sxs-lookup"><span data-stu-id="12631-107">_uliRow_</span></span>
  
> <span data-ttu-id="12631-108">dans Numéro de ligne séquentiel qui représente une ligne spécifique.</span><span class="sxs-lookup"><span data-stu-id="12631-108">[in] A sequential row number that represents a specific row.</span></span> <span data-ttu-id="12631-109">La nouvelle ligne est placée après la ligne que le numéro indique.</span><span class="sxs-lookup"><span data-stu-id="12631-109">The new row will be placed after the row that the number indicates.</span></span> <span data-ttu-id="12631-110">Le paramètre _uliRow_ peut contenir des numéros de ligne compris entre 0 et n, où n représente le nombre total de lignes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="12631-110">The  _uliRow_ parameter can contains row numbers from 0 through n, where n is the total number of rows in the table.</span></span> <span data-ttu-id="12631-111">Le passage de n dans _uliRow_ ajoute la ligne à la fin du tableau.</span><span class="sxs-lookup"><span data-stu-id="12631-111">Passing n in  _uliRow_ appends the row to the end of the table.</span></span> 
    
 <span data-ttu-id="12631-112">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="12631-112">_lpSRow_</span></span>
  
> <span data-ttu-id="12631-113">dans Pointeur vers une structure [SRow](srow.md) qui décrit la ligne à insérer.</span><span class="sxs-lookup"><span data-stu-id="12631-113">[in] A pointer to an [SRow](srow.md) structure that describes the row to be inserted.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="12631-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="12631-114">Return value</span></span>

<span data-ttu-id="12631-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="12631-115">S_OK</span></span> 
  
> <span data-ttu-id="12631-116">La ligne a été insérée.</span><span class="sxs-lookup"><span data-stu-id="12631-116">The row was successfully inserted.</span></span>
    
<span data-ttu-id="12631-117">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="12631-117">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="12631-118">Une ligne qui a la même valeur pour sa colonne d'index que la ligne à insérer existe déjà dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="12631-118">A row that has the same value for its index column as the row to be inserted already exists in the table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="12631-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="12631-119">Remarks</span></span>

<span data-ttu-id="12631-120">La méthode **ITableData:: HrInsertRow** insère une ligne dans un tableau à une position particulière.</span><span class="sxs-lookup"><span data-stu-id="12631-120">The **ITableData::HrInsertRow** method inserts a row into a table at a particular position.</span></span> <span data-ttu-id="12631-121">La nouvelle ligne est insérée après la ligne qui se trouve à l'emplacement spécifié par le paramètre _uliRow_ .</span><span class="sxs-lookup"><span data-stu-id="12631-121">The new row is inserted after the row that is in the position specified by the  _uliRow_ parameter.</span></span> 
  
<span data-ttu-id="12631-122">Si _uliRow_ est défini sur le nombre de lignes du tableau, la nouvelle ligne est ajoutée à la fin du tableau.</span><span class="sxs-lookup"><span data-stu-id="12631-122">If  _uliRow_ is set to the number of rows in the table, the new row is appended to the end of the table.</span></span> 
  
<span data-ttu-id="12631-123">La propriété qui agit comme colonne d'index pour la table doit être incluse dans le membre **lpProps** de la structure [SRow](srow.md) vers laquelle pointe le paramètre _lpSRow_ .</span><span class="sxs-lookup"><span data-stu-id="12631-123">The property that acts as the index column for the table must be included in the **lpProps** member of the [SRow](srow.md) structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="12631-124">Cette propriété d'index, généralement **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), est utilisée pour identifier la ligne de manière unique pour les tâches de maintenance futures.</span><span class="sxs-lookup"><span data-stu-id="12631-124">This index property, typically **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), is used to uniquely identify the row for future maintenance tasks.</span></span>
  
<span data-ttu-id="12631-125">Les colonnes de propriétés de la structure **SRow** n'ont pas besoin d'être dans le même ordre que les colonnes de propriétés de la table.</span><span class="sxs-lookup"><span data-stu-id="12631-125">The property columns in the **SRow** structure do not have to be in the same order as the property columns in the table.</span></span> 
  
<span data-ttu-id="12631-126">Une fois que la ligne est insérée, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable:: Advise](imapitable-advise.md) pour s'inscrire aux notifications.</span><span class="sxs-lookup"><span data-stu-id="12631-126">After the row is inserted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="12631-127">Aucune notification n'est envoyée si la ligne insérée n'est pas incluse dans l'affichage en raison d'une restriction.</span><span class="sxs-lookup"><span data-stu-id="12631-127">No notification is sent if the inserted row is not included in the view due to a restriction.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="12631-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12631-128">See also</span></span>



[<span data-ttu-id="12631-129">SRow</span><span class="sxs-lookup"><span data-stu-id="12631-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="12631-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="12631-130">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="12631-131">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="12631-131">ITableData : IUnknown</span></span>](itabledataiunknown.md)

