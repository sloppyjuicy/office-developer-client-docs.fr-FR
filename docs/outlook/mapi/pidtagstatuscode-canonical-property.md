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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a60bc55686e883cabd144af3a9badfb55f835472
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593122"
---
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="be7a8-103">Propriété canonique PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="be7a8-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="be7a8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be7a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be7a8-105">Contient un masque de bits d’indicateurs qui indiquent l’état actuel d’une ressource de session.</span><span class="sxs-lookup"><span data-stu-id="be7a8-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="be7a8-106">Tous les fournisseurs de services de définissent les codes d’état comme MAPI pour créer des rapports sur l’état du sous-système, le spouleur MAPI et le carnet d’adresses intégré.</span><span class="sxs-lookup"><span data-stu-id="be7a8-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be7a8-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="be7a8-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="be7a8-108">PR_STATUS_CODE</span><span class="sxs-lookup"><span data-stu-id="be7a8-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="be7a8-109">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="be7a8-109">Identifier:</span></span>  <br/> |<span data-ttu-id="be7a8-110">0x3E04</span><span class="sxs-lookup"><span data-stu-id="be7a8-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="be7a8-111">Type de données :</span><span class="sxs-lookup"><span data-stu-id="be7a8-111">Data type:</span></span>  <br/> |<span data-ttu-id="be7a8-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="be7a8-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="be7a8-113">Domaine :</span><span class="sxs-lookup"><span data-stu-id="be7a8-113">Area:</span></span>  <br/> |<span data-ttu-id="be7a8-114">État MAPI</span><span class="sxs-lookup"><span data-stu-id="be7a8-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be7a8-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="be7a8-115">Remarks</span></span>

<span data-ttu-id="be7a8-116">Le code d’état doit apparaître dans le fichier Mapisvc.inf pour tous les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="be7a8-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="be7a8-117">Objets d’état sont implémentés par MAPI et par tous les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="be7a8-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="be7a8-118">Il existe deux jeux de valeurs valides pour les codes d’état, un ensemble de tous les objets d’état et un autre ensemble pour les fournisseurs de transport uniquement.</span><span class="sxs-lookup"><span data-stu-id="be7a8-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="be7a8-119">Tous les objets d’état peuvent définir cette propriété sur les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="be7a8-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="be7a8-120">STATUS_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="be7a8-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="be7a8-121">Indique que la ressource est opérationnelle.</span><span class="sxs-lookup"><span data-stu-id="be7a8-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="be7a8-122">VALEUR</span><span class="sxs-lookup"><span data-stu-id="be7a8-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="be7a8-123">Indique que la ressource est un problème.</span><span class="sxs-lookup"><span data-stu-id="be7a8-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="be7a8-124">Pour les fournisseurs de service, la valeur indique que le fournisseur bientôt est arrêté à la fin de la session en cours.</span><span class="sxs-lookup"><span data-stu-id="be7a8-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="be7a8-125">STATUS_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="be7a8-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="be7a8-126">Indique que les données locales uniquement ou les services sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="be7a8-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="be7a8-127">Fournisseurs de transport peuvent également définir leur statut **PR_STATUS_CODE** propriétés des objets aux valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="be7a8-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="be7a8-128">STATUS_INBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="be7a8-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="be7a8-129">Indique que le fournisseur de transport reçoit un message entrant.</span><span class="sxs-lookup"><span data-stu-id="be7a8-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="be7a8-130">STATUS_INBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="be7a8-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="be7a8-131">Indique que le fournisseur de transport peut recevoir des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="be7a8-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="be7a8-132">STATUS_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="be7a8-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="be7a8-133">Indique que le fournisseur de transport téléchargement des messages à partir de la file d’attente entrante.</span><span class="sxs-lookup"><span data-stu-id="be7a8-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="be7a8-134">STATUS_OUTBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="be7a8-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="be7a8-135">Indique que le fournisseur de transport reçoit un message sortant.</span><span class="sxs-lookup"><span data-stu-id="be7a8-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="be7a8-136">STATUS_OUTBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="be7a8-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="be7a8-137">Indique que le fournisseur de transport peut gérer les messages sortants.</span><span class="sxs-lookup"><span data-stu-id="be7a8-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="be7a8-138">STATUS_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="be7a8-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="be7a8-139">Indique que le fournisseur de transport est téléchargement des messages à partir de sa file d’attente sortante.</span><span class="sxs-lookup"><span data-stu-id="be7a8-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="be7a8-140">STATUS_REMOTE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="be7a8-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="be7a8-141">Indique que le fournisseur de transport prend en charge l’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="be7a8-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="be7a8-142">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="be7a8-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="be7a8-143">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="be7a8-143">Header files</span></span>

<span data-ttu-id="be7a8-144">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be7a8-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="be7a8-145">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="be7a8-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="be7a8-146">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="be7a8-146">Mapitags.h</span></span>
  
> <span data-ttu-id="be7a8-147">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="be7a8-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be7a8-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be7a8-148">See also</span></span>



[<span data-ttu-id="be7a8-149">Propriété canonique PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="be7a8-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="be7a8-150">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="be7a8-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be7a8-151">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="be7a8-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be7a8-152">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="be7a8-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be7a8-153">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="be7a8-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

