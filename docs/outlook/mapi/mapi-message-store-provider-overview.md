---
title: Vue d’ensemble du fournisseur MAPI message magasin
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eae44469-b217-4d05-b47f-5a0b1fab7056
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 614d9ab1037f0fc2735112801e30e530bfafe4db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569070"
---
# <a name="mapi-message-store-provider-overview"></a>Vue d’ensemble du fournisseur MAPI message magasin
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournisseurs de magasins message gérer le stockage et la récupération de messages et d’autres informations pour les utilisateurs d’applications clientes. Les informations du message sont organisées à l’aide d’un système hiérarchique appelé une banque de messages. La banque de messages est implémentée dans plusieurs niveaux, avec des conteneurs appelés dossiers contiennent des messages de différents types. Il n’existe aucune limite au nombre de niveaux dans une banque de messages ; les dossiers peuvent contenir le nombre de sous-dossiers. 
  
L’illustration suivante montre l’architecture de banque de messages hiérarchique.
  
**Architecture de banque de messages**
  
![Architecture de banque de messages] (media/amapi_03.gif "Architecture de banque de messages")
  
L’illustration montre deux dossiers, avec un sous-dossier. Utilisateurs d’applications clientes peuvent accéder à une vue récapitulative des messages contenus dans chaque dossier ou les consulter individuellement avec un formulaire. Si le client affiche un formulaire standard MAPI fournit ou un formulaire personnalisé qui fournit un développeur de formulaire varie selon le type ou la classe du message. Le premier dossier contient des remarques et utilise le formulaire de note standard MAPI. Le deuxième dossier contient les messages de demande d’inventaire et utilise un formulaire personnalisé inventaire. Les informations sur les deux formes représentent les propriétés du message.
  
Vous pouvez utiliser les données du magasin de message dans de diverses façons. Outre l’utilisation de données pour la messagerie électronique classique, vous pouvez utiliser les dossiers comme un forum de discussion publics, comme un référentiel de documents de référence, ou en tant que conteneur pour la messagerie vocale, calendrier, contacts ou tâches, par exemple. Une banque de messages unique peut contenir plusieurs types d’informations. Plusieurs clients peuvent installer la même base de messages. Cela permet le partage de données simple et rapide. 
  
Dossiers de banque de messages vous permettent de trier et filtrer les messages et de personnaliser l’affichage des messages dans une interface utilisateur. Liens vers les messages filtrés sont stockés dans des dossiers spéciaux appelés dossiers de résultats de recherche. L’utilisateur d’une application cliente entre les critères de filtrage qui MAPI fait référence à une restriction, et les critères est appliquée aux messages stockés dans un ou plusieurs dossiers. Par exemple, un utilisateur peut souhaiter afficher uniquement les messages qui traitent un sujet particulier et ont dates d’arrivée qui sont le plus récents que la dernière semaine. Références pour les messages qui correspondent aux critères sont répertoriés dans le dossier de recherche et les messages réels restent dans leurs dossiers standard.
  
Les messages sont les unités de données qui sont transférées à partir d’un utilisateur ou une application à un autre utilisateur ou l’application. Chaque message contient certains texte du message, avec la mise en forme simple ou complexe et les informations d’enveloppe de message qui sont utilisées pour la transmission. Certains messages contiennent une ou plusieurs pièces jointes, ou des données supplémentaires relatives aux transportés avec un message sous la forme d’un fichier, un autre message ou un objet OLE. 
  
Selon le message le fournisseur de magasins, un utilisateur peut enregistrer un nouveau message en cours d’écriture en outre aux messages qui ont été envoyés ou reçus. Les messages peuvent être copiés ou déplacés d’un dossier à un autre avec chaque copie de devenir un message distinct qui peut être copié, supprimé ou modifié individuellement. Une autre fonctionnalité que fournisseurs activer la base de certains messages est la capacité pour modifier un message après avoir été reçu et est stockée dans son dossier. Un utilisateur peut tirer parti de cette fonctionnalité pour faire pivoter un message de télécopie reçus de haut en bas. L’utilisateur peut enregistrer l’affichage approprié dans le dossier pour les consulter ultérieurement. 
  
## <a name="see-also"></a>Voir aussi

- [Architecture et des fonctionnalités MAPI](mapi-features-and-architecture.md)

