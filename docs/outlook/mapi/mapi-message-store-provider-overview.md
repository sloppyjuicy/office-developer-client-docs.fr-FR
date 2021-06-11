---
title: Vue d’ensemble du fournisseur de magasin de messages MAPI
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
# <a name="mapi-message-store-provider-overview"></a>Vue d’ensemble du fournisseur de magasin de messages MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de magasins de messages gèrent le stockage et la récupération des messages et d’autres informations pour les utilisateurs d’applications clientes. Les informations de message sont organisées à l’aide d’un système hiérarchique appelé magasin de messages. La magasin de messages est implémentée dans plusieurs niveaux, avec des conteneurs appelés dossiers contenant des messages de différents types. Il n’existe aucune limite au nombre de niveaux dans une magasin de messages ; peuvent contenir de nombreux sous-dossiers. 
  
L’illustration suivante illustre l’architecture hiérarchique de la boutique de messages.
  
**Architecture de banque de messages**
  
![Architecture de la boutique de messages -]Architecture de la boutique de(media/amapi_03.gif "messages")
  
La figure montre deux dossiers, un avec un sous-dossier. Les utilisateurs de l’application cliente peuvent accéder à un affichage récapitulatif des messages contenus dans chaque dossier ou les afficher individuellement avec un formulaire. Le fait que le client affiche un formulaire standard que MAPI fournit ou un formulaire personnalisé qu’un développeur de formulaire fournit dépend du type ou de la classe du message. Le premier dossier contient les messages de note et utilise le formulaire de note standard MAPI. Le deuxième dossier contient les messages de demande d’inventaire et utilise un formulaire d’inventaire personnalisé. Les informations des deux formulaires représentent les propriétés du message.
  
Vous pouvez utiliser les données de la boutique de messages de différentes manières. Outre l’utilisation de données pour la messagerie électronique traditionnelle, vous pouvez utiliser des dossiers comme forum de discussion publique, comme référentiel de documents de référence ou comme conteneur pour la messagerie vocale, le calendrier, les contacts ou les tâches, par exemple. Une seule magasin de messages peut contenir de nombreux types d’informations. Plusieurs clients peuvent installer la même magasin de messages. Le partage des données est ainsi facile et rapide. 
  
Les dossiers de la boutique de messages vous permettent de trier et de filtrer des messages et de personnaliser l’affichage des messages dans une interface utilisateur. Les liens vers les messages filtrés sont placés dans des dossiers spéciaux appelés dossiers de résultats de recherche. L’utilisateur d’une application cliente entre des critères de filtrage, que MAPI appelle une restriction, et les critères sont appliqués aux messages stockés dans un ou plusieurs dossiers. Par exemple, un utilisateur peut vouloir afficher uniquement les messages qui traitent d’un sujet particulier et dont les dates d’arrivée sont plus récentes que la semaine dernière. Les références aux messages qui correspondent aux critères sont répertoriées dans le dossier de recherche et les messages réels restent dans leurs dossiers habituels.
  
Les messages sont les unités de données transférées d’un utilisateur ou d’une application vers un autre utilisateur ou une autre application. Chaque message contient du texte de message, avec une mise en forme simple ou complexe, ainsi que des informations d’enveloppe de message utilisées pour la transmission. Certains messages incluent une ou plusieurs pièces jointes, ou des données supplémentaires liées à un message et transporté avec celui-ci sous la forme d’un fichier, d’un autre message ou d’un objet OLE. 
  
Selon le fournisseur de la boutique de messages, un utilisateur peut enregistrer un nouveau message en cours d’écriture en plus des messages qui ont été envoyés ou reçus. Les messages peuvent être copiés ou déplacés d’un dossier vers un autre, chaque copie devient un message distinct qui peut être copié, supprimé ou modifié individuellement. Une autre fonctionnalité activée par certains fournisseurs de magasins de messages est la possibilité de modifier un message après sa réception et de le stocker dans son dossier. Un utilisateur peut tirer parti de cette fonctionnalité pour faire pivoter un message de télécopie arrivé à l’envers. L’utilisateur peut stocker la vue correcte dans le dossier pour un affichage ultérieur. 
  
## <a name="see-also"></a>Voir aussi

- [Fonctionnalités et architecture MAPI](mapi-features-and-architecture.md)

