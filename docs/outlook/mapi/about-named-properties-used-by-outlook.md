---
title: À propos des propriétés nommées utilisées par Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: 'Dernière modification : 25 juin 2012'
ms.openlocfilehash: aa4d52d25f120e8b3e2a4c0dcaa4845ad576127a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566228"
---
# <a name="about-named-properties-used-by-outlook"></a><span data-ttu-id="5fba4-103">À propos des propriétés nommées utilisées par Outlook</span><span class="sxs-lookup"><span data-stu-id="5fba4-103">About Named Properties Used by Outlook</span></span>

  
  
<span data-ttu-id="5fba4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fba4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5fba4-p101">L’interface MAPI (Messaging Application Programming Interface) intègre une fonctionnalité permettant d’affecter des noms à certaines propriétés pour le mappage de ces noms avec des identificateurs uniques et de rendre ce mappage nom-identificateur permanent dans l’ensemble des sessions. Les propriétés nommées sont identifiées par un nom et un identificateur global unique (GUID) pour un jeu de propriétés. Le nom peut être un nombre ou une chaîne. Pour Microsoft Outlook 2013 ou Microsoft Outlook 2010, le jeu de propriétés est souvent un espace de noms défini par Outlook 2013 ou Outlook 2010, tel que **PSETID_Appointment**.</span><span class="sxs-lookup"><span data-stu-id="5fba4-p101">MAPI provides a facility for assigning names to certain properties, for mapping these names to unique identifiers, and for making this name-to-identifier mapping persistent across sessions. Named properties are identified by a name and a globally unique identifier (GUID) for a property set. The name can be a number or a string. For Microsoft Outlook 2013 or Microsoft Outlook 2010, the property set is often a namespace defined by Outlook 2013 or Outlook 2010, such as **PSETID_Appointment**.</span></span> 
  
<span data-ttu-id="5fba4-p102">Les propriétés nommées sont manipulées à l’aide des fonctions [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). Le nom et le GUID du jeu de propriétés sont transmis à la fonction [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir un identificateur de propriété valide pour la session MAPI en cours. Dans la mesure où cet identificateur de propriété peut varier d’un ordinateur à un autre, la seule manière cohérente d’accéder à une propriété nommée est de connaître son nom et son GUID de jeu de propriétés. La plage des identificateurs est toujours comprise dans la plage 0x8000 et 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="5fba4-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span></span> 
  
<span data-ttu-id="5fba4-p103">Tout objet qui implémente l’interface [IMAPIProp : IUnknown](imapipropiunknown.md) peut prendre en charge des propriétés nommées. Plus précisément, un fournisseur de services MAPI ou un client MAPI doit implémenter [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir des valeurs de propriétés nommées. La définition de propriétés nommées utilisées par Outlook 2013 ou Outlook 2010 n’est pas prise en charge en raison du risque d’endommagement des données partagées avec d’autres clients ou fournisseurs MAPI.</span><span class="sxs-lookup"><span data-stu-id="5fba4-p103">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span></span> 
  
<span data-ttu-id="5fba4-p104">Outlook 2013 et Outlook 2010 utilisent des propriétés nommées MAPI pour implémenter bon nombre de leurs fonctionnalités comme la sécurité des pièces jointes et les contre-propositions de réunion. Par-dessus ces données sous-jacentes, Outlook 2013 et Outlook 2010 exposent certaines de ces propriétés en tant que propriétés d’élément dans leurs modèles objet Outlook 2010 et Outlook 2013. Par exemple, la propriété **Email1Address** de l’objet **ContactItem** dans le modèle objet correspond à la [propriété canonique PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) nommée dans l’espace de noms **PSETID_Address**. Toutefois, en général, en raison de problèmes de compatibilité et d’intégrité des données, de nombreuses propriétés MAPI utilisées par Outlook 2013 et Outlook 2010 ne sont pas exposées dans le modèle objet.</span><span class="sxs-lookup"><span data-stu-id="5fba4-p104">Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model.</span></span> 
  
<span data-ttu-id="5fba4-120">Cette référence décrit un nombre de propriétés nommées répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="5fba4-120">This reference describes a number of named properties that are listed below.</span></span>
  
<span data-ttu-id="5fba4-121">Les propriétés nommées dans l’espace de noms **PSETID_Address** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5fba4-121">Named properties in the **PSETID_Address** namespace are the following:</span></span> 
  
- [<span data-ttu-id="5fba4-122">Propriété canonique PidLidEmail1AddressType</span><span class="sxs-lookup"><span data-stu-id="5fba4-122">PidLidEmail1AddressType Canonical Property</span></span>](pidlidemail1addresstype-canonical-property.md)
    
- [<span data-ttu-id="5fba4-123">Propriété canonique PidLidEmail1EmailAddress</span><span class="sxs-lookup"><span data-stu-id="5fba4-123">PidLidEmail1EmailAddress Canonical Property</span></span>](pidlidemail1emailaddress-canonical-property.md)
    
- [<span data-ttu-id="5fba4-124">Propriété canonique PidLidEmail1OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="5fba4-124">PidLidEmail1OriginalEntryId Canonical Property</span></span>](pidlidemail1originalentryid-canonical-property.md)
    
- [<span data-ttu-id="5fba4-125">Propriété canonique PidLidEmail2AddressType</span><span class="sxs-lookup"><span data-stu-id="5fba4-125">PidLidEmail2AddressType Canonical Property</span></span>](pidlidemail2addresstype-canonical-property.md)
    
- [<span data-ttu-id="5fba4-126">Propriété canonique PidLidEmail2DisplayName</span><span class="sxs-lookup"><span data-stu-id="5fba4-126">PidLidEmail2DisplayName Canonical Property</span></span>](pidlidemail2displayname-canonical-property.md)
    
- [<span data-ttu-id="5fba4-127">Propriété canonique PidLidEmail2EmailAddress</span><span class="sxs-lookup"><span data-stu-id="5fba4-127">PidLidEmail2EmailAddress Canonical Property</span></span>](pidlidemail2emailaddress-canonical-property.md)
    
- [<span data-ttu-id="5fba4-128">Propriété canonique PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="5fba4-128">PidLidEmail2OriginalDisplayName Canonical Property</span></span>](pidlidemail2originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="5fba4-129">Propriété canonique PidLidEmail2OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="5fba4-129">PidLidEmail2OriginalEntryId Canonical Property</span></span>](pidlidemail2originalentryid-canonical-property.md)
    
- [<span data-ttu-id="5fba4-130">Propriété canonique PidLidEmail3AddressType</span><span class="sxs-lookup"><span data-stu-id="5fba4-130">PidLidEmail3AddressType Canonical Property</span></span>](pidlidemail3addresstype-canonical-property.md)
    
- [<span data-ttu-id="5fba4-131">Propriété canonique PidLidEmail3DisplayName</span><span class="sxs-lookup"><span data-stu-id="5fba4-131">PidLidEmail3DisplayName Canonical Property</span></span>](pidlidemail3displayname-canonical-property.md)
    
- [<span data-ttu-id="5fba4-132">Propriété canonique PidLidEmail3EmailAddress</span><span class="sxs-lookup"><span data-stu-id="5fba4-132">PidLidEmail3EmailAddress Canonical Property</span></span>](pidlidemail3emailaddress-canonical-property.md)
    
- [<span data-ttu-id="5fba4-133">Propriété canonique PidLidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="5fba4-133">PidLidEmail3OriginalDisplayName Canonical Property</span></span>](pidlidemail3originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="5fba4-134">Propriété canonique PidLidEmail3OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="5fba4-134">PidLidEmail3OriginalEntryId Canonical Property</span></span>](pidlidemail3originalentryid-canonical-property.md)
    
- [<span data-ttu-id="5fba4-135">Propriété canonique PidLidEmail1DisplayName</span><span class="sxs-lookup"><span data-stu-id="5fba4-135">PidLidEmail1DisplayName Canonical Property</span></span>](pidlidemail1displayname-canonical-property.md)
    
- [<span data-ttu-id="5fba4-136">Propriété canonique PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="5fba4-136">PidLidEmail1OriginalDisplayName Canonical Property</span></span>](pidlidemail1originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="5fba4-137">Propriété canonique PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="5fba4-137">PidLidFileUnder Canonical Property</span></span>](pidlidfileunder-canonical-property.md)
    
- [<span data-ttu-id="5fba4-138">Propriété canonique PidLidInstantMessagingAddress</span><span class="sxs-lookup"><span data-stu-id="5fba4-138">PidLidInstantMessagingAddress Canonical Property</span></span>](pidlidinstantmessagingaddress-canonical-property.md)
    
- [<span data-ttu-id="5fba4-139">Propriété canonique PidLidWorkAddressCity</span><span class="sxs-lookup"><span data-stu-id="5fba4-139">PidLidWorkAddressCity Canonical Property</span></span>](pidlidworkaddresscity-canonical-property.md)
    
- [<span data-ttu-id="5fba4-140">Propriété canonique PidLidWorkAddressCountry</span><span class="sxs-lookup"><span data-stu-id="5fba4-140">PidLidWorkAddressCountry Canonical Property</span></span>](pidlidworkaddresscountry-canonical-property.md)
    
- [<span data-ttu-id="5fba4-141">Propriété canonique PidLidWorkAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="5fba4-141">PidLidWorkAddressPostalCode Canonical Property</span></span>](pidlidworkaddresspostalcode-canonical-property.md)
    
- [<span data-ttu-id="5fba4-142">Propriété canonique PidLidWorkAddressPostOfficeBox</span><span class="sxs-lookup"><span data-stu-id="5fba4-142">PidLidWorkAddressPostOfficeBox Canonical Property</span></span>](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [<span data-ttu-id="5fba4-143">Propriété canonique PidLidWorkAddressState</span><span class="sxs-lookup"><span data-stu-id="5fba4-143">PidLidWorkAddressState Canonical Property</span></span>](pidlidworkaddressstate-canonical-property.md)
    
- [<span data-ttu-id="5fba4-144">Propriété canonique PidLidWorkAddressStreet</span><span class="sxs-lookup"><span data-stu-id="5fba4-144">PidLidWorkAddressStreet Canonical Property</span></span>](pidlidworkaddressstreet-canonical-property.md)
    
- [<span data-ttu-id="5fba4-145">Propriété canonique PidLidYomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="5fba4-145">PidLidYomiCompanyName Canonical Property</span></span>](pidlidyomicompanyname-canonical-property.md)
    
- [<span data-ttu-id="5fba4-146">Propriété canonique PidLidYomiFirstName</span><span class="sxs-lookup"><span data-stu-id="5fba4-146">PidLidYomiFirstName Canonical Property</span></span>](pidlidyomifirstname-canonical-property.md)
    
- [<span data-ttu-id="5fba4-147">Propriété canonique PidLidYomiLastName</span><span class="sxs-lookup"><span data-stu-id="5fba4-147">PidLidYomiLastName Canonical Property</span></span>](pidlidyomilastname-canonical-property.md)
    
<span data-ttu-id="5fba4-148">Les propriétés nommées dans l’espace de noms **PSETID_Appointment** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5fba4-148">Named properties in the **PSETID_Appointment** namespace are the following:</span></span> 
  
- [<span data-ttu-id="5fba4-149">Propriété canonique PidLidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="5fba4-149">PidLidAllAttendeesString Canonical Property</span></span>](pidlidallattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="5fba4-150">Propriété canonique PidLidAppointmentCounterProposal</span><span class="sxs-lookup"><span data-stu-id="5fba4-150">PidLidAppointmentCounterProposal Canonical Property</span></span>](pidlidappointmentcounterproposal-canonical-property.md)
    
- [<span data-ttu-id="5fba4-151">Propriété canonique PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="5fba4-151">PidLidAppointmentDuration Canonical Property</span></span>](pidlidappointmentduration-canonical-property.md)
    
- [<span data-ttu-id="5fba4-152">Propriété canonique PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="5fba4-152">PidLidAppointmentEndWhole Canonical Property</span></span>](pidlidappointmentendwhole-canonical-property.md)
    
- [<span data-ttu-id="5fba4-153">Propriété canonique PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="5fba4-153">PidLidAppointmentStartWhole Canonical Property</span></span>](pidlidappointmentstartwhole-canonical-property.md)
    
- [<span data-ttu-id="5fba4-154">Propriété canonique PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="5fba4-154">PidLidBusyStatus Canonical Property</span></span>](pidlidbusystatus-canonical-property.md)
    
- [<span data-ttu-id="5fba4-155">Propriété canonique PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="5fba4-155">PidLidCcAttendeesString Canonical Property</span></span>](pidlidccattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="5fba4-156">Propriété canonique PidLidLocation</span><span class="sxs-lookup"><span data-stu-id="5fba4-156">PidLidLocation Canonical Property</span></span>](pidlidlocation-canonical-property.md)
    
- [<span data-ttu-id="5fba4-157">Propriété canonique PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="5fba4-157">PidLidRecurring Canonical Property</span></span>](pidlidrecurring-canonical-property.md)
    
- [<span data-ttu-id="5fba4-158">Propriété canonique PidLidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="5fba4-158">PidLidToAttendeesString Canonical Property</span></span>](pidlidtoattendeesstring-canonical-property.md)
    
<span data-ttu-id="5fba4-159">Les propriétés nommées dans l’espace de noms **PSETID_Common** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5fba4-159">Named properties in the **PSETID_Common** namespace are the following:</span></span> 
  
- [<span data-ttu-id="5fba4-160">Propriété canonique PidLidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="5fba4-160">PidLidCommonEnd Canonical Property</span></span>](pidlidcommonend-canonical-property.md)
    
- [<span data-ttu-id="5fba4-161">Propriété canonique PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="5fba4-161">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)
    
- [<span data-ttu-id="5fba4-162">Propriété canonique PidLidCompanies</span><span class="sxs-lookup"><span data-stu-id="5fba4-162">PidLidCompanies Canonical Property</span></span>](pidlidcompanies-canonical-property.md)
    
- [<span data-ttu-id="5fba4-163">Propriété canonique PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="5fba4-163">PidLidContacts Canonical Property</span></span>](pidlidcontacts-canonical-property.md)
    
- [<span data-ttu-id="5fba4-164">Propriété canonique PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="5fba4-164">PidLidCustomFlag Canonical Property</span></span>](pidlidcustomflag-canonical-property.md)
    
- [<span data-ttu-id="5fba4-165">Propriété canonique PidLidFormPropStream</span><span class="sxs-lookup"><span data-stu-id="5fba4-165">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="5fba4-166">Propriété canonique PidLidFormStorage</span><span class="sxs-lookup"><span data-stu-id="5fba4-166">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="5fba4-167">Propriété canonique PidLidHeaderItem</span><span class="sxs-lookup"><span data-stu-id="5fba4-167">PidLidHeaderItem Canonical Property</span></span>](pidlidheaderitem-canonical-property.md)
    
- [<span data-ttu-id="5fba4-168">Propriété canonique PidLidPageDirStream</span><span class="sxs-lookup"><span data-stu-id="5fba4-168">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="5fba4-169">Propriété canonique PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="5fba4-169">PidLidPropertyDefinitionStream Canonical Property</span></span>](pidlidpropertydefinitionstream-canonical-property.md)
    
- [<span data-ttu-id="5fba4-170">Propriété canonique PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="5fba4-170">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)
    
- [<span data-ttu-id="5fba4-171">Propriété canonique PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="5fba4-171">PidLidReminderTime Canonical Property</span></span>](pidlidremindertime-canonical-property.md)
    
- [<span data-ttu-id="5fba4-172">Propriété canonique PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="5fba4-172">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)
    
- [<span data-ttu-id="5fba4-173">Propriété canonique PidLidScriptStream</span><span class="sxs-lookup"><span data-stu-id="5fba4-173">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
- [<span data-ttu-id="5fba4-174">Propriété canonique PidLidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="5fba4-174">PidLidSmartNoAttach Canonical Property</span></span>](pidlidsmartnoattach-canonical-property.md)
    
- [<span data-ttu-id="5fba4-175">Propriété canonique PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="5fba4-175">PidLidToDoTitle Canonical Property</span></span>](pidlidtodotitle-canonical-property.md)
    
- [<span data-ttu-id="5fba4-176">Propriété canonique PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="5fba4-176">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)
    
<span data-ttu-id="5fba4-177">Les propriétés nommées dans l’espace de noms **PSETID_Meeting** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5fba4-177">Named properties in the **PSETID_Meeting** namespace are the following:</span></span> 
  
- [<span data-ttu-id="5fba4-178">Propriété canonique PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="5fba4-178">PidLidMeetingType Canonical Property</span></span>](pidlidmeetingtype-canonical-property.md)
    
<span data-ttu-id="5fba4-179">Les propriétés nommées dans l’espace de noms **PSETID_Task** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5fba4-179">Named properties in the **PSETID_Task** namespace are the following:</span></span> 
  
- [<span data-ttu-id="5fba4-180">Propriété canonique PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="5fba4-180">PidLidTaskActualEffort Canonical Property</span></span>](pidlidtaskactualeffort-canonical-property.md)
    
- [<span data-ttu-id="5fba4-181">Propriété canonique PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="5fba4-181">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
    
- [<span data-ttu-id="5fba4-182">Propriété canonique PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="5fba4-182">PidLidTaskEstimatedEffort Canonical Property</span></span>](pidlidtaskestimatedeffort-canonical-property.md)
    
- [<span data-ttu-id="5fba4-183">Propriété canonique PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="5fba4-183">PidLidTaskFRecurring Canonical Property</span></span>](pidlidtaskfrecurring-canonical-property.md)
    
- [<span data-ttu-id="5fba4-184">Propriété canonique PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="5fba4-184">PidLidTaskStartDate Canonical Property</span></span>](pidlidtaskstartdate-canonical-property.md)
    
- [<span data-ttu-id="5fba4-185">Propriété canonique PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="5fba4-185">PidLidTaskStatus Canonical Property</span></span>](pidlidtaskstatus-canonical-property.md)
    
<span data-ttu-id="5fba4-186">Les propriétés nommées dans l’espace de noms **PS_INTERNET_HEADERS** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5fba4-186">Named properties in the **PS_INTERNET_HEADERS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="5fba4-187">Propriété canonique PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="5fba4-187">PidTagInternetReturnPath Canonical Property</span></span>](pidtaginternetreturnpath-canonical-property.md)
    
<span data-ttu-id="5fba4-188">Les propriétés nommées dans l’espace de noms **PSETID_Log** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5fba4-188">Named properties in the **PSETID_Log** namespace are the following:</span></span> 
  
- [<span data-ttu-id="5fba4-189">Propriété canonique PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="5fba4-189">PidLidLogDuration Canonical Property</span></span>](pidlidlogduration-canonical-property.md)
    
- [<span data-ttu-id="5fba4-190">Propriété canonique PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="5fba4-190">PidLidLogEnd Canonical Property</span></span>](pidlidlogend-canonical-property.md)
    
- [<span data-ttu-id="5fba4-191">Propriété canonique PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="5fba4-191">PidLidLogStart Canonical Property</span></span>](pidlidlogstart-canonical-property.md)
    
- [<span data-ttu-id="5fba4-192">Propriété canonique PidLidLogType</span><span class="sxs-lookup"><span data-stu-id="5fba4-192">PidLidLogType Canonical Property</span></span>](pidlidlogtype-canonical-property.md)
    
<span data-ttu-id="5fba4-193">Les propriétés nommées dans l’espace de noms **PS_PUBLIC_STRINGS** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5fba4-193">Named properties in the **PS_PUBLIC_STRINGS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="5fba4-194">Propriété canonique PidNameKeywords</span><span class="sxs-lookup"><span data-stu-id="5fba4-194">PidNameKeywords Canonical Property</span></span>](pidnamekeywords-canonical-property.md)
    
- [<span data-ttu-id="5fba4-195">Propriété canonique PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="5fba4-195">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a><span data-ttu-id="5fba4-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fba4-196">See also</span></span>



[<span data-ttu-id="5fba4-197">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="5fba4-197">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="5fba4-198">Procédure pour déterminer si Outlook a uniquement téléchargé l’en-tête d’un message</span><span class="sxs-lookup"><span data-stu-id="5fba4-198">Determine if Outlook downloaded only the header of a message</span></span>](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[<span data-ttu-id="5fba4-199">Obtention de l’adresse e-mail d’un contact</span><span class="sxs-lookup"><span data-stu-id="5fba4-199">Get the email address of a Contact item</span></span>](how-to-get-the-email-address-of-a-contact-item.md)
  
[<span data-ttu-id="5fba4-200">Suppression de la définition de formulaire personnalisé enregistrée avec un message</span><span class="sxs-lookup"><span data-stu-id="5fba4-200">Remove custom form definition saved with a message</span></span>](how-to-remove-custom-form-definition-saved-with-a-message.md)

