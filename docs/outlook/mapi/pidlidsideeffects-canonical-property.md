---
title: Propriété canonique PidLidSideEffects
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: fa29a55a5fc2ce89e125909d13a2c14a347ef831
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594025"
---
# <a name="pidlidsideeffects-canonical-property"></a><span data-ttu-id="cd036-103">Propriété canonique PidLidSideEffects</span><span class="sxs-lookup"><span data-stu-id="cd036-103">PidLidSideEffects Canonical Property</span></span>

  
  
<span data-ttu-id="cd036-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd036-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd036-105">Détermine comment un objet message est géré par le client agissant sur l’entrée de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="cd036-105">Controls how a message object is handled by the client when acting on end-user input.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cd036-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="cd036-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd036-107">dispidSideEffects</span><span class="sxs-lookup"><span data-stu-id="cd036-107">dispidSideEffects</span></span>  <br/> |
|<span data-ttu-id="cd036-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="cd036-108">Property set:</span></span>  <br/> |<span data-ttu-id="cd036-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="cd036-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="cd036-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="cd036-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cd036-111">0x00008510</span><span class="sxs-lookup"><span data-stu-id="cd036-111">0x00008510</span></span>  <br/> |
|<span data-ttu-id="cd036-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="cd036-112">Data type:</span></span>  <br/> |<span data-ttu-id="cd036-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cd036-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cd036-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="cd036-114">Area:</span></span>  <br/> |<span data-ttu-id="cd036-115">Configuration d’exécution</span><span class="sxs-lookup"><span data-stu-id="cd036-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd036-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="cd036-116">Remarks</span></span>

<span data-ttu-id="cd036-117">Doit être définie à une opération de bits ou zéro ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="cd036-117">Must be set to a bitwise or zero or more of the following flags.</span></span>
  
|<span data-ttu-id="cd036-118">**Nom**</span><span class="sxs-lookup"><span data-stu-id="cd036-118">**Name**</span></span>|<span data-ttu-id="cd036-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="cd036-119">**Value**</span></span>|<span data-ttu-id="cd036-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="cd036-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cd036-121">seOpenToDelete</span><span class="sxs-lookup"><span data-stu-id="cd036-121">seOpenToDelete</span></span>  <br/> |<span data-ttu-id="cd036-122">0x0001</span><span class="sxs-lookup"><span data-stu-id="cd036-122">0x0001</span></span>  <br/> |<span data-ttu-id="cd036-123">Un traitement supplémentaire est requis sur l’objet de message lors de la suppression.</span><span class="sxs-lookup"><span data-stu-id="cd036-123">Additional processing is required on the message object when deleting.</span></span>  <br/> |
|<span data-ttu-id="cd036-124">seNoFrame</span><span class="sxs-lookup"><span data-stu-id="cd036-124">seNoFrame</span></span>  <br/> |<span data-ttu-id="cd036-125">0x0008</span><span class="sxs-lookup"><span data-stu-id="cd036-125">0x0008</span></span>  <br/> |<span data-ttu-id="cd036-126">Aucune interface utilisateur n’est associé à l’objet du message.</span><span class="sxs-lookup"><span data-stu-id="cd036-126">No UI is associated with the message object.</span></span>  <br/> |
|<span data-ttu-id="cd036-127">seCoerceToInbox</span><span class="sxs-lookup"><span data-stu-id="cd036-127">seCoerceToInbox</span></span>  <br/> |<span data-ttu-id="cd036-128">0x0010</span><span class="sxs-lookup"><span data-stu-id="cd036-128">0x0010</span></span>  <br/> |<span data-ttu-id="cd036-129">Un traitement supplémentaire est requis sur l’objet de message lorsque le déplacement ou la copie à un objet folder dont la propriété **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) « erreur. Remarque ».</span><span class="sxs-lookup"><span data-stu-id="cd036-129">Additional processing is required on the message object when moving or copying to a folder object with a **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of "IPF.Note".</span></span>  <br/> |
|<span data-ttu-id="cd036-130">seOpenTocopy</span><span class="sxs-lookup"><span data-stu-id="cd036-130">seOpenTocopy</span></span>  <br/> |<span data-ttu-id="cd036-131">0 x 0020</span><span class="sxs-lookup"><span data-stu-id="cd036-131">0x0020</span></span>  <br/> |<span data-ttu-id="cd036-132">Un traitement supplémentaire est requis sur l’objet de message lors de la copie dans un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="cd036-132">Additional processing is required on the message object when copying to another folder.</span></span>  <br/> |
|<span data-ttu-id="cd036-133">seOpenToMove</span><span class="sxs-lookup"><span data-stu-id="cd036-133">seOpenToMove</span></span>  <br/> |<span data-ttu-id="cd036-134">0x0040</span><span class="sxs-lookup"><span data-stu-id="cd036-134">0x0040</span></span>  <br/> |<span data-ttu-id="cd036-135">Un traitement supplémentaire est requis sur l’objet de message lors du déplacement vers un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="cd036-135">Additional processing is required on the message object when moving to another folder.</span></span>  <br/> |
|<span data-ttu-id="cd036-136">seOpenForCtxMenu</span><span class="sxs-lookup"><span data-stu-id="cd036-136">seOpenForCtxMenu</span></span>  <br/> |<span data-ttu-id="cd036-137">0 x 0100</span><span class="sxs-lookup"><span data-stu-id="cd036-137">0x0100</span></span>  <br/> |<span data-ttu-id="cd036-138">Un traitement supplémentaire est requis sur l’objet de message lors de l’affichage des verbes à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="cd036-138">Additional processing is required on the message object when displaying verbs to the end-user.</span></span>  <br/> |
|<span data-ttu-id="cd036-139">seCannotUndoDelete</span><span class="sxs-lookup"><span data-stu-id="cd036-139">seCannotUndoDelete</span></span>  <br/> |<span data-ttu-id="cd036-140">0 x 0400</span><span class="sxs-lookup"><span data-stu-id="cd036-140">0x0400</span></span>  <br/> |<span data-ttu-id="cd036-141">Ne peut pas annuler l’opération de suppression, ne doit pas être définie sauf si la valeur est « seOpenToDelete ».</span><span class="sxs-lookup"><span data-stu-id="cd036-141">Cannot undo delete operation, must not be set unless "seOpenToDelete" is set.</span></span>  <br/> |
|<span data-ttu-id="cd036-142">seCannotUndoCopy</span><span class="sxs-lookup"><span data-stu-id="cd036-142">seCannotUndoCopy</span></span>  <br/> |<span data-ttu-id="cd036-143">0 x 0800</span><span class="sxs-lookup"><span data-stu-id="cd036-143">0x0800</span></span>  <br/> |<span data-ttu-id="cd036-144">Ne peut pas annuler l’opération de copie, ne doit pas être définie sauf si la valeur est « seOpenTocopy ».</span><span class="sxs-lookup"><span data-stu-id="cd036-144">Cannot undo copy operation, must not be set unless "seOpenTocopy" is set.</span></span>  <br/> |
|<span data-ttu-id="cd036-145">seCannotUndoMove</span><span class="sxs-lookup"><span data-stu-id="cd036-145">seCannotUndoMove</span></span>  <br/> |<span data-ttu-id="cd036-146">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="cd036-146">0x1000</span></span>  <br/> |<span data-ttu-id="cd036-147">Ne peut pas annuler l’opération de déplacement, ne doit pas être définie sauf si la valeur est « seOpenToMove ».</span><span class="sxs-lookup"><span data-stu-id="cd036-147">Cannot undo move operation, must not be set unless "seOpenToMove" is set.</span></span>  <br/> |
|<span data-ttu-id="cd036-148">seHasScript</span><span class="sxs-lookup"><span data-stu-id="cd036-148">seHasScript</span></span>  <br/> |<span data-ttu-id="cd036-149">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="cd036-149">0x2000</span></span>  <br/> |<span data-ttu-id="cd036-150">L’objet du message contient un script de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="cd036-150">The message object contains end-user script.</span></span>  <br/> |
|<span data-ttu-id="cd036-151">seOpenToPermDelete</span><span class="sxs-lookup"><span data-stu-id="cd036-151">seOpenToPermDelete</span></span>  <br/> |<span data-ttu-id="cd036-152">0 x 4000</span><span class="sxs-lookup"><span data-stu-id="cd036-152">0x4000</span></span>  <br/> |<span data-ttu-id="cd036-153">Un traitement supplémentaire est nécessaire pour supprimer définitivement l’objet du message.</span><span class="sxs-lookup"><span data-stu-id="cd036-153">Additional processing is required to permanently delete the message object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="cd036-154">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="cd036-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cd036-155">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="cd036-155">Protocol specifications</span></span>

<span data-ttu-id="cd036-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd036-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd036-157">Fournit une définition de propriété et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="cd036-157">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cd036-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd036-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd036-159">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="cd036-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="cd036-160">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd036-160">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd036-161">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="cd036-161">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cd036-162">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="cd036-162">Header files</span></span>

<span data-ttu-id="cd036-163">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd036-163">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd036-164">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="cd036-164">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd036-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd036-165">See also</span></span>



[<span data-ttu-id="cd036-166">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="cd036-166">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd036-167">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="cd036-167">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd036-168">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="cd036-168">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd036-169">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="cd036-169">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

