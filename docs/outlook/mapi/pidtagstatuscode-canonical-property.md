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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: efd0dcc8fc01fa433cbbf30936244e4818f8b14a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786830"
---
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="cc61e-103">Propriété canonique PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="cc61e-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="cc61e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cc61e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cc61e-105">Contient un masque de bits d’indicateurs qui indiquent l’état actuel d’une ressource de session.</span><span class="sxs-lookup"><span data-stu-id="cc61e-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="cc61e-106">Tous les fournisseurs de services de définissent les codes d’état comme MAPI pour créer des rapports sur l’état du sous-système, le spouleur MAPI et le carnet d’adresses intégré.</span><span class="sxs-lookup"><span data-stu-id="cc61e-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc61e-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="cc61e-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc61e-108">PR_STATUS_CODE</span><span class="sxs-lookup"><span data-stu-id="cc61e-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="cc61e-109">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="cc61e-109">Identifier:</span></span>  <br/> |<span data-ttu-id="cc61e-110">0x3E04</span><span class="sxs-lookup"><span data-stu-id="cc61e-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="cc61e-111">Type de données :</span><span class="sxs-lookup"><span data-stu-id="cc61e-111">Data type:</span></span>  <br/> |<span data-ttu-id="cc61e-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cc61e-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cc61e-113">Zone :</span><span class="sxs-lookup"><span data-stu-id="cc61e-113">Area:</span></span>  <br/> |<span data-ttu-id="cc61e-114">État MAPI</span><span class="sxs-lookup"><span data-stu-id="cc61e-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc61e-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="cc61e-115">Remarks</span></span>

<span data-ttu-id="cc61e-116">Le code d’état doit apparaître dans le fichier Mapisvc.inf pour tous les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="cc61e-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="cc61e-117">Objets d’état sont implémentés par MAPI et par tous les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="cc61e-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="cc61e-118">Il existe deux jeux de valeurs valides pour les codes d’état, un ensemble de tous les objets d’état et un autre ensemble pour les fournisseurs de transport uniquement.</span><span class="sxs-lookup"><span data-stu-id="cc61e-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="cc61e-119">Tous les objets d’état peuvent définir cette propriété sur les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="cc61e-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="cc61e-120">STATUS_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="cc61e-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="cc61e-121">Indique que la ressource est opérationnelle.</span><span class="sxs-lookup"><span data-stu-id="cc61e-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="cc61e-122">VALEUR</span><span class="sxs-lookup"><span data-stu-id="cc61e-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="cc61e-123">Indique que la ressource est un problème.</span><span class="sxs-lookup"><span data-stu-id="cc61e-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="cc61e-124">Pour les fournisseurs de service, la valeur indique que le fournisseur bientôt est arrêté à la fin de la session en cours.</span><span class="sxs-lookup"><span data-stu-id="cc61e-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="cc61e-125">STATUS_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="cc61e-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="cc61e-126">Indique que les données locales uniquement ou les services sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="cc61e-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="cc61e-127">Fournisseurs de transport peuvent également définir leur statut **PR_STATUS_CODE** propriétés des objets aux valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="cc61e-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="cc61e-128">STATUS_INBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="cc61e-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="cc61e-129">Indique que le fournisseur de transport reçoit un message entrant.</span><span class="sxs-lookup"><span data-stu-id="cc61e-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="cc61e-130">STATUS_INBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="cc61e-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="cc61e-131">Indique que le fournisseur de transport peut recevoir des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="cc61e-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="cc61e-132">STATUS_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="cc61e-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="cc61e-133">Indique que le fournisseur de transport téléchargement des messages à partir de la file d’attente entrante.</span><span class="sxs-lookup"><span data-stu-id="cc61e-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="cc61e-134">STATUS_OUTBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="cc61e-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="cc61e-135">Indique que le fournisseur de transport reçoit un message sortant.</span><span class="sxs-lookup"><span data-stu-id="cc61e-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="cc61e-136">STATUS_OUTBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="cc61e-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="cc61e-137">Indique que le fournisseur de transport peut gérer les messages sortants.</span><span class="sxs-lookup"><span data-stu-id="cc61e-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="cc61e-138">STATUS_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="cc61e-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="cc61e-139">Indique que le fournisseur de transport est téléchargement des messages à partir de sa file d’attente sortante.</span><span class="sxs-lookup"><span data-stu-id="cc61e-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="cc61e-140">STATUS_REMOTE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="cc61e-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="cc61e-141">Indique que le fournisseur de transport prend en charge l’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="cc61e-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="cc61e-142">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="cc61e-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cc61e-143">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="cc61e-143">Header files</span></span>

<span data-ttu-id="cc61e-144">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc61e-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc61e-145">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="cc61e-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc61e-146">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="cc61e-146">Mapitags.h</span></span>
  
> <span data-ttu-id="cc61e-147">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="cc61e-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc61e-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc61e-148">See also</span></span>



[<span data-ttu-id="cc61e-149">Propriété canonique PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="cc61e-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="cc61e-150">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="cc61e-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc61e-151">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="cc61e-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc61e-152">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="cc61e-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc61e-153">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="cc61e-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

