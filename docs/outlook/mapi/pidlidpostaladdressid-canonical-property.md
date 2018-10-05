---
title: Propriété canonique PidLidPostalAddressId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPostalAddressId
api_type:
- COM
ms.assetid: 30fdfb20-1e12-442a-bfa0-8c18c15fa5c3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 83f3c0559a3317de3789f8c93d024f08ada3e735
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399024"
---
# <a name="pidlidpostaladdressid-canonical-property"></a>Propriété canonique PidLidPostalAddressId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie l’adresse physique adresse postale du contact.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidPostalAddressId  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID de type long (capot) :  <br/> |0x00008022  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

Le cas échéant, cette propriété doit avoir une des valeurs qui sont spécifiés dans le tableau ci-dessous ou dans [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx). Si ce n’est pas définie, l’application doit supposer que la valeur est « 0 x 00000000 ».
  
|**Valeur**|**Description**|
|:-----|:-----|
|0x00000000  <br/> |Aucune adresse n’est sélectionné comme adresse postale. **PR_STREET_ADDRESS** ([PidTagStreetAddress](pidtagstreetaddress-canonical-property.md)), **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)), **PR_STATE_OR_PROVINCE** ([PidTagStateOrProvince](pidtagstateorprovince-canonical-property.md)), **PR_POSTAL_CODE** ([PidTagPostalCode](pidtagpostalcode-canonical-property.md)), **PR_COUNTRY** ([ PidTagCountry](pidtagcountry-canonical-property.md)), **dispidAddressCountryCode** ([PidLidAddressCountryCode](pidlidaddresscountrycode-canonical-property.md)) et **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) tous ne doivent pas être définie.  <br/> |
|0x00000001  <br/> |L’adresse personnelle est l’adresse postale. Les valeurs de **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX** ([PidTagPostOfficeBox](pidtagpostofficebox-canonical-property.md)), **PR_COUNTRY**, **dispidAddressCountryCode **, et les propriétés **PR_POSTAL_ADDRESS** doivent être égales aux valeurs de la **PR_HOME_ADDRESS_STREET** ([PidTagHomeAddressStreet](pidtaghomeaddressstreet-canonical-property.md)), **PR_HOME_ADDRESS_CITY** ([PidTagHomeAddressCity](pidtaghomeaddresscity-canonical-property.md)), **PR_HOME_ ADDRESS_STATE_OR_PROVINCE** ([PidTagHomeAddressStateOrProvince](pidtaghomeaddressstateorprovince-canonical-property.md)), **PR_HOME_ADDRESS_POSTAL_CODE** ([PidTagHomeAddressPostalCode](pidtaghomeaddresspostalcode-canonical-property.md)), **PR_HOME_ADDRESS_POST_OFFICE_BOX** ([ PidTagHomeAddressPostOfficeBox](pidtaghomeaddresspostofficebox-canonical-property.md)), **PR_HOME_ADDRESS_COUNTRY** ([PidTagHomeAddressCountry](pidtaghomeaddresscountry-canonical-property.md)), **dispidHomeAddressCountryCode** ([PidLidHomeAddressCountryCode](pidlidhomeaddresscountrycode-canonical-property.md)) et **dispidHomeAddress** () [PidLidHomeAddress](pidlidhomeaddress-canonical-property.md)) propriétés, respectivement.  <br/> |
|0x00000002  <br/> |L’adresse professionnelle est l’adresse postale. Les valeurs de **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX**, **PR_COUNTRY**, **dispidAddressCountryCode**et **PR_POSTAL_ADDRESS **propriétés doivent être égales aux valeurs de la **dispidWorkAddressStreet** ([PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)), **dispidWorkAddressCity** ([PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)), **dispidWorkAddressState** ([ PidLidWorkAddressState](pidlidworkaddressstate-canonical-property.md)), **dispidWorkAddressPostalCode** ([PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md)), **dispidWorkAddressPostOfficeBox** ([PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md)), **dispidWorkAddressCountry **([PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md)), **dispidWorkAddressCountryCode** ([PidLidWorkAddressCountryCode](pidlidworkaddresscountrycode-canonical-property.md)) et les propriétés **dispidWorkAddress** ([PidLidWorkAddress](pidlidworkaddress-canonical-property.md)), respectivement.  <br/> |
|0 x 00000003  <br/> |L’autre adresse est l’adresse postale. Les valeurs de la barre d’outils, **PR_STREET_ADDRESS**, **PR_LOCALITY** **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX**, **PR_COUNTRY**, **dispidAddressCountryCode**et **PR_POSTAL_ADDRESS **propriétés doivent être égales aux valeurs de la **PR_OTHER_ADDRESS_STREET** ([PidTagOtherAddressStreet](pidtagotheraddressstreet-canonical-property.md)), **PR_OTHER_ADDRESS_CITY** ([PidTagOtherAddressCity](pidtagotheraddresscity-canonical-property.md)), **PR_OTHER_ADDRESS_STATE_OR_PROVINCE** () [PidTagOtherAddressStateOrProvince](pidtagotheraddressstateorprovince-canonical-property.md)), **PR_OTHER_ADDRESS_POSTAL_CODE** ([PidTagOtherAddressPostalCode](pidtagotheraddresspostalcode-canonical-property.md)), **PR_OTHER_ADDRESS_POST_OFFICE_BOX** ([PidTagOtherAddressPostOfficeBox](pidtagotheraddresspostofficebox-canonical-property.md)), ** dispidOtherAddressCountryCode** ([PidLidOtherAddressCountryCode](pidlidotheraddresscountrycode-canonical-property.md)) et les propriétés **dispidOtherAddress** ([PidLidOtherAddress](pidlidotheraddress-canonical-property.md)), respectivement.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

