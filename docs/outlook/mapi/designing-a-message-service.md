---
title: Conception d’un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4b100f3daf901bf72cf9998b8678ad597646ef73
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584618"
---
# <a name="designing-a-message-service"></a>Conception d’un service de messagerie

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avant de commencer à écrire du code pour prendre en charge votre service de message, il est important de créer une conception. Résolvez les problèmes suivants dans votre processus de conception :
  
1. Déterminez le nombre de fournisseurs de services à inclure dans le service de messagerie. Incluez uniquement les fournisseurs de services associés (c’est-à-dire, les fournisseurs qui fonctionnent avec le même système de messagerie) dans votre service. Les fournisseurs de services non liés n’appartiennent pas au même service de messagerie. Utilisez le profil pour l’intégration de fournisseurs de services et de services de messagerie non liés.
    
2. Déterminez le type de fournisseur de services à inclure dans le service de messagerie. La plupart des services de messge incluent un fournisseur de chacun des types courants. Autrement dit, le service de messagerie classique dispose d’un fournisseur de carnet d’adresses, d’un fournisseur de magasins de messages et d’un fournisseur de transport.
    
3. Déterminez le nombre de DLLs qui doivent contenir le service de message. Le nombre de DLL qu’un service de message utilise dépend des facteurs suivants :
    
   - Degré de complexité que vous êtes prêt à gérer en tant qu’auteur du service de message.
    
   - Type de fournisseurs de services dans le service de messagerie.
    
   - Relation que le service de message peut avoir avec un autre service de message.
    
   Étant donné que MAPI stocke un seul point d’entrée pour chaque type de fournisseur, n’incluez pas plusieurs fournisseurs du même type dans une seule DLL. S’il est logique d’inclure plusieurs fournisseurs d’un type, implémentez-les dans des DLL distinctes ou leur faire partager une fonction de point d’entrée. Une autre option consiste à implémenter des services de message associés, ou des services de message qui peuvent utiliser le même code d’installation et de configuration et la même fonction de point d’entrée DLL, dans une DLL.
    
   Si possible, restez simple et utilisez une DLL qui contient l’implémentation de tous les fournisseurs de services dans le service de messagerie et tout le code pour installer et configurer le service de messagerie. Si cela n’est pas possible, vous pouvez implémenter une DLL pour le code d’installation et de configuration et une seule DLL pour tous les fournisseurs de services ou une DLL pour chaque fournisseur.
    
4. Déterminez un nom pour la DLL ou les DLL du service de message. 
    
## <a name="see-also"></a>Voir aussi

- [Implémentation du service de message](message-service-implementation.md)

