---
title: Identificateurs d'entrée MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 84c37696-da7a-42e0-b8c0-29658a6c9a48
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 4c414b9f8a1d70fd5eea94da326674a749ccefe2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297878"
---
# <a name="mapi-entry-identifiers"></a>Identificateurs d'entrée MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les identificateurs d'entrée sont des parties de données binaires stockées dans une structure [EntryID](entryid.md) qui permettent d'identifier et d'ouvrir de manière unique un objet MAPI. La plupart des objets MAPI comportent des identificateurs d'entrée. Les identificateurs d'entrée pour les objets sont similaires aux noms de fichier des fichiers. Toutefois, ils ne sont pas transmissibles et ne peuvent pas être utilisés sur des systèmes autres que le système dont ils sont originaires. 
  
## <a name="entry-identifiers"></a>Identificateurs d'entrée

Les fournisseurs de banques de messages affectent des identificateurs d'entrée aux banques de messages, aux dossiers et aux messages; les fournisseurs de carnets d'adresses les assignent aux conteneurs du carnet d'adresses, aux listes de distribution et aux utilisateurs de messagerie. Les identificateurs d'entrée sont également utilisés pour ouvrir un objet représenté par une ligne dans un tableau, tel qu'un objet état dans le tableau d'État. Les objets stockent leurs identificateurs d'entrée dans leur propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
  
Tandis que les fournisseurs de services créent, attribuent et examinent des identificateurs d'entrée, les applications clientes les utilisent uniquement en tant qu'outils pour l'ouverture d'objets. Pour les clients, les identificateurs d'entrée sont des parties opaques de données binaires et n'ont rien à faire avec le système de messagerie sous-jacent. 
  
Les clients appellent la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) d'un objet pour récupérer sa propriété **PR_ENTRYID** ou la méthode [IMAPITable:: QueryColumns](imapitable-querycolumns.md) pour extraire la colonne qui contient la propriété **PR_ENTRYID** . 
  
Les identificateurs d'entrée sont transmis en tant que paramètres aux méthodes **OpenEntry** et **CompareEntryIDs** . Plusieurs objets MAPI implémentent les méthodes **OpenEntry** et **CompareEntryIDs** . Avec **OpenEntry**, les clients peuvent ouvrir un objet. Avec **CompareEntryIDs**, les clients peuvent comparer deux identificateurs d'entrée pour déterminer s'ils font référence au même objet. Étant donné que les identificateurs d'entrée ne sont pas nécessairement de type binaire comparable, les clients doivent les comparer par la méthode **CompareEntryIDs** . 
  
Les clients doivent toujours transmettre des identificateurs d'entrée naturellement alignés dans leurs appels aux fournisseurs de services, car même si les fournisseurs de services doivent gérer les identificateurs d'entrée qui sont alignés de manière arbitraire, cela n'est pas toujours le cas. Une adresse de mémoire naturellement alignée permet à l'ordinateur d'accéder à n'importe quel type de données pris en charge à cette adresse sans générer de faute d'alignement. Le facteur d'alignement naturel est généralement le même facteur d'alignement utilisé par l'allocateur de mémoire système et est généralement de 8 octets.
  
Les identificateurs d'entrée se comportent en deux types: à court terme et à long terme. Les identificateurs d'entrée à court terme sont plus rapides à construire, mais leur unicité n'est garantie que pendant la durée de vie de la session en cours sur la station de travail actuelle. Les identificateurs d'entrée à long terme ont une durée de vie plus longue. Les identificateurs d'entrée à court terme sont utilisés principalement pour les lignes des tables et des entrées dans les boîtes de dialogue, tandis que les identificateurs d'entrée à long terme sont utilisés pour de nombreux objets tels que les messages, les dossiers et les listes de distribution.
  
## <a name="see-also"></a>Voir aussi



[D�veloppement d'applications MAPI](mapi-application-development.md)

