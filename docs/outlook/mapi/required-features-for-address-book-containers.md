---
title: Fonctionnalités requises pour les conteneurs de carnets d’adresses
description: Décrit les fonctionnalités requises des fournisseurs de carnets d’adresses qui ont des conteneurs, modifiables ou en lecture seule, et comment vous les implémentez.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3e221944-5dc9-4cce-8b47-73af84427aea
ms.openlocfilehash: 60229614b9ca9669faa6345eba913714bffffd28
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752427"
---
# <a name="required-features-for-address-book-containers"></a>Fonctionnalités requises pour les conteneurs de carnets d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La plupart des fournisseurs de carnets d’adresses prennent en charge au moins un conteneur, dont certains sont modifiables. Les conteneurs de carnets d’adresses peuvent fournir le contenu et les tables hiérarchiques, les fonctionnalités de recherche et la résolution de noms. Les conteneurs modifiables permettent la suppression d’entrées telles que les utilisateurs de messagerie, les listes de distribution ou d’autres conteneurs, ainsi que l’ajout d’entrées d’entrées dans d’autres conteneurs ou de modèles uniques.
  
Le tableau suivant décrit les fonctionnalités requises des fournisseurs de carnets d’adresses qui ont des conteneurs, modifiables ou en lecture seule, et comment vous les implémentez.
  
|**Fonctionnalité**|**Modalités de mise en œuvre**|
|:-----|:-----|
|Accéder aux utilisateurs de messagerie  <br/> |Implémentez la méthode [IABLogon::OpenEntry](iablogon-openentry.md) . Pour plus d’informations, consultez [Ouverture des entrées du carnet d’adresses](opening-address-book-entries.md). |
|Comparer les utilisateurs de messagerie  <br/> |Implémentez la méthode [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) . Pour plus d’informations, consultez [Comparaison des entrées de carnet d’adresses](comparing-address-book-entries.md). |
|Créer des utilisateurs de messagerie  <br/> |1. Fournissez une liste de modèles de création dans une table unique en prenant en charge la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Pour plus d’informations, consultez [Implémentation d’un conteneur One-Off Table](implementing-a-container-one-off-table.md). 2. Implémentez la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) . Pour plus d’informations, consultez [Ajout d’entrées de carnet d’adresses](adding-address-book-entries.md). |
|Copier des utilisateurs de messagerie  <br/> |Implémentez la méthode [IABContainer::CopyEntries](iabcontainer-copyentries.md) . Pour plus d’informations, consultez [Copier les entrées du carnet d’adresses](copying-address-book-entries.md). |
|Supprimer les utilisateurs de messagerie  <br/> |Implémentez la méthode [IABContainer::D eleteEntries](iabcontainer-deleteentries.md) . Pour plus d’informations, consultez [Suppression des entrées de carnet d’adresses](removing-address-book-entries.md). |
|Fournir des informations récapitulatives sur les utilisateurs de messagerie  <br/> |Prise en charge de la propriété conteneur **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). For more information, see [Tables des mati�res](contents-tables.md). |
|Fournir des informations détaillées sur les utilisateurs de messagerie  <br/> |Prenez en charge la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) sur les utilisateurs de messagerie et les listes de distribution. Pour plus d’informations, consultez [Afficher les informations sur les destinataires](displaying-recipient-information.md) et [afficher les tables](display-tables.md). |
|Fournir des informations détaillées sur un conteneur  <br/> |Prenez en charge la propriété **PR_DETAILS_TABLE** sur le conteneur. Pour plus d’informations, consultez [Afficher les informations sur les destinataires](displaying-recipient-information.md) et [afficher les tables](display-tables.md). |
|Fournir une liste hiérarchique de conteneurs  <br/> |Prise en charge de la propriété conteneur **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)). Pour plus d’informations, consultez [Tables hiérarchiques](hierarchy-tables.md). |
|Prise en charge des propriétés utilisateur de messagerie  <br/> |Implémentez l’interface [IMailUser : IMAPIProp](imailuserimapiprop.md) . |
|Résoudre les noms ambigus  <br/> | Prise en charge de la restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).  Implémentez éventuellement la méthode [IABContainer::ResolveNames](iabcontainer-resolvenames.md) . For more information, see [L'impl�mentation de la r�solution de noms](implementing-name-resolution.md). |
   

