---
title: Identificateurs d’entrée MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 84c37696-da7a-42e0-b8c0-29658a6c9a48
ms.openlocfilehash: f15ce3bbeebb819d00d281acc862d08da09abbac
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369160"
---
# <a name="mapi-entry-identifiers"></a>Identificateurs d’entrée MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les identificateurs d’entrée sont des éléments de données binaires stockés dans une structure [ENTRYID](entryid.md) qui sont utilisés pour identifier et ouvrir un objet MAPI de manière unique. La plupart des objets MAPI ont des identificateurs d’entrée. Les identificateurs d’entrée pour les objets sont analogues aux noms de fichiers. Toutefois, ils ne peuvent pas être transmis et ne peuvent pas être utilisés sur des systèmes autres que le système d’origine. 
  
## <a name="entry-identifiers"></a>Identificateurs d’entrée

Les fournisseurs de magasins de messages attribuent des identificateurs d’entrée aux magasins de messages, aux dossiers et aux messages ; les fournisseurs de carnets d’adresses les affectent à des conteneurs de carnets d’adresses, à des listes de distribution et à des utilisateurs de messagerie; Les identificateurs d’entrée sont également utilisés pour ouvrir un objet représenté par une ligne dans une table, tel qu’un objet d’état dans la table d’état. Les objets stockent leurs identificateurs d’entrée dans **PR_ENTRYID** propriété ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
  
Tandis que les fournisseurs de services créent, affectent et examinent les identificateurs d’entrée, les applications clientes les utilisent uniquement comme outils pour ouvrir des objets. Pour les clients, les identificateurs d’entrée sont des éléments opaques de données binaires et n’ont rien à voir avec le système de messagerie sous-jacent. 
  
Les clients appellent la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) d’un objet pour récupérer sa propriété **PR_ENTRYID** ou la méthode [IMAPITable::QueryColumns](imapitable-querycolumns.md) d’une table pour récupérer la colonne qui contient la propriété **PR_ENTRYID** . 
  
Les identificateurs d’entrée sont transmis en tant que paramètres aux méthodes **OpenEntry** et **CompareEntryIDs** . Plusieurs objets MAPI implémentent **les méthodes OpenEntry** et **CompareEntryIDs** . Avec **OpenEntry**, les clients peuvent ouvrir un objet. Avec **CompareEntryIDs**, les clients peuvent comparer deux identificateurs d’entrée pour déterminer s’ils font référence au même objet. Étant donné que les identificateurs d’entrée ne sont pas nécessairement des données binaires comparables, les clients doivent les comparer par la méthode **CompareEntryIDs** . 
  
Les clients doivent toujours transmettre des identificateurs d’entrée alignés naturellement dans leurs appels aux fournisseurs de services, car bien que les fournisseurs de services doivent gérer les identificateurs d’entrée qui sont arbitrairement alignés, ce n’est pas toujours le cas. Une adresse mémoire alignée naturellement permet à l’ordinateur d’accéder à n’importe quel type de données qu’il prend en charge à cette adresse sans générer de panne d’alignement. Le facteur d’alignement naturel est généralement le même facteur d’alignement que celui utilisé par l’allocation de mémoire système et est généralement de 8 octets.
  
Les identificateurs d’entrée sont de deux types : à court terme et à long terme. Les identificateurs d’entrée à court terme sont plus rapides à construire, mais leur unicité est garantie uniquement pendant toute la durée de vie de la session en cours sur la station de travail actuelle. Les identificateurs d’entrée à long terme ont une durée de vie plus longue. Les identificateurs d’entrée à court terme sont principalement utilisés pour les lignes dans les tables et les entrées dans les boîtes de dialogue, tandis que les identificateurs d’entrée à long terme sont utilisés pour de nombreux objets tels que les messages, les dossiers et les listes de distribution.
  
## <a name="see-also"></a>Voir aussi



[D�veloppement d'applications MAPI](mapi-application-development.md)

