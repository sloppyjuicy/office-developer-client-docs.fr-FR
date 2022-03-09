---
title: Chargement d’un message dans un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
ms.openlocfilehash: 46fb39e8fdd45d69a5e6f118a4ffa64b9f68fb27
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371246"
---
# <a name="loading-a-message-into-a-form"></a>Chargement d’un message dans un formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour charger un message existant dans un formulaire à l’aide d’un serveur de formulaires, utilisez l’une des stratégies suivantes.
  
- Appelez [IMAPISession::P repareForm](imapisession-prepareform.md) pour créer un jeton, puis [IMAPISession::ShowForm](imapisession-showform.md) pour afficher le formulaire. 
    
- [Appelez IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md). 
    
L’utilisation **de la stratégie PrepareForm** et **ShowForm** est relativement simple, mais elle se traduit par des formulaires modaux par rapport à votre client. Cela est dû au fait que l’appel **à ShowForm** ne revient pas tant que le formulaire n’est pas sorti. Si vous devez gérer les formulaires de manière asynchrone, n’utilisez pas cette stratégie. 
  
L’utilisation **de la stratégie LoadForm** est plus difficile, car la méthode nécessite plusieurs paramètres. Ces paramètres indiquent au gestionnaire de formulaire de lancer le serveur de formulaires approprié dans le contexte approprié et d’afficher le message approprié. Si le serveur de formulaires est déjà en cours d’exécution, le gestionnaire de formulaire charge le message dans le serveur de formulaires sans lancer une nouvelle instance du serveur de formulaires. 
  
Pour spécifier le serveur de formulaire à lancer, passez la classe de message gérée par le serveur cible dans le contenu du  _paramètre lpszMessageClass_ . La classe de message appropriée peut être déterminée en récupérant la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) du message à charger. Parfois, il n’existe pas de serveur de formulaires pour la classe de message spécifiée, uniquement un serveur de formulaires qui gère les messages appartenant à la superclasse du message. Si vous préférez que le message soit chargé uniquement par un serveur de formulaires spécifiquement destiné à gérer les messages de cette classe, définissez l’indicateur MAPIFORM_EXACTMATCH dans **l’appel LoadForm** . Pour plus d’informations, voir [CLASSES de message MAPI](mapi-message-classes.md).
  
 **LoadForm** nécessite également un pointeur vers le site de message de votre visionneuse et le contexte d’affichage, ainsi que la valeur des propriétés **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) et **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message cible.
  

