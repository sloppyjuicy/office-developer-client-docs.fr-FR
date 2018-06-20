---
title: IMAPITable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable
api_type:
- COM
ms.assetid: f25be2b1-0f94-4a0c-b29d-d2201dc70ab7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0ffaf5909c978059343067c93a2b30f5969327e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784098"
---
# <a name="imapitable--iunknown"></a><span data-ttu-id="34551-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="34551-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="34551-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34551-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34551-105">Fournit une vue en lecture seule d’une table.</span><span class="sxs-lookup"><span data-stu-id="34551-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="34551-106">**IMAPITable** est utilisée par les clients et les fournisseurs de services pour manipuler l’apparence d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="34551-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34551-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="34551-107">Header file:</span></span>  <br/> |<span data-ttu-id="34551-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34551-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="34551-109">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="34551-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="34551-110">Objets table</span><span class="sxs-lookup"><span data-stu-id="34551-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="34551-111">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="34551-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="34551-112">Fournisseurs de services et MAPI</span><span class="sxs-lookup"><span data-stu-id="34551-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="34551-113">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="34551-113">Called by:</span></span>  <br/> |<span data-ttu-id="34551-114">Applications clientes, les fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="34551-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="34551-115">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="34551-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="34551-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="34551-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="34551-117">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="34551-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="34551-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="34551-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="34551-119">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="34551-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="34551-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="34551-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="34551-121">Retourne une structure [MAPIERROR](mapierror.md) contenant des informations sur l’erreur précédente dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="34551-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="34551-122">Conseiller</span><span class="sxs-lookup"><span data-stu-id="34551-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="34551-123">Enregistre pour recevoir une notification d’événements spécifiés affectant la table.</span><span class="sxs-lookup"><span data-stu-id="34551-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="34551-124">L’avertissement</span><span class="sxs-lookup"><span data-stu-id="34551-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="34551-125">Annule l’envoi de notifications précédemment configurées avec un appel à la méthode **IMAPITable::Advise** .</span><span class="sxs-lookup"><span data-stu-id="34551-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="34551-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="34551-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="34551-127">Renvoie l’état et le type de la table.</span><span class="sxs-lookup"><span data-stu-id="34551-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="34551-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="34551-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="34551-129">Définit les propriétés et l’ordre des propriétés apparaissent sous forme de colonnes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="34551-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="34551-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="34551-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="34551-131">Renvoie une liste de colonnes pour la table.</span><span class="sxs-lookup"><span data-stu-id="34551-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="34551-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="34551-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="34551-133">Renvoie le nombre total de lignes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="34551-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="34551-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="34551-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="34551-135">Déplace le curseur à un emplacement spécifique dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="34551-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="34551-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="34551-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="34551-137">Déplace le curseur à une position en fraction approximative dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="34551-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="34551-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="34551-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="34551-139">Extrait la position de ligne de tableau en cours du curseur, basée sur une valeur décimale.</span><span class="sxs-lookup"><span data-stu-id="34551-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="34551-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="34551-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="34551-141">Trouve la ligne suivante dans une table qui répond aux critères de recherche spécifiques.</span><span class="sxs-lookup"><span data-stu-id="34551-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="34551-142">Restreindre</span><span class="sxs-lookup"><span data-stu-id="34551-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="34551-143">Applique un filtre à une table, réduisant la ligne valeur uniquement les lignes correspondant aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="34551-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="34551-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="34551-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="34551-145">Marque la position actuelle de la table.</span><span class="sxs-lookup"><span data-stu-id="34551-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="34551-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="34551-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="34551-147">Libère la mémoire associée à un signet.</span><span class="sxs-lookup"><span data-stu-id="34551-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="34551-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="34551-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="34551-149">Trie les lignes de la table en fonction des critères de tri.</span><span class="sxs-lookup"><span data-stu-id="34551-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="34551-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="34551-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="34551-151">Récupère l’ordre de tri en cours pour une table.</span><span class="sxs-lookup"><span data-stu-id="34551-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="34551-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="34551-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="34551-153">Renvoie une ou plusieurs lignes d’une table, en commençant à l’emplacement du curseur.</span><span class="sxs-lookup"><span data-stu-id="34551-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="34551-154">Abandonner</span><span class="sxs-lookup"><span data-stu-id="34551-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="34551-155">Arrête toutes les opérations asynchrones en cours pour la table.</span><span class="sxs-lookup"><span data-stu-id="34551-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="34551-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="34551-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="34551-157">Développe une catégorie de table réduite, ajouter les lignes de feuilles appartenant à la catégorie à l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="34551-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="34551-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="34551-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="34551-159">Réduire une catégorie de table étendue, suppression des lignes feuille appartenant à la catégorie à partir de l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="34551-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="34551-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="34551-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="34551-161">Interrompt le traitement jusqu'à ce qu’un ou plusieurs asynchrones opérations en cours sur la table est terminé.</span><span class="sxs-lookup"><span data-stu-id="34551-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="34551-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="34551-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="34551-163">Retourne les données nécessaires à la recréation en cours réduit ou développé état d’une table, voir.</span><span class="sxs-lookup"><span data-stu-id="34551-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="34551-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="34551-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="34551-165">Reconstruit l’état actuel de développés ou réduit d’une table, voir l’aide de données qui a été enregistrées par un appel antérieur à la méthode **IMAPITable::GetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="34551-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="34551-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34551-166">See also</span></span>



[<span data-ttu-id="34551-167">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="34551-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

