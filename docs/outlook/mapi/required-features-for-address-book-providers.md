---
title: Fonctionnalités requises pour les fournisseurs de carnets d'adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e2ccddd7-65e8-41f6-8e21-a4ae98190a96
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 56ca15440c8d323dbab1b6a92a01941106b86934
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421395"
---
# <a name="required-features-for-address-book-providers"></a>Fonctionnalités requises pour les fournisseurs de carnets d'adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de carnet d'adresses peuvent utiliser des informations sur les destinataires, qu'elles soient temporaires ou permanentes, locales ou distantes, compréhensibles par un ou plusieurs systèmes de messagerie et mises en forme pour un fichier disque ou une table de base de données. Un fournisseur de carnet d'adresses peut implémenter un grand nombre de fonctionnalités, ajoutant ainsi de la valeur et améliorent l'interopérabilité avec les clients et les autres fournisseurs. Toutefois, certaines fonctionnalités sont requises.
  
Le tableau suivant décrit les fonctionnalités requises de tous les fournisseurs de carnets d'adresses et les étapes à suivre pour les implémenter.
  
|**Fonctionnalité**|**Comment implémenter**|
|:-----|:-----|
|Ouverture de session  <br/> | Implémentez une fonction de point d'entrée. Pour plus d'informations, consultez la rubrique [implémentation d'une fonction de point d'entrée de fournisseur de carnet d'adresses](implementing-an-address-book-provider-entry-point-function.md).  <br/>  Implémentez la méthode [IABProvider:: Logon](iabprovider-logon.md) . Pour plus d'informations, consultez la rubrique [implémentation du fournisseur de carnet d'adresses Logon and Logoff](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Fermeture de session  <br/> |Implémentez la méthode [IABProvider:: Shutdown](iabprovider-shutdown.md) . Pour plus d'informations, consultez la rubrique [implémentation du fournisseur de carnet d'adresses Logon and Logoff](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Créer des identificateurs d'entrée  <br/> |Prise en charge de la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Pour plus d'informations, consultez la rubrique identificateurs d' [entrée MAPI](mapi-entry-identifiers.md) et identificateurs de [carnet d'adresses](address-book-identifiers.md).  <br/> |
|Contribuer à la table d'État  <br/> | Implémentez les méthodes appropriées de l'interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) . Pour plus d'informations, voir état de l' [objet](status-object-implementation.md).  <br/>  Prendre en charge les propriétés de table d'État requises. Pour plus d'informations, consultez la rubrique [tables d'État](status-tables.md).  <br/>  Appelez [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md).  <br/> |
|Fournir une prise en charge limitée des objets d'État  <br/> | Implémentez la méthode [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) .  <br/>  Renvoyer MAPI_E_NO_SUPPORT à partir des autres méthodes **IMAPIStatus** .  <br/> |
|Prise en charge de la configuration interactive et par programme  <br/> | Implémentez une fonction de point d'entrée de service de messagerie.  <br/>  Implémenter une table d'affichage. Pour plus d'informations, consultez la rubrique [affichage des tables](display-tables.md) et de l'implémentation des tables d' [affichage](display-table-implementation.md).  <br/>  Implémentez une feuille de propriétés ou appelez la méthode [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) . Pour plus d'informations, consultez la rubrique implémentation de la [feuille de propriétés](property-sheet-implementation.md).  <br/> |
   
En outre, si votre fournisseur prend en charge la création de destinataires, vous devez fournir une liste de modèles de création. Fournissez cette liste en implémentant la méthode [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) pour inclure tous les modèles pris en charge par votre fournisseur et la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) de chaque conteneur pour ouvrir le **PR_CREATE_TEMPLATES** ([ PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) et inclut tous les modèles pris en charge par le conteneur. Pour plus d'informations, reportez-vous à la rubrique [implementIng One-Off tables](implementing-one-off-tables.md).
  

