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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386725"
---
# <a name="pidtagconflictitems-canonical-property"></a><span data-ttu-id="d6ec0-103">Propriété canonique PidTagConflictItems</span><span class="sxs-lookup"><span data-stu-id="d6ec0-103">PidTagConflictItems Canonical Property</span></span>

  
  
<span data-ttu-id="d6ec0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6ec0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6ec0-105">Contient un ou plusieurs identificateurs d’éléments qui ont été impliquées dans une résolution de conflit automatique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-105">Contains one or more entry IDs of items that have been involved in an automatic conflict resolution.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="d6ec0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d6ec0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6ec0-107">PR_CONFLICT_ITEMS</span><span class="sxs-lookup"><span data-stu-id="d6ec0-107">PR_CONFLICT_ITEMS</span></span>  <br/> |
|<span data-ttu-id="d6ec0-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d6ec0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6ec0-109">0x1098</span><span class="sxs-lookup"><span data-stu-id="d6ec0-109">0x1098</span></span>  <br/> |
|<span data-ttu-id="d6ec0-110">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="d6ec0-110">Property type:</span></span>  <br/> |<span data-ttu-id="d6ec0-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="d6ec0-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="d6ec0-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d6ec0-112">Area:</span></span>  <br/> |<span data-ttu-id="d6ec0-113">PARTAGE DE CONNEXION INTERNET</span><span class="sxs-lookup"><span data-stu-id="d6ec0-113">ICS</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6ec0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d6ec0-114">Remarks</span></span>

<span data-ttu-id="d6ec0-115">Les types d’éléments Microsoft Outlook standards qui prennent en charge la résolution automatique de conflit sont les types d’éléments standard suivantes : éléments de rendez-vous, contacts, éléments de journal, éléments de courrier, éléments de réunion, éléments pense-bête et éléments de tâche.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-115">The types of standard Microsoft Outlook items that support automatic conflict resolution include the following standard item types: appointment items, contact items, journal items, mail items, meeting items, sticky note items, and task items.</span></span> <span data-ttu-id="d6ec0-116">Un élément appartenant à une classe de message dérivée d’une de ces types d’éléments standard également prend en charge la résolution automatique de conflit.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-116">An item belonging to a message class that derives from one of these standard item types also supports automatic conflict resolution.</span></span> <span data-ttu-id="d6ec0-117">Dans Microsoft Outlook 2003 et Microsoft Office Outlook 2007, lorsque Outlook synchronise les éléments et considère qu’il est possible que la copie résultante ne peut pas contenir toutes les données essentielles, Outlook stocke les copies en conflit dans les **conflits** dossier sous le dossier **Problèmes de synchronisation** .</span><span class="sxs-lookup"><span data-stu-id="d6ec0-117">In Microsoft Outlook 2003 and Microsoft Office Outlook 2007, when Outlook synchronizes items and considers that there is a possibility that the resultant copy may not contain all essential data, Outlook stores the conflicting copies in the **Conflicts** folder, under the **Sync Issues** folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d6ec0-118">**Problèmes de synchronisation** et ses sous-dossiers sont masqués jusqu'à ce que vous cliquez sur **Liste des dossiers** dans le menu **Atteindre** .</span><span class="sxs-lookup"><span data-stu-id="d6ec0-118">**Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu.</span></span> 
  
<span data-ttu-id="d6ec0-119">Un élément expose la propriété **PR_CONFLICT_ITEMS** si elle est un des types d’éléments qui prennent en charge la résolution automatique de conflit, a été dans une résolution de conflit ou a été placé dans le dossier **conflits** en raison d’une résolution de conflit.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-119">An item exposes the **PR_CONFLICT_ITEMS** property if it is one of the item types that support automatic conflict resolution, has won in a conflict resolution, or was placed in the **Conflicts** folder because of a conflict resolution.</span></span> <span data-ttu-id="d6ec0-120">Le dossier dans lequel se trouve l’élément détermine le contenu de **PR_CONFLICT_ITEMS**.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-120">The folder in which the item is placed determines the content of **PR_CONFLICT_ITEMS**.</span></span> <span data-ttu-id="d6ec0-121">Si l’élément se trouve dans un dossier autre que le dossier **conflits** et l’élément expose la propriété **PR_CONFLICT_ITEMS** , l’élément doit avoir conclues la résolution de conflit et **PR_CONFLICT_ITEMS** contient un ou plusieurs identificateurs d’entrée de ces éléments perdus au cours de la résolution de conflit.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-121">If the item is located in some folder other than the **Conflicts** folder, and the item exposes the **PR_CONFLICT_ITEMS** property, the item must have won the conflict resolution, and **PR_CONFLICT_ITEMS** would contain one or more entry IDs of those items that lost in the conflict resolution.</span></span> <span data-ttu-id="d6ec0-122">Si l’élément se trouve dans le dossier **conflits** et l’élément expose la propriété **PR_CONFLICT_ITEMS** , cet élément doit avoir perdu la résolution de conflit et **PR_CONFLICT_ITEMS** contient l’identificateur d’entrée de l’élément conclues dans le conflit résolution.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-122">If the item is located in the **Conflicts** folder and the item exposes the **PR_CONFLICT_ITEMS** property, this item must have lost the conflict resolution, and **PR_CONFLICT_ITEMS** would contain the entry ID of the item that won in the conflict resolution.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d6ec0-123">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d6ec0-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6ec0-124">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="d6ec0-124">Protocol specifications</span></span>

<span data-ttu-id="d6ec0-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6ec0-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6ec0-126">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d6ec0-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6ec0-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6ec0-128">Gère la synchronisation des données de l’objet messagerie entre un serveur et un client.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-128">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6ec0-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d6ec0-129">Header files</span></span>

<span data-ttu-id="d6ec0-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6ec0-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6ec0-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="d6ec0-132">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="d6ec0-132">Mapitags.h</span></span>
  
> <span data-ttu-id="d6ec0-133">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="d6ec0-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6ec0-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6ec0-134">See also</span></span>



[<span data-ttu-id="d6ec0-135">À propos des ajouts MAPI</span><span class="sxs-lookup"><span data-stu-id="d6ec0-135">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="d6ec0-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d6ec0-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6ec0-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d6ec0-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6ec0-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d6ec0-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6ec0-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d6ec0-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

