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
ms.openlocfilehash: 968768fe75286b93bf12e349a4845fdfaa1923e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784478"
---
# <a name="itabledata--iunknown"></a><span data-ttu-id="1f8af-103">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f8af-103">ITableData : IUnknown</span></span>

  
  
<span data-ttu-id="1f8af-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1f8af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1f8af-105">Fournit des méthodes utilitaires pour l’utilisation des tableaux.</span><span class="sxs-lookup"><span data-stu-id="1f8af-105">Provides utility methods for working with tables.</span></span> <span data-ttu-id="1f8af-106">MAPI fournit des objets de données de table ou des objets qui implémentent **ITableData** pour aider les fournisseurs de services à effectuer la maintenance de la table.</span><span class="sxs-lookup"><span data-stu-id="1f8af-106">MAPI provides table data objects or objects that implement **ITableData** to help service providers perform table maintenance.</span></span> <span data-ttu-id="1f8af-107">Pour obtenir un objet de données de table, les fournisseurs de services appellent la fonction [Create table](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="1f8af-107">To obtain a table data object, service providers call the [CreateTable](createtable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f8af-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="1f8af-108">Header file:</span></span>  <br/> |<span data-ttu-id="1f8af-109">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1f8af-109">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1f8af-110">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="1f8af-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="1f8af-111">Objets de données de table</span><span class="sxs-lookup"><span data-stu-id="1f8af-111">Table data objects</span></span>  <br/> |
|<span data-ttu-id="1f8af-112">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="1f8af-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="1f8af-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="1f8af-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="1f8af-114">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="1f8af-114">Called by:</span></span>  <br/> |<span data-ttu-id="1f8af-115">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="1f8af-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="1f8af-116">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="1f8af-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1f8af-117">IID_IMAPITableData</span><span class="sxs-lookup"><span data-stu-id="1f8af-117">IID_IMAPITableData</span></span>  <br/> |
|<span data-ttu-id="1f8af-118">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="1f8af-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="1f8af-119">LPTABLEDATA</span><span class="sxs-lookup"><span data-stu-id="1f8af-119">LPTABLEDATA</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1f8af-120">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="1f8af-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1f8af-121">HrGetView</span><span class="sxs-lookup"><span data-stu-id="1f8af-121">HrGetView</span></span>](itabledata-hrgetview.md) <br/> |<span data-ttu-id="1f8af-122">Crée un affichage tableau, qui retourne un pointeur vers une implémentation [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="1f8af-122">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span>  <br/> |
|[<span data-ttu-id="1f8af-123">HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="1f8af-123">HrModifyRow</span></span>](itabledata-hrmodifyrow.md) <br/> |<span data-ttu-id="1f8af-124">Insérer une nouvelle ligne de tableau, en remplaçant éventuellement une ligne existante.</span><span class="sxs-lookup"><span data-stu-id="1f8af-124">Inserts a new table row, possibly replacing an existing row.</span></span>  <br/> |
|[<span data-ttu-id="1f8af-125">HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="1f8af-125">HrDeleteRow</span></span>](itabledata-hrdeleterow.md) <br/> |<span data-ttu-id="1f8af-126">Supprime une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="1f8af-126">Deletes a table row.</span></span>  <br/> |
|[<span data-ttu-id="1f8af-127">HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="1f8af-127">HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="1f8af-128">Récupère une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="1f8af-128">Retrieves a table row.</span></span>  <br/> |
|[<span data-ttu-id="1f8af-129">HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="1f8af-129">HrEnumRow</span></span>](itabledata-hrenumrow.md) <br/> |<span data-ttu-id="1f8af-130">Récupère une ligne en fonction de sa position dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="1f8af-130">Retrieves a row based on its position in the table.</span></span>  <br/> |
|[<span data-ttu-id="1f8af-131">HrNotify</span><span class="sxs-lookup"><span data-stu-id="1f8af-131">HrNotify</span></span>](itabledata-hrnotify.md) <br/> |<span data-ttu-id="1f8af-132">Envoie une notification pour une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="1f8af-132">Sends a notification for a table row.</span></span>  <br/> |
|[<span data-ttu-id="1f8af-133">HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="1f8af-133">HrInsertRow</span></span>](itabledata-hrinsertrow.md) <br/> |<span data-ttu-id="1f8af-134">Insère une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="1f8af-134">Inserts a table row.</span></span>  <br/> |
|[<span data-ttu-id="1f8af-135">HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="1f8af-135">HrModifyRows</span></span>](itabledata-hrmodifyrows.md) <br/> |<span data-ttu-id="1f8af-136">Insère plusieurs lignes de tableau, remplaçant éventuellement les lignes existantes.</span><span class="sxs-lookup"><span data-stu-id="1f8af-136">Inserts multiple table rows, possibly replacing existing rows.</span></span>  <br/> |
|[<span data-ttu-id="1f8af-137">HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="1f8af-137">HrDeleteRows</span></span>](itabledata-hrdeleterows.md) <br/> |<span data-ttu-id="1f8af-138">Supprime plusieurs lignes de tableau.</span><span class="sxs-lookup"><span data-stu-id="1f8af-138">Deletes multiple table rows.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f8af-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="1f8af-139">Remarks</span></span>

<span data-ttu-id="1f8af-140">L’implémentation de MAPI de **ITableData** fonctionne avec des tableaux en maintenant les restrictions associées et toutes les données en mémoire, rendant inapproprié pour une utilisation avec des tables très volumineuses.</span><span class="sxs-lookup"><span data-stu-id="1f8af-140">The MAPI implementation of **ITableData** works with tables by holding all of the data and any associated restrictions in memory, making it unsuitable for use with very large tables.</span></span> <span data-ttu-id="1f8af-141">Restrictions de grande taille et des opérations complexes, telles que la catégorisation ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1f8af-141">Large restrictions and complex operations such as categorization are not supported.</span></span> 
  
<span data-ttu-id="1f8af-142">Objets de données de table identifient les lignes à l’aide d’une colonne d’index, une propriété qui est la garantie d’avoir une valeur unique pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="1f8af-142">Table data objects identify rows by using an index column, a property that is guaranteed to have a unique value for each row.</span></span> <span data-ttu-id="1f8af-143">La plupart des fournisseurs de services utilisent la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) en tant que colonne de l’index.</span><span class="sxs-lookup"><span data-stu-id="1f8af-143">Most service providers use the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property as the index column.</span></span> <span data-ttu-id="1f8af-144">Propriétés ayant plusieurs valeurs ne peuvent pas être utilisées comme une colonne d’index.</span><span class="sxs-lookup"><span data-stu-id="1f8af-144">Properties that have multiple values cannot be used as an index column.</span></span>
  
<span data-ttu-id="1f8af-145">Objets de données de table de génèrent une notification unique quel que soit le nombre de lignes affectées par une modification ou la suppression.</span><span class="sxs-lookup"><span data-stu-id="1f8af-145">Table data objects generate a single notification regardless of the number of rows affected by a change or deletion.</span></span> <span data-ttu-id="1f8af-146">Si une ligne dans une opération cible n’existe pas, une ligne est ajoutée.</span><span class="sxs-lookup"><span data-stu-id="1f8af-146">If a target row in an operation does not exist, a row is added.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1f8af-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f8af-147">See also</span></span>



[<span data-ttu-id="1f8af-148">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="1f8af-148">MAPI Interfaces</span></span>](mapi-interfaces.md)

