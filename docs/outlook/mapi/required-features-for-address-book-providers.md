---
title: Fonctionnalités requises pour les fournisseurs de carnets d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e2ccddd7-65e8-41f6-8e21-a4ae98190a96
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6aec3720bae9dbc6a0b1e8edf01ae42fa725595b
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62781183"
---
# <a name="required-features-for-address-book-providers"></a>Fonctionnalités requises pour les fournisseurs de carnets d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de carnets d’adresses peuvent utiliser des informations de destinataire temporaires ou permanentes, locales ou distantes, compréhensibles par un ou plusieurs systèmes de messagerie et formatées pour un fichier disque ou une table de base de données. Un fournisseur de carnet d’adresses peut implémenter diverses fonctionnalités, ce qui ajoute de la valeur et améliore l’interopérabilité avec les clients et d’autres fournisseurs. Toutefois, quelques fonctionnalités sont requises.
  
Le tableau suivant décrit les fonctionnalités requises pour tous les fournisseurs de carnets d’adresses et les étapes à suivre pour les implémenter.
  
|**Fonctionnalité**|**Modalités de mise en œuvre**|
|:-----|:-----|
|Ouverture de session  <br/> | Implémenter une fonction de point d’entrée. Pour plus d’informations, voir [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).  [Implémenter la méthode IABProvider::Logon](iabprovider-logon.md). Pour plus d’informations, voir [Implementing Address Book Provider Logon and Logoff](implementing-address-book-provider-logon-and-logoff.md). |
|Ouverture de session  <br/> |[Implémenter la méthode IABProvider::Shutdown](iabprovider-shutdown.md). Pour plus d’informations, voir [Implementing Address Book Provider Logon and Logoff](implementing-address-book-provider-logon-and-logoff.md). |
|Créer des identificateurs d’entrée  <br/> |Assurer la prise en **charge PR_ENTRYID** propriété ([PidTagEntryId](pidtagentryid-canonical-property.md)). Pour plus d’informations, voir [Identificateurs d’entrée MAPI](mapi-entry-identifiers.md) et [identificateurs de carnet d’adresses](address-book-identifiers.md). |
|Contribuer au tableau d’état  <br/> | Implémenter les méthodes appropriées de l’interface [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) . Pour plus d’informations, voir [Status Object Implementation](status-object-implementation.md).  Prise en charge des propriétés de table d’état requises. Pour plus d’informations, voir [Tableaux d’état](status-tables.md).  [Appelez IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md). |
|Fournir une prise en charge limitée des objets d’état  <br/> | [Implémentez la méthode IMAPIStatus::ValidateState](imapistatus-validatestate.md).  Renvoyer MAPI_E_NO_SUPPORT des autres **méthodes IMAPIStatus** . |
|Prise en charge de la configuration interactive et par programme  <br/> | Implémenter une fonction de point d’entrée de service de message.  Implémenter un tableau d’affichage. Pour plus d’informations, voir [Tableaux d’affichage](display-tables.md) et [Implémentation de tableaux d’affichage](display-table-implementation.md).  Implémentez une feuille de propriétés ou appelez la [méthode IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) . Pour plus d’informations, voir [Implémentation de la feuille de propriétés](property-sheet-implementation.md). |
   
En outre, si votre fournisseur prend en charge la création de destinataires, vous devez fournir une liste de modèles de création. Fournissez cette liste en implémentant la méthode [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) pour inclure tous les modèles pris en charge par votre fournisseur et la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de chaque conteneur pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) et inclure tous les modèles pris en charge par le conteneur. Pour plus d’informations, voir [Implementing One-Off Tables](implementing-one-off-tables.md).
  

