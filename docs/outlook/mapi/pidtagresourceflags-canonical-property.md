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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2fb9eed0beaf7269ac90a021dae650355484ebc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436229"
---
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="8a543-103">Propriété canonique PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="8a543-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="8a543-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a543-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a543-105">Contient un masque de réindicateur des indicateurs pour les services de messagerie et les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="8a543-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a543-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8a543-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a543-107">PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="8a543-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="8a543-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8a543-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a543-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="8a543-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="8a543-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8a543-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a543-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8a543-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8a543-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8a543-112">Area:</span></span>  <br/> |<span data-ttu-id="8a543-113">MAPI commun</span><span class="sxs-lookup"><span data-stu-id="8a543-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a543-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8a543-114">Remarks</span></span>

<span data-ttu-id="8a543-115">Cette propriété décrit les caractéristiques d'un service de messagerie, d'un fournisseur de services ou d'un objet d'État.</span><span class="sxs-lookup"><span data-stu-id="8a543-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="8a543-116">Les indicateurs définis pour cette propriété dépendent de son contexte.</span><span class="sxs-lookup"><span data-stu-id="8a543-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="8a543-117">Par exemple, certains indicateurs ne sont valides que pour les objets d'État et les autres indicateurs uniquement pour les colonnes du tableau de service de message.</span><span class="sxs-lookup"><span data-stu-id="8a543-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="8a543-118">Les indicateurs sont de trois classes: statique, modifiable et dynamique.</span><span class="sxs-lookup"><span data-stu-id="8a543-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="8a543-119">Les indicateurs statiques sont définis par MAPI à partir de données dans MAPISVC. INF et jamais modifié.</span><span class="sxs-lookup"><span data-stu-id="8a543-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="8a543-120">Les indicateurs modifiables sont définis par MAPI à partir de MAPISVC. INF, mais peut être modifié par la suite.</span><span class="sxs-lookup"><span data-stu-id="8a543-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="8a543-121">Les indicateurs dynamiques peuvent être définis et réinitialisés par des méthodes MAPI.</span><span class="sxs-lookup"><span data-stu-id="8a543-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="8a543-122">Pour un service de messagerie, un ou plusieurs des indicateurs suivants peuvent être définis dans cette propriété:</span><span class="sxs-lookup"><span data-stu-id="8a543-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="8a543-123">SERVICE_CREATE_WITH_STORE</span><span class="sxs-lookup"><span data-stu-id="8a543-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="8a543-124">Réservé.</span><span class="sxs-lookup"><span data-stu-id="8a543-124">Reserved.</span></span> <span data-ttu-id="8a543-125">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="8a543-125">Do not use.</span></span>
    
<span data-ttu-id="8a543-126">SERVICE_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="8a543-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="8a543-127">Dynamique.</span><span class="sxs-lookup"><span data-stu-id="8a543-127">Dynamic.</span></span> <span data-ttu-id="8a543-128">Le service de messagerie contient le magasin par défaut.</span><span class="sxs-lookup"><span data-stu-id="8a543-128">The message service contains the default store.</span></span> <span data-ttu-id="8a543-129">Une interface utilisateur doit s'afficher pour inviter l'utilisateur à confirmer avant de supprimer ou de retirer ce service du profil.</span><span class="sxs-lookup"><span data-stu-id="8a543-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="8a543-130">SERVICE_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="8a543-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="8a543-131">Liée.</span><span class="sxs-lookup"><span data-stu-id="8a543-131">Static.</span></span> <span data-ttu-id="8a543-132">Indicateur de niveau de service qui doit être défini pour indiquer qu'aucun des fournisseurs dans le service de messagerie ne peut être utilisé pour fournir une identité.</span><span class="sxs-lookup"><span data-stu-id="8a543-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="8a543-133">Cet indicateur ou SERVICE_PRIMARY_IDENTITY doit être défini, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="8a543-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="8a543-134">SERVICE_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="8a543-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="8a543-135">Modifiable.</span><span class="sxs-lookup"><span data-stu-id="8a543-135">Modifiable.</span></span> <span data-ttu-id="8a543-136">Le service de messagerie correspondant contient le fournisseur utilisé pour l'identité principale de cette session.</span><span class="sxs-lookup"><span data-stu-id="8a543-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="8a543-137">Utilisez [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) pour définir cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="8a543-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="8a543-138">Cet indicateur ou SERVICE_NO_PRIMARY_IDENTITY doit être défini, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="8a543-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="8a543-139">SERVICE_SINGLE_COPY</span><span class="sxs-lookup"><span data-stu-id="8a543-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="8a543-140">Liée.</span><span class="sxs-lookup"><span data-stu-id="8a543-140">Static.</span></span> <span data-ttu-id="8a543-141">Toute tentative de création ou de copie de ce service de messagerie dans un profil où le service existe déjà échouera.</span><span class="sxs-lookup"><span data-stu-id="8a543-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="8a543-142">Pour créer un service de messagerie à copie unique, ajoutez la propriété **PR_RESOURCE_FLAGS** à la section du service dans MAPISVC. INF et définissez cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="8a543-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="8a543-143">Pour un fournisseur de services, un ou plusieurs des indicateurs suivants peuvent être définis dans **PR_RESOURCE_FLAGS**:</span><span class="sxs-lookup"><span data-stu-id="8a543-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="8a543-144">HOOK_INBOUND</span><span class="sxs-lookup"><span data-stu-id="8a543-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="8a543-145">Liée.</span><span class="sxs-lookup"><span data-stu-id="8a543-145">Static.</span></span> <span data-ttu-id="8a543-146">Le hook de spouleur doit traiter les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="8a543-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="8a543-147">HOOK_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="8a543-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="8a543-148">Liée.</span><span class="sxs-lookup"><span data-stu-id="8a543-148">Static.</span></span> <span data-ttu-id="8a543-149">Le hook de spouleur doit traiter les messages sortants.</span><span class="sxs-lookup"><span data-stu-id="8a543-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="8a543-150">STATUS_DEFAULT_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="8a543-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="8a543-151">Modifiable.</span><span class="sxs-lookup"><span data-stu-id="8a543-151">Modifiable.</span></span> <span data-ttu-id="8a543-152">Cette identité doit être appliquée aux messages sortants si le profil contient plusieurs instances de ce fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="8a543-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="8a543-153">Cela peut se produire si plusieurs instances d'un fournisseur de transport unique apparaissent dans le profil.</span><span class="sxs-lookup"><span data-stu-id="8a543-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="8a543-154">STATUS_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="8a543-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="8a543-155">Modifiable.</span><span class="sxs-lookup"><span data-stu-id="8a543-155">Modifiable.</span></span> <span data-ttu-id="8a543-156">Il s'agit de la Banque de messages par défaut pour le profil.</span><span class="sxs-lookup"><span data-stu-id="8a543-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="8a543-157">STATUS_NEED_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="8a543-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="8a543-158">Dynamique.</span><span class="sxs-lookup"><span data-stu-id="8a543-158">Dynamic.</span></span> <span data-ttu-id="8a543-159">Les dossiers standard de cette banque de messages, y compris le dossier racine de message, n'ont pas encore été vérifiés.</span><span class="sxs-lookup"><span data-stu-id="8a543-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="8a543-160">MAPI définit et efface cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="8a543-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="8a543-161">STATUS_NO_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="8a543-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="8a543-162">Liée.</span><span class="sxs-lookup"><span data-stu-id="8a543-162">Static.</span></span> <span data-ttu-id="8a543-163">Cette banque de messages ne peut pas devenir la Banque de messages par défaut pour le profil.</span><span class="sxs-lookup"><span data-stu-id="8a543-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="8a543-164">STATUS_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="8a543-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="8a543-165">Liée.</span><span class="sxs-lookup"><span data-stu-id="8a543-165">Static.</span></span> <span data-ttu-id="8a543-166">Ce fournisseur ne fournit pas d'identité dans sa ligne d'État.</span><span class="sxs-lookup"><span data-stu-id="8a543-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="8a543-167">Cet indicateur ou STATUS_PRIMARY_IDENTITY doit être défini.</span><span class="sxs-lookup"><span data-stu-id="8a543-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="8a543-168">STATUS_OWN_STORE</span><span class="sxs-lookup"><span data-stu-id="8a543-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="8a543-169">Liée.</span><span class="sxs-lookup"><span data-stu-id="8a543-169">Static.</span></span> <span data-ttu-id="8a543-170">Ce fournisseur de transport est étroitement couplé à une banque de messages et fournit la propriété **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) dans sa ligne d'État.</span><span class="sxs-lookup"><span data-stu-id="8a543-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="8a543-171">STATUS_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="8a543-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="8a543-172">Modifiable.</span><span class="sxs-lookup"><span data-stu-id="8a543-172">Modifiable.</span></span> <span data-ttu-id="8a543-173">Ce fournisseur fournit l'identité principale pour la session; l'identificateur d'entrée pour l'objet qui fournit l'identité est renvoyé depuis [IMAPISession:: QueryIdentity](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="8a543-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="8a543-174">Cet indicateur ou **STATUS_NO_PRIMARY_IDENTITY** doit être défini.</span><span class="sxs-lookup"><span data-stu-id="8a543-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="8a543-175">STATUS_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="8a543-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="8a543-176">Modifiable.</span><span class="sxs-lookup"><span data-stu-id="8a543-176">Modifiable.</span></span> <span data-ttu-id="8a543-177">Cette banque de messages doit être utilisée lorsqu'une application cliente se connecte.</span><span class="sxs-lookup"><span data-stu-id="8a543-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="8a543-178">Une fois ouvert, ce magasin doit être défini comme magasin par défaut pour le profil.</span><span class="sxs-lookup"><span data-stu-id="8a543-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="8a543-179">STATUS_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="8a543-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="8a543-180">Modifiable.</span><span class="sxs-lookup"><span data-stu-id="8a543-180">Modifiable.</span></span> <span data-ttu-id="8a543-181">Cette banque de messages doit être utilisée si le magasin principal n'est pas disponible lorsqu'une application cliente se connecte.</span><span class="sxs-lookup"><span data-stu-id="8a543-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="8a543-182">Une fois ouvert, ce magasin doit être défini comme magasin par défaut pour le profil.</span><span class="sxs-lookup"><span data-stu-id="8a543-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="8a543-183">STATUS_SIMPLE_STORE</span><span class="sxs-lookup"><span data-stu-id="8a543-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="8a543-184">Dynamique.</span><span class="sxs-lookup"><span data-stu-id="8a543-184">Dynamic.</span></span> <span data-ttu-id="8a543-185">Cette banque de messages sera utilisée par le simple MAPI comme banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="8a543-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="8a543-186">STATUS_TEMP_SECTION</span><span class="sxs-lookup"><span data-stu-id="8a543-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="8a543-187">Dynamique.</span><span class="sxs-lookup"><span data-stu-id="8a543-187">Dynamic.</span></span> <span data-ttu-id="8a543-188">Cette banque de messages ne doit pas être publiée dans la table de banque de messages et sera supprimée du profil après la fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="8a543-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="8a543-189">STATUS_XP_PREFER_LAST</span><span class="sxs-lookup"><span data-stu-id="8a543-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="8a543-190">Liée.</span><span class="sxs-lookup"><span data-stu-id="8a543-190">Static.</span></span> <span data-ttu-id="8a543-191">Ce transport s'attend à être le dernier transport sélectionné pour envoyer un message lorsque plusieurs fournisseurs de transport peuvent transmettre le message.</span><span class="sxs-lookup"><span data-stu-id="8a543-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="8a543-192">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8a543-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8a543-193">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="8a543-193">Header files</span></span>

<span data-ttu-id="8a543-194">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8a543-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a543-195">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8a543-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a543-196">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8a543-196">Mapitags.h</span></span>
  
> <span data-ttu-id="8a543-197">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="8a543-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a543-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a543-198">See also</span></span>



[<span data-ttu-id="8a543-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="8a543-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="8a543-200">Propriété canonique PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="8a543-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="8a543-201">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8a543-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a543-202">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8a543-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a543-203">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8a543-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a543-204">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8a543-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

