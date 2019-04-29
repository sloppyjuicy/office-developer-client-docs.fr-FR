---
title: Gestionnaire de formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3059183103ca2552505486b5ec54366729ae4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430195"
---
# <a name="mapi-form-manager"></a>Gestionnaire de formulaires MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un gestionnaire de formulaires est un objet qui implémente l'interface [IMAPIFormMgr](imapiformmgriunknown.md) . La plupart des organisations utilisent le gestionnaire de formulaires fourni avec MAPI, appelé gestionnaire de formulaires par défaut. Toutefois, une organisation peut remplacer le gestionnaire de formulaires par défaut par un responsable de formulaire personnalisé si vous le souhaitez. Le gestionnaire de formulaires prend en charge la recherche de formulaires dans les bibliothèques de formulaires, le chargement de formulaires en réponse aux demandes de l'utilisateur et l'installation de formulaires dans la bibliothèque de formulaires locale d'un utilisateur, une bibliothèque de formulaires de dossiers ou une bibliothèque de formulaires personnels. 
  
Pour qu'un utilisateur interagisse avec un message, une instance du serveur de formulaire pour la classe de message du message doit être créée et activée pour afficher le message et exécuter l'opération demandée sur le message. Comme décrit dans la rubrique [bibliothèques de formulaires MAPI](mapi-form-libraries.md), l'implémentation d'un formulaire peut exister à différents emplacements (bibliothèques de formulaires) et il n'est pas garanti qu'un formulaire ou son serveur sera disponible localement ou à l'État en cours d'exécution lorsqu'un utilisateur souhaite interagir avec elle. Le gestionnaire de formulaires prend en charge les détails de la recherche et de l'activation du formulaire.
  
Les clients utilisent les services fournis par le gestionnaire de formulaires pour rechercher et activer des formulaires. L'interface **IMAPIFormMgr** est implémentée par le gestionnaire de formulaires et est appelée par les clients pour accéder à ses services. Le gestionnaire de formulaires est un composant essentiel, car il masque presque tous les détails de la recherche et de l'activation de formulaires à partir de clients de messagerie. 
  
Lors du chargement des serveurs de formulaires, le gestionnaire de formulaires par défaut charge le formulaire à partir de la première bibliothèque de formulaires dans laquelle une implémentation pour la classe de message du formulaire est trouvée. Le gestionnaire de formulaires par défaut recherche les bibliothèques de formulaires dans l'ordre suivant:
  
1. Bibliothèque de formulaires locale de l'utilisateur. Cette bibliothèque de formulaires fait l'objet d'une recherche dans un premier temps, car elle fournit l'accès le plus rapide à l'implémentation d'un formulaire si celle-ci est installée dans la bibliothèque de formulaires locale.
    
2. Bibliothèque de formulaires de dossier du conteneur du message — le dossier dans lequel le message en cours de chargement est stocké.
    
3. Bibliothèque de formulaires personnels de l'utilisateur.
    
Un gestionnaire de formulaires personnalisés peut effectuer des recherches dans les bibliothèques de formulaires disponibles dans n'importe quel ordre ou implémenter d'autres bibliothèques de formulaires telles qu'une bibliothèque de formulaires à l'échelle de l'organisation. Pour plus d'informations sur les bibliothèques de formulaires, consultez la rubrique [bibliothèques de formulaires MAPI](mapi-form-libraries.md). 
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

