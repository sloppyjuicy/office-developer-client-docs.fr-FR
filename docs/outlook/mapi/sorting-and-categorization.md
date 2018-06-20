---
title: Tri et classement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Dernière modification : 08 novembre 2011'
ms.openlocfilehash: 5e63d276d25a26f937e9b4f44575fea1030f52d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787209"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="d445b-103">Tri et classement</span><span class="sxs-lookup"><span data-stu-id="d445b-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="d445b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d445b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d445b-105">Tri d’un tableau place les lignes dans un ordre significatif pour la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="d445b-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="d445b-106">Par exemple, une visionneuse pourrait être préférable de voir la table des matières d’un dossier trié par objet du message, afin que tous les threads d’une conversation ensemble pendant une autre visionneuse souhaiterez les messages triés par le nom de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="d445b-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="d445b-107">Une table nouvellement instanciée n’est pas nécessairement triée selon un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="d445b-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="d445b-108">Il existe deux types de tri :</span><span class="sxs-lookup"><span data-stu-id="d445b-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="d445b-109">Tri standard</span><span class="sxs-lookup"><span data-stu-id="d445b-109">Standard sorting</span></span>
    
- <span data-ttu-id="d445b-110">Classés tri</span><span class="sxs-lookup"><span data-stu-id="d445b-110">Categorized sorting</span></span> 
    
<span data-ttu-id="d445b-111">Tri standard, toutes les lignes sont affichées dans une liste simple à l’aide d’une ou plusieurs colonnes comme clé de tri.</span><span class="sxs-lookup"><span data-stu-id="d445b-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="d445b-112">Tri par catégorie, les lignes sont affichés hiérarchiquement avec une ou plusieurs colonnes comme clé de tri.</span><span class="sxs-lookup"><span data-stu-id="d445b-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="d445b-113">Dans chaque catégorie, il est une ligne d’en-tête spécial qui contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="d445b-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="d445b-114">L’ou les colonnes qui constituent la clé de tri</span><span class="sxs-lookup"><span data-stu-id="d445b-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="d445b-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d445b-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="d445b-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d445b-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="d445b-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d445b-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="d445b-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d445b-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="d445b-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d445b-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="d445b-120">Mis en retrait sous la ligne d’en-tête sont toutes les lignes de la table contenant des colonnes avec des valeurs qui correspondent à la clé de tri.</span><span class="sxs-lookup"><span data-stu-id="d445b-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="d445b-121">Ces lignes sont appelées les lignes de feuille.</span><span class="sxs-lookup"><span data-stu-id="d445b-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="d445b-122">Lignes de feuille contient toutes les colonnes dans la colonne valeur moins les colonnes de clés de tri.</span><span class="sxs-lookup"><span data-stu-id="d445b-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="d445b-123">Les tables de contenu des dossiers prennent généralement en charge le tri par catégorie en plus de tri standard.</span><span class="sxs-lookup"><span data-stu-id="d445b-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="d445b-124">Les tables de contenu des conteneurs de carnet d’adresses prennent généralement en charge uniquement le tri standard.</span><span class="sxs-lookup"><span data-stu-id="d445b-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="d445b-125">Une catégorie peut avoir deux états : réduits et développés.</span><span class="sxs-lookup"><span data-stu-id="d445b-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="d445b-126">Lorsqu’une catégorie est dans l’état réduit, la ligne d’en-tête est renvoyée à partir de [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="d445b-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="d445b-127">Lorsqu’une catégorie est dans l’état développé, toutes les lignes associées à la catégorie sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="d445b-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="d445b-128">Cela inclut la ligne d’en-tête et les lignes de feuille.</span><span class="sxs-lookup"><span data-stu-id="d445b-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="d445b-129">Chaque catégorie dans un affichage tableau peut être développé ou réduit de manière indépendante.</span><span class="sxs-lookup"><span data-stu-id="d445b-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="d445b-130">Autrement dit, pas toutes les catégories doivent être dans le même état en même temps ; des catégories peuvent être réduits tandis que d’autres personnes sont développés.</span><span class="sxs-lookup"><span data-stu-id="d445b-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="d445b-131">L’utilisateur d’une table, voir décide comment il est affiché.</span><span class="sxs-lookup"><span data-stu-id="d445b-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="d445b-132">Une option commune consiste à utiliser un contrôle fourni dans le SDK de Windows appelée le contrôle treeview.</span><span class="sxs-lookup"><span data-stu-id="d445b-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="d445b-133">Contrôles TreeView sont les zones de liste qui prennent en charge les informations dans une structure d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="d445b-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="d445b-134">Lignes d’en-tête pour les catégories dans l’état développé sont marqués avec un signe moins, tandis que les lignes d’en-tête pour les catégories dans l’état réduit sont marquées avec un signe plus.</span><span class="sxs-lookup"><span data-stu-id="d445b-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="d445b-135">Catégories de l’étendue sont affichés avec les lignes de feuille en retrait sous les lignes d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="d445b-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="d445b-136">Pour réduire et développer une catégorie, une application cliente ou un fournisseur de services utilise les éléments suivants [IMAPITable : IUnknown](imapitableiunknown.md) méthodes :</span><span class="sxs-lookup"><span data-stu-id="d445b-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="d445b-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="d445b-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="d445b-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="d445b-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="d445b-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="d445b-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="d445b-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="d445b-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="d445b-141">Pour plus d’informations sur le tri, les threads d’une conversation voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d445b-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="d445b-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="d445b-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="d445b-143">Propriété canonique PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="d445b-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="d445b-144">Propriété canonique PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="d445b-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="d445b-145">Propriété canonique PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="d445b-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="d445b-146">Propriété canonique PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="d445b-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="d445b-147">Propriété canonique PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="d445b-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="d445b-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="d445b-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="d445b-149">Tri des tableaux après avoir défini les Restrictions et les colonnes</span><span class="sxs-lookup"><span data-stu-id="d445b-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="d445b-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d445b-150">See also</span></span>



[<span data-ttu-id="d445b-151">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="d445b-151">MAPI Tables</span></span>](mapi-tables.md)

