---
title: Identificateurs d’entrée MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 84c37696-da7a-42e0-b8c0-29658a6c9a48
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d8c9fb0b24d8954fae75274bfbedca9d7c62de93
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567859"
---
# <a name="mapi-entry-identifiers"></a>Identificateurs d’entrée MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Identificateurs d’entrée sont des éléments de données binaires stockées dans une structure [ENTRYID](entryid.md) qui servent à identifier et ouvrir un objet MAPI de manière unique. La plupart des objets MAPI ont des identificateurs d’entrée. Identificateurs d’entrée pour les objets sont similaires aux noms des fichiers. Toutefois, elles ne sont pas transmissible et ne peut pas être utilisés sur les systèmes autres que le système qu'ils provient. 
  
## <a name="entry-identifiers"></a>Identificateurs d’entrée

Fournisseurs de banque de messages affecter des identificateurs d’entrée pour les banques de messages, les dossiers et messages ; fournisseurs de carnet d’adresses affecter aux conteneurs de carnet d’adresses, les listes de distribution et les utilisateurs de messagerie. Identificateurs d’entrée sont également utilisés pour ouvrir un objet représenté par une ligne dans une table, comme un objet d’état dans la table d’état. Objets de banque de leurs identificateurs d’entrée dans leur propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
  
Tandis que les fournisseurs de services de créer, affectent et examiner les identificateurs d’entrée, les applications client utiliser uniquement en tant qu’outils pour ouvrir des objets. Aux clients, identificateurs d’entrée sont des données binaires opaque et aient rien à voir avec le système de messagerie sous-jacent. 
  
Les clients appeler la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) d’un objet à récupérer sa propriété **PR_ENTRYID** ou d’une table [IMAPITable::QueryColumns](imapitable-querycolumns.md) pour récupérer la colonne qui contient la propriété **PR_ENTRYID** . 
  
Identificateurs d’entrée sont transmises aux méthodes **OpenEntry** et **CompareEntryIDs** en tant que paramètres. Plusieurs objets MAPI implémentent les méthodes **OpenEntry** et **CompareEntryIDs** . Avec **OpenEntry**, les clients peuvent ouvrir un objet. Avec **CompareEntryIDs**, les clients peuvent comparer deux identificateurs d’entrée pour déterminer si elles font référence au même objet. Étant donné que les identificateurs d’entrée ne sont pas nécessairement binaires comparables, les clients doivent comparer à la méthode **CompareEntryIDs** . 
  
Clients doivent toujours passer des identificateurs d’entrée aligné naturellement dans leurs appels aux fournisseurs de services, étant donné que bien que les fournisseurs de services doivent gérer les identificateurs d’entrée arbitrairement alignés, ce n’est pas toujours le cas. Une adresse de la mémoire alignée naturellement permet d’accéder à n’importe quel type de données que pris en charge à l’adresse sans générer une erreur d’alignement de l’ordinateur. Le facteur d’alignement naturel est généralement le même facteur d’alignement utilisé par l’allocation de mémoire système et est généralement 8 octets.
  
Identificateurs d’entrée sont de deux types : à court terme et à long terme. Identificateurs d’entrée à court terme sont plus rapides à construire, mais leur unicité est garantie uniquement pendant la durée de la session en cours sur la station de travail en cours. Les identificateurs d’entrée à long terme ont une durée de vie prolongée plus. Identificateurs d’entrée à court terme sont utilisées principalement pour les lignes de tableaux et des entrées dans les boîtes de dialogue, tandis que les identificateurs d’entrée à long terme sont utilisées pour de nombreux objets tels que les messages, dossiers et listes de distribution.
  
## <a name="see-also"></a>Voir aussi



[D�veloppement d'applications MAPI](mapi-application-development.md)

