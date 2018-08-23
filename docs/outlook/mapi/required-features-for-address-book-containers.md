---
title: Fonctionnalités requises pour les conteneurs du carnet d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e221944-5dc9-4cce-8b47-73af84427aea
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 050a26f4b4e6c353881189f8c7b71c2e4c378d03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577211"
---
# <a name="required-features-for-address-book-containers"></a>Fonctionnalités requises pour les conteneurs du carnet d’adresses

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
La plupart des fournisseurs de carnet d’adresses prend en charge au moins un conteneur, certains d'entre eux modifiable. Conteneurs de carnet d’adresses peuvent fournir de contenu et tables de hiérarchie, des fonctions de recherche et la résolution de nom. Conteneurs modifiables autoriser la suppression des entrées telles que la messagerie des utilisateurs, des listes de distribution, ou autres conteneurs et l’ajout des entrées à partir d’entrées dans d’autres conteneurs ou à partir de modèles uniques.
  
Le tableau suivant décrit les fonctionnalités qui sont requises pour les fournisseurs de carnet d’adresses qui ont des conteneurs, modifiables ou en lecture seule, et comment les implémenter.
  
|**Fonctionnalité**|**Comment mettre en œuvre**|
|:-----|:-----|
|Accéder à des utilisateurs de messagerie  <br/> |Implémentez la méthode [IABLogon::OpenEntry](iablogon-openentry.md) . Pour plus d’informations, voir les [Entrées de carnet d’adresses de l’ouverture](opening-address-book-entries.md).  <br/> |
|Comparer les utilisateurs de messagerie  <br/> |Implémentez la méthode [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) . Pour plus d’informations, voir [Comparaison des entrées de carnet d’adresses](comparing-address-book-entries.md).  <br/> |
|Créer des utilisateurs de messagerie  <br/> |1. fournir une liste des modèles de création d’une table unique en prenant en charge la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Pour plus d’informations, voir [mise en œuvre d’une Table unique du conteneur](implementing-a-container-one-off-table.md).  <br/> 2. implémenter la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) . Pour plus d’informations, voir [Ajouter des entrées de carnet d’adresses](adding-address-book-entries.md).  <br/> |
|Copier des utilisateurs de messagerie  <br/> |Implémentez la méthode [IABContainer::CopyEntries](iabcontainer-copyentries.md) . Pour plus d’informations, voir [Copie des entrées de carnet d’adresses](copying-address-book-entries.md).  <br/> |
|Supprimer des utilisateurs de messagerie  <br/> |Implémentez la méthode [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) . Pour plus d’informations, voir [Suppression des entrées de carnet d’adresses](removing-address-book-entries.md).  <br/> |
|Fournir des informations récapitulatives concernant les utilisateurs de messagerie  <br/> |Prend en charge la propriété container **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). For more information, see [Tables des mati�res](contents-tables.md).  <br/> |
|Fournir des informations détaillées sur les utilisateurs de messagerie  <br/> |Prend en charge la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) sur les listes de distribution et les utilisateurs de messagerie. Pour plus d’informations, voir [Affichage des informations sur les destinataires](displaying-recipient-information.md) et [Afficher des Tables](display-tables.md).  <br/> |
|Fournir des informations détaillées sur un conteneur  <br/> |Prise en charge de la propriété **PR_DETAILS_TABLE** sur le conteneur. Pour plus d’informations, voir [Affichage des informations sur les destinataires](displaying-recipient-information.md) et [Afficher des Tables](display-tables.md).  <br/> |
|Fournir une liste hiérarchique des conteneurs  <br/> |Prend en charge la propriété container **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)). Pour plus d’informations, voir les [Tables de hiérarchie](hierarchy-tables.md).  <br/> |
|Prise en charge des propriétés de l’utilisateur de messagerie  <br/> |Implémenter le [IMailUser : IMAPIProp](imailuserimapiprop.md) interface.  <br/> |
|Résoudre les noms ambigus  <br/> | Prend en charge la restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).  <br/>  Vous pouvez également implémenter la méthode [IABContainer::ResolveNames](iabcontainer-resolvenames.md) . For more information, see [L'impl�mentation de la r�solution de noms](implementing-name-resolution.md).  <br/> |
   

