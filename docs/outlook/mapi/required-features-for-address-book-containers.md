---
title: Fonctionnalités requises pour les conteneurs du carnet d'adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e221944-5dc9-4cce-8b47-73af84427aea
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: abdbd9030e0ea053d39b49ecc76a78821be9df82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328706"
---
# <a name="required-features-for-address-book-containers"></a>Fonctionnalités requises pour les conteneurs du carnet d'adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La plupart des fournisseurs de carnets d'adresses prennent en charge au moins un conteneur, dont certains sont modifiables. Les conteneurs du carnet d'adresses peuvent fournir des tables de contenu et de hiérarchie, des fonctionnalités de recherche et la résolution de noms. Les conteneurs modifiables autorisent la suppression des entrées telles que les utilisateurs de messagerie, les listes de distribution ou d'autres conteneurs, ainsi que l'ajout d'entrées provenant d'entrées dans d'autres conteneurs ou de modèles uniques.
  
Le tableau suivant décrit les fonctionnalités requises pour les fournisseurs de carnet d'adresses qui ont des conteneurs, modifiables ou en lecture seule, et comment les implémenter.
  
|**Fonctionnalité**|**Comment implémenter**|
|:-----|:-----|
|Accéder aux utilisateurs de messagerie  <br/> |Implémentez la méthode [IABLogon:: OpenEntry](iablogon-openentry.md) . Pour plus d'informations, consultez la rubrique [ouverture des entrées de carnet d'adresses](opening-address-book-entries.md).  <br/> |
|Comparer les utilisateurs de messagerie  <br/> |Implémentez la méthode [IABLogon:: CompareEntryIDs](iablogon-compareentryids.md) . Pour plus d'informations, consultez la rubrique [comparaison des entrées du carnet d'adresses](comparing-address-book-entries.md).  <br/> |
|Créer des utilisateurs de messagerie  <br/> |1. fournissez une liste de modèles de création dans une table ponctuelle en prenant en charge la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Pour plus d'informations, reportez-vous à [la rubrique implémentation d'une table ponctuelle de conteneur](implementing-a-container-one-off-table.md).  <br/> 2. implémentez la méthode [IABContainer:: CreateEntry](iabcontainer-createentry.md) . Pour plus d'informations, consultez la rubrique [Ajout d'entrées de carnet d'adresses](adding-address-book-entries.md).  <br/> |
|Copier les utilisateurs de messagerie  <br/> |Implémentez la méthode [IABContainer:: CopyEntries](iabcontainer-copyentries.md) . Pour plus d'informations, consultez la rubrique [copie des entrées du carnet d'adresses](copying-address-book-entries.md).  <br/> |
|Supprimer des utilisateurs de messagerie  <br/> |Implémentez la méthode [IABContainer::D eleteentries](iabcontainer-deleteentries.md) . Pour plus d'informations, consultez la rubrique [suppression des entrées de carnet d'adresses](removing-address-book-entries.md).  <br/> |
|Fournir des informations récapitulatives sur les utilisateurs de messagerie  <br/> |Prendre en charge la propriété Container **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). For more information, see [Tables des mati�res](contents-tables.md).  <br/> |
|Fournir des informations détaillées sur les utilisateurs de messagerie  <br/> |Prendre en charge la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) sur les utilisateurs de messagerie et les listes de distribution. Pour plus d'informations, consultez la rubrique [affichage des informations sur](displaying-recipient-information.md) les destinataires et [affichage des tables](display-tables.md).  <br/> |
|Fournir des informations détaillées sur un conteneur  <br/> |Prendre en charge la propriété **PR_DETAILS_TABLE** sur le conteneur. Pour plus d'informations, consultez la rubrique [affichage des informations sur](displaying-recipient-information.md) les destinataires et [affichage des tables](display-tables.md).  <br/> |
|Fournir une liste hiérarchique de conteneurs  <br/> |Prendre en charge la propriété Container **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)). Pour plus d'informations, consultez la rubrique [Hierarchy tables](hierarchy-tables.md).  <br/> |
|Prendre en charge les propriétés utilisateur de messagerie  <br/> |Implémentez l'interface [IMailUser: IMAPIProp](imailuserimapiprop.md) .  <br/> |
|Résoudre les noms ambigus  <br/> | Prendre en charge la restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).  <br/>  Implémentez éventuellement la méthode [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) . For more information, see [L'impl�mentation de la r�solution de noms](implementing-name-resolution.md).  <br/> |
   

