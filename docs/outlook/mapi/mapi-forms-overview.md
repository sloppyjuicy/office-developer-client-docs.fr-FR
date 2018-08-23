---
title: Vue d’ensemble des formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 29132f24547dc744efcd6f2b6e4a8f6af87ab53c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574411"
---
# <a name="mapi-forms-overview"></a>Vue d’ensemble des formulaires MAPI
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un formulaire MAPI est une visionneuse pour un message. Chaque message possède une classe de message qui dicte le formulaire particulier qui est utilisé en tant que sa visionneuse. MAPI définit plusieurs classes de message et a mis en œuvre les formulaires pour l’affichage des messages de ces classes. Les développeurs de logiciels clients peuvent créer des formulaires personnalisés pour l’affichage des messages créés à l’aide de nouvelles classes et nouvelles classes de message.
  
Chaque formulaire personnalisé implémente un ensemble de commandes de menus standard, telles que **Ouvrir**, **créer**, **Supprimer**et **réponse**, et un ensemble de commandes qui sont spécifiques à la forme particulière. Certaines des commandes de formulaire sont intégrés dans l’interface utilisateur de l’application cliente lorsque le formulaire est actif ; autres commandes remplacent complètement les commandes client. 
  
L’illustration suivante montre la relation entre les composants MAPI impliqués dans l’aide de formulaires. 
  
**Architecture de formulaire MAPI**
  
![Architecture de formulaire MAPI] (media/forms01.gif "Architecture de formulaire MAPI")
  
Dans le diagramme, notez que le Gestionnaire de formulaire joue un rôle qui est similaire aux autres fournisseurs de services MAPI, même s’il n’est pas un fournisseur de services. Le Gestionnaire de formulaire est une DLL remplaçable qui implémente des interfaces MAPI. Bien que les développeurs peuvent implémenter leur propre responsable de formulaire, la plupart des environnements utiliseront le Gestionnaire de formulaire fourni par Microsoft en raison de la complexité du responsable de l’écran.
  
La liste suivante décrit les composants dans le schéma et leurs relations à d’autres composants :
  
- Client de messagerie : une application qui peut utiliser les objets de formulaire. Le client de messagerie utilise les interfaces de formulaire MAPI pour communiquer avec le Gestionnaire de formulaire pour charger des messages dans les objets de formulaire.
    
- Interfaces de formulaire MAPI : une norme pour la communication entre les composants MAPI qui sont associés aux formulaires.
    
- Gestionnaire de formulaire : la DLL qui utilisent des clients de messagerie pour gérer l’installation des formulaires dans les bibliothèques de formulaires, le chargement des serveurs de formulaire et la communication entre les clients de messagerie et les serveurs de formulaire initiale.
    
- Bibliothèques de formulaires : stockage Permanent pour les fichiers exécutables associés à des serveurs de formulaire.
    
- Serveurs de formulaire : les fichiers exécutables qui implémentent un formulaire. Serveurs de formulaire créent des objets et des interfaces utilisateur pour traiter des messages spécifiques. Ce fichier exécutable est également un serveur OLE et respecte les conventions OLE habituelles.
    
- Objets de formulaire : objets exécution créés par les serveurs de formulaire qui correspondent à des messages spécifiques. Objets de formulaire exécutent dans le même contexte de processus comme serveur de formulaire.
    
Pour plus d’informations sur les composants de formulaire MAPI, voir [Formulaires MAPI](mapi-forms.md).
  
## <a name="see-also"></a>Voir aussi

- [Architecture et des fonctionnalités MAPI](mapi-features-and-architecture.md)

