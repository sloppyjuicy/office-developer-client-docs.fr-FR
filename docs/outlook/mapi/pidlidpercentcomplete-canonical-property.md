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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cf4edcc22deafe47fccb4fa44782b33aa18b8cec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587179"
---
# <a name="pidlidpercentcomplete-canonical-property"></a><span data-ttu-id="b7968-103">Propriété canonique PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="b7968-103">PidLidPercentComplete Canonical Property</span></span>

  
  
<span data-ttu-id="b7968-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7968-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7968-105">Indique la progression de l’utilisateur a effectué sur une tâche.</span><span class="sxs-lookup"><span data-stu-id="b7968-105">Indicates the progress the user has made on a task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7968-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b7968-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7968-107">dispidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="b7968-107">dispidPercentComplete</span></span>  <br/> |
|<span data-ttu-id="b7968-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="b7968-108">Property set:</span></span>  <br/> |<span data-ttu-id="b7968-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b7968-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b7968-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="b7968-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b7968-111">0x00008102</span><span class="sxs-lookup"><span data-stu-id="b7968-111">0x00008102</span></span>  <br/> |
|<span data-ttu-id="b7968-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b7968-112">Data type:</span></span>  <br/> |<span data-ttu-id="b7968-113">PT_R8</span><span class="sxs-lookup"><span data-stu-id="b7968-113">PT_R8</span></span>  <br/> |
|<span data-ttu-id="b7968-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b7968-114">Area:</span></span>  <br/> |<span data-ttu-id="b7968-115">Task</span><span class="sxs-lookup"><span data-stu-id="b7968-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7968-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="b7968-116">Remarks</span></span>

<span data-ttu-id="b7968-117">La valeur de cette propriété doit être un nombre supérieur ou égal à 0,0 et inférieure ou égale à 1.0, où 1.0 indique que le travail est terminé et 0.0 indique que le travail n’a pas commencé.</span><span class="sxs-lookup"><span data-stu-id="b7968-117">The value of this property must be a number greater than or equal to 0.0 and less than or equal to 1.0, where 1.0 indicates that work is completed and 0.0 indicates that work has not begun.</span></span>
  
<span data-ttu-id="b7968-118">Pour un objet de message avec indicateur de temps, la valeur de cette propriété doit être définie sur 1.0 si l’objet est marquée terminée et doit être définie à 0.0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b7968-118">For a time-flagged message object, the value of this property must be set to 1.0 if the object is flagged completed, and should be set to 0.0 otherwise.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b7968-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b7968-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7968-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="b7968-120">Protocol specifications</span></span>

<span data-ttu-id="b7968-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7968-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7968-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="b7968-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7968-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7968-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7968-124">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="b7968-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="b7968-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7968-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7968-126">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="b7968-126">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="b7968-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7968-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7968-128">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="b7968-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="b7968-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7968-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7968-130">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="b7968-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="b7968-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7968-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7968-132">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="b7968-132">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b7968-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b7968-133">Header files</span></span>

<span data-ttu-id="b7968-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7968-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7968-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b7968-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7968-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7968-136">See also</span></span>



[<span data-ttu-id="b7968-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b7968-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7968-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b7968-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7968-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b7968-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7968-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b7968-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

