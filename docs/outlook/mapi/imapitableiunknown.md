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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d6a13799da4ef9315f9c23317fa18853d71c72f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420114"
---
# <a name="imapitable--iunknown"></a><span data-ttu-id="2e97f-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e97f-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="2e97f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e97f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e97f-105">Fournit une vue en lecture seule d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="2e97f-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="2e97f-106">**IMAPITable est utilisé** par les clients et les fournisseurs de services pour manipuler la façon dont une table apparaît.</span><span class="sxs-lookup"><span data-stu-id="2e97f-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e97f-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2e97f-107">Header file:</span></span>  <br/> |<span data-ttu-id="2e97f-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e97f-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2e97f-109">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="2e97f-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="2e97f-110">Objets Table</span><span class="sxs-lookup"><span data-stu-id="2e97f-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="2e97f-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="2e97f-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="2e97f-112">Fournisseurs de services et MAPI</span><span class="sxs-lookup"><span data-stu-id="2e97f-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="2e97f-113">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="2e97f-113">Called by:</span></span>  <br/> |<span data-ttu-id="2e97f-114">Applications clientes, fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="2e97f-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="2e97f-115">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="2e97f-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2e97f-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="2e97f-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="2e97f-117">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="2e97f-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="2e97f-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="2e97f-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2e97f-119">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="2e97f-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2e97f-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="2e97f-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="2e97f-121">Renvoie une [structure MAPIERROR](mapierror.md) contenant des informations sur l’erreur précédente sur le tableau.</span><span class="sxs-lookup"><span data-stu-id="2e97f-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-122">Conseiller</span><span class="sxs-lookup"><span data-stu-id="2e97f-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="2e97f-123">S’inscrit pour recevoir une notification des événements spécifiés affectant la table.</span><span class="sxs-lookup"><span data-stu-id="2e97f-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-124">Unadvise</span><span class="sxs-lookup"><span data-stu-id="2e97f-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="2e97f-125">Annule l’envoi de notifications précédemment définies avec un appel à la **méthode IMAPITable::Advise.**</span><span class="sxs-lookup"><span data-stu-id="2e97f-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="2e97f-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="2e97f-127">Renvoie l’état et le type du tableau.</span><span class="sxs-lookup"><span data-stu-id="2e97f-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="2e97f-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="2e97f-129">Définit les propriétés et l’ordre particuliers des propriétés à voir apparaître sous la valeur de colonnes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="2e97f-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="2e97f-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="2e97f-131">Renvoie une liste de colonnes pour le tableau.</span><span class="sxs-lookup"><span data-stu-id="2e97f-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="2e97f-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="2e97f-133">Renvoie le nombre total de lignes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="2e97f-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="2e97f-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="2e97f-135">Déplace le curseur à une position spécifique dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="2e97f-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="2e97f-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="2e97f-137">Déplace le curseur vers une position fractionnaire approximative dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="2e97f-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="2e97f-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="2e97f-139">Extrait la position de ligne de tableau actuelle du curseur, en fonction d’une valeur fractionnaire.</span><span class="sxs-lookup"><span data-stu-id="2e97f-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="2e97f-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="2e97f-141">Recherche la ligne suivante dans un tableau qui correspond à des critères de recherche spécifiques.</span><span class="sxs-lookup"><span data-stu-id="2e97f-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-142">Restrict</span><span class="sxs-lookup"><span data-stu-id="2e97f-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="2e97f-143">Applique un filtre à un tableau, en réduisant le jeu de lignes uniquement aux lignes correspondant aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="2e97f-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="2e97f-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="2e97f-145">Marque la position actuelle du tableau.</span><span class="sxs-lookup"><span data-stu-id="2e97f-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="2e97f-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="2e97f-147">Libère la mémoire associée à un signet.</span><span class="sxs-lookup"><span data-stu-id="2e97f-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="2e97f-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="2e97f-149">Trie les lignes du tableau en fonction des critères de tri.</span><span class="sxs-lookup"><span data-stu-id="2e97f-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="2e97f-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="2e97f-151">Extrait l’ordre de tri actuel d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="2e97f-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="2e97f-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="2e97f-153">Renvoie une ou plusieurs lignes d’un tableau, en commençant à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="2e97f-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-154">Abandonner</span><span class="sxs-lookup"><span data-stu-id="2e97f-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="2e97f-155">Arrête toutes les opérations asynchrones en cours pour la table.</span><span class="sxs-lookup"><span data-stu-id="2e97f-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="2e97f-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="2e97f-157">Développe une catégorie de tableaux réduire, en ajoutant les lignes de feuille appartenant à la catégorie à l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="2e97f-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="2e97f-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="2e97f-159">Cette propriété permet de réduire une catégorie de tableaux développés, en supprimant les lignes de feuille appartenant à la catégorie de l’affichage Tableau.</span><span class="sxs-lookup"><span data-stu-id="2e97f-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="2e97f-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="2e97f-161">Suspend le traitement jusqu’à ce qu’une ou plusieurs opérations asynchrones en cours sur la table soient terminées.</span><span class="sxs-lookup"><span data-stu-id="2e97f-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="2e97f-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="2e97f-163">Renvoie les données nécessaires pour reconstruire l’état actuel, réduire ou développé, d’une table classée.</span><span class="sxs-lookup"><span data-stu-id="2e97f-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="2e97f-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="2e97f-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="2e97f-165">Reconstruit l’état étendu ou réduire actuel d’une table classée à l’aide de données enregistrées par un appel précédent à la méthode **IMAPITable::GetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="2e97f-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e97f-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e97f-166">See also</span></span>



[<span data-ttu-id="2e97f-167">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="2e97f-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

