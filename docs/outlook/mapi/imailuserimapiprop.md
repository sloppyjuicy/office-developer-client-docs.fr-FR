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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7a6971504ec8f4f5ac8593b6b78777a12ff92b3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564562"
---
# <a name="imailuser--imapiprop"></a>IMailUser : IMAPIProp

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Permet d’accéder aux nombreuses propriétés qui sont associés à des utilisateurs de messagerie. L’interface **IMailUser** est implémentée par les objets utilisateur de messagerie. **IMailUser** hérite de la [IMAPIProp : IUnknown](imapipropiunknown.md) interface et n’a aucune méthode unique qui lui est propre. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposés par :  <br/> |Objets utilisateur de messagerie  <br/> |
|Implémentée par :  <br/> |Fournisseurs de carnet d’adresses  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMailUser  <br/> |
|Type de pointeur :  <br/> |LPMAILUSER  <br/> |
|Modèle de transaction :  <br/> |Traitées  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

Cette interface n’a pas de méthodes uniques.
  
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**Clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Cinq propriétés requises sont appelées les propriétés d’adresse de base pour les destinataires :
  
- **TYPEADR_PR**
    
- **PR_DISPLAY_NAME**
    
- **ADRESSE_EMAIL_PR**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
Ces propriétés sont considérés comme spéciale car de nombreux autres groupes de propriétés similaires sont créées d’après ce groupe de base. Les autres groupes sont utilisés pour décrire un destinataire dans différents rôles, comme un message s d’origine ou déléguer l’expéditeur. Pour plus d’informations sur ces propriétés et comment les utiliser, voir [Types d’adresses MAPI](mapi-address-types.md).
  
Les utilisateurs de messagerie peut afficher une collection de leurs propriétés en prenant en charge la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **PR_DETAILS_TABLE** est une table d’affichage qui décrit la disposition d’une boîte de dialogue Détails ou une page de propriétés à onglets qui affiche des informations sur les propriétés de destinataire. MAPI crée les boîtes de dialogue Détails lorsqu’un client appelle la méthode [IAddrBook::Details](iaddrbook-details.md) . 
  
Objets d’utilisateur de messagerie peuvent avoir les propriétés facultatives associées. MAPI définit de nombreuses propriétés qui fournissent des informations d’adressage supplémentaires à propos d’un utilisateur de messagerie. Toutes ces propriétés sont des chaînes de caractères. La liste suivante affiche les propriétés les plus couramment utilisées :
  
- **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) 
    
- **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)) 
    
- **PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md)) 
    
- **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) 
    
- **PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md)) 
    
- **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)) 
    
- **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) 
    
Pour obtenir une liste complète des propriétés, voir [Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

