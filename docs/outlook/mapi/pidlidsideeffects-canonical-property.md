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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 479ba1990f7cac1768fc5e514e3fc55f017e4a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785407"
---
# <a name="pidlidsideeffects-canonical-property"></a><span data-ttu-id="d0c50-103">Propriété canonique PidLidSideEffects</span><span class="sxs-lookup"><span data-stu-id="d0c50-103">PidLidSideEffects Canonical Property</span></span>

  
  
<span data-ttu-id="d0c50-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0c50-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0c50-105">Détermine comment un objet message est géré par le client agissant sur l’entrée de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="d0c50-105">Controls how a message object is handled by the client when acting on end-user input.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d0c50-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d0c50-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0c50-107">dispidSideEffects</span><span class="sxs-lookup"><span data-stu-id="d0c50-107">dispidSideEffects</span></span>  <br/> |
|<span data-ttu-id="d0c50-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="d0c50-108">Property set:</span></span>  <br/> |<span data-ttu-id="d0c50-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d0c50-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d0c50-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="d0c50-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d0c50-111">0x00008510</span><span class="sxs-lookup"><span data-stu-id="d0c50-111">0x00008510</span></span>  <br/> |
|<span data-ttu-id="d0c50-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d0c50-112">Data type:</span></span>  <br/> |<span data-ttu-id="d0c50-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d0c50-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d0c50-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="d0c50-114">Area:</span></span>  <br/> |<span data-ttu-id="d0c50-115">Configuration d’exécution</span><span class="sxs-lookup"><span data-stu-id="d0c50-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0c50-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="d0c50-116">Remarks</span></span>

<span data-ttu-id="d0c50-117">Doit être définie à une opération de bits ou zéro ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="d0c50-117">Must be set to a bitwise or zero or more of the following flags.</span></span>
  
|<span data-ttu-id="d0c50-118">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d0c50-118">**Name**</span></span>|<span data-ttu-id="d0c50-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="d0c50-119">**Value**</span></span>|<span data-ttu-id="d0c50-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="d0c50-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d0c50-121">seOpenToDelete</span><span class="sxs-lookup"><span data-stu-id="d0c50-121">seOpenToDelete</span></span>  <br/> |<span data-ttu-id="d0c50-122">0x0001</span><span class="sxs-lookup"><span data-stu-id="d0c50-122">0x0001</span></span>  <br/> |<span data-ttu-id="d0c50-123">Un traitement supplémentaire est requis sur l’objet de message lors de la suppression.</span><span class="sxs-lookup"><span data-stu-id="d0c50-123">Additional processing is required on the message object when deleting.</span></span>  <br/> |
|<span data-ttu-id="d0c50-124">seNoFrame</span><span class="sxs-lookup"><span data-stu-id="d0c50-124">seNoFrame</span></span>  <br/> |<span data-ttu-id="d0c50-125">0x0008</span><span class="sxs-lookup"><span data-stu-id="d0c50-125">0x0008</span></span>  <br/> |<span data-ttu-id="d0c50-126">Aucune interface utilisateur n’est associé à l’objet du message.</span><span class="sxs-lookup"><span data-stu-id="d0c50-126">No UI is associated with the message object.</span></span>  <br/> |
|<span data-ttu-id="d0c50-127">seCoerceToInbox</span><span class="sxs-lookup"><span data-stu-id="d0c50-127">seCoerceToInbox</span></span>  <br/> |<span data-ttu-id="d0c50-128">0x0010</span><span class="sxs-lookup"><span data-stu-id="d0c50-128">0x0010</span></span>  <br/> |<span data-ttu-id="d0c50-129">Un traitement supplémentaire est requis sur l’objet de message lorsque le déplacement ou la copie à un objet folder dont la propriété **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) « erreur. Remarque ».</span><span class="sxs-lookup"><span data-stu-id="d0c50-129">Additional processing is required on the message object when moving or copying to a folder object with a **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of "IPF.Note".</span></span>  <br/> |
|<span data-ttu-id="d0c50-130">seOpenTocopy</span><span class="sxs-lookup"><span data-stu-id="d0c50-130">seOpenTocopy</span></span>  <br/> |<span data-ttu-id="d0c50-131">0 x 0020</span><span class="sxs-lookup"><span data-stu-id="d0c50-131">0x0020</span></span>  <br/> |<span data-ttu-id="d0c50-132">Un traitement supplémentaire est requis sur l’objet de message lors de la copie dans un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="d0c50-132">Additional processing is required on the message object when copying to another folder.</span></span>  <br/> |
|<span data-ttu-id="d0c50-133">seOpenToMove</span><span class="sxs-lookup"><span data-stu-id="d0c50-133">seOpenToMove</span></span>  <br/> |<span data-ttu-id="d0c50-134">0x0040</span><span class="sxs-lookup"><span data-stu-id="d0c50-134">0x0040</span></span>  <br/> |<span data-ttu-id="d0c50-135">Un traitement supplémentaire est requis sur l’objet de message lors du déplacement vers un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="d0c50-135">Additional processing is required on the message object when moving to another folder.</span></span>  <br/> |
|<span data-ttu-id="d0c50-136">seOpenForCtxMenu</span><span class="sxs-lookup"><span data-stu-id="d0c50-136">seOpenForCtxMenu</span></span>  <br/> |<span data-ttu-id="d0c50-137">0 x 0100</span><span class="sxs-lookup"><span data-stu-id="d0c50-137">0x0100</span></span>  <br/> |<span data-ttu-id="d0c50-138">Un traitement supplémentaire est requis sur l’objet de message lors de l’affichage des verbes à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="d0c50-138">Additional processing is required on the message object when displaying verbs to the end-user.</span></span>  <br/> |
|<span data-ttu-id="d0c50-139">seCannotUndoDelete</span><span class="sxs-lookup"><span data-stu-id="d0c50-139">seCannotUndoDelete</span></span>  <br/> |<span data-ttu-id="d0c50-140">0 x 0400</span><span class="sxs-lookup"><span data-stu-id="d0c50-140">0x0400</span></span>  <br/> |<span data-ttu-id="d0c50-141">Ne peut pas annuler l’opération de suppression, ne doit pas être définie sauf si la valeur est « seOpenToDelete ».</span><span class="sxs-lookup"><span data-stu-id="d0c50-141">Cannot undo delete operation, must not be set unless "seOpenToDelete" is set.</span></span>  <br/> |
|<span data-ttu-id="d0c50-142">seCannotUndoCopy</span><span class="sxs-lookup"><span data-stu-id="d0c50-142">seCannotUndoCopy</span></span>  <br/> |<span data-ttu-id="d0c50-143">0 x 0800</span><span class="sxs-lookup"><span data-stu-id="d0c50-143">0x0800</span></span>  <br/> |<span data-ttu-id="d0c50-144">Ne peut pas annuler l’opération de copie, ne doit pas être définie sauf si la valeur est « seOpenTocopy ».</span><span class="sxs-lookup"><span data-stu-id="d0c50-144">Cannot undo copy operation, must not be set unless "seOpenTocopy" is set.</span></span>  <br/> |
|<span data-ttu-id="d0c50-145">seCannotUndoMove</span><span class="sxs-lookup"><span data-stu-id="d0c50-145">seCannotUndoMove</span></span>  <br/> |<span data-ttu-id="d0c50-146">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="d0c50-146">0x1000</span></span>  <br/> |<span data-ttu-id="d0c50-147">Ne peut pas annuler l’opération de déplacement, ne doit pas être définie sauf si la valeur est « seOpenToMove ».</span><span class="sxs-lookup"><span data-stu-id="d0c50-147">Cannot undo move operation, must not be set unless "seOpenToMove" is set.</span></span>  <br/> |
|<span data-ttu-id="d0c50-148">seHasScript</span><span class="sxs-lookup"><span data-stu-id="d0c50-148">seHasScript</span></span>  <br/> |<span data-ttu-id="d0c50-149">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="d0c50-149">0x2000</span></span>  <br/> |<span data-ttu-id="d0c50-150">L’objet du message contient un script de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="d0c50-150">The message object contains end-user script.</span></span>  <br/> |
|<span data-ttu-id="d0c50-151">seOpenToPermDelete</span><span class="sxs-lookup"><span data-stu-id="d0c50-151">seOpenToPermDelete</span></span>  <br/> |<span data-ttu-id="d0c50-152">0 x 4000</span><span class="sxs-lookup"><span data-stu-id="d0c50-152">0x4000</span></span>  <br/> |<span data-ttu-id="d0c50-153">Un traitement supplémentaire est nécessaire pour supprimer définitivement l’objet du message.</span><span class="sxs-lookup"><span data-stu-id="d0c50-153">Additional processing is required to permanently delete the message object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d0c50-154">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d0c50-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d0c50-155">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="d0c50-155">Protocol specifications</span></span>

<span data-ttu-id="d0c50-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0c50-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0c50-157">Fournit une définition de propriété et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="d0c50-157">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d0c50-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0c50-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0c50-159">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="d0c50-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="d0c50-160">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0c50-160">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0c50-161">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="d0c50-161">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d0c50-162">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d0c50-162">Header files</span></span>

<span data-ttu-id="d0c50-163">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0c50-163">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0c50-164">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d0c50-164">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0c50-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0c50-165">See also</span></span>



[<span data-ttu-id="d0c50-166">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d0c50-166">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0c50-167">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d0c50-167">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0c50-168">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d0c50-168">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0c50-169">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="d0c50-169">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

