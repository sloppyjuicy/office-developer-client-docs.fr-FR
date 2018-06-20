---
title: Gestionnaire de formulaire MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d12d879ea5a82c5e0e3978d90694b3851aaac5cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784606"
---
# <a name="mapi-form-manager"></a>Gestionnaire de formulaire MAPI

  
  
**S’applique à**: Outlook 
  
Un gestionnaire de formulaire est un objet qui implémente l’interface [IMAPIFormMgr](imapiformmgriunknown.md) . La plupart des organisations utiliseront le Gestionnaire de formulaire fourni avec MAPI, appelé le Gestionnaire de formulaire par défaut. Toutefois, une organisation peut remplacer le Gestionnaire de formulaire par défaut avec un gestionnaire de formulaire personnalisé si vous le souhaitez. Le Gestionnaire de formulaire se charge de localisation des formulaires dans les bibliothèques de formulaires, le chargement des formulaires en réponse aux requêtes des utilisateurs et l’installation de formulaires dans la bibliothèque de formulaires local, bibliothèque de formulaires de dossier ou bibliothèque de formulaires personnels d’un utilisateur. 
  
Pour un utilisateur d’interagir avec un message, une instance du serveur de formulaire pour la classe de message du message doit être créée et activée pour afficher le message et d’effectuer l’opération demandée dans le message. Comme décrit dans la rubrique [Bibliothèques de formulaires MAPI](mapi-form-libraries.md), mise en œuvre d’un formulaire peut exister dans plusieurs emplacements (bibliothèques de formulaires) et il n’existe aucune garantie qu’un formulaire ou à son serveur sera disponible localement ou en cours d’exécution d’état lorsqu’un utilisateur souhaite interagir avec lui. Le Gestionnaire de formulaire prend en charge les détails de localisation et d’activation du formulaire.
  
Clients utilisent les services fournis par le Gestionnaire de formulaire pour rechercher et d’activer les formulaires. L’interface **IMAPIFormMgr** est implémentée par le Gestionnaire de formulaire et est appelé par les clients pour accéder à ses services. Le Gestionnaire de formulaire est un composant essentiel, car il masque presque tous les détails de la recherche et activer des formulaires à partir de clients de messagerie. 
  
Lors du chargement des serveurs de formulaire, le Gestionnaire de formulaire par défaut charge le formulaire à partir de la première bibliothèque de formulaires dans laquelle se trouve une implémentation de la classe de message du formulaire. Le Gestionnaire de formulaire par défaut recherche les bibliothèques de formulaires dans l’ordre suivant :
  
1. Bibliothèque de formulaires local de l’utilisateur. Cette bibliothèque de formulaires est recherchée en premier, car elle fournit un accès rapide à l’implémentation d’un formulaire si l’implémentation est installée dans la bibliothèque de formulaires local.
    
2. La bibliothèque de formulaires dossier du conteneur du message : le dossier dans lequel est stocké le message en cours de chargement.
    
3. Bibliothèque de formulaires personnels de l’utilisateur.
    
Un gestionnaire de formulaire personnalisé peut rechercher les bibliothèques de formulaires disponibles dans n’importe quel ordre, ou peut implémenter des autres bibliothèques de formulaires, par exemple une bibliothèque de formulaires de l’organisation. Pour plus d’informations sur les bibliothèques de formulaires, voir [Bibliothèques de formulaires MAPI](mapi-form-libraries.md). 
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

