---
title: Prise en charge des recherches dans les fournisseurs de magasins de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
ms.openlocfilehash: 2afb371118fe28fff8c40e49682b7c081e33cf79
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380962"
---
# <a name="supporting-searches-in-message-store-providers"></a>Prise en charge des recherches dans les fournisseurs de magasins de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes ont souvent des composants d’interface utilisateur dédiés à la recherche de messages dans une magasin de messages. Les critères de recherche sont spécifiés dans l’interface [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) au moyen des méthodes [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) et [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) . 
  
Les clients utilisent la propriété **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) de l’objet de magasin de messages pour identifier le dossier racine dans la magasin de messages qui contient des dossiers pour les résultats de la recherche. Le dossier de résultats de recherche est souvent un dossier au niveau supérieur de la magasin de messages qui ne fait pas partie de l’arborescence des dossiers IPM et qui est donc masqué.
  
Que votre fournisseur de magasins de messages utilise un dossier de résultats de recherche permanent ou en crée un lorsqu’un client ouvre l’identificateur d’entrée stocké dans la **propriété PR_FINDER_ENTRYID** est un détail d’implémentation. Il est un peu plus facile pour votre fournisseur de magasin de messages d’utiliser un dossier permanent créé lors de la création de la magasin de messages, car cela évite la complication de la vérification de l’identificateur d’entrée chaque fois qu’un dossier est ouvert pour déterminer s’il faut créer un dossier de résultats de recherche. Toutefois, tous les fournisseurs de magasins de messages ne peuvent pas le faire . notamment, les banques de messages en lecture seule qui fournissent une interface MAPI à une base de données héritée ne sont souvent pas autorisées ou ne peuvent pas créer un dossier de résultats de recherche permanent dans le mécanisme de stockage sous-jacent. 
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

