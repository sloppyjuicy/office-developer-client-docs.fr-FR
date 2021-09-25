---
title: Mise en œuvre d’une visionneuse de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 624bc14887f05052f69776d9862716bab3c9e47f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567353"
---
# <a name="implementing-a-form-viewer"></a>Mise en œuvre d’une visionneuse de formulaires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une visionneuse de formulaires comprend trois objets : un site de message, un sink de conseil d’affichage et un contexte d’affichage. Chacun de ces objets vous permet d’interagir avec un serveur de formulaires et ses formulaires.
  
Un site de message est un objet qui implémente l’interface [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) et aide les serveurs de formulaires à effectuer des tâches telles que le déplacement, l’enregistrement ou la suppression de messages, la création de nouveaux messages ou le lancement de serveurs de formulaires. Les sites de messages sont utilisés par des formulaires pour obtenir des informations sur l’état de votre client par rapport à différents fournisseurs de services. Par exemple, un formulaire peut utiliser votre site de message pour obtenir un pointeur vers votre magasin de messages actuel, un message ou un dossier. 
  
Il existe deux types de méthodes dans l’interface **IMAPIMessageSite** : 
  
- Méthodes qui fournissent des informations aux objets de formulaire.
    
- Méthodes qui manipulent des messages.
    
Les méthodes qui fournissent des informations aux objets de formulaire sont simples à implémenter. Dans tous les cas, à l’exception de [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), vous devez déjà avoir les informations requises par chaque méthode.
  
Les méthodes qui manipulent les messages doivent agir comme si elles avaient été déclenchées via votre interface utilisateur normale. Par exemple, si un objet de formulaire appelle votre méthode [IMAPIMessageSite::NewMessage,](imapimessagesite-newmessage.md) se comporte comme si l’utilisateur avait choisi de composer un nouveau message personnalisé avec votre interface utilisateur normale. Les commandes qui génèrent généralement ce comportement sont **Composer,** **Ouvrir,** **Répondre,** Répondre à tous les **destinataires** et **Forward**. 
  
Un contexte d’affichage est un objet qui implémente l’interface [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) et fournit aux serveurs de formulaires un contexte pour le message actuel, ce qui permet aux serveurs de passer facilement au message suivant ou précédent dans le dossier. Un formulaire utilise un contexte d’affichage pour le partage d’informations. Avec un objet de contexte d’affichage, un formulaire peut : 
  
- Inscrivez-vous auprès de votre client pour recevoir des notifications.
    
- Activez le message suivant ou précédent dans le dossier.
    
- Obtenir des informations d’impression.
    
- Obtenir l’état de votre client.
    
- Obtenez un flux qui peut être utilisé pour enregistrer la version texte d’un message.
    
Similaires aux méthodes de l’interface [IMAPIMessageSite : IUnknown,](imapimessagesiteiunknown.md) les méthodes dans **IMAPIViewContext** correspondent aux actions de l’utilisateur et aux fonctionnalités clientes liées au contexte d’affichage. Par exemple, un contexte d’affichage est impliqué dans l’activation du message suivant ou précédent, le tri du contenu du dossier et le filtrage du contenu du dossier. 
  
Il n’est pas important de savoir quel mécanisme vous fournissez aux utilisateurs pour activer ces fonctionnalités, mais il est important que la sémantique de ces fonctionnalités soit bien m me aux méthodes de l’interface **IMAPIViewContext.** 
  
Un réception de conseil d’affichage est un objet qui implémente l’interface [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) et gère les notifications provenant de serveurs de formulaires qui affectent votre visionneuse et aident les utilisateurs de formulaires et de formulaires à collaborer. Pour plus d’informations, voir [Envoyer et recevoir des notifications de formulaire.](sending-and-receiving-form-notifications.md) 
  

