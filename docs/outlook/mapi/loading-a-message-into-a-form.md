---
title: Chargement d’un Message dans un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d677958b1a429201c05b5195c58bd7462d0f3d37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784523"
---
# <a name="loading-a-message-into-a-form"></a>Chargement d’un Message dans un formulaire

  
  
**S’applique à**: Outlook 
  
Pour charger un message existant dans un formulaire à l’aide d’un serveur de formulaire, utilisez une des stratégies suivantes.
  
- Appelez [IMAPISession::PrepareForm](imapisession-prepareform.md) pour créer un jeton et puis [IMAPISession::ShowForm](imapisession-showform.md) pour afficher le formulaire. 
    
- Appelez [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md). 
    
À l’aide de la stratégie **PrepareForm** et **ShowForm** est relativement simple, mais il les résultats dans les formulaires sont modales par rapport à votre client. Il s’agit, car l’appel vers **ShowForm** ne retourne pas jusqu'à ce que le formulaire s’est arrêté. Si vous avez besoin gérer les formulaires en mode asynchrone, n’utilisez pas cette stratégie. 
  
À l’aide de la stratégie **LoadForm** est plus difficile, car la méthode requiert plusieurs paramètres. Ces paramètres indiquer au Gestionnaire de formulaire pour lancer le formulaire correct de serveur dans le contexte approprié et afficher le message approprié. Si le serveur de formulaire est en cours d’exécution, le Gestionnaire de formulaire charge le message sur le serveur de formulaire sans lancer une nouvelle instance du serveur de formulaire. 
  
Pour spécifier le serveur de formulaire à la barre de lancement, passez à la classe de message gérée par le serveur cible dans le contenu du paramètre _lpszMessageClass_ . La classe de message approprié peut être déterminée en récupérant la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) du message à charger. Il n’est parfois aucun serveur de formulaire pour la classe de message spécifiée uniquement un serveur de formulaire qui gère les messages de la superclasse du message. Si vous préférez que le message d’être chargé uniquement par un serveur de formulaire spécifiquement conçu pour gérer les messages de cette classe, définir l’indicateur MAPIFORM_EXACTMATCH dans l’appel **LoadForm** . Pour plus d’informations, consultez [Classes de Message MAPI](mapi-message-classes.md).
  
 **LoadForm** requiert également un pointeur vers le site de messagerie de l’afficheur et contexte d’affichage et la valeur du message cible **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) et **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) Propriétés.
  

