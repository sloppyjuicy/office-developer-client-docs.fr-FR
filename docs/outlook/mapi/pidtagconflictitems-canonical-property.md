---
title: Propriété canonique PidTagConflictItems
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConflictItems
api_type:
- HeaderDef
ms.assetid: 0d147827-f0e2-dcc1-4427-c4a2f48ca801
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338016"
---
# <a name="pidtagconflictitems-canonical-property"></a><span data-ttu-id="1a66a-103">Propriété canonique PidTagConflictItems</span><span class="sxs-lookup"><span data-stu-id="1a66a-103">PidTagConflictItems Canonical Property</span></span>

  
  
<span data-ttu-id="1a66a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a66a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a66a-105">Contient un ou plusieurs identificateurs d'entrée d'éléments impliqués dans une résolution automatique des conflits.</span><span class="sxs-lookup"><span data-stu-id="1a66a-105">Contains one or more entry IDs of items that have been involved in an automatic conflict resolution.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="1a66a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1a66a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a66a-107">PR_CONFLICT_ITEMS</span><span class="sxs-lookup"><span data-stu-id="1a66a-107">PR_CONFLICT_ITEMS</span></span>  <br/> |
|<span data-ttu-id="1a66a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1a66a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a66a-109">0x1098</span><span class="sxs-lookup"><span data-stu-id="1a66a-109">0x1098</span></span>  <br/> |
|<span data-ttu-id="1a66a-110">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="1a66a-110">Property type:</span></span>  <br/> |<span data-ttu-id="1a66a-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="1a66a-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="1a66a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1a66a-112">Area:</span></span>  <br/> |<span data-ttu-id="1a66a-113">DÛMENT</span><span class="sxs-lookup"><span data-stu-id="1a66a-113">ICS</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a66a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a66a-114">Remarks</span></span>

<span data-ttu-id="1a66a-115">Les types d'éléments Microsoft Outlook standard qui prennent en charge la résolution automatique des conflits incluent les types d'éléments standard suivants: les éléments de rendez-vous, les éléments de contact, les éléments de journal, les éléments de courrier, les éléments de réunion, les éléments de notes de pense-bête et les tâches.</span><span class="sxs-lookup"><span data-stu-id="1a66a-115">The types of standard Microsoft Outlook items that support automatic conflict resolution include the following standard item types: appointment items, contact items, journal items, mail items, meeting items, sticky note items, and task items.</span></span> <span data-ttu-id="1a66a-116">Un élément appartenant à une classe de message qui dérive de l'un de ces types d'éléments standard prend également en charge la résolution automatique des conflits.</span><span class="sxs-lookup"><span data-stu-id="1a66a-116">An item belonging to a message class that derives from one of these standard item types also supports automatic conflict resolution.</span></span> <span data-ttu-id="1a66a-117">Dans Microsoft Outlook 2003 et Microsoft Office Outlook 2007, lorsque Outlook synchronise les éléments et estime qu'il est possible que la copie résultante ne contienne pas toutes les données essentielles, Outlook stocke les copies conflictuelles dans les **conflits** . dossier, sous le dossier **problèmes de synchronisation** .</span><span class="sxs-lookup"><span data-stu-id="1a66a-117">In Microsoft Outlook 2003 and Microsoft Office Outlook 2007, when Outlook synchronizes items and considers that there is a possibility that the resultant copy may not contain all essential data, Outlook stores the conflicting copies in the **Conflicts** folder, under the **Sync Issues** folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1a66a-118">Les **problèmes de synchronisation** et ses sous-dossiers sont masqués jusqu'à ce que vous cliquiez sur liste des **dossiers** dans le menu **atteindre** .</span><span class="sxs-lookup"><span data-stu-id="1a66a-118">**Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu.</span></span> 
  
<span data-ttu-id="1a66a-119">Un élément expose la propriété **PR_CONFLICT_ITEMS** s'il s'agit d'un des types d'éléments qui prennent en charge la résolution automatique des conflits, qu'il a remporté une résolution de conflit ou qu'il a été placé dans le dossier **conflits** en raison d'une résolution de conflit.</span><span class="sxs-lookup"><span data-stu-id="1a66a-119">An item exposes the **PR_CONFLICT_ITEMS** property if it is one of the item types that support automatic conflict resolution, has won in a conflict resolution, or was placed in the **Conflicts** folder because of a conflict resolution.</span></span> <span data-ttu-id="1a66a-120">Le dossier dans lequel l'élément est placé détermine le contenu de **PR_CONFLICT_ITEMS**.</span><span class="sxs-lookup"><span data-stu-id="1a66a-120">The folder in which the item is placed determines the content of **PR_CONFLICT_ITEMS**.</span></span> <span data-ttu-id="1a66a-121">Si l'élément se trouve dans un dossier autre que le dossier **conflits** et que l'élément expose la propriété **PR_CONFLICT_ITEMS** , l'élément doit avoir gagné la résolution de conflit et **PR_CONFLICT_ITEMS** contenir un ou plusieurs identificateurs d'entrée de les éléments perdus dans la résolution des conflits.</span><span class="sxs-lookup"><span data-stu-id="1a66a-121">If the item is located in some folder other than the **Conflicts** folder, and the item exposes the **PR_CONFLICT_ITEMS** property, the item must have won the conflict resolution, and **PR_CONFLICT_ITEMS** would contain one or more entry IDs of those items that lost in the conflict resolution.</span></span> <span data-ttu-id="1a66a-122">Si l'élément se trouve dans le dossier **conflits** et que l'élément expose la propriété **PR_CONFLICT_ITEMS** , cet élément doit avoir perdu la résolution de conflit, et **PR_CONFLICT_ITEMS** contient l'ID d'entrée de l'élément qui a été remporté dans le conflit. résolution.</span><span class="sxs-lookup"><span data-stu-id="1a66a-122">If the item is located in the **Conflicts** folder and the item exposes the **PR_CONFLICT_ITEMS** property, this item must have lost the conflict resolution, and **PR_CONFLICT_ITEMS** would contain the entry ID of the item that won in the conflict resolution.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1a66a-123">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="1a66a-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a66a-124">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="1a66a-124">Protocol specifications</span></span>

<span data-ttu-id="1a66a-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a66a-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a66a-126">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="1a66a-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1a66a-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a66a-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a66a-128">Gère la synchronisation des données d'objet de messagerie entre un serveur et un client.</span><span class="sxs-lookup"><span data-stu-id="1a66a-128">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a66a-129">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="1a66a-129">Header files</span></span>

<span data-ttu-id="1a66a-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1a66a-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a66a-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1a66a-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="1a66a-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="1a66a-132">Mapitags.h</span></span>
  
> <span data-ttu-id="1a66a-133">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="1a66a-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a66a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a66a-134">See also</span></span>



[<span data-ttu-id="1a66a-135">À propos des ajouts MAPI</span><span class="sxs-lookup"><span data-stu-id="1a66a-135">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="1a66a-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1a66a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a66a-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1a66a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a66a-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1a66a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a66a-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1a66a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

