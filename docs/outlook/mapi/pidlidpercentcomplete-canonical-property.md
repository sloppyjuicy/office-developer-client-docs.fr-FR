---
title: Propriété canonique PidLidPercentComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidPercentComplete
api_type:
- COM
ms.assetid: e63792b1-9580-4702-a6d7-dd3ae5007a4a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f4675362de1e9efe4ef16285723cddeface9c403
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785337"
---
# <a name="pidlidpercentcomplete-canonical-property"></a><span data-ttu-id="040de-103">Propriété canonique PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="040de-103">PidLidPercentComplete Canonical Property</span></span>

  
  
<span data-ttu-id="040de-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="040de-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="040de-105">Indique la progression de l’utilisateur a effectué sur une tâche.</span><span class="sxs-lookup"><span data-stu-id="040de-105">Indicates the progress the user has made on a task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="040de-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="040de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="040de-107">dispidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="040de-107">dispidPercentComplete</span></span>  <br/> |
|<span data-ttu-id="040de-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="040de-108">Property set:</span></span>  <br/> |<span data-ttu-id="040de-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="040de-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="040de-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="040de-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="040de-111">0x00008102</span><span class="sxs-lookup"><span data-stu-id="040de-111">0x00008102</span></span>  <br/> |
|<span data-ttu-id="040de-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="040de-112">Data type:</span></span>  <br/> |<span data-ttu-id="040de-113">PT_R8</span><span class="sxs-lookup"><span data-stu-id="040de-113">PT_R8</span></span>  <br/> |
|<span data-ttu-id="040de-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="040de-114">Area:</span></span>  <br/> |<span data-ttu-id="040de-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="040de-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="040de-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="040de-116">Remarks</span></span>

<span data-ttu-id="040de-117">La valeur de cette propriété doit être un nombre supérieur ou égal à 0,0 et inférieure ou égale à 1.0, où 1.0 indique que le travail est terminé et 0.0 indique que le travail n’a pas commencé.</span><span class="sxs-lookup"><span data-stu-id="040de-117">The value of this property must be a number greater than or equal to 0.0 and less than or equal to 1.0, where 1.0 indicates that work is completed and 0.0 indicates that work has not begun.</span></span>
  
<span data-ttu-id="040de-118">Pour un objet de message avec indicateur de temps, la valeur de cette propriété doit être définie sur 1.0 si l’objet est marquée terminée et doit être définie à 0.0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="040de-118">For a time-flagged message object, the value of this property must be set to 1.0 if the object is flagged completed, and should be set to 0.0 otherwise.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="040de-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="040de-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="040de-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="040de-120">Protocol specifications</span></span>

<span data-ttu-id="040de-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="040de-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="040de-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="040de-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="040de-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="040de-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="040de-124">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="040de-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="040de-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="040de-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="040de-126">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="040de-126">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="040de-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="040de-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="040de-128">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="040de-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="040de-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="040de-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="040de-130">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="040de-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="040de-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="040de-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="040de-132">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="040de-132">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="040de-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="040de-133">Header files</span></span>

<span data-ttu-id="040de-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="040de-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="040de-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="040de-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="040de-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="040de-136">See also</span></span>



[<span data-ttu-id="040de-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="040de-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="040de-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="040de-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="040de-139">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="040de-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="040de-140">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="040de-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

