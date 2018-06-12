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
# <a name="about-named-properties-used-by-outlook"></a>� propos des propri�t�s nomm�es utilis�es par Outlook

  
  
**S’applique à**: Outlook 
  
MAPI fournit un proc�d� pour l'affectation des noms pour certaines propri�t�s, pour le mappage de ces noms � des identificateurs uniques et pour rendre ce nom-�-identificateur mappage persistent entre les sessions. Les propri�t�s nomm�es sont identifi�es par un nom et un identificateur global unique (GUID) d'un jeu de propri�t�s. Le nom peut �tre un nombre ou une cha�ne. Pour Microsoft�Outlook�2013 ou Microsoft�Outlook�2010, le jeu de propri�t�s est souvent un espace de noms d�fini par Outlook�2013 ou Outlook 2010, par exemple **PSETID_Appointment**. 
  
Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range. 
  
Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook�2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients. 
  
Outlook�2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook�2013 and Outlook 2010 expose some of these properties as item properties in their Outlook�2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [Propri�t� canonique PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook�2013 and Outlook 2010 are not exposed in the object model. 
  
Cette r�f�rence d�crit certaines des propri�t�s nomm�es qui sont r�pertori�s ci-dessous.
  
Les propri�t�s nomm�es dans l'espace de noms **PSETID_Address** sont les suivantes : 
  
- [Propri�t� canonique PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)
    
- [Propri�t� canonique PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)
    
- [Propri�t� canonique PidLidEmail1OriginalEntryId](pidlidemail1originalentryid-canonical-property.md)
    
- [Propri�t� canonique PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)
    
- [Propri�t� canonique PidLidEmail2DisplayName](pidlidemail2displayname-canonical-property.md)
    
- [Propri�t� canonique PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)
    
- [Propri�t� canonique PidLidEmail2OriginalDisplayName](pidlidemail2originaldisplayname-canonical-property.md)
    
- [Propri�t� canonique PidLidEmail2OriginalEntryId](pidlidemail2originalentryid-canonical-property.md)
    
- [Propri�t� canonique PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)
    
- [Propri�t� canonique PidLidEmail3DisplayName](pidlidemail3displayname-canonical-property.md)
    
- [Propri�t� canonique PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)
    
- [Propri�t� canonique PidLidEmail3OriginalDisplayName](pidlidemail3originaldisplayname-canonical-property.md)
    
- [Propri�t� canonique PidLidEmail3OriginalEntryId](pidlidemail3originalentryid-canonical-property.md)
    
- [Propri�t� canonique PidLidEmail1DisplayName](pidlidemail1displayname-canonical-property.md)
    
- [Propri�t� canonique PidLidEmail1OriginalDisplayName](pidlidemail1originaldisplayname-canonical-property.md)
    
- [Propri�t� canonique PidLidFileUnder](pidlidfileunder-canonical-property.md)
    
- [Propri�t� canonique PidLidInstantMessagingAddress](pidlidinstantmessagingaddress-canonical-property.md)
    
- [Propri�t� canonique PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)
    
- [Propri�t� canonique PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md)
    
- [Propri�t� canonique PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md)
    
- [Propri�t� canonique PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [Propri�t� canonique PidLidWorkAddressState](pidlidworkaddressstate-canonical-property.md)
    
- [Propri�t� canonique PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)
    
- [Propri�t� canonique PidLidYomiCompanyName](pidlidyomicompanyname-canonical-property.md)
    
- [Propri�t� canonique PidLidYomiFirstName](pidlidyomifirstname-canonical-property.md)
    
- [Propri�t� canonique PidLidYomiLastName](pidlidyomilastname-canonical-property.md)
    
Les propri�t�s nomm�es dans l'espace de noms **PSETID_Appointment** sont les suivantes : 
  
- [Propri�t� canonique PidLidAllAttendeesString](pidlidallattendeesstring-canonical-property.md)
    
- [Propri�t� canonique PidLidAppointmentCounterProposal](pidlidappointmentcounterproposal-canonical-property.md)
    
- [Propri�t� canonique PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)
    
- [Propri�t� canonique PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)
    
- [Propri�t� canonique PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)
    
- [Propri�t� canonique PidLidBusyStatus](pidlidbusystatus-canonical-property.md)
    
- [Propri�t� canonique PidLidCcAttendeesString](pidlidccattendeesstring-canonical-property.md)
    
- [Propri�t� canonique PidLidLocation](pidlidlocation-canonical-property.md)
    
- [Propri�t� canonique PidLidRecurring](pidlidrecurring-canonical-property.md)
    
- [Propri�t� canonique PidLidToAttendeesString](pidlidtoattendeesstring-canonical-property.md)
    
Les propri�t�s nomm�es dans l'espace de noms **PSETID_Common** sont les suivantes : 
  
- [Propri�t� canonique PidLidCommonEnd](pidlidcommonend-canonical-property.md)
    
- [Propri�t� canonique PidLidCommonStart](pidlidcommonstart-canonical-property.md)
    
- [Propri�t� canonique PidLidCompanies](pidlidcompanies-canonical-property.md)
    
- [Propri�t� canonique PidLidContacts](pidlidcontacts-canonical-property.md)
    
- [Propri�t� canonique PidLidCustomFlag](pidlidcustomflag-canonical-property.md)
    
- [Propri�t� canonique PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [Propri�t� canonique PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [Propri�t� canonique PidLidHeaderItem](pidlidheaderitem-canonical-property.md)
    
- [Propri�t� canonique PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [Propri�t� canonique PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)
    
- [Propri�t� canonique PidLidReminderSet](pidlidreminderset-canonical-property.md)
    
- [Propri�t� canonique PidLidReminderTime](pidlidremindertime-canonical-property.md)
    
- [Propri�t� canonique PidLidFlagRequest](pidlidflagrequest-canonical-property.md)
    
- [Propri�t� canonique PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
- [Propri�t� canonique PidLidSmartNoAttach](pidlidsmartnoattach-canonical-property.md)
    
- [Propri�t� canonique PidLidToDoTitle](pidlidtodotitle-canonical-property.md)
    
- [Propri�t� canonique PidLidUseTnef](pidlidusetnef-canonical-property.md)
    
Les propri�t�s nomm�es dans l'espace de noms **PSETID_Meeting** sont les suivantes : 
  
- [Propri�t� canonique PidLidMeetingType](pidlidmeetingtype-canonical-property.md)
    
Les propri�t�s nomm�es dans l'espace de noms **PSETID_Task** sont les suivantes : 
  
- [Propri�t� canonique PidLidTaskActualEffort](pidlidtaskactualeffort-canonical-property.md)
    
- [Propri�t� canonique PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)
    
- [Propri�t� canonique PidLidTaskEstimatedEffort](pidlidtaskestimatedeffort-canonical-property.md)
    
- [Propri�t� canonique PidLidTaskFRecurring](pidlidtaskfrecurring-canonical-property.md)
    
- [Propri�t� canonique PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)
    
- [Propri�t� canonique PidLidTaskStatus](pidlidtaskstatus-canonical-property.md)
    
Les propri�t�s nomm�es dans l'espace de noms **PS_INTERNET_HEADERS** sont les suivantes : 
  
- [Propri�t� canonique PidTagInternetReturnPath](pidtaginternetreturnpath-canonical-property.md)
    
Les propri�t�s nomm�es dans l'espace de noms **PSETID_Log** sont les suivantes : 
  
- [Propri�t� canonique PidLidLogDuration](pidlidlogduration-canonical-property.md)
    
- [Propri�t� canonique PidLidLogEnd](pidlidlogend-canonical-property.md)
    
- [Propri�t� canonique PidLidLogStart](pidlidlogstart-canonical-property.md)
    
- [Propri�t� canonique PidLidLogType](pidlidlogtype-canonical-property.md)
    
Les propri�t�s nomm�es dans l'espace de noms **PS_PUBLIC_STRINGS** sont les suivantes : 
  
- [Propri�t� canonique PidNameKeywords](pidnamekeywords-canonical-property.md)
    
- [Propri�t� canonique PidNameExchangeJunkEmailMoveStamp](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a>Voir aussi



[Constantes MAPI](mapi-constants.md)
  
[Déterminer si Outlook téléchargés uniquement l’en-tête d’un Message](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[Obtenir l’adresse de messagerie d’un élément de Contact](how-to-get-the-email-address-of-a-contact-item.md)
  
[Supprimer la définition du formulaire personnalisé enregistrée avec un Message](how-to-remove-custom-form-definition-saved-with-a-message.md)

