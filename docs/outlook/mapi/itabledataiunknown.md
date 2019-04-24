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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3992bea899239ee5975505dec366490d6bbe1698
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348768"
---
# <a name="itabledata--iunknown"></a><span data-ttu-id="9de1f-103">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9de1f-103">ITableData : IUnknown</span></span>

  
  
<span data-ttu-id="9de1f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9de1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9de1f-105">Fournit des méthodes utilitaires pour utiliser des tableaux.</span><span class="sxs-lookup"><span data-stu-id="9de1f-105">Provides utility methods for working with tables.</span></span> <span data-ttu-id="9de1f-106">MAPI fournit des objets de données de tableau ou des objets qui implémentent **ITableData** pour aider les fournisseurs de services à effectuer la maintenance des tables.</span><span class="sxs-lookup"><span data-stu-id="9de1f-106">MAPI provides table data objects or objects that implement **ITableData** to help service providers perform table maintenance.</span></span> <span data-ttu-id="9de1f-107">Pour obtenir un objet de données de table, les fournisseurs de services appellent la fonction [CreateTable](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="9de1f-107">To obtain a table data object, service providers call the [CreateTable](createtable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9de1f-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="9de1f-108">Header file:</span></span>  <br/> |<span data-ttu-id="9de1f-109">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="9de1f-109">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9de1f-110">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="9de1f-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="9de1f-111">Objets de données de tableau</span><span class="sxs-lookup"><span data-stu-id="9de1f-111">Table data objects</span></span>  <br/> |
|<span data-ttu-id="9de1f-112">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="9de1f-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="9de1f-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="9de1f-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="9de1f-114">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="9de1f-114">Called by:</span></span>  <br/> |<span data-ttu-id="9de1f-115">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="9de1f-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="9de1f-116">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="9de1f-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9de1f-117">IID_IMAPITableData</span><span class="sxs-lookup"><span data-stu-id="9de1f-117">IID_IMAPITableData</span></span>  <br/> |
|<span data-ttu-id="9de1f-118">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="9de1f-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="9de1f-119">LPTABLEDATA</span><span class="sxs-lookup"><span data-stu-id="9de1f-119">LPTABLEDATA</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9de1f-120">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="9de1f-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9de1f-121">HrGetView</span><span class="sxs-lookup"><span data-stu-id="9de1f-121">HrGetView</span></span>](itabledata-hrgetview.md) <br/> |<span data-ttu-id="9de1f-122">Crée un affichage tableau en renvoyant un pointeur vers une implémentation [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="9de1f-122">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span>  <br/> |
|[<span data-ttu-id="9de1f-123">HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="9de1f-123">HrModifyRow</span></span>](itabledata-hrmodifyrow.md) <br/> |<span data-ttu-id="9de1f-124">Insère une nouvelle ligne de tableau, éventuellement en remplaçant une ligne existante.</span><span class="sxs-lookup"><span data-stu-id="9de1f-124">Inserts a new table row, possibly replacing an existing row.</span></span>  <br/> |
|[<span data-ttu-id="9de1f-125">HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="9de1f-125">HrDeleteRow</span></span>](itabledata-hrdeleterow.md) <br/> |<span data-ttu-id="9de1f-126">Supprime une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="9de1f-126">Deletes a table row.</span></span>  <br/> |
|[<span data-ttu-id="9de1f-127">HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="9de1f-127">HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="9de1f-128">Récupère une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="9de1f-128">Retrieves a table row.</span></span>  <br/> |
|[<span data-ttu-id="9de1f-129">HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="9de1f-129">HrEnumRow</span></span>](itabledata-hrenumrow.md) <br/> |<span data-ttu-id="9de1f-130">Récupère une ligne en fonction de sa position dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="9de1f-130">Retrieves a row based on its position in the table.</span></span>  <br/> |
|[<span data-ttu-id="9de1f-131">HrNotify</span><span class="sxs-lookup"><span data-stu-id="9de1f-131">HrNotify</span></span>](itabledata-hrnotify.md) <br/> |<span data-ttu-id="9de1f-132">Envoie une notification pour une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="9de1f-132">Sends a notification for a table row.</span></span>  <br/> |
|[<span data-ttu-id="9de1f-133">HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="9de1f-133">HrInsertRow</span></span>](itabledata-hrinsertrow.md) <br/> |<span data-ttu-id="9de1f-134">Insère une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="9de1f-134">Inserts a table row.</span></span>  <br/> |
|[<span data-ttu-id="9de1f-135">HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="9de1f-135">HrModifyRows</span></span>](itabledata-hrmodifyrows.md) <br/> |<span data-ttu-id="9de1f-136">Insère plusieurs lignes de tableau, susceptibles de remplacer des lignes existantes.</span><span class="sxs-lookup"><span data-stu-id="9de1f-136">Inserts multiple table rows, possibly replacing existing rows.</span></span>  <br/> |
|[<span data-ttu-id="9de1f-137">HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="9de1f-137">HrDeleteRows</span></span>](itabledata-hrdeleterows.md) <br/> |<span data-ttu-id="9de1f-138">Supprime plusieurs lignes de tableau.</span><span class="sxs-lookup"><span data-stu-id="9de1f-138">Deletes multiple table rows.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9de1f-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="9de1f-139">Remarks</span></span>

<span data-ttu-id="9de1f-140">L'implémentation MAPI de **ITableData** fonctionne avec les tableaux en stockant toutes les données et toutes les restrictions associées dans la mémoire, ce qui rend l'utilisation inappropriée avec des tables très volumineuses.</span><span class="sxs-lookup"><span data-stu-id="9de1f-140">The MAPI implementation of **ITableData** works with tables by holding all of the data and any associated restrictions in memory, making it unsuitable for use with very large tables.</span></span> <span data-ttu-id="9de1f-141">Les restrictions importantes et les opérations complexes telles que la catégorisation ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9de1f-141">Large restrictions and complex operations such as categorization are not supported.</span></span> 
  
<span data-ttu-id="9de1f-142">Les objets de données de tableau identifient les lignes à l'aide d'une colonne d'index, une propriété dont la valeur est garantie pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="9de1f-142">Table data objects identify rows by using an index column, a property that is guaranteed to have a unique value for each row.</span></span> <span data-ttu-id="9de1f-143">La plupart des fournisseurs de services utilisent la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) en tant que colonne d'index.</span><span class="sxs-lookup"><span data-stu-id="9de1f-143">Most service providers use the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property as the index column.</span></span> <span data-ttu-id="9de1f-144">Les propriétés qui ont plusieurs valeurs ne peuvent pas être utilisées en tant que colonne d'index.</span><span class="sxs-lookup"><span data-stu-id="9de1f-144">Properties that have multiple values cannot be used as an index column.</span></span>
  
<span data-ttu-id="9de1f-145">Les objets de données de tableau génèrent une seule notification, quel que soit le nombre de lignes affectées par une modification ou une suppression.</span><span class="sxs-lookup"><span data-stu-id="9de1f-145">Table data objects generate a single notification regardless of the number of rows affected by a change or deletion.</span></span> <span data-ttu-id="9de1f-146">S'il n'existe pas de ligne cible dans une opération, une ligne est ajoutée.</span><span class="sxs-lookup"><span data-stu-id="9de1f-146">If a target row in an operation does not exist, a row is added.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9de1f-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9de1f-147">See also</span></span>



[<span data-ttu-id="9de1f-148">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="9de1f-148">MAPI Interfaces</span></span>](mapi-interfaces.md)

