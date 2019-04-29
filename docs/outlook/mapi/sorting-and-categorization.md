---
title: Tri et catégorisation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Dernière modification: 08 08, 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418483"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="d7de4-103">Tri et catégorisation</span><span class="sxs-lookup"><span data-stu-id="d7de4-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="d7de4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7de4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7de4-105">Trier un tableau place les lignes dans un ordre approprié pour la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="d7de4-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="d7de4-106">Par exemple, une visionneuse peut préférer consulter la table des matières d'un dossier triée par objet de message de sorte que tous les threads d'une conversation soient réunis tandis qu'une autre peut souhaiter que les messages soient triés en fonction du nom de l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="d7de4-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="d7de4-107">Une table nouvellement instanciée n'est pas nécessairement triée dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="d7de4-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="d7de4-108">Il existe deux types de tri:</span><span class="sxs-lookup"><span data-stu-id="d7de4-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="d7de4-109">Tri standard</span><span class="sxs-lookup"><span data-stu-id="d7de4-109">Standard sorting</span></span>
    
- <span data-ttu-id="d7de4-110">Tri par catégorie</span><span class="sxs-lookup"><span data-stu-id="d7de4-110">Categorized sorting</span></span> 
    
<span data-ttu-id="d7de4-111">Avec le tri standard, toutes les lignes s'affichent dans une liste plate à l'aide d'une ou de plusieurs colonnes en tant que clé de tri.</span><span class="sxs-lookup"><span data-stu-id="d7de4-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="d7de4-112">Avec le tri par catégorie, les lignes sont affichées hiérarchiquement avec une ou plusieurs colonnes en tant que clé de tri.</span><span class="sxs-lookup"><span data-stu-id="d7de4-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="d7de4-113">Dans chaque catégorie, il existe une ligne d'en-tête spéciale qui contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7de4-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="d7de4-114">La ou les colonnes qui composent la clé de tri</span><span class="sxs-lookup"><span data-stu-id="d7de4-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="d7de4-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d7de4-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="d7de4-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d7de4-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="d7de4-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d7de4-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="d7de4-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d7de4-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="d7de4-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d7de4-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="d7de4-120">Le retrait sous la ligne d'en-tête contient toutes les lignes de la table qui contiennent des colonnes avec des valeurs qui correspondent à la clé de tri.</span><span class="sxs-lookup"><span data-stu-id="d7de4-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="d7de4-121">Ces lignes sont appelées lignes feuille.</span><span class="sxs-lookup"><span data-stu-id="d7de4-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="d7de4-122">Les lignes de feuille contiennent toutes les colonnes de l'ensemble de colonnes moins les colonnes de clés de tri.</span><span class="sxs-lookup"><span data-stu-id="d7de4-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="d7de4-123">Les tables de contenu des dossiers prennent généralement en charge le tri par catégorie en plus du tri standard.</span><span class="sxs-lookup"><span data-stu-id="d7de4-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="d7de4-124">Les tables de contenu des conteneurs du carnet d'adresses prennent généralement en charge uniquement le tri standard.</span><span class="sxs-lookup"><span data-stu-id="d7de4-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="d7de4-125">Une catégorie peut avoir deux États: réduite et développée.</span><span class="sxs-lookup"><span data-stu-id="d7de4-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="d7de4-126">Lorsqu'une catégorie est réduite, seule la ligne d'en-tête est renvoyée à partir de l'état [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="d7de4-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="d7de4-127">Lorsqu'une catégorie est dans l'état développé, toutes les lignes associées à la catégorie sont renvoyées.</span><span class="sxs-lookup"><span data-stu-id="d7de4-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="d7de4-128">Cela inclut la ligne d'en-tête et les lignes de feuille.</span><span class="sxs-lookup"><span data-stu-id="d7de4-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="d7de4-129">Chaque catégorie dans un affichage tableau peut être développée ou réduite indépendamment.</span><span class="sxs-lookup"><span data-stu-id="d7de4-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="d7de4-130">Autrement dit, toutes les catégories ne doivent pas être dans le même État en même temps; certaines catégories peuvent être réduites, tandis que d'autres sont développées.</span><span class="sxs-lookup"><span data-stu-id="d7de4-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="d7de4-131">L'utilisateur d'un tableau classé détermine son mode d'affichage.</span><span class="sxs-lookup"><span data-stu-id="d7de4-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="d7de4-132">Une option commune consiste à utiliser un contrôle fourni dans le kit de développement logiciel (SDK) Windows appelé contrôle TreeView.</span><span class="sxs-lookup"><span data-stu-id="d7de4-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="d7de4-133">Les contrôles TreeView sont des zones de liste qui prennent en charge les informations dans une structure arborescente.</span><span class="sxs-lookup"><span data-stu-id="d7de4-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="d7de4-134">Les lignes d'en-tête pour les catégories dans l'état développé sont signalées par un signe moins tandis que les lignes de titre pour les catégories dans l'État réduit sont signalées par un signe plus.</span><span class="sxs-lookup"><span data-stu-id="d7de4-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="d7de4-135">Les catégories développées sont affichées avec les lignes de feuille mises en retrait sous les lignes d'en-tête.</span><span class="sxs-lookup"><span data-stu-id="d7de4-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="d7de4-136">Pour réduire et développer une catégorie, une application cliente ou un fournisseur de services utilise la méthode [IMAPITable suivante: méthodes IUnknown](imapitableiunknown.md) :</span><span class="sxs-lookup"><span data-stu-id="d7de4-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="d7de4-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="d7de4-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="d7de4-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="d7de4-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="d7de4-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="d7de4-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="d7de4-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="d7de4-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="d7de4-141">Pour plus d'informations sur le tri des threads d'une conversation, consultez les rubriques suivantes:</span><span class="sxs-lookup"><span data-stu-id="d7de4-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="d7de4-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="d7de4-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="d7de4-143">Propriété canonique PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="d7de4-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="d7de4-144">Propriété canonique PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="d7de4-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="d7de4-145">Propriété canonique PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="d7de4-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="d7de4-146">Propriété canonique PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="d7de4-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="d7de4-147">Propriété canonique PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="d7de4-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="d7de4-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="d7de4-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="d7de4-149">Tri des tables après la définition des colonnes et des restrictions</span><span class="sxs-lookup"><span data-stu-id="d7de4-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="d7de4-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7de4-150">See also</span></span>



[<span data-ttu-id="d7de4-151">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="d7de4-151">MAPI Tables</span></span>](mapi-tables.md)

