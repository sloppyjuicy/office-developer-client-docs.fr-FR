---
title: Prise en charge des recherches dans les fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f206623103f810b2868502aea7c6804cd306f022
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573193"
---
# <a name="supporting-searches-in-message-store-providers"></a>Prise en charge des recherches dans les fournisseurs de banques de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes ont fréquemment certains composants d’interface utilisateur consacrées à la recherche de messages dans une banque de messages. Critères de recherche sont spécifiés dans le [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface via les méthodes [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) et [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) . 
  
Clients utilisent la propriété **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) de l’objet de banque de message pour identifier le dossier racine dans le magasin de message qui contient les dossiers de résultats de recherche. Le dossier de résultats de recherche est souvent un dossier au niveau supérieur de la banque de messages qui ne fait pas partie de l’arborescence de dossiers IPM et, par conséquent, masqué.
  
Si votre fournisseur de magasin de message utilise un dossier de résultats de recherche permanente ou crée un lorsqu’un client ouvre l’identificateur d’entrée stockée dans la propriété **PR_FINDER_ENTRYID** est un détail d’implémentation. Il est un peu plus facile de votre fournisseur de magasin de message à utiliser un dossier permanent qui est créé lors de la création de la banque de messages, car cela évite la complication de vérification de l’identificateur d’entrée à chaque ouverture d’un dossier pour voir s’il faut créer un dossier de résultats de recherche. Toutefois, tous les fournisseurs de banque de message peuvent faire. en particulier, banques de message en lecture seule ou qui fournissent une interface MAPI pour une base de données hérité souvent ne sont pas autorisés ou ne parvenez pas à créer un dossier de résultats de recherche permanente dans le mécanisme de stockage sous-jacent. 
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

