---
title: Gestionnaire de formulaire MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
ms.openlocfilehash: 2e7fa6dfc9b0d4fae30ce781272f0bc017ac0f3a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369111"
---
# <a name="mapi-form-manager"></a>Gestionnaire de formulaire MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un gestionnaire de formulaires est un objet qui implémente l’interface [IMAPIFormMgr](imapiformmgriunknown.md) . La plupart des organisations utilisent le gestionnaire de formulaires fourni avec MAPI, appelé gestionnaire de formulaires par défaut. Toutefois, une organisation peut remplacer le gestionnaire de formulaires par défaut par un gestionnaire de formulaires personnalisé si vous le souhaitez. Le gestionnaire de formulaires s’occupe de la localisation des formulaires dans les bibliothèques de formulaires, du chargement des formulaires en réponse aux demandes des utilisateurs et de l’installation des formulaires dans la bibliothèque de formulaires locale, la bibliothèque de formulaires de dossiers ou la bibliothèque de formulaires personnels d’un utilisateur. 
  
Pour qu’un utilisateur interagisse avec un message, une instance du serveur de formulaires pour la classe de message du message doit être créée et activée pour afficher le message et effectuer l’opération demandée sur le message. Comme décrit dans la rubrique [Bibliothèques de formulaires MAPI](mapi-form-libraries.md), l’implémentation d’un formulaire peut exister à différents emplacements (bibliothèques de formulaires) et il n’est pas garanti qu’un formulaire ou son serveur sera disponible localement ou dans un état d’exécution lorsqu’un utilisateur souhaite interagir avec celui-ci. Le gestionnaire de formulaires s’occupe des détails de la localisation et de l’activation du formulaire.
  
Les clients utilisent les services fournis par le gestionnaire de formulaires pour rechercher et activer des formulaires. **L’interface IMAPIFormMgr** est implémentée par le gestionnaire de formulaires et est appelée par les clients pour accéder à ses services. Le gestionnaire de formulaires est un composant essentiel, car il masque presque tous les détails de recherche et d’activation des formulaires des clients de messagerie. 
  
Lors du chargement des serveurs de formulaires, le gestionnaire de formulaires par défaut charge le formulaire à partir de la première bibliothèque de formulaires dans laquelle une implémentation de la classe de message du formulaire est trouvée. Le gestionnaire de formulaires par défaut recherche les bibliothèques de formulaires dans l’ordre suivant :
  
1. Bibliothèque de formulaires locale de l’utilisateur. Cette bibliothèque de formulaires est d’abord recherché, car elle fournit l’accès le plus rapide à l’implémentation d’un formulaire si l’implémentation est installée dans la bibliothèque de formulaires locale.
    
2. Bibliothèque de formulaires de dossiers du conteneur du message : le dossier dans lequel le message en cours de chargement est stocké.
    
3. Bibliothèque de formulaires personnels de l’utilisateur.
    
Un gestionnaire de formulaires personnalisé peut effectuer des recherches dans les bibliothèques de formulaires disponibles dans n’importe quel ordre ou implémenter d’autres bibliothèques de formulaires telles qu’une bibliothèque de formulaires à l’échelle de l’organisation. Pour plus d’informations sur les bibliothèques de formulaires, voir [MAPI Form Libraries](mapi-form-libraries.md). 
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

