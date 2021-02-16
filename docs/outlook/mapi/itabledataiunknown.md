---
title: ITableData IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3992bea899239ee5975505dec366490d6bbe1698
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430594"
---
# <a name="itabledata--iunknown"></a><span data-ttu-id="7b7c0-103">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b7c0-103">ITableData : IUnknown</span></span>

  
  
<span data-ttu-id="7b7c0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b7c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b7c0-105">Fournit des méthodes utilitaires pour travailler avec des tableaux.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-105">Provides utility methods for working with tables.</span></span> <span data-ttu-id="7b7c0-106">MAPI fournit des objets de données de table ou des objets qui implémentent **ITableData** pour aider les fournisseurs de services à effectuer la maintenance de table.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-106">MAPI provides table data objects or objects that implement **ITableData** to help service providers perform table maintenance.</span></span> <span data-ttu-id="7b7c0-107">Pour obtenir un objet de données de table, les fournisseurs de services appellent [la fonction CreateTable.](createtable.md)</span><span class="sxs-lookup"><span data-stu-id="7b7c0-107">To obtain a table data object, service providers call the [CreateTable](createtable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b7c0-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7b7c0-108">Header file:</span></span>  <br/> |<span data-ttu-id="7b7c0-109">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7b7c0-109">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7b7c0-110">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="7b7c0-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="7b7c0-111">Objets de données de tableau</span><span class="sxs-lookup"><span data-stu-id="7b7c0-111">Table data objects</span></span>  <br/> |
|<span data-ttu-id="7b7c0-112">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="7b7c0-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="7b7c0-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="7b7c0-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="7b7c0-114">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="7b7c0-114">Called by:</span></span>  <br/> |<span data-ttu-id="7b7c0-115">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="7b7c0-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="7b7c0-116">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="7b7c0-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7b7c0-117">IID_IMAPITableData</span><span class="sxs-lookup"><span data-stu-id="7b7c0-117">IID_IMAPITableData</span></span>  <br/> |
|<span data-ttu-id="7b7c0-118">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="7b7c0-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="7b7c0-119">LPTABLEDATA</span><span class="sxs-lookup"><span data-stu-id="7b7c0-119">LPTABLEDATA</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7b7c0-120">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="7b7c0-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7b7c0-121">HrGetView</span><span class="sxs-lookup"><span data-stu-id="7b7c0-121">HrGetView</span></span>](itabledata-hrgetview.md) <br/> |<span data-ttu-id="7b7c0-122">Crée une vue de tableau, renvoyant un pointeur vers une [implémentation IMAPITable.](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="7b7c0-122">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span>  <br/> |
|[<span data-ttu-id="7b7c0-123">HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="7b7c0-123">HrModifyRow</span></span>](itabledata-hrmodifyrow.md) <br/> |<span data-ttu-id="7b7c0-124">Insère une nouvelle ligne de tableau, éventuellement en remplaçant une ligne existante.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-124">Inserts a new table row, possibly replacing an existing row.</span></span>  <br/> |
|[<span data-ttu-id="7b7c0-125">HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="7b7c0-125">HrDeleteRow</span></span>](itabledata-hrdeleterow.md) <br/> |<span data-ttu-id="7b7c0-126">Supprime une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-126">Deletes a table row.</span></span>  <br/> |
|[<span data-ttu-id="7b7c0-127">HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="7b7c0-127">HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="7b7c0-128">Récupère une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-128">Retrieves a table row.</span></span>  <br/> |
|[<span data-ttu-id="7b7c0-129">HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="7b7c0-129">HrEnumRow</span></span>](itabledata-hrenumrow.md) <br/> |<span data-ttu-id="7b7c0-130">Extrait une ligne en fonction de sa position dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-130">Retrieves a row based on its position in the table.</span></span>  <br/> |
|[<span data-ttu-id="7b7c0-131">HrNotify</span><span class="sxs-lookup"><span data-stu-id="7b7c0-131">HrNotify</span></span>](itabledata-hrnotify.md) <br/> |<span data-ttu-id="7b7c0-132">Envoie une notification pour une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-132">Sends a notification for a table row.</span></span>  <br/> |
|[<span data-ttu-id="7b7c0-133">HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="7b7c0-133">HrInsertRow</span></span>](itabledata-hrinsertrow.md) <br/> |<span data-ttu-id="7b7c0-134">Insère une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-134">Inserts a table row.</span></span>  <br/> |
|[<span data-ttu-id="7b7c0-135">HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="7b7c0-135">HrModifyRows</span></span>](itabledata-hrmodifyrows.md) <br/> |<span data-ttu-id="7b7c0-136">Insère plusieurs lignes de tableau, en remplaçant éventuellement les lignes existantes.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-136">Inserts multiple table rows, possibly replacing existing rows.</span></span>  <br/> |
|[<span data-ttu-id="7b7c0-137">HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="7b7c0-137">HrDeleteRows</span></span>](itabledata-hrdeleterows.md) <br/> |<span data-ttu-id="7b7c0-138">Supprime plusieurs lignes de tableau.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-138">Deletes multiple table rows.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b7c0-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="7b7c0-139">Remarks</span></span>

<span data-ttu-id="7b7c0-140">L’implémentation MAPI **d’ITableData** fonctionne avec les tables en maintenant toutes les données et les restrictions associées en mémoire, ce qui la rend inadaptée pour une utilisation avec des tableaux très grands.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-140">The MAPI implementation of **ITableData** works with tables by holding all of the data and any associated restrictions in memory, making it unsuitable for use with very large tables.</span></span> <span data-ttu-id="7b7c0-141">Les restrictions importantes et les opérations complexes telles que la catégorisation ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-141">Large restrictions and complex operations such as categorization are not supported.</span></span> 
  
<span data-ttu-id="7b7c0-142">Les objets de données de tableau identifient les lignes à l’aide d’une colonne d’index, propriété dont la valeur est unique pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-142">Table data objects identify rows by using an index column, a property that is guaranteed to have a unique value for each row.</span></span> <span data-ttu-id="7b7c0-143">La plupart des fournisseurs de services **utilisent la PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) comme colonne d’index.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-143">Most service providers use the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property as the index column.</span></span> <span data-ttu-id="7b7c0-144">Les propriétés qui ont plusieurs valeurs ne peuvent pas être utilisées comme colonne d’index.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-144">Properties that have multiple values cannot be used as an index column.</span></span>
  
<span data-ttu-id="7b7c0-145">Les objets de données de tableau génèrent une notification unique, quel que soit le nombre de lignes affectées par une modification ou une suppression.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-145">Table data objects generate a single notification regardless of the number of rows affected by a change or deletion.</span></span> <span data-ttu-id="7b7c0-146">Si une ligne cible dans une opération n’existe pas, une ligne est ajoutée.</span><span class="sxs-lookup"><span data-stu-id="7b7c0-146">If a target row in an operation does not exist, a row is added.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7b7c0-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b7c0-147">See also</span></span>



[<span data-ttu-id="7b7c0-148">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="7b7c0-148">MAPI Interfaces</span></span>](mapi-interfaces.md)

