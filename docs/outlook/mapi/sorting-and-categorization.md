---
title: Tri et catégorisation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418483"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="4d57e-103">Tri et catégorisation</span><span class="sxs-lookup"><span data-stu-id="4d57e-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="4d57e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d57e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d57e-105">Le tri d’un tableau place les lignes dans un ordre logique pour sa visionneuse.</span><span class="sxs-lookup"><span data-stu-id="4d57e-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="4d57e-106">Par exemple, une visionneuse peut préférer voir la table des matières d’un dossier trié par objet du message afin que tous les threads d’une conversation soient ensemble, tandis qu’une autre visionneuse souhaite peut-être trier les messages par le nom de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="4d57e-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="4d57e-107">Une table nouvellement ins instantiée n’est pas nécessairement triée dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="4d57e-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="4d57e-108">Il existe deux types de tri :</span><span class="sxs-lookup"><span data-stu-id="4d57e-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="4d57e-109">Tri standard</span><span class="sxs-lookup"><span data-stu-id="4d57e-109">Standard sorting</span></span>
    
- <span data-ttu-id="4d57e-110">Tri catégorisé</span><span class="sxs-lookup"><span data-stu-id="4d57e-110">Categorized sorting</span></span> 
    
<span data-ttu-id="4d57e-111">Avec le tri standard, toutes les lignes sont affichées dans une liste plate en utilisant une ou plusieurs colonnes comme clé de tri.</span><span class="sxs-lookup"><span data-stu-id="4d57e-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="4d57e-112">Avec le tri catégorisé, les lignes sont affichées hiérarchiquement avec une ou plusieurs colonnes comme clé de tri.</span><span class="sxs-lookup"><span data-stu-id="4d57e-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="4d57e-113">Dans chaque catégorie, il existe une ligne de titre spéciale qui contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4d57e-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="4d57e-114">Colonne ou colonnes qui font la clé de tri</span><span class="sxs-lookup"><span data-stu-id="4d57e-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="4d57e-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4d57e-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="4d57e-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4d57e-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="4d57e-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4d57e-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="4d57e-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4d57e-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="4d57e-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4d57e-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="4d57e-120">Le retrait sous la ligne de titre correspond à toutes les lignes du tableau qui contiennent des colonnes dont les valeurs correspondent à la clé de tri.</span><span class="sxs-lookup"><span data-stu-id="4d57e-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="4d57e-121">Ces lignes sont appelées lignes feuilles.</span><span class="sxs-lookup"><span data-stu-id="4d57e-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="4d57e-122">Les lignes de feuille contiennent toutes les colonnes du jeu de colonnes moins les colonnes de touche de tri.</span><span class="sxs-lookup"><span data-stu-id="4d57e-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="4d57e-123">Les tables des matières des dossiers peuvent souvent prendre en charge le tri catégorisé en plus du tri standard.</span><span class="sxs-lookup"><span data-stu-id="4d57e-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="4d57e-124">Les tables de contenu des conteneurs de carnet d’adresses ne prend généralement en charge que le tri standard.</span><span class="sxs-lookup"><span data-stu-id="4d57e-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="4d57e-125">Une catégorie peut avoir deux états : collapsed et expanded.</span><span class="sxs-lookup"><span data-stu-id="4d57e-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="4d57e-126">Lorsqu’une catégorie est dans l’état collapsed, seule la ligne de titre est renvoyée à partir [d’IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="4d57e-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="4d57e-127">Lorsqu’une catégorie est dans l’état développé, toutes les lignes associées à la catégorie sont renvoyées.</span><span class="sxs-lookup"><span data-stu-id="4d57e-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="4d57e-128">Cela inclut la ligne de titre et les lignes de feuille.</span><span class="sxs-lookup"><span data-stu-id="4d57e-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="4d57e-129">Chaque catégorie d’une vue de table peut être étendue ou réduire indépendamment.</span><span class="sxs-lookup"><span data-stu-id="4d57e-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="4d57e-130">Autrement dit, toutes les catégories ne doivent pas être dans le même état en même temps ; Certaines catégories peuvent être réduire tandis que d’autres sont étendues.</span><span class="sxs-lookup"><span data-stu-id="4d57e-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="4d57e-131">L’utilisateur d’un tableau catégorisé décide de son affichage.</span><span class="sxs-lookup"><span data-stu-id="4d57e-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="4d57e-132">Une option courante consiste à utiliser un contrôle fourni dans le SDK Windows appelé contrôle Treeview.</span><span class="sxs-lookup"><span data-stu-id="4d57e-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="4d57e-133">Les contrôles Treeview sont des zones de liste qui gèrent les informations dans une structure arborescence.</span><span class="sxs-lookup"><span data-stu-id="4d57e-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="4d57e-134">Les lignes de titre pour les catégories à l’état développé sont marquées avec un signe moins, tandis que les lignes de titre pour les catégories dans l’état collapsed sont marquées avec un signe plus.</span><span class="sxs-lookup"><span data-stu-id="4d57e-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="4d57e-135">Les catégories étendues sont affichées avec les lignes de feuille en retrait sous les lignes de titre.</span><span class="sxs-lookup"><span data-stu-id="4d57e-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="4d57e-136">Pour réduire et développer une catégorie, une application cliente ou un fournisseur de services utilise les méthodes [IMAPITable : IUnknown](imapitableiunknown.md) suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d57e-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="4d57e-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="4d57e-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="4d57e-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="4d57e-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="4d57e-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="4d57e-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="4d57e-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="4d57e-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="4d57e-141">Pour plus d’informations sur le tri des threads d’une conversation, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d57e-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="4d57e-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="4d57e-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="4d57e-143">Propriété canonique PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="4d57e-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="4d57e-144">Propriété canonique PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="4d57e-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="4d57e-145">Propriété canonique PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="4d57e-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="4d57e-146">Propriété canonique PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="4d57e-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="4d57e-147">Propriété canonique PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="4d57e-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="4d57e-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="4d57e-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="4d57e-149">Tri des tableaux après la définition de colonnes et de restrictions</span><span class="sxs-lookup"><span data-stu-id="4d57e-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="4d57e-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d57e-150">See also</span></span>



[<span data-ttu-id="4d57e-151">MAPI Tables</span><span class="sxs-lookup"><span data-stu-id="4d57e-151">MAPI Tables</span></span>](mapi-tables.md)

