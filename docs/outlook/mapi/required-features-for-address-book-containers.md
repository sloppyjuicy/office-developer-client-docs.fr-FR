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
ms.openlocfilehash: bfba7dcb4513873245c6141f3da32884c4d93402
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62781176"
---
# <a name="required-features-for-address-book-containers"></a>Fonctionnalités requises pour les conteneurs de carnet d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La plupart des fournisseurs de carnet d’adresses peuvent prendre en charge au moins un conteneur, dont certains peuvent être modifiables. Les conteneurs de carnet d’adresses peuvent fournir des tables de contenu et de hiérarchie, des fonctionnalités de recherche et la résolution de noms. Les conteneurs modifiables permettent la suppression d’entrées telles que des utilisateurs de messagerie, des listes de distribution ou d’autres conteneurs, ainsi que l’ajout d’entrées d’entrées dans d’autres conteneurs ou de modèles unique.
  
Le tableau suivant décrit les fonctionnalités requises pour les fournisseurs de carnets d’adresses qui ont des conteneurs, modifiables ou en lecture seule, et la façon dont vous les implémentez.
  
|**Fonctionnalité**|**Modalités de mise en œuvre**|
|:-----|:-----|
|Accéder aux utilisateurs de messagerie  <br/> |[Implémenter la méthode IABLogon::OpenEntry](iablogon-openentry.md). Pour plus d’informations, voir [Ouverture des entrées du carnet d’adresses](opening-address-book-entries.md). |
|Comparer les utilisateurs de messagerie  <br/> |[Implémenter la méthode IABLogon::CompareEntryIDs](iablogon-compareentryids.md). Pour plus d’informations, voir [Comparaison des entrées de carnet d’adresses](comparing-address-book-entries.md). |
|Créer des utilisateurs de messagerie  <br/> |1. Fournissez une liste de modèles de création dans une table unique en PR_CREATE_TEMPLATES propriété **(**[PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Pour plus d’informations, [voir Implementing a Container One-Off Table](implementing-a-container-one-off-table.md). 2. [Implémentez la méthode IABContainer::CreateEntry](iabcontainer-createentry.md). Pour plus d’informations, voir [Ajout d’entrées de carnet d’adresses](adding-address-book-entries.md). |
|Copier les utilisateurs de messagerie  <br/> |[Implémentez la méthode IABContainer::CopyEntries](iabcontainer-copyentries.md). Pour plus d’informations, voir [Copie des entrées de carnet d’adresses](copying-address-book-entries.md). |
|Supprimer des utilisateurs de messagerie  <br/> |[Implémentez la méthode IABContainer::D eleteEntries](iabcontainer-deleteentries.md). Pour plus d’informations, voir [Suppression des entrées de carnet d’adresses](removing-address-book-entries.md). |
|Fournir des informations récapitulatifs sur les utilisateurs de messagerie  <br/> |Prise en charge de la **propriété PR_CONTAINER_CONTENTS** conteneur ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). For more information, see [Tables des mati�res](contents-tables.md). |
|Fournir des informations détaillées sur les utilisateurs de messagerie  <br/> |Prise en **charge PR_DETAILS_TABLE** propriété ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) sur les utilisateurs de messagerie et les listes de distribution. Pour plus d’informations, voir [Afficher les informations sur le destinataire](displaying-recipient-information.md) et [Afficher les tableaux](display-tables.md). |
|Fournir des informations détaillées sur un conteneur  <br/> |Prise en charge **PR_DETAILS_TABLE** propriété sur le conteneur. Pour plus d’informations, voir [Afficher les informations sur le destinataire](displaying-recipient-information.md) et [Afficher les tableaux](display-tables.md). |
|Fournir une liste hiérarchique de conteneurs  <br/> |Prise en charge de la **propriété PR_CONTAINER_HIERARCHY** conteneur ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)). Pour plus d’informations, [voir Tableaux de hiérarchie](hierarchy-tables.md). |
|Prise en charge des propriétés utilisateur de messagerie  <br/> |[Implémenter l’interface IMailUser : IMAPIProp](imailuserimapiprop.md). |
|Résoudre les noms ambigus  <br/> | Prise en **charge PR_ANR** restriction de propriété ([PidTagAnr](pidtaganr-canonical-property.md)).  Implémenter éventuellement [la méthode IABContainer::ResolveNames](iabcontainer-resolvenames.md) . For more information, see [L'impl�mentation de la r�solution de noms](implementing-name-resolution.md). |
   

