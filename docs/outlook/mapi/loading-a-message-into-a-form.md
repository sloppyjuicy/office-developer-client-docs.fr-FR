---
title: Chargement d'un message dans un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: afecd3b334dd2cf7b2953916872982e6459a8434
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355744"
---
# <a name="loading-a-message-into-a-form"></a>Chargement d'un message dans un formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour charger un message existant dans un formulaire à l'aide d'un serveur de formulaires, utilisez l'une des stratégies suivantes.
  
- Appelez [IMAPISession::P repareform](imapisession-prepareform.md) pour créer un jeton, puis [IMAPISession:: ShowForm](imapisession-showform.md) pour afficher le formulaire. 
    
- Appelez [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md). 
    
L'utilisation de la stratégie **PrepareForm** et **ShowForm** est relativement facile, mais elle génère des formulaires modaux par rapport à votre client. Cela est dû au fait que l'appel à **ShowForm** ne renvoie pas tant que le formulaire n'est pas sorti. Si vous devez gérer les formulaires de manière asynchrone, n'utilisez pas cette stratégie. 
  
L'utilisation de la stratégie **LoadForm** est plus difficile, car la méthode nécessite plusieurs paramètres. Ces paramètres indiquent au gestionnaire de formulaires de lancer le serveur de formulaires approprié dans le contexte approprié et d'afficher le message approprié. Si le serveur de formulaires est déjà en cours d'exécution, le gestionnaire de formulaires charge le message dans le serveur de formulaire sans lancer une nouvelle instance du serveur de formulaires. 
  
Pour spécifier le serveur de formulaires à lancer, transmettez la classe de message gérée par le serveur cible dans le contenu du paramètre _lpszMessageClass_ . La classe de message appropriée peut être déterminée en récupérant la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) du message à charger. Parfois, il n'existe pas de serveur de formulaires pour la classe de message spécifiée, mais uniquement un serveur de formulaires qui gère les messages appartenant à la superclasse du message. Si vous préférez que le message soit chargé uniquement par un serveur de formulaires spécialement conçu pour gérer les messages de cette classe, définissez l'indicateur MAPIFORM_EXACTMATCH dans l'appel **LoadForm** . Pour plus d'informations, consultez la rubrique [MAPI message classes](mapi-message-classes.md).
  
 **LoadForm** nécessite également un pointeur vers le site de messages de votre visionneuse et le contexte d'affichage, ainsi que la valeur pour le **PR_MSG_STATUS** du message cible ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) et **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) Propriétés.
  

