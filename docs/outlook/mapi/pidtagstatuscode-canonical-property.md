---
title: Propriété canonique PidTagStatusCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusCode
api_type:
- COM
ms.assetid: e29190c5-52c3-4ef7-98db-699487c54325
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 751be8abe02dfb1d5bab2bcbbbc0cbd2a8243f85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418513"
---
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="06149-103">Propriété canonique PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="06149-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="06149-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06149-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06149-105">Contient un masque de réindicateur des indicateurs qui indiquent l'état actuel d'une ressource de session.</span><span class="sxs-lookup"><span data-stu-id="06149-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="06149-106">Tous les fournisseurs de services définissent les codes d'État comme le fait MAPI pour indiquer l'état du sous-système, le spouleur MAPI et le carnet d'adresses intégré.</span><span class="sxs-lookup"><span data-stu-id="06149-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06149-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="06149-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="06149-108">PR_STATUS_CODE</span><span class="sxs-lookup"><span data-stu-id="06149-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="06149-109">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="06149-109">Identifier:</span></span>  <br/> |<span data-ttu-id="06149-110">0x3E04</span><span class="sxs-lookup"><span data-stu-id="06149-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="06149-111">Type de données :</span><span class="sxs-lookup"><span data-stu-id="06149-111">Data type:</span></span>  <br/> |<span data-ttu-id="06149-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="06149-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="06149-113">Domaine :</span><span class="sxs-lookup"><span data-stu-id="06149-113">Area:</span></span>  <br/> |<span data-ttu-id="06149-114">État MAPI</span><span class="sxs-lookup"><span data-stu-id="06149-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06149-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="06149-115">Remarks</span></span>

<span data-ttu-id="06149-116">Le code d'État doit apparaître dans le fichier MAPISVC. inf pour tous les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="06149-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="06149-117">Les objets d'État sont implémentés par MAPI et par tous les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="06149-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="06149-118">Il existe deux ensembles de valeurs valides pour les codes d'État, un ensemble pour tous les objets d'État et un autre ensemble pour les fournisseurs de transport uniquement.</span><span class="sxs-lookup"><span data-stu-id="06149-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="06149-119">Tous les objets d'État peuvent définir cette propriété avec les valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="06149-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="06149-120">STATUS_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="06149-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="06149-121">Indique que la ressource est opérationnelle.</span><span class="sxs-lookup"><span data-stu-id="06149-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="06149-122">STATUS_FAILURE</span><span class="sxs-lookup"><span data-stu-id="06149-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="06149-123">Indique que la ressource rencontre un problème.</span><span class="sxs-lookup"><span data-stu-id="06149-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="06149-124">Pour les fournisseurs de services, STATUS_FAILURE indique que le fournisseur peut bientôt être arrêté pour mettre fin à la session en cours.</span><span class="sxs-lookup"><span data-stu-id="06149-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="06149-125">STATUS_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="06149-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="06149-126">Indique que seules les données locales ou les services sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="06149-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="06149-127">Les fournisseurs de transport peuvent également définir les propriétés **PR_STATUS_CODE** de leurs objets d'État sur les valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="06149-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="06149-128">STATUS_INBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="06149-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="06149-129">Indique que le fournisseur de transport reçoit un message entrant.</span><span class="sxs-lookup"><span data-stu-id="06149-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="06149-130">STATUS_INBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="06149-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="06149-131">Indique que le fournisseur de transport peut recevoir des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="06149-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="06149-132">STATUS_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="06149-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="06149-133">Indique que le fournisseur de transport télécharge les messages à partir de la file d'attente entrante.</span><span class="sxs-lookup"><span data-stu-id="06149-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="06149-134">STATUS_OUTBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="06149-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="06149-135">Indique que le fournisseur de transport reçoit un message sortant.</span><span class="sxs-lookup"><span data-stu-id="06149-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="06149-136">STATUS_OUTBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="06149-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="06149-137">Indique que le fournisseur de transport peut gérer les messages sortants.</span><span class="sxs-lookup"><span data-stu-id="06149-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="06149-138">STATUS_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="06149-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="06149-139">Indique que le fournisseur de transport télécharge les messages à partir de sa file d'attente sortante.</span><span class="sxs-lookup"><span data-stu-id="06149-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="06149-140">STATUS_REMOTE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="06149-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="06149-141">Indique que le fournisseur de transport prend en charge l'accès à distance.</span><span class="sxs-lookup"><span data-stu-id="06149-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="06149-142">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="06149-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="06149-143">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="06149-143">Header files</span></span>

<span data-ttu-id="06149-144">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="06149-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="06149-145">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="06149-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="06149-146">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="06149-146">Mapitags.h</span></span>
  
> <span data-ttu-id="06149-147">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="06149-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06149-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06149-148">See also</span></span>



[<span data-ttu-id="06149-149">Propriété canonique PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="06149-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="06149-150">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="06149-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06149-151">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="06149-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06149-152">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="06149-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06149-153">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="06149-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

