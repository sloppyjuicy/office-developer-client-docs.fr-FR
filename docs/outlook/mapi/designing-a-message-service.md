---
title: Conception d’un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 19a8a939685c440901f3f57d72baf673a579e590
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316722"
---
# <a name="designing-a-message-service"></a>Conception d’un service de messagerie

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avant de commencer à écrire du code pour prendre en charge votre service de messagerie, il est important de créer une conception. Résolvez les problèmes suivants dans votre processus de conception:
  
1. Déterminez le nombre de fournisseurs de services à inclure dans le service de messagerie. Incluez uniquement les fournisseurs de services associés (c'est-à-dire, les fournisseurs qui fonctionnent avec le même système de messagerie) dans votre service. Les fournisseurs de services non liés n'appartiennent pas au même service de messagerie. Utiliser le profil pour intégrer des services de messagerie et des fournisseurs de services non liés.
    
2. Déterminez le type de fournisseurs de services à inclure dans le service de messagerie. La plupart des services messge incluent un fournisseur de chacun des types courants. Autrement dit, le service de messagerie type dispose d'un fournisseur de carnet d'adresses, d'un fournisseur de banque de messages et d'un fournisseur de transport.
    
3. Déterminez le nombre de dll qui doivent contenir le service de messagerie. Le nombre de dll qu'un service de messagerie utilise dépend des éléments suivants:
    
   - Le degré de complexité que vous êtes prêt à prendre en charge par le service de messagerie.
    
   - Le type de fournisseurs de services dans le service de messagerie.
    
   - Relation que le service de messagerie peut avoir avec un autre service de messagerie.
    
   Étant donné que MAPI ne stocke qu'un seul point d'entrée pour chaque type de fournisseur, n'incluez pas plusieurs fournisseurs du même type dans une seule DLL. S'il est logique d'inclure plusieurs fournisseurs d'un même type, vous devez les implémenter dans des dll distinctes ou les faire partager une fonction de point d'entrée. Une autre option consiste à implémenter des services de message associés ou des services de messagerie qui peuvent utiliser les mêmes code d'installation et de configuration et la même fonction de point d'entrée de DLL dans une DLL.
    
   Si possible, simplifiez-la et utilisez une DLL qui contient l'implémentation de tous les fournisseurs de services dans le service de messagerie et tout le code pour installer et configurer le service de messagerie. Si cela n'est pas possible, vous pouvez implémenter une DLL pour le code d'installation et de configuration et une DLL unique pour tous les fournisseurs de services ou une DLL pour chaque fournisseur.
    
4. Déterminez un nom pour la DLL ou les dll du service de messagerie. 
    
## <a name="see-also"></a>Voir aussi

- [Implémentation du service de messagerie](message-service-implementation.md)

