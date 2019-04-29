---
title: Vue d'ensemble des formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4e7d48f6f6a47ce28aa0e1291ccef209b998c18e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432519"
---
# <a name="mapi-forms-overview"></a>Vue d'ensemble des formulaires MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un formulaire MAPI est une visionneuse pour un message. Chaque message a une classe de message qui régit le formulaire particulier utilisé comme afficheur. MAPI définit plusieurs classes de message et a implémenté les formulaires pour afficher les messages de ces classes. Les développeurs de logiciels clients peuvent créer des classes de message et des formulaires personnalisés pour afficher les messages créés à l'aide des nouvelles classes.
  
Chaque formulaire personnalisé implémente un ensemble de commandes de menu standard, telles que **Open**, **Create**, **Delete**, and **reply**, ainsi qu'un ensemble de commandes propres au formulaire particulier. Certaines commandes de formulaire sont intégrées à l'interface utilisateur de l'application cliente lorsque le formulaire est actif; les autres commandes de formulaire remplacent complètement les commandes client. 
  
L'illustration suivante montre la relation entre les composants MAPI impliqués dans l'utilisation de formulaires. 
  
**Architecture de formulaire MAPI**
  
![Architecture des formulaires MAPI] (media/forms01.gif "Architecture des formulaires MAPI")
  
Dans le diagramme, Notez que le gestionnaire de formulaires joue un rôle semblable aux autres fournisseurs de services MAPI, bien qu'il ne s'agisse pas d'un fournisseur de services lui-même. Le gestionnaire de formulaires est une DLL remplaçable qui implémente certaines interfaces MAPI. Bien que les développeurs puissent implémenter leur propre gestionnaire de formulaires, la plupart des environnements utiliseront le gestionnaire de formulaires fourni par Microsoft en raison de la complexité du gestionnaire de formulaires.
  
La liste suivante décrit les composants du diagramme et leur relation avec d'autres composants:
  
- Client de messagerie: une application qui peut utiliser des objets de formulaire. Le client de messagerie utilise les interfaces de formulaire MAPI pour communiquer avec le gestionnaire de formulaires afin de charger les messages dans les objets Form.
    
- Interfaces de formulaires MAPI: norme définie pour la communication entre les composants MAPI liés aux formulaires.
    
- Gestionnaire de formulaires: DLL utilisée par les clients de messagerie pour gérer l'installation des formulaires dans les bibliothèques de formulaires, le chargement des serveurs de formulaires et la communication initiale entre les clients de messagerie et les serveurs de formulaires.
    
- Bibliothèques de formulaires: stockage permanent pour les fichiers exécutables associés aux serveurs de formulaires.
    
- Serveurs de formulaires: fichiers exécutables qui implémentent un formulaire. Les serveurs de formulaires créent des objets de formulaire et des interfaces utilisateur pour traiter des messages spécifiques. Cet exécutable est également un serveur OLE et respecte les conventions OLE habituelles.
    
- Objets de formulaire: objets d'exécution créés par des serveurs de formulaires qui correspondent à des messages spécifiques. Les objets de formulaire s'exécutent dans le même contexte de processus que leur serveur de formulaires.
    
Pour plus d'informations sur les composants de formulaire MAPI, consultez la rubrique [MAPI Forms](mapi-forms.md).
  
## <a name="see-also"></a>Voir aussi

- [Architecture et fonctionnalités MAPI](mapi-features-and-architecture.md)

