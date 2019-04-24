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
ms.openlocfilehash: 2d57e6a195036ead9eb42666876e91a72f65eb8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331296"
---
# <a name="pidlidsideeffects-canonical-property"></a><span data-ttu-id="deda3-103">Propriété canonique PidLidSideEffects</span><span class="sxs-lookup"><span data-stu-id="deda3-103">PidLidSideEffects Canonical Property</span></span>

  
  
<span data-ttu-id="deda3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="deda3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="deda3-105">Contrôle la façon dont un objet message est géré par le client lorsqu'il agit sur l'entrée de l'utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="deda3-105">Controls how a message object is handled by the client when acting on end-user input.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="deda3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="deda3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="deda3-107">dispidSideEffects</span><span class="sxs-lookup"><span data-stu-id="deda3-107">dispidSideEffects</span></span>  <br/> |
|<span data-ttu-id="deda3-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="deda3-108">Property set:</span></span>  <br/> |<span data-ttu-id="deda3-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="deda3-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="deda3-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="deda3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="deda3-111">0x00008510</span><span class="sxs-lookup"><span data-stu-id="deda3-111">0x00008510</span></span>  <br/> |
|<span data-ttu-id="deda3-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="deda3-112">Data type:</span></span>  <br/> |<span data-ttu-id="deda3-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="deda3-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="deda3-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="deda3-114">Area:</span></span>  <br/> |<span data-ttu-id="deda3-115">Configuration de l'exécution</span><span class="sxs-lookup"><span data-stu-id="deda3-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="deda3-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="deda3-116">Remarks</span></span>

<span data-ttu-id="deda3-117">Doit être défini sur une valeur de bits or zéro ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="deda3-117">Must be set to a bitwise or zero or more of the following flags.</span></span>
  
|<span data-ttu-id="deda3-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="deda3-118">**Name**</span></span>|<span data-ttu-id="deda3-119">**Value**</span><span class="sxs-lookup"><span data-stu-id="deda3-119">**Value**</span></span>|<span data-ttu-id="deda3-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="deda3-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="deda3-121">seOpenToDelete</span><span class="sxs-lookup"><span data-stu-id="deda3-121">seOpenToDelete</span></span>  <br/> |<span data-ttu-id="deda3-122">0x0001</span><span class="sxs-lookup"><span data-stu-id="deda3-122">0x0001</span></span>  <br/> |<span data-ttu-id="deda3-123">Un traitement supplémentaire est requis sur l'objet message lors de la suppression.</span><span class="sxs-lookup"><span data-stu-id="deda3-123">Additional processing is required on the message object when deleting.</span></span>  <br/> |
|<span data-ttu-id="deda3-124">seNoFrame</span><span class="sxs-lookup"><span data-stu-id="deda3-124">seNoFrame</span></span>  <br/> |<span data-ttu-id="deda3-125">0x0008</span><span class="sxs-lookup"><span data-stu-id="deda3-125">0x0008</span></span>  <br/> |<span data-ttu-id="deda3-126">Aucune interface utilisateur n'est associée à l'objet message.</span><span class="sxs-lookup"><span data-stu-id="deda3-126">No UI is associated with the message object.</span></span>  <br/> |
|<span data-ttu-id="deda3-127">seCoerceToInbox</span><span class="sxs-lookup"><span data-stu-id="deda3-127">seCoerceToInbox</span></span>  <br/> |<span data-ttu-id="deda3-128">0x0010</span><span class="sxs-lookup"><span data-stu-id="deda3-128">0x0010</span></span>  <br/> |<span data-ttu-id="deda3-129">Un traitement supplémentaire est requis sur l'objet message lors du transfert ou de la copie d'un objet Folder avec une propriété **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) de «IPF. Note».</span><span class="sxs-lookup"><span data-stu-id="deda3-129">Additional processing is required on the message object when moving or copying to a folder object with a **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of "IPF.Note".</span></span>  <br/> |
|<span data-ttu-id="deda3-130">seOpenTocopy</span><span class="sxs-lookup"><span data-stu-id="deda3-130">seOpenTocopy</span></span>  <br/> |<span data-ttu-id="deda3-131">0x0020</span><span class="sxs-lookup"><span data-stu-id="deda3-131">0x0020</span></span>  <br/> |<span data-ttu-id="deda3-132">Un traitement supplémentaire est requis sur l'objet message lors de la copie dans un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="deda3-132">Additional processing is required on the message object when copying to another folder.</span></span>  <br/> |
|<span data-ttu-id="deda3-133">seOpenToMove</span><span class="sxs-lookup"><span data-stu-id="deda3-133">seOpenToMove</span></span>  <br/> |<span data-ttu-id="deda3-134">0x0040</span><span class="sxs-lookup"><span data-stu-id="deda3-134">0x0040</span></span>  <br/> |<span data-ttu-id="deda3-135">Un traitement supplémentaire est requis sur l'objet message lors du passage à un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="deda3-135">Additional processing is required on the message object when moving to another folder.</span></span>  <br/> |
|<span data-ttu-id="deda3-136">seOpenForCtxMenu</span><span class="sxs-lookup"><span data-stu-id="deda3-136">seOpenForCtxMenu</span></span>  <br/> |<span data-ttu-id="deda3-137">0x0100</span><span class="sxs-lookup"><span data-stu-id="deda3-137">0x0100</span></span>  <br/> |<span data-ttu-id="deda3-138">Un traitement supplémentaire est requis sur l'objet message lors de l'affichage des verbes à l'utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="deda3-138">Additional processing is required on the message object when displaying verbs to the end-user.</span></span>  <br/> |
|<span data-ttu-id="deda3-139">seCannotUndoDelete</span><span class="sxs-lookup"><span data-stu-id="deda3-139">seCannotUndoDelete</span></span>  <br/> |<span data-ttu-id="deda3-140">0x0400</span><span class="sxs-lookup"><span data-stu-id="deda3-140">0x0400</span></span>  <br/> |<span data-ttu-id="deda3-141">Impossible d'annuler l'opération de suppression, elle ne doit pas être définie sauf si «seOpenToDelete» est défini.</span><span class="sxs-lookup"><span data-stu-id="deda3-141">Cannot undo delete operation, must not be set unless "seOpenToDelete" is set.</span></span>  <br/> |
|<span data-ttu-id="deda3-142">seCannotUndoCopy</span><span class="sxs-lookup"><span data-stu-id="deda3-142">seCannotUndoCopy</span></span>  <br/> |<span data-ttu-id="deda3-143">0x0800</span><span class="sxs-lookup"><span data-stu-id="deda3-143">0x0800</span></span>  <br/> |<span data-ttu-id="deda3-144">Impossible d'annuler l'opération de copie, ne doit pas être défini sauf si «seOpenTocopy» est défini.</span><span class="sxs-lookup"><span data-stu-id="deda3-144">Cannot undo copy operation, must not be set unless "seOpenTocopy" is set.</span></span>  <br/> |
|<span data-ttu-id="deda3-145">seCannotUndoMove</span><span class="sxs-lookup"><span data-stu-id="deda3-145">seCannotUndoMove</span></span>  <br/> |<span data-ttu-id="deda3-146">0x1000</span><span class="sxs-lookup"><span data-stu-id="deda3-146">0x1000</span></span>  <br/> |<span data-ttu-id="deda3-147">Impossible d'annuler l'opération de déplacement, ne doit pas être défini sauf si «seOpenToMove» est défini.</span><span class="sxs-lookup"><span data-stu-id="deda3-147">Cannot undo move operation, must not be set unless "seOpenToMove" is set.</span></span>  <br/> |
|<span data-ttu-id="deda3-148">seHasScript</span><span class="sxs-lookup"><span data-stu-id="deda3-148">seHasScript</span></span>  <br/> |<span data-ttu-id="deda3-149">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="deda3-149">0x2000</span></span>  <br/> |<span data-ttu-id="deda3-150">L'objet message contient le script de l'utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="deda3-150">The message object contains end-user script.</span></span>  <br/> |
|<span data-ttu-id="deda3-151">seOpenToPermDelete</span><span class="sxs-lookup"><span data-stu-id="deda3-151">seOpenToPermDelete</span></span>  <br/> |<span data-ttu-id="deda3-152">0x4000</span><span class="sxs-lookup"><span data-stu-id="deda3-152">0x4000</span></span>  <br/> |<span data-ttu-id="deda3-153">Un traitement supplémentaire est nécessaire pour supprimer définitivement l'objet message.</span><span class="sxs-lookup"><span data-stu-id="deda3-153">Additional processing is required to permanently delete the message object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="deda3-154">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="deda3-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="deda3-155">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="deda3-155">Protocol specifications</span></span>

<span data-ttu-id="deda3-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="deda3-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="deda3-157">Fournit la définition des jeux de propriétés et les références aux spécifications du protocole Exchange Server associé.</span><span class="sxs-lookup"><span data-stu-id="deda3-157">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="deda3-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="deda3-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="deda3-159">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="deda3-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="deda3-160">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="deda3-160">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="deda3-161">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="deda3-161">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="deda3-162">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="deda3-162">Header files</span></span>

<span data-ttu-id="deda3-163">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="deda3-163">Mapidefs.h</span></span>
  
> <span data-ttu-id="deda3-164">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="deda3-164">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="deda3-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="deda3-165">See also</span></span>



[<span data-ttu-id="deda3-166">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="deda3-166">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="deda3-167">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="deda3-167">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="deda3-168">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="deda3-168">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="deda3-169">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="deda3-169">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

