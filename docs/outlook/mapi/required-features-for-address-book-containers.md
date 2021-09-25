---
title: Fonctionnalités requises pour les conteneurs de carnet d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3e221944-5dc9-4cce-8b47-73af84427aea
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 71a8a6ae48bd9da08eb9cf0cb6dad7b6fde7c129
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609662"
---
# <a name="required-features-for-address-book-containers"></a>Fonctionnalités requises pour les conteneurs de carnet d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La plupart des fournisseurs de carnet d’adresses peuvent prendre en charge au moins un conteneur, dont certains peuvent être modifiables. Les conteneurs de carnet d’adresses peuvent fournir des tables de contenu et de hiérarchie, des fonctionnalités de recherche et la résolution de noms. Les conteneurs modifiables permettent la suppression d’entrées telles que des utilisateurs de messagerie, des listes de distribution ou d’autres conteneurs, ainsi que l’ajout d’entrées d’entrées dans d’autres conteneurs ou de modèles unique.
  
Le tableau suivant décrit les fonctionnalités requises pour les fournisseurs de carnets d’adresses qui ont des conteneurs, modifiables ou en lecture seule, et la façon dont vous les implémentez.
  
|**Fonctionnalité**|**Modalités de mise en œuvre**|
|:-----|:-----|
|Accéder aux utilisateurs de messagerie  <br/> |Implémenter [la méthode IABLogon::OpenEntry.](iablogon-openentry.md) Pour plus d’informations, voir [Ouverture des entrées du carnet d’adresses.](opening-address-book-entries.md)  <br/> |
|Comparer les utilisateurs de messagerie  <br/> |Implémenter [la méthode IABLogon::CompareEntryIDs.](iablogon-compareentryids.md) Pour plus d’informations, voir [Comparaison des entrées de carnet d’adresses.](comparing-address-book-entries.md)  <br/> |
|Créer des utilisateurs de messagerie  <br/> |1. Fournissez une liste de modèles de création dans une table unique en PR_CREATE_TEMPLATES **(** [PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) propriété. Pour plus d’informations, [voir Implementing a Container One-Off Table](implementing-a-container-one-off-table.md).  <br/> 2. Implémentez [la méthode IABContainer::CreateEntry.](iabcontainer-createentry.md) Pour plus d’informations, voir [Ajout d’entrées de carnet d’adresses.](adding-address-book-entries.md)  <br/> |
|Copier les utilisateurs de messagerie  <br/> |Implémentez [la méthode IABContainer::CopyEntries.](iabcontainer-copyentries.md) Pour plus d’informations, voir [Copie des entrées du carnet d’adresses.](copying-address-book-entries.md)  <br/> |
|Supprimer des utilisateurs de messagerie  <br/> |Implémentez [la méthode IABContainer::D eleteEntries.](iabcontainer-deleteentries.md) Pour plus d’informations, voir [Suppression des entrées de carnet d’adresses.](removing-address-book-entries.md)  <br/> |
|Fournir des informations récapitulatifs sur les utilisateurs de messagerie  <br/> |Prise en charge de la **propriété PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). For more information, see [Tables des mati�res](contents-tables.md).  <br/> |
|Fournir des informations détaillées sur les utilisateurs de messagerie  <br/> |Prise en **charge PR_DETAILS_TABLE** propriété ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) sur les utilisateurs de messagerie et les listes de distribution. Pour plus d’informations, voir [Afficher les informations sur le destinataire](displaying-recipient-information.md) et Afficher les [tableaux.](display-tables.md)  <br/> |
|Fournir des informations détaillées sur un conteneur  <br/> |Prise en charge **PR_DETAILS_TABLE** propriété sur le conteneur. Pour plus d’informations, voir [Afficher les informations sur le destinataire](displaying-recipient-information.md) et Afficher les [tableaux.](display-tables.md)  <br/> |
|Fournir une liste hiérarchique de conteneurs  <br/> |Prise en charge de la **propriété PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)). Pour plus d’informations, [voir Tables hiérarchiques.](hierarchy-tables.md)  <br/> |
|Prise en charge des propriétés utilisateur de messagerie  <br/> |Implémenter [l’interface IMailUser : IMAPIProp.](imailuserimapiprop.md)  <br/> |
|Résoudre les noms ambigus  <br/> | Prise en **charge PR_ANR** restriction de propriété ([PidTagAnr](pidtaganr-canonical-property.md)).  <br/>  Implémenter éventuellement [la méthode IABContainer::ResolveNames.](iabcontainer-resolvenames.md) For more information, see [L'impl�mentation de la r�solution de noms](implementing-name-resolution.md).  <br/> |
   

