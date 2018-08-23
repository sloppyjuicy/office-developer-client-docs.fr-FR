---
title: Fonctionnalités requises pour les fournisseurs de carnet d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e2ccddd7-65e8-41f6-8e21-a4ae98190a96
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 919b21490bb3b4418ba291e8e06198028c995b00
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570869"
---
# <a name="required-features-for-address-book-providers"></a>Fonctionnalités requises pour les fournisseurs de carnet d’adresses

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournisseurs de carnet d’adresses peuvent fonctionner avec les informations de destinataire qui sont temporaire ou permanent, local ou distant, compréhensibles par un ou plusieurs systèmes de messagerie et mise en forme d’une table de base de données ou le fichier disque. Il existe une variété de fonctionnalités qu’un fournisseur de carnet d’adresses peut implémenter ainsi valeur et améliore l’interopérabilité avec les clients et d’autres fournisseurs. Toutefois, certaines fonctionnalités sont requises.
  
Le tableau suivant décrit les fonctionnalités qui sont requises pour tous les fournisseurs de carnet d’adresses et les étapes à suivre pour implémenter les.
  
|**Fonctionnalité**|**Comment mettre en œuvre**|
|:-----|:-----|
|Ouverture de session  <br/> | Implémenter une fonction de point d’entrée. Pour plus d’informations, voir [l’implémentation d’une fonction Point d’entrée adresse livre fournisseur](implementing-an-address-book-provider-entry-point-function.md).  <br/>  Implémentez la méthode [IABProvider::Logon](iabprovider-logon.md) . Pour plus d’informations, voir [implémentation de la connexion au fournisseur du carnet d’adresses et de fermeture de session](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Fermeture de session  <br/> |Implémentez la méthode [IABProvider::Shutdown](iabprovider-shutdown.md) . Pour plus d’informations, voir [implémentation de la connexion au fournisseur du carnet d’adresses et de fermeture de session](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Créer des identificateurs d’entrée  <br/> |Prendre en charge la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Pour plus d’informations, voir [Identificateurs de carnet d’adresses](address-book-identifiers.md)et les [Identificateurs d’entrée MAPI](mapi-entry-identifiers.md) .  <br/> |
|Contribuer à la table d’état  <br/> | Implémenter les méthodes appropriées de la [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface. Pour plus d’informations, voir [Implémentation d’objet état](status-object-implementation.md).  <br/>  Prend en charge les propriétés de la table d’état obligatoire. Pour plus d’informations, voir [Tableaux d’état](status-tables.md).  <br/>  Appelez [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md).  <br/> |
|Objet état limité en charge  <br/> | Implémentez la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .  <br/>  Retourner MAPI_E_NO_SUPPORT d’autres méthodes **IMAPIStatus** .  <br/> |
|Configuration de prise en charge interactive et par programmation  <br/> | Implémenter une fonction de point d’entrée de message service.  <br/>  Implémenter un tableau d’affichage. Pour plus d’informations, voir [Afficher des Tables](display-tables.md) et [Implémentation de tableau d’affichage](display-table-implementation.md).  <br/>  Implémenter une feuille de propriétés ou appeler la méthode [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) . Pour plus d’informations, voir [Implémentation de feuille de propriétés](property-sheet-implementation.md).  <br/> |
   
En outre, si votre fournisseur prend en charge la création de destinataires, vous devez fournir une liste de modèles de création. Fournir cette liste en implémentant la méthode [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) pour inclure tous les modèles pris en charge par votre fournisseur et la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de chaque conteneur pour ouvrir la **PR_CREATE_TEMPLATES** ([ PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) propriété et inclure tous les modèles pris en charge par le conteneur. Pour plus d’informations, voir [Implémentation de Tables uniques](implementing-one-off-tables.md).
  

