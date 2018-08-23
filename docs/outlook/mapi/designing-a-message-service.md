---
title: Conception d’un service de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b572ebcec0a33d2134f4cf19b88e3132cbd47117
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581999"
---
# <a name="designing-a-message-service"></a>Conception d’un service de message

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Avant de commencer à écrire du code pour prendre en charge votre service de message, il est important de créer une conception. Résoudre les problèmes dans votre processus de conception suivants :
  
1. Déterminer le nombre de fournisseurs de services doivent être inclus dans le service de message. Inclure uniquement les fournisseurs de service associées (autrement dit, les fournisseurs qui fonctionnent avec le même système de messagerie) dans votre service. Fournisseurs de services indépendant n’appartiennent pas dans le même service de message. Utiliser le profil pour l’intégration de fournisseurs de services indépendants et les services de messagerie.
    
2. Déterminer le type de fournisseurs de services doit être inclus dans le service de message. La plupart des services volante inclut un fournisseur de chacun des types courants. Autrement dit, le service de message par défaut a fournisseur de carnet d’adresses d’un fournisseur de magasins d’un message et fournisseur de transport d’un seul.
    
3. Déterminer le nombre de DLL doit contenir le service de message. Le nombre de DLL qui utilise un service de message dépend des éléments suivants :
    
   - Degré de complexité en tant que l’auteur du message du service de message sont prêts à gérer.
    
   - Le type de fournisseurs de services dans le service de message.
    
   - La relation dont le service de message avec un autre service de message.
    
   Étant donné que MAPI stocke le point d’une seule entrée pour chaque type de fournisseur, n’incluez pas plusieurs fournisseurs du même type dans une DLL unique. S’il convient d’inclure plusieurs fournisseurs d’un type, les implémenter dans des DLL distinctes ou demandez-leur de partager une fonction de point d’entrée. Une autre option consiste à implémenter des services de messagerie connexes ou message les services qui sont en mesure d’utiliser la même installation et le code de configuration et la même DLL point d’entrée fonction dans une DLL.
    
   Si possible, la simplicité et utiliser une DLL qui contient l’implémentation de tous les fournisseurs de service dans le service de message et tout le code pour installer et configurer le service de message. Si ce n’est pas possible, vous pouvez implémenter une DLL de code de l’installation et la configuration et une DLL unique pour tous les fournisseurs de services ou une DLL pour chaque fournisseur.
    
4. Déterminer un nom pour le service de message DLL ou la DLL. 
    
## <a name="see-also"></a>Voir aussi

- [Implémentation du service de messagerie](message-service-implementation.md)

