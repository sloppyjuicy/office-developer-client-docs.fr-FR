---
title: � propos des propri�t�s nomm�es utilis�es par Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 75a08db313ac1b38a400fb329eefa914858ec71e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782846"
---
# <a name="about-named-properties-used-by-outlook"></a><span data-ttu-id="ae302-103">� propos des propri�t�s nomm�es utilis�es par Outlook</span><span class="sxs-lookup"><span data-stu-id="ae302-103">About Named Properties Used by Outlook</span></span>

  
  
<span data-ttu-id="ae302-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ae302-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ae302-p101">MAPI fournit un proc�d� pour l'affectation des noms pour certaines propri�t�s, pour le mappage de ces noms � des identificateurs uniques et pour rendre ce nom-�-identificateur mappage persistent entre les sessions. Les propri�t�s nomm�es sont identifi�es par un nom et un identificateur global unique (GUID) d'un jeu de propri�t�s. Le nom peut �tre un nombre ou une cha�ne. Pour Microsoft�Outlook�2013 ou Microsoft�Outlook�2010, le jeu de propri�t�s est souvent un espace de noms d�fini par Outlook�2013 ou Outlook 2010, par exemple **PSETID_Appointment**.</span><span class="sxs-lookup"><span data-stu-id="ae302-p101">MAPI provides a facility for assigning names to certain properties, for mapping these names to unique identifiers, and for making this name-to-identifier mapping persistent across sessions. Named properties are identified by a name and a globally unique identifier (GUID) for a property set. The name can be a number or a string. For Microsoft Outlook 2013 or Microsoft Outlook 2010, the property set is often a namespace defined by Outlook 2013 or Outlook 2010, such as **PSETID_Appointment**.</span></span> 
  
<span data-ttu-id="ae302-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span><span class="sxs-lookup"><span data-stu-id="ae302-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span></span> 
  
<span data-ttu-id="ae302-p103">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook�2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span><span class="sxs-lookup"><span data-stu-id="ae302-p103">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span></span> 
  
<span data-ttu-id="ae302-p104">Outlook�2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook�2013 and Outlook 2010 expose some of these properties as item properties in their Outlook�2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [Propri�t� canonique PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook�2013 and Outlook 2010 are not exposed in the object model.</span><span class="sxs-lookup"><span data-stu-id="ae302-p104">Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model.</span></span> 
  
<span data-ttu-id="ae302-120">Cette r�f�rence d�crit certaines des propri�t�s nomm�es qui sont r�pertori�s ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ae302-120">This reference describes a number of named properties that are listed below.</span></span>
  
<span data-ttu-id="ae302-121">Les propri�t�s nomm�es dans l'espace de noms **PSETID_Address** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae302-121">Named properties in the **PSETID_Address** namespace are the following:</span></span> 
  
- [<span data-ttu-id="ae302-122">Propri�t� canonique PidLidEmail1AddressType</span><span class="sxs-lookup"><span data-stu-id="ae302-122">PidLidEmail1AddressType Canonical Property</span></span>](pidlidemail1addresstype-canonical-property.md)
    
- [<span data-ttu-id="ae302-123">Propri�t� canonique PidLidEmail1EmailAddress</span><span class="sxs-lookup"><span data-stu-id="ae302-123">PidLidEmail1EmailAddress Canonical Property</span></span>](pidlidemail1emailaddress-canonical-property.md)
    
- [<span data-ttu-id="ae302-124">Propri�t� canonique PidLidEmail1OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="ae302-124">PidLidEmail1OriginalEntryId Canonical Property</span></span>](pidlidemail1originalentryid-canonical-property.md)
    
- [<span data-ttu-id="ae302-125">Propri�t� canonique PidLidEmail2AddressType</span><span class="sxs-lookup"><span data-stu-id="ae302-125">PidLidEmail2AddressType Canonical Property</span></span>](pidlidemail2addresstype-canonical-property.md)
    
- [<span data-ttu-id="ae302-126">Propri�t� canonique PidLidEmail2DisplayName</span><span class="sxs-lookup"><span data-stu-id="ae302-126">PidLidEmail2DisplayName Canonical Property</span></span>](pidlidemail2displayname-canonical-property.md)
    
- [<span data-ttu-id="ae302-127">Propri�t� canonique PidLidEmail2EmailAddress</span><span class="sxs-lookup"><span data-stu-id="ae302-127">PidLidEmail2EmailAddress Canonical Property</span></span>](pidlidemail2emailaddress-canonical-property.md)
    
- [<span data-ttu-id="ae302-128">Propri�t� canonique PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="ae302-128">PidLidEmail2OriginalDisplayName Canonical Property</span></span>](pidlidemail2originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="ae302-129">Propri�t� canonique PidLidEmail2OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="ae302-129">PidLidEmail2OriginalEntryId Canonical Property</span></span>](pidlidemail2originalentryid-canonical-property.md)
    
- [<span data-ttu-id="ae302-130">Propri�t� canonique PidLidEmail3AddressType</span><span class="sxs-lookup"><span data-stu-id="ae302-130">PidLidEmail3AddressType Canonical Property</span></span>](pidlidemail3addresstype-canonical-property.md)
    
- [<span data-ttu-id="ae302-131">Propri�t� canonique PidLidEmail3DisplayName</span><span class="sxs-lookup"><span data-stu-id="ae302-131">PidLidEmail3DisplayName Canonical Property</span></span>](pidlidemail3displayname-canonical-property.md)
    
- [<span data-ttu-id="ae302-132">Propri�t� canonique PidLidEmail3EmailAddress</span><span class="sxs-lookup"><span data-stu-id="ae302-132">PidLidEmail3EmailAddress Canonical Property</span></span>](pidlidemail3emailaddress-canonical-property.md)
    
- [<span data-ttu-id="ae302-133">Propri�t� canonique PidLidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="ae302-133">PidLidEmail3OriginalDisplayName Canonical Property</span></span>](pidlidemail3originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="ae302-134">Propri�t� canonique PidLidEmail3OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="ae302-134">PidLidEmail3OriginalEntryId Canonical Property</span></span>](pidlidemail3originalentryid-canonical-property.md)
    
- [<span data-ttu-id="ae302-135">Propri�t� canonique PidLidEmail1DisplayName</span><span class="sxs-lookup"><span data-stu-id="ae302-135">PidLidEmail1DisplayName Canonical Property</span></span>](pidlidemail1displayname-canonical-property.md)
    
- [<span data-ttu-id="ae302-136">Propri�t� canonique PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="ae302-136">PidLidEmail1OriginalDisplayName Canonical Property</span></span>](pidlidemail1originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="ae302-137">Propri�t� canonique PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="ae302-137">PidLidFileUnder Canonical Property</span></span>](pidlidfileunder-canonical-property.md)
    
- [<span data-ttu-id="ae302-138">Propri�t� canonique PidLidInstantMessagingAddress</span><span class="sxs-lookup"><span data-stu-id="ae302-138">PidLidInstantMessagingAddress Canonical Property</span></span>](pidlidinstantmessagingaddress-canonical-property.md)
    
- [<span data-ttu-id="ae302-139">Propri�t� canonique PidLidWorkAddressCity</span><span class="sxs-lookup"><span data-stu-id="ae302-139">PidLidWorkAddressCity Canonical Property</span></span>](pidlidworkaddresscity-canonical-property.md)
    
- [<span data-ttu-id="ae302-140">Propri�t� canonique PidLidWorkAddressCountry</span><span class="sxs-lookup"><span data-stu-id="ae302-140">PidLidWorkAddressCountry Canonical Property</span></span>](pidlidworkaddresscountry-canonical-property.md)
    
- [<span data-ttu-id="ae302-141">Propri�t� canonique PidLidWorkAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="ae302-141">PidLidWorkAddressPostalCode Canonical Property</span></span>](pidlidworkaddresspostalcode-canonical-property.md)
    
- [<span data-ttu-id="ae302-142">Propri�t� canonique PidLidWorkAddressPostOfficeBox</span><span class="sxs-lookup"><span data-stu-id="ae302-142">PidLidWorkAddressPostOfficeBox Canonical Property</span></span>](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [<span data-ttu-id="ae302-143">Propri�t� canonique PidLidWorkAddressState</span><span class="sxs-lookup"><span data-stu-id="ae302-143">PidLidWorkAddressState Canonical Property</span></span>](pidlidworkaddressstate-canonical-property.md)
    
- [<span data-ttu-id="ae302-144">Propri�t� canonique PidLidWorkAddressStreet</span><span class="sxs-lookup"><span data-stu-id="ae302-144">PidLidWorkAddressStreet Canonical Property</span></span>](pidlidworkaddressstreet-canonical-property.md)
    
- [<span data-ttu-id="ae302-145">Propri�t� canonique PidLidYomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="ae302-145">PidLidYomiCompanyName Canonical Property</span></span>](pidlidyomicompanyname-canonical-property.md)
    
- [<span data-ttu-id="ae302-146">Propri�t� canonique PidLidYomiFirstName</span><span class="sxs-lookup"><span data-stu-id="ae302-146">PidLidYomiFirstName Canonical Property</span></span>](pidlidyomifirstname-canonical-property.md)
    
- [<span data-ttu-id="ae302-147">Propri�t� canonique PidLidYomiLastName</span><span class="sxs-lookup"><span data-stu-id="ae302-147">PidLidYomiLastName Canonical Property</span></span>](pidlidyomilastname-canonical-property.md)
    
<span data-ttu-id="ae302-148">Les propri�t�s nomm�es dans l'espace de noms **PSETID_Appointment** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae302-148">Named properties in the **PSETID_Appointment** namespace are the following:</span></span> 
  
- [<span data-ttu-id="ae302-149">Propri�t� canonique PidLidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="ae302-149">PidLidAllAttendeesString Canonical Property</span></span>](pidlidallattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="ae302-150">Propri�t� canonique PidLidAppointmentCounterProposal</span><span class="sxs-lookup"><span data-stu-id="ae302-150">PidLidAppointmentCounterProposal Canonical Property</span></span>](pidlidappointmentcounterproposal-canonical-property.md)
    
- [<span data-ttu-id="ae302-151">Propri�t� canonique PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="ae302-151">PidLidAppointmentDuration Canonical Property</span></span>](pidlidappointmentduration-canonical-property.md)
    
- [<span data-ttu-id="ae302-152">Propri�t� canonique PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="ae302-152">PidLidAppointmentEndWhole Canonical Property</span></span>](pidlidappointmentendwhole-canonical-property.md)
    
- [<span data-ttu-id="ae302-153">Propri�t� canonique PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="ae302-153">PidLidAppointmentStartWhole Canonical Property</span></span>](pidlidappointmentstartwhole-canonical-property.md)
    
- [<span data-ttu-id="ae302-154">Propri�t� canonique PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="ae302-154">PidLidBusyStatus Canonical Property</span></span>](pidlidbusystatus-canonical-property.md)
    
- [<span data-ttu-id="ae302-155">Propri�t� canonique PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="ae302-155">PidLidCcAttendeesString Canonical Property</span></span>](pidlidccattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="ae302-156">Propri�t� canonique PidLidLocation</span><span class="sxs-lookup"><span data-stu-id="ae302-156">PidLidLocation Canonical Property</span></span>](pidlidlocation-canonical-property.md)
    
- [<span data-ttu-id="ae302-157">Propri�t� canonique PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="ae302-157">PidLidRecurring Canonical Property</span></span>](pidlidrecurring-canonical-property.md)
    
- [<span data-ttu-id="ae302-158">Propri�t� canonique PidLidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="ae302-158">PidLidToAttendeesString Canonical Property</span></span>](pidlidtoattendeesstring-canonical-property.md)
    
<span data-ttu-id="ae302-159">Les propri�t�s nomm�es dans l'espace de noms **PSETID_Common** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae302-159">Named properties in the **PSETID_Common** namespace are the following:</span></span> 
  
- [<span data-ttu-id="ae302-160">Propri�t� canonique PidLidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="ae302-160">PidLidCommonEnd Canonical Property</span></span>](pidlidcommonend-canonical-property.md)
    
- [<span data-ttu-id="ae302-161">Propri�t� canonique PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="ae302-161">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)
    
- [<span data-ttu-id="ae302-162">Propri�t� canonique PidLidCompanies</span><span class="sxs-lookup"><span data-stu-id="ae302-162">PidLidCompanies Canonical Property</span></span>](pidlidcompanies-canonical-property.md)
    
- [<span data-ttu-id="ae302-163">Propri�t� canonique PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="ae302-163">PidLidContacts Canonical Property</span></span>](pidlidcontacts-canonical-property.md)
    
- [<span data-ttu-id="ae302-164">Propri�t� canonique PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="ae302-164">PidLidCustomFlag Canonical Property</span></span>](pidlidcustomflag-canonical-property.md)
    
- [<span data-ttu-id="ae302-165">Propri�t� canonique PidLidFormPropStream</span><span class="sxs-lookup"><span data-stu-id="ae302-165">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="ae302-166">Propri�t� canonique PidLidFormStorage</span><span class="sxs-lookup"><span data-stu-id="ae302-166">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="ae302-167">Propri�t� canonique PidLidHeaderItem</span><span class="sxs-lookup"><span data-stu-id="ae302-167">PidLidHeaderItem Canonical Property</span></span>](pidlidheaderitem-canonical-property.md)
    
- [<span data-ttu-id="ae302-168">Propri�t� canonique PidLidPageDirStream</span><span class="sxs-lookup"><span data-stu-id="ae302-168">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="ae302-169">Propri�t� canonique PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="ae302-169">PidLidPropertyDefinitionStream Canonical Property</span></span>](pidlidpropertydefinitionstream-canonical-property.md)
    
- [<span data-ttu-id="ae302-170">Propri�t� canonique PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="ae302-170">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)
    
- [<span data-ttu-id="ae302-171">Propri�t� canonique PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="ae302-171">PidLidReminderTime Canonical Property</span></span>](pidlidremindertime-canonical-property.md)
    
- [<span data-ttu-id="ae302-172">Propri�t� canonique PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="ae302-172">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)
    
- [<span data-ttu-id="ae302-173">Propri�t� canonique PidLidScriptStream</span><span class="sxs-lookup"><span data-stu-id="ae302-173">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
- [<span data-ttu-id="ae302-174">Propri�t� canonique PidLidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="ae302-174">PidLidSmartNoAttach Canonical Property</span></span>](pidlidsmartnoattach-canonical-property.md)
    
- [<span data-ttu-id="ae302-175">Propri�t� canonique PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="ae302-175">PidLidToDoTitle Canonical Property</span></span>](pidlidtodotitle-canonical-property.md)
    
- [<span data-ttu-id="ae302-176">Propri�t� canonique PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="ae302-176">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)
    
<span data-ttu-id="ae302-177">Les propri�t�s nomm�es dans l'espace de noms **PSETID_Meeting** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae302-177">Named properties in the **PSETID_Meeting** namespace are the following:</span></span> 
  
- [<span data-ttu-id="ae302-178">Propri�t� canonique PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="ae302-178">PidLidMeetingType Canonical Property</span></span>](pidlidmeetingtype-canonical-property.md)
    
<span data-ttu-id="ae302-179">Les propri�t�s nomm�es dans l'espace de noms **PSETID_Task** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae302-179">Named properties in the **PSETID_Task** namespace are the following:</span></span> 
  
- [<span data-ttu-id="ae302-180">Propri�t� canonique PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="ae302-180">PidLidTaskActualEffort Canonical Property</span></span>](pidlidtaskactualeffort-canonical-property.md)
    
- [<span data-ttu-id="ae302-181">Propri�t� canonique PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="ae302-181">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
    
- [<span data-ttu-id="ae302-182">Propri�t� canonique PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="ae302-182">PidLidTaskEstimatedEffort Canonical Property</span></span>](pidlidtaskestimatedeffort-canonical-property.md)
    
- [<span data-ttu-id="ae302-183">Propri�t� canonique PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="ae302-183">PidLidTaskFRecurring Canonical Property</span></span>](pidlidtaskfrecurring-canonical-property.md)
    
- [<span data-ttu-id="ae302-184">Propri�t� canonique PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="ae302-184">PidLidTaskStartDate Canonical Property</span></span>](pidlidtaskstartdate-canonical-property.md)
    
- [<span data-ttu-id="ae302-185">Propri�t� canonique PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="ae302-185">PidLidTaskStatus Canonical Property</span></span>](pidlidtaskstatus-canonical-property.md)
    
<span data-ttu-id="ae302-186">Les propri�t�s nomm�es dans l'espace de noms **PS_INTERNET_HEADERS** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae302-186">Named properties in the **PS_INTERNET_HEADERS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="ae302-187">Propri�t� canonique PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="ae302-187">PidTagInternetReturnPath Canonical Property</span></span>](pidtaginternetreturnpath-canonical-property.md)
    
<span data-ttu-id="ae302-188">Les propri�t�s nomm�es dans l'espace de noms **PSETID_Log** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae302-188">Named properties in the **PSETID_Log** namespace are the following:</span></span> 
  
- [<span data-ttu-id="ae302-189">Propri�t� canonique PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="ae302-189">PidLidLogDuration Canonical Property</span></span>](pidlidlogduration-canonical-property.md)
    
- [<span data-ttu-id="ae302-190">Propri�t� canonique PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="ae302-190">PidLidLogEnd Canonical Property</span></span>](pidlidlogend-canonical-property.md)
    
- [<span data-ttu-id="ae302-191">Propri�t� canonique PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="ae302-191">PidLidLogStart Canonical Property</span></span>](pidlidlogstart-canonical-property.md)
    
- [<span data-ttu-id="ae302-192">Propri�t� canonique PidLidLogType</span><span class="sxs-lookup"><span data-stu-id="ae302-192">PidLidLogType Canonical Property</span></span>](pidlidlogtype-canonical-property.md)
    
<span data-ttu-id="ae302-193">Les propri�t�s nomm�es dans l'espace de noms **PS_PUBLIC_STRINGS** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae302-193">Named properties in the **PS_PUBLIC_STRINGS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="ae302-194">Propri�t� canonique PidNameKeywords</span><span class="sxs-lookup"><span data-stu-id="ae302-194">PidNameKeywords Canonical Property</span></span>](pidnamekeywords-canonical-property.md)
    
- [<span data-ttu-id="ae302-195">Propri�t� canonique PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="ae302-195">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a><span data-ttu-id="ae302-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae302-196">See also</span></span>



[<span data-ttu-id="ae302-197">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ae302-197">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ae302-198">Déterminer si Outlook téléchargés uniquement l’en-tête d’un Message</span><span class="sxs-lookup"><span data-stu-id="ae302-198">Determine if Outlook Downloaded Only the Header of a Message</span></span>](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[<span data-ttu-id="ae302-199">Obtenir l’adresse de messagerie d’un élément de Contact</span><span class="sxs-lookup"><span data-stu-id="ae302-199">Get the Email Address of a Contact Item</span></span>](how-to-get-the-email-address-of-a-contact-item.md)
  
[<span data-ttu-id="ae302-200">Supprimer la définition du formulaire personnalisé enregistrée avec un Message</span><span class="sxs-lookup"><span data-stu-id="ae302-200">Remove Custom Form Definition Saved With a Message</span></span>](how-to-remove-custom-form-definition-saved-with-a-message.md)

