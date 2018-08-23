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
ms.openlocfilehash: c6cdb07e1cbe68d90c6dcd9d5418f700ea5abc3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589650"
---
# <a name="handling-mapi-forms"></a>Gestion des formulaires MAPI

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un formulaire MAPI est une visionneuse pour un message d’une classe particulière. Les clients qui autorisent leurs aux utilisateurs de travailler avec des messages appartenant à une variété de classes de message doivent être écrite pour gérer une variété de formulaires MAPI. Pour gérer plusieurs formulaires, clients implémentent un composant appelé une visionneuse de formulaire qui contient les trois objets suivants :
  
- Un objet de site de message, qui prend en charge la [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface. 
    
- Un affichage de notification récepteur, qui prend en charge la [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface. 
    
- Un objet de contexte d’affichage, qui prend en charge la [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface. 
    
Chacun de ces objets est utilisée par un composant appelé le serveur de formulaire qui implémente chaque formulaire, la gestion de son emplacement de stockage et de notifications générées par les clients de gestion de l’affichage. Un autre composant, le fournisseur de bibliothèque de formulaires, implémente un gestionnaire de formulaire. Le Gestionnaire de formulaire gère les bibliothèques de formulaires qui stockent des fichiers exécutables du formulaire serveur. Cette administration comprend du chargement du formulaire adéquat de serveur et gestion de la première communication entre le serveur et le client.
  
Le diagramme suivant illustre la relation entre un client et les autres composants de l’architecture de formulaire MAPI.
  
## <a name="mapi-form-architecture"></a>Architecture de formulaire MAPI
  
![Architecture de formulaire MAPI] (media/forms01.gif "Architecture de formulaire MAPI")
  
Plans de votre client gérer les formulaires MAPI, vous pouvez utiliser le gestionnaire formulaire [IMAPIFormMgr : IUnknown](imapiformmgriunknown.md) interface pour effectuer des tâches de base cinq : 
  
- Lancez le serveur de formulaire MAPI approprié lorsqu’un message est ouvert ou composé.
    
- Afficher les icônes de serveurs formulaire dans les tables de contenu des dossiers.
    
- Envoyer et recevoir des notifications de formulaire. Pour plus d’informations, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).
    
- Autoriser les utilisateurs à installer ou supprimer des serveurs de formulaire à partir de bibliothèques de formulaires. Pour plus d’informations, voir [Gestion d’une bibliothèque de formulaires](maintaining-a-form-library.md).
    
- Autoriser les utilisateurs à associer des serveurs de formulaire à certains dossiers.
    
Pour accéder au Gestionnaire de formulaire, appelez la fonction de [MAPIOpenFormMgr](mapiopenformmgr.md) qu’une seule fois lors de l’initialisation. 
  
## <a name="in-this-section"></a>Dans cette section

- [L’implémentation d’une visionneuse de formulaire](implementing-a-form-viewer.md): explique comment implémenter une visionneuse de formulaire à l’aide d’un affichage de notification récepteur, un site de message et un contexte de vue.
    
- [L’implémentation des verbes formulaire Standard](implementing-standard-form-verbs.md): explique comment implémenter les verbes pour l’utilisateur clique sur de menu ou un bouton sur les formulaires MAPI.
    
- [Envoi et réception des Notifications](sending-and-receiving-form-notifications.md): décrit comment envoyer et recevoir des notifications de formulaire.
    
- [Maintenance d’une bibliothèque de formulaires](maintaining-a-form-library.md): décrit comment mettre à jour d’une bibliothèque qui contient toutes les informations importantes sur un formulaire.
    
- [Chargement d’un Message dans un formulaire](loading-a-message-into-a-form.md): décrit comment charger un message dans un formulaire.
    
- [Composer un nouveau Message à l’aide d’un formulaire](composing-a-new-message-by-using-a-form.md): explique comment créer un message à l’aide d’un formulaire.
    
- [Afficher les icônes de formulaire](displaying-form-icons.md): décrit les étapes pour l’affichage d’une icône avec un formulaire.
    
## <a name="see-also"></a>Voir aussi

- [Formulaires MAPI](mapi-forms.md)
- [Développement de serveurs de formulaires MAPI](developing-mapi-form-servers.md)

