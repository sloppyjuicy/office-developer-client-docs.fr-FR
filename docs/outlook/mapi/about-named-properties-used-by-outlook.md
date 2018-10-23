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
# <a name="about-named-properties-used-by-outlook"></a>À propos des propriétés nommées utilisées par Outlook

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’interface MAPI (Messaging Application Programming Interface) intègre une fonctionnalité permettant d’affecter des noms à certaines propriétés pour le mappage de ces noms avec des identificateurs uniques et de rendre ce mappage nom-identificateur permanent dans l’ensemble des sessions. Les propriétés nommées sont identifiées par un nom et un identificateur global unique (GUID) pour un jeu de propriétés. Le nom peut être un nombre ou une chaîne. Pour Microsoft Outlook 2013 ou Microsoft Outlook 2010, le jeu de propriétés est souvent un espace de noms défini par Outlook 2013 ou Outlook 2010, tel que **PSETID_Appointment**. 
  
Les propriétés nommées sont manipulées à l’aide des fonctions [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). Le nom et le GUID du jeu de propriétés sont transmis à la fonction [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir un identificateur de propriété valide pour la session MAPI en cours. Dans la mesure où cet identificateur de propriété peut varier d’un ordinateur à un autre, la seule manière cohérente d’accéder à une propriété nommée est de connaître son nom et son GUID de jeu de propriétés. La plage des identificateurs est toujours comprise dans la plage 0x8000 et 0xFFFE. 
  
Tout objet qui implémente l’interface [IMAPIProp : IUnknown](imapipropiunknown.md) peut prendre en charge des propriétés nommées. Plus précisément, un fournisseur de services MAPI ou un client MAPI doit implémenter [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir des valeurs de propriétés nommées. La définition de propriétés nommées utilisées par Outlook 2013 ou Outlook 2010 n’est pas prise en charge en raison du risque d’endommagement des données partagées avec d’autres clients ou fournisseurs MAPI. 
  
Outlook 2013 et Outlook 2010 utilisent des propriétés nommées MAPI pour implémenter bon nombre de leurs fonctionnalités comme la sécurité des pièces jointes et les contre-propositions de réunion. Par-dessus ces données sous-jacentes, Outlook 2013 et Outlook 2010 exposent certaines de ces propriétés en tant que propriétés d’élément dans leurs modèles objet Outlook 2010 et Outlook 2013. Par exemple, la propriété **Email1Address** de l’objet **ContactItem** dans le modèle objet correspond à la [propriété canonique PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) nommée dans l’espace de noms **PSETID_Address**. Toutefois, en général, en raison de problèmes de compatibilité et d’intégrité des données, de nombreuses propriétés MAPI utilisées par Outlook 2013 et Outlook 2010 ne sont pas exposées dans le modèle objet. 
  
Cette référence décrit un nombre de propriétés nommées répertoriées ci-dessous.
  
Les propriétés nommées dans l’espace de noms **PSETID_Address** sont les suivantes : 
  
- [Propriété canonique PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)
    
- [Propriété canonique PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)
    
- [Propriété canonique PidLidEmail1OriginalEntryId](pidlidemail1originalentryid-canonical-property.md)
    
- [Propriété canonique PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)
    
- [Propriété canonique PidLidEmail2DisplayName](pidlidemail2displayname-canonical-property.md)
    
- [Propriété canonique PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)
    
- [Propriété canonique PidLidEmail2OriginalDisplayName](pidlidemail2originaldisplayname-canonical-property.md)
    
- [Propriété canonique PidLidEmail2OriginalEntryId](pidlidemail2originalentryid-canonical-property.md)
    
- [Propriété canonique PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)
    
- [Propriété canonique PidLidEmail3DisplayName](pidlidemail3displayname-canonical-property.md)
    
- [Propriété canonique PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)
    
- [Propriété canonique PidLidEmail3OriginalDisplayName](pidlidemail3originaldisplayname-canonical-property.md)
    
- [Propriété canonique PidLidEmail3OriginalEntryId](pidlidemail3originalentryid-canonical-property.md)
    
- [Propriété canonique PidLidEmail1DisplayName](pidlidemail1displayname-canonical-property.md)
    
- [Propriété canonique PidLidEmail1OriginalDisplayName](pidlidemail1originaldisplayname-canonical-property.md)
    
- [Propriété canonique PidLidFileUnder](pidlidfileunder-canonical-property.md)
    
- [Propriété canonique PidLidInstantMessagingAddress](pidlidinstantmessagingaddress-canonical-property.md)
    
- [Propriété canonique PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)
    
- [Propriété canonique PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md)
    
- [Propriété canonique PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md)
    
- [Propriété canonique PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [Propriété canonique PidLidWorkAddressState](pidlidworkaddressstate-canonical-property.md)
    
- [Propriété canonique PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)
    
- [Propriété canonique PidLidYomiCompanyName](pidlidyomicompanyname-canonical-property.md)
    
- [Propriété canonique PidLidYomiFirstName](pidlidyomifirstname-canonical-property.md)
    
- [Propriété canonique PidLidYomiLastName](pidlidyomilastname-canonical-property.md)
    
Les propriétés nommées dans l’espace de noms **PSETID_Appointment** sont les suivantes : 
  
- [Propriété canonique PidLidAllAttendeesString](pidlidallattendeesstring-canonical-property.md)
    
- [Propriété canonique PidLidAppointmentCounterProposal](pidlidappointmentcounterproposal-canonical-property.md)
    
- [Propriété canonique PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)
    
- [Propriété canonique PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)
    
- [Propriété canonique PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)
    
- [Propriété canonique PidLidBusyStatus](pidlidbusystatus-canonical-property.md)
    
- [Propriété canonique PidLidCcAttendeesString](pidlidccattendeesstring-canonical-property.md)
    
- [Propriété canonique PidLidLocation](pidlidlocation-canonical-property.md)
    
- [Propriété canonique PidLidRecurring](pidlidrecurring-canonical-property.md)
    
- [Propriété canonique PidLidToAttendeesString](pidlidtoattendeesstring-canonical-property.md)
    
Les propriétés nommées dans l’espace de noms **PSETID_Common** sont les suivantes : 
  
- [Propriété canonique PidLidCommonEnd](pidlidcommonend-canonical-property.md)
    
- [Propriété canonique PidLidCommonStart](pidlidcommonstart-canonical-property.md)
    
- [Propriété canonique PidLidCompanies](pidlidcompanies-canonical-property.md)
    
- [Propriété canonique PidLidContacts](pidlidcontacts-canonical-property.md)
    
- [Propriété canonique PidLidCustomFlag](pidlidcustomflag-canonical-property.md)
    
- [Propriété canonique PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [Propriété canonique PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [Propriété canonique PidLidHeaderItem](pidlidheaderitem-canonical-property.md)
    
- [Propriété canonique PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [Propriété canonique PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)
    
- [Propriété canonique PidLidReminderSet](pidlidreminderset-canonical-property.md)
    
- [Propriété canonique PidLidReminderTime](pidlidremindertime-canonical-property.md)
    
- [Propriété canonique PidLidFlagRequest](pidlidflagrequest-canonical-property.md)
    
- [Propriété canonique PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
- [Propriété canonique PidLidSmartNoAttach](pidlidsmartnoattach-canonical-property.md)
    
- [Propriété canonique PidLidToDoTitle](pidlidtodotitle-canonical-property.md)
    
- [Propriété canonique PidLidUseTnef](pidlidusetnef-canonical-property.md)
    
Les propriétés nommées dans l’espace de noms **PSETID_Meeting** sont les suivantes : 
  
- [Propriété canonique PidLidMeetingType](pidlidmeetingtype-canonical-property.md)
    
Les propriétés nommées dans l’espace de noms **PSETID_Task** sont les suivantes : 
  
- [Propriété canonique PidLidTaskActualEffort](pidlidtaskactualeffort-canonical-property.md)
    
- [Propriété canonique PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)
    
- [Propriété canonique PidLidTaskEstimatedEffort](pidlidtaskestimatedeffort-canonical-property.md)
    
- [Propriété canonique PidLidTaskFRecurring](pidlidtaskfrecurring-canonical-property.md)
    
- [Propriété canonique PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)
    
- [Propriété canonique PidLidTaskStatus](pidlidtaskstatus-canonical-property.md)
    
Les propriétés nommées dans l’espace de noms **PS_INTERNET_HEADERS** sont les suivantes : 
  
- [Propriété canonique PidTagInternetReturnPath](pidtaginternetreturnpath-canonical-property.md)
    
Les propriétés nommées dans l’espace de noms **PSETID_Log** sont les suivantes : 
  
- [Propriété canonique PidLidLogDuration](pidlidlogduration-canonical-property.md)
    
- [Propriété canonique PidLidLogEnd](pidlidlogend-canonical-property.md)
    
- [Propriété canonique PidLidLogStart](pidlidlogstart-canonical-property.md)
    
- [Propriété canonique PidLidLogType](pidlidlogtype-canonical-property.md)
    
Les propriétés nommées dans l’espace de noms **PS_PUBLIC_STRINGS** sont les suivantes : 
  
- [Propriété canonique PidNameKeywords](pidnamekeywords-canonical-property.md)
    
- [Propriété canonique PidNameExchangeJunkEmailMoveStamp](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a>Voir aussi



[Constantes MAPI](mapi-constants.md)
  
[Procédure pour déterminer si Outlook a uniquement téléchargé l’en-tête d’un message](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[Obtention de l’adresse e-mail d’un contact](how-to-get-the-email-address-of-a-contact-item.md)
  
[Suppression de la définition de formulaire personnalisé enregistrée avec un message](how-to-remove-custom-form-definition-saved-with-a-message.md)

