---
title: IMailUser IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMailUser
api_type:
- COM
ms.assetid: 74c25870-62d9-484a-9a99-4dc35c52479e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a0e109fe95120483e700bab5b82f6d7cb75e2e28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436593"
---
# <a name="imailuser--imapiprop"></a>IMailUser : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder aux nombreuses propriétés associées aux utilisateurs de messagerie. **L’interface IMailUser est** implémentée par les objets utilisateur de messagerie. **IMailUser** hérite de l’interface [IMAPIProp : IUnknown](imapipropiunknown.md) et n’a aucune méthode unique propre. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets utilisateur de messagerie  <br/> |
|Implémenté par :  <br/> |Fournisseurs de carnets d’adresses  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMailUser  <br/> |
|Type de pointeur :  <br/> |LPMAILUSER  <br/> |
|Modèle de transaction :  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

Cette interface n’a pas de méthode unique.
  
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Cinq des propriétés requises sont appelées propriétés d’adresse de base pour les destinataires :
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
Ces propriétés sont considérées comme spéciales, car de nombreux autres groupes de propriétés similaires reposent sur ce groupe de base. Les autres groupes sont utilisés pour décrire un destinataire dans différents rôles, tels que l’expéditeur d’origine ou l’expéditeur délégué d’un message. Pour plus d’informations sur ces propriétés et leur utilisation, voir [Types d’adresses MAPI.](mapi-address-types.md)
  
Les utilisateurs de messagerie peuvent afficher une collection de leurs propriétés en PR_DETAILS_TABLE la propriété **(** [PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **PR_DETAILS_TABLE** est un tableau d’affichage qui décrit la disposition d’une boîte de dialogue détails ou d’une page de propriétés à onglets qui affiche les informations de propriété du destinataire. MAPI crée des boîtes de dialogue de détails lorsqu’un client appelle la méthode [IAddrBook::D etails.](iaddrbook-details.md) 
  
Les objets utilisateur de messagerie peuvent être associés à d’autres propriétés facultatives. MAPI définit de nombreuses propriétés qui fournissent des informations d’adressa ment supplémentaires sur un utilisateur de messagerie. Toutes ces propriétés sont des chaînes de caractères. La liste suivante présente les propriétés les plus couramment utilisées :
  
- **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) 
    
- **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)) 
    
- **PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md)) 
    
- **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) 
    
- **PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md)) 
    
- **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)) 
    
- **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) 
    
Pour obtenir la liste complète des propriétés, voir [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

