---
title: Fonctionnalités requises pour les fournisseurs de carnets d’adresses
description: Décrit les fonctionnalités requises de tous les fournisseurs de carnets d’adresses et les étapes à suivre pour les implémenter.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e2ccddd7-65e8-41f6-8e21-a4ae98190a96
ms.openlocfilehash: f418e08d88bd2914e11aeacd5fe72107d68db1af
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752420"
---
# <a name="required-features-for-address-book-providers"></a>Fonctionnalités requises pour les fournisseurs de carnets d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de carnets d’adresses peuvent utiliser des informations de destinataire temporaires ou permanentes, locales ou distantes, compréhensibles par un ou plusieurs systèmes de messagerie et mises en forme pour un fichier disque ou une table de base de données. Il existe diverses fonctionnalités qu’un fournisseur de carnets d’adresses peut implémenter, ce qui ajoute de la valeur et améliore l’interopérabilité avec les clients et d’autres fournisseurs. Toutefois, quelques fonctionnalités sont requises.
  
Le tableau suivant décrit les fonctionnalités requises de tous les fournisseurs de carnets d’adresses et les étapes à suivre pour les implémenter.
  
|**Fonctionnalité**|**Modalités de mise en œuvre**|
|:-----|:-----|
|Ouverture de session  <br/> | Implémentez une fonction de point d’entrée. Pour plus d’informations, consultez [Implémentation d’une fonction de point d’entrée du fournisseur de carnet d’adresses](implementing-an-address-book-provider-entry-point-function.md).  Implémentez la méthode [IABProvider::Logon](iabprovider-logon.md) . Pour plus d’informations, consultez [Implémentation de l’ouverture de session et de la fermeture de session du fournisseur de carnets d’adresses](implementing-address-book-provider-logon-and-logoff.md). |
|Fermeture de session  <br/> |Implémentez la méthode [IABProvider::Shutdown](iabprovider-shutdown.md) . Pour plus d’informations, consultez [Implémentation de l’ouverture de session et de la fermeture de session du fournisseur de carnets d’adresses](implementing-address-book-provider-logon-and-logoff.md). |
|Créer des identificateurs d’entrée  <br/> |Prenez en charge la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Pour plus d’informations, consultez [Identificateurs d’entrée MAPI](mapi-entry-identifiers.md) et [Identificateurs de carnet d’adresses](address-book-identifiers.md). |
|Contribuer à la table d’état  <br/> | Implémentez les méthodes appropriées de l’interface [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) . Pour plus d’informations, consultez [l’implémentation de l’objet Status](status-object-implementation.md).  Prenez en charge les propriétés de table d’état requises. Pour plus d’informations, consultez [Tables d’état](status-tables.md).  Appelez [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md). |
|Fournir une prise en charge limitée des objets d’état  <br/> | Implémentez la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .  Retournez MAPI_E_NO_SUPPORT à partir des autres méthodes **IMAPIStatus** . |
|Prise en charge de la configuration interactive et par programmation  <br/> | Implémentez une fonction de point d’entrée de service de message.  Implémentez une table d’affichage. Pour plus d’informations, consultez [Tables d’affichage](display-tables.md) et [Implémentation de table d’affichage](display-table-implementation.md).  Implémentez une feuille de propriétés ou appelez la méthode [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) . Pour plus d’informations, consultez [Implémentation de la feuille de propriétés](property-sheet-implementation.md). |
   
En outre, si votre fournisseur prend en charge la création de destinataires, vous devez fournir une liste de modèles de création. Fournissez cette liste en implémentant la méthode [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) pour inclure tous les modèles pris en charge par votre fournisseur et la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de chaque conteneur pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) et inclure tous les modèles pris en charge par le conteneur. Pour plus d’informations, consultez [Implémentation de One-Off tables](implementing-one-off-tables.md).
  

