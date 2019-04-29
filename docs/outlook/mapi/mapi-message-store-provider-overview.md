---
title: Vue d'ensemble du fournisseur de banque de messages MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eae44469-b217-4d05-b47f-5a0b1fab7056
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5d4ef074523cd654c3db2d686494d9a4f864e7cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429312"
---
# <a name="mapi-message-store-provider-overview"></a>Vue d'ensemble du fournisseur de banque de messages MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de banques de messages gèrent le stockage et l'extraction des messages et d'autres informations pour les utilisateurs des applications clientes. Les informations du message sont organisées à l'aide d'un système hiérarchique appelé Banque de messages. La Banque de messages est implémentée à plusieurs niveaux, avec des conteneurs appelés dossiers contenant des messages de types différents. Il n'y a pas de limite au nombre de niveaux dans une banque de messages; les dossiers peuvent contenir de nombreux sous-dossiers. 
  
L'illustration suivante montre l'architecture de la Banque de messages hiérarchique.
  
**Architecture de banque de messages**
  
![Architecture] de la Banque de messages (media/amapi_03.gif "Architecture") de la Banque de messages
  
La figure illustre deux dossiers, un avec un sous-dossier. Les utilisateurs des applications clientes peuvent accéder à une vue récapitulative des messages contenus dans chaque dossier ou les afficher individuellement à l'aide d'un formulaire. Si le client affiche un formulaire standard que les fournitures MAPI ou un formulaire personnalisé fourni par un développeur de formulaires dépend du type ou de la classe du message. Le premier dossier contient les messages de note et utilise le formulaire de note standard MAPI. Le deuxième dossier contient les messages de demande d'inventaire et utilise un formulaire d'inventaire personnalisé. Les informations contenues dans les deux formulaires représentent les propriétés du message.
  
Vous pouvez utiliser des données de banque de messages de différentes manières. Outre l'utilisation de données pour le courrier électronique traditionnel, vous pouvez utiliser des dossiers comme un forum de discussion publique, comme référentiel pour des documents de référence ou comme conteneur pour la messagerie vocale, le calendrier, les contacts ou les tâches, par exemple. Un seul magasin de messages peut contenir de nombreux types d'informations. Plusieurs clients peuvent installer la même Banque de messages. Le partage des données est ainsi facile et rapide. 
  
Les dossiers de banque de messages vous permettent de trier et de filtrer des messages et de personnaliser l'affichage des messages dans une interface utilisateur. Les liens vers les messages filtrés sont conservés dans des dossiers spéciaux appelés dossiers de résultats de recherche. L'utilisateur d'une application cliente entre les critères de filtrage auxquels MAPI fait référence en tant que restriction, et les critères sont appliqués aux messages stockés dans un ou plusieurs dossiers. Par exemple, un utilisateur peut souhaiter afficher uniquement les messages qui concernent un sujet particulier et ont des dates d'arrivée plus récentes que la semaine dernière. Les références aux messages qui répondent aux critères sont répertoriées dans le dossier de recherche, et les véritables messages restent dans leurs dossiers ordinaires.
  
Les messages sont les unités de données transférées à partir d'un utilisateur ou d'une application vers un autre utilisateur ou une autre application. Chaque message contient un texte de message, avec une mise en forme simple ou complexe et des informations d'enveloppe de message utilisées pour la transmission. Certains messages incluent une ou plusieurs pièces jointes, ou des données supplémentaires liées à un message et transportées avec un message sous la forme d'un fichier, d'un autre message ou d'un objet OLE. 
  
En fonction du fournisseur de banque de messages, un utilisateur peut enregistrer un nouveau message en cours d'écriture en plus des messages qui ont été envoyés ou reçus. Les messages peuvent être copiés ou déplacés d'un dossier à un autre, chaque copie devenant un message distinct qui peut être copié, supprimé ou modifié individuellement. La possibilité de modifier un message après qu'il a été reçu et de le stocker dans son dossier est une autre fonctionnalité activée par certains fournisseurs de banques de messages. Un utilisateur peut tirer parti de cette fonctionnalité pour faire pivoter un message de télécopie qui est arrivé à l'envers. L'utilisateur peut stocker l'affichage approprié dans le dossier pour un affichage ultérieur. 
  
## <a name="see-also"></a>Voir aussi

- [Architecture et fonctionnalités MAPI](mapi-features-and-architecture.md)

