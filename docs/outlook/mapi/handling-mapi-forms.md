---
title: Gestion des formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c1589d49-2ebe-48ce-85c7-b70fb7c1bb67
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 91347f0c34b8d7b76e4e456397a1faa061f3b2c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423054"
---
# <a name="handling-mapi-forms"></a>Gestion des formulaires MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un formulaire MAPI est une visionneuse pour un message d’une classe particulière. Les clients qui permettent à leurs utilisateurs de travailler avec des messages appartenant à diverses classes de messages doivent être écrits pour gérer une variété de formulaires MAPI. Pour gérer plusieurs formulaires, les clients implémentent un composant appelé visionneuse de formulaires qui contient les trois objets suivants :
  
- Objet de site de message, qui prend en charge l’interface [IMAPIMessageSite : IUnknown.](imapimessagesiteiunknown.md) 
    
- Un sink de conseil d’affichage, qui prend en charge [l’interface IMAPIViewAdviseSink : IUnknown.](imapiviewadvisesinkiunknown.md) 
    
- Objet de contexte d’affichage, qui prend en charge l’interface [IMAPIViewContext : IUnknown.](imapiviewcontextiunknown.md) 
    
Chacun de ces objets est utilisé par un composant appelé serveur de formulaires qui implémente chaque formulaire, qui gère son stockage et les notifications générées par les clients qui gèrent l’affichage. Un autre composant, le fournisseur de bibliothèque de formulaires, implémente un gestionnaire de formulaires. Le gestionnaire de formulaires administre les bibliothèques de formulaires, qui stockent les fichiers exécutables du serveur de formulaires. Cette administration inclut le chargement du serveur de formulaire approprié et la gestion de la communication initiale entre le serveur et le client.
  
Le diagramme suivant illustre la relation entre un client et les autres parties de l’architecture de formulaire MAPI.
  
## <a name="mapi-form-architecture"></a>Architecture de formulaire MAPI
  
![Architecture de formulaire MAPI - Architecture](media/forms01.gif "de formulaire MAPI")
  
Si votre client prévoit de gérer des formulaires MAPI, vous utiliserez l’interface [IMAPIFormMgr : IUnknown](imapiformmgriunknown.md) du gestionnaire de formulaires pour effectuer cinq tâches de base : 
  
- Lancez le serveur de formulaire MAPI approprié lorsqu’un message est ouvert ou composé.
    
- Afficher les icônes des serveurs de formulaires dans les tables de contenu des dossiers.
    
- Envoyer et recevoir des notifications de formulaire. Pour plus d’informations, voir [Envoyer et recevoir des notifications de formulaire.](sending-and-receiving-form-notifications.md)
    
- Autoriser les utilisateurs à installer ou à supprimer des serveurs de formulaires des bibliothèques de formulaires. Pour plus d’informations, [voir Maintenance d’une bibliothèque de formulaires.](maintaining-a-form-library.md)
    
- Autoriser les utilisateurs à associer des serveurs de formulaires à des dossiers particuliers.
    
Pour accéder au gestionnaire de formulaires, appelez la [fonction MAPIOpenFormMgr](mapiopenformmgr.md) une fois lors de l’initialisation. 
  
## <a name="in-this-section"></a>Dans cette section

- [Mise en œuvre d’une](implementing-a-form-viewer.md)visionneuse de formulaires : décrit comment implémenter une visionneuse de formulaires à l’aide d’un sink de conseil d’affichage, d’un site de message et d’un contexte d’affichage.
    
- [Implémentation des verbes de](implementing-standard-form-verbs.md)formulaire standard : décrit comment implémenter les verbes pour les clics de menu ou de bouton utilisateur sur les formulaires MAPI.
    
- [Envoi et réception de notifications de formulaire :](sending-and-receiving-form-notifications.md)décrit comment envoyer et recevoir des notifications de formulaire.
    
- [Maintenance d’une bibliothèque de](maintaining-a-form-library.md)formulaires : décrit comment gérer une bibliothèque qui contient toutes les informations importantes sur un formulaire.
    
- [Chargement d’un message dans un formulaire](loading-a-message-into-a-form.md): décrit comment charger un message dans un formulaire.
    
- [Composition d’un nouveau message à l’aide d’un formulaire](composing-a-new-message-by-using-a-form.md): décrit comment composer un message à l’aide d’un formulaire.
    
- [Affichage des icônes de formulaire](displaying-form-icons.md): décrit les étapes d’affichage d’une icône avec un formulaire.
    
## <a name="see-also"></a>Voir aussi

- [Formulaires MAPI](mapi-forms.md)
- [Développement de serveurs de formulaire MAPI](developing-mapi-form-servers.md)

