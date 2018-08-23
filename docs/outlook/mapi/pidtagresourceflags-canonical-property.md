---
title: Propriété canonique PidTagResourceFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceFlags
api_type:
- COM
ms.assetid: 69be9ad3-006a-459e-9cd4-eb3f609d71ad
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 875b37183134a6c5beca76ab7910cf601d1b6175
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567502"
---
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="e06c4-103">Propriété canonique PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="e06c4-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="e06c4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e06c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e06c4-105">Contient un masque de bits d’indicateurs pour les fournisseurs et les services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="e06c4-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e06c4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e06c4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e06c4-107">PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="e06c4-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="e06c4-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e06c4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e06c4-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="e06c4-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="e06c4-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e06c4-110">Data type:</span></span>  <br/> |<span data-ttu-id="e06c4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e06c4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e06c4-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e06c4-112">Area:</span></span>  <br/> |<span data-ttu-id="e06c4-113">MAPI courantes</span><span class="sxs-lookup"><span data-stu-id="e06c4-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e06c4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e06c4-114">Remarks</span></span>

<span data-ttu-id="e06c4-115">Cette propriété décrit les caractéristiques d’un service de message, un fournisseur de services ou un objet d’état.</span><span class="sxs-lookup"><span data-stu-id="e06c4-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="e06c4-116">Les indicateurs qui sont définis pour cette propriété dépendant de son contexte.</span><span class="sxs-lookup"><span data-stu-id="e06c4-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="e06c4-117">Par exemple, certains indicateurs sont valides uniquement pour les objets d’état et d’autres indicateurs uniquement pour les colonnes dans la table de service de message.</span><span class="sxs-lookup"><span data-stu-id="e06c4-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="e06c4-118">Les indicateurs sont de trois classes : modifiable, statiques et dynamiques.</span><span class="sxs-lookup"><span data-stu-id="e06c4-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="e06c4-119">Indicateurs statiques sont définis par MAPI à partir des données dans le fichier MAPISVC.inf. INF et n’a jamais été modifié.</span><span class="sxs-lookup"><span data-stu-id="e06c4-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="e06c4-120">Modifiables indicateurs sont définis par MAPI à partir du fichier MAPISVC.inf. INF mais peut être modifiée par la suite.</span><span class="sxs-lookup"><span data-stu-id="e06c4-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="e06c4-121">Indicateurs dynamiques pouvant être définies et réinitialiser par les méthodes MAPI.</span><span class="sxs-lookup"><span data-stu-id="e06c4-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="e06c4-122">Pour un service de message, un ou plusieurs des indicateurs suivants peuvent être défini dans cette propriété :</span><span class="sxs-lookup"><span data-stu-id="e06c4-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="e06c4-123">SERVICE_CREATE_WITH_STORE</span><span class="sxs-lookup"><span data-stu-id="e06c4-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="e06c4-124">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e06c4-124">Reserved.</span></span> <span data-ttu-id="e06c4-125">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="e06c4-125">Do not use.</span></span>
    
<span data-ttu-id="e06c4-126">SERVICE_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="e06c4-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="e06c4-127">Dynamique.</span><span class="sxs-lookup"><span data-stu-id="e06c4-127">Dynamic.</span></span> <span data-ttu-id="e06c4-128">Le service de message contient la banque par défaut.</span><span class="sxs-lookup"><span data-stu-id="e06c4-128">The message service contains the default store.</span></span> <span data-ttu-id="e06c4-129">Une interface utilisateur doit être affichée demander à l’utilisateur de confirmer la suppression ou le déplacement de ce service s’en déconnecter le profil.</span><span class="sxs-lookup"><span data-stu-id="e06c4-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="e06c4-130">SERVICE_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="e06c4-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="e06c4-131">Statique.</span><span class="sxs-lookup"><span data-stu-id="e06c4-131">Static.</span></span> <span data-ttu-id="e06c4-132">L’indicateur au niveau de service qui doit être défini pour indiquer qu’aucun des fournisseurs dans le service de message peut être utilisée pour fournir une identité.</span><span class="sxs-lookup"><span data-stu-id="e06c4-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="e06c4-133">Cet indicateur ou SERVICE_PRIMARY_IDENTITY doit être ensemble, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="e06c4-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="e06c4-134">SERVICE_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="e06c4-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="e06c4-135">Modifiable.</span><span class="sxs-lookup"><span data-stu-id="e06c4-135">Modifiable.</span></span> <span data-ttu-id="e06c4-136">Le service de message correspondant contient le fournisseur utilisé pour l’identité du principale pour cette session.</span><span class="sxs-lookup"><span data-stu-id="e06c4-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="e06c4-137">[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) permet de définir cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="e06c4-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="e06c4-138">Cet indicateur ou SERVICE_NO_PRIMARY_IDENTITY doit être ensemble, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="e06c4-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="e06c4-139">SERVICE_SINGLE_COPY</span><span class="sxs-lookup"><span data-stu-id="e06c4-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="e06c4-140">Statique.</span><span class="sxs-lookup"><span data-stu-id="e06c4-140">Static.</span></span> <span data-ttu-id="e06c4-141">Toute tentative pour créer ou copier ce service de message dans un profil dans lequel le service existe déjà échouera.</span><span class="sxs-lookup"><span data-stu-id="e06c4-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="e06c4-142">Pour créer une copie unique service de message ajouter la propriété **PR_RESOURCE_FLAGS** à la section du service dans le fichier MAPISVC.inf. INF et de définir cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="e06c4-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="e06c4-143">Pour un fournisseur de services, un ou plusieurs des indicateurs suivants peuvent être définies dans **PR_RESOURCE_FLAGS**:</span><span class="sxs-lookup"><span data-stu-id="e06c4-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="e06c4-144">HOOK_INBOUND</span><span class="sxs-lookup"><span data-stu-id="e06c4-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="e06c4-145">Statique.</span><span class="sxs-lookup"><span data-stu-id="e06c4-145">Static.</span></span> <span data-ttu-id="e06c4-146">Le crochet spouleur doit traiter les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="e06c4-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="e06c4-147">HOOK_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="e06c4-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="e06c4-148">Statique.</span><span class="sxs-lookup"><span data-stu-id="e06c4-148">Static.</span></span> <span data-ttu-id="e06c4-149">Le crochet spouleur doit traiter les messages sortants.</span><span class="sxs-lookup"><span data-stu-id="e06c4-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="e06c4-150">STATUS_DEFAULT_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="e06c4-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="e06c4-151">Modifiable.</span><span class="sxs-lookup"><span data-stu-id="e06c4-151">Modifiable.</span></span> <span data-ttu-id="e06c4-152">Ce paramètre identity doit être appliqué aux messages sortants si le profil contient plusieurs instances de ce fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="e06c4-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="e06c4-153">Cela peut se produire si plusieurs instances d’un fournisseur de transport unique s’affichent dans le profil.</span><span class="sxs-lookup"><span data-stu-id="e06c4-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="e06c4-154">STATUS_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="e06c4-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="e06c4-155">Modifiable.</span><span class="sxs-lookup"><span data-stu-id="e06c4-155">Modifiable.</span></span> <span data-ttu-id="e06c4-156">Cette banque de messages est la banque par défaut pour le profil.</span><span class="sxs-lookup"><span data-stu-id="e06c4-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="e06c4-157">STATUS_NEED_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="e06c4-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="e06c4-158">Dynamique.</span><span class="sxs-lookup"><span data-stu-id="e06c4-158">Dynamic.</span></span> <span data-ttu-id="e06c4-159">Les dossiers standards dans cette banque de messages, y compris le dossier racine du message interpersonnel (IPM), n’ont pas encore été vérifiées.</span><span class="sxs-lookup"><span data-stu-id="e06c4-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="e06c4-160">MAPI Active et désactive cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="e06c4-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="e06c4-161">STATUS_NO_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="e06c4-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="e06c4-162">Statique.</span><span class="sxs-lookup"><span data-stu-id="e06c4-162">Static.</span></span> <span data-ttu-id="e06c4-163">Cette banque de messages est incapable de devenir la banque de messages par défaut pour le profil.</span><span class="sxs-lookup"><span data-stu-id="e06c4-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="e06c4-164">STATUS_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="e06c4-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="e06c4-165">Statique.</span><span class="sxs-lookup"><span data-stu-id="e06c4-165">Static.</span></span> <span data-ttu-id="e06c4-166">Ce fournisseur ne pas de fournir une identité dans sa ligne d’état.</span><span class="sxs-lookup"><span data-stu-id="e06c4-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="e06c4-167">Cet indicateur ou STATUS_PRIMARY_IDENTITY doit être défini.</span><span class="sxs-lookup"><span data-stu-id="e06c4-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="e06c4-168">STATUS_OWN_STORE</span><span class="sxs-lookup"><span data-stu-id="e06c4-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="e06c4-169">Statique.</span><span class="sxs-lookup"><span data-stu-id="e06c4-169">Static.</span></span> <span data-ttu-id="e06c4-170">Ce fournisseur de transport fortement couplé à une banque de messages et fournit la propriété **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) dans la ligne d’état.</span><span class="sxs-lookup"><span data-stu-id="e06c4-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="e06c4-171">STATUS_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="e06c4-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="e06c4-172">Modifiable.</span><span class="sxs-lookup"><span data-stu-id="e06c4-172">Modifiable.</span></span> <span data-ttu-id="e06c4-173">Ce fournisseur fournit l’identité du principale pour la session ; l’identificateur d’entrée pour l’objet fournissant l’identité est renvoyé à partir de [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="e06c4-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="e06c4-174">Cet indicateur ou **STATUS_NO_PRIMARY_IDENTITY** doit être défini.</span><span class="sxs-lookup"><span data-stu-id="e06c4-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="e06c4-175">STATUS_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="e06c4-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="e06c4-176">Modifiable.</span><span class="sxs-lookup"><span data-stu-id="e06c4-176">Modifiable.</span></span> <span data-ttu-id="e06c4-177">Cette banque de messages doit être utilisé lorsqu’une application cliente se connecte.</span><span class="sxs-lookup"><span data-stu-id="e06c4-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="e06c4-178">Une fois ouvert, ce magasin doit être défini en tant que la banque par défaut pour le profil.</span><span class="sxs-lookup"><span data-stu-id="e06c4-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="e06c4-179">STATUS_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="e06c4-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="e06c4-180">Modifiable.</span><span class="sxs-lookup"><span data-stu-id="e06c4-180">Modifiable.</span></span> <span data-ttu-id="e06c4-181">Cette banque de messages doit être utilisé si la banque principale n’est pas disponible lorsqu’une application cliente se connecte.</span><span class="sxs-lookup"><span data-stu-id="e06c4-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="e06c4-182">Une fois ouvert, ce magasin doit être défini en tant que la banque par défaut pour le profil.</span><span class="sxs-lookup"><span data-stu-id="e06c4-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="e06c4-183">STATUS_SIMPLE_STORE</span><span class="sxs-lookup"><span data-stu-id="e06c4-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="e06c4-184">Dynamique.</span><span class="sxs-lookup"><span data-stu-id="e06c4-184">Dynamic.</span></span> <span data-ttu-id="e06c4-185">Permettra de cette banque de messages par l’interface Simple MAPI en tant que la banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="e06c4-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="e06c4-186">STATUS_TEMP_SECTION</span><span class="sxs-lookup"><span data-stu-id="e06c4-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="e06c4-187">Dynamique.</span><span class="sxs-lookup"><span data-stu-id="e06c4-187">Dynamic.</span></span> <span data-ttu-id="e06c4-188">Cette banque de messages ne doit pas être publiée dans la table et du profil est supprimée après la fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="e06c4-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="e06c4-189">STATUS_XP_PREFER_LAST</span><span class="sxs-lookup"><span data-stu-id="e06c4-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="e06c4-190">Statique.</span><span class="sxs-lookup"><span data-stu-id="e06c4-190">Static.</span></span> <span data-ttu-id="e06c4-191">Ce transport est censé être le dernier transport sélectionné pour envoyer un message lorsque plusieurs fournisseurs de transport sont en mesure de transmettre le message.</span><span class="sxs-lookup"><span data-stu-id="e06c4-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="e06c4-192">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e06c4-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e06c4-193">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e06c4-193">Header files</span></span>

<span data-ttu-id="e06c4-194">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e06c4-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="e06c4-195">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e06c4-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="e06c4-196">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="e06c4-196">Mapitags.h</span></span>
  
> <span data-ttu-id="e06c4-197">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="e06c4-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e06c4-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e06c4-198">See also</span></span>



[<span data-ttu-id="e06c4-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="e06c4-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="e06c4-200">Propriété canonique PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="e06c4-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="e06c4-201">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e06c4-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e06c4-202">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e06c4-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e06c4-203">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e06c4-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e06c4-204">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e06c4-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

