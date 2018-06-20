---
title: L’implémentation d’une visionneuse de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 645f98342b4b3ec2bebf3f233f719bd5cae69da9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784151"
---
# <a name="implementing-a-form-viewer"></a>L’implémentation d’une visionneuse de formulaire

  
  
**S’applique à**: Outlook 
  
Une visionneuse de formulaire comprend trois objets : un site de message, un affichage de notification récepteur et un contexte de vue. Chacun de ces objets vous permet d’interagir avec un serveur de la forme et ses formes.
  
Un site de message est un objet qui implémente le [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface et vous aide à des serveurs de formulaire avec des tâches telles que le déplacement, l’enregistrement, la suppression des messages, création de nouveaux messages ou lancement de nouveaux serveurs de formulaire. Sites de message sont utilisés par les formulaires pour obtenir des informations sur l’état de votre client en ce qui concerne les différents fournisseurs de services. Par exemple, un formulaire peut utiliser votre site de message pour obtenir un pointeur vers la banque de messages en cours, un message ou un dossier. 
  
Il existe deux types de méthodes de l’interface **IMAPIMessageSite** : 
  
- Méthodes qui fournissent des informations aux objets du formulaire.
    
- Méthodes qui manipulent des messages.
    
Les méthodes qui fournissent des informations aux objets de formulaire sont faciles à implémenter. Dans tous les cas, à l’exception de [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), vous devez avoir déjà disponibles les informations requises par chaque méthode.
  
Les méthodes qui manipulent des messages doivent agir comme s’ils avaient été déclenchées par le biais de votre interface utilisateur standard. Par exemple, si un objet form appelle votre méthode [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) , se comportent comme si l’utilisateur a choisi de créer un nouveau message personnalisé avec votre interface utilisateur standard. **Composition**, **Ouvrir**, **réponse**, **répondre à tous les destinataires**et **Transférer**se trouvent les commandes qui génèrent généralement ce comportement. 
  
Un contexte de vue est un objet qui implémente le [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface et fournit des serveurs de formulaire avec un contexte pour le message en cours, ce qui permet de serveurs passer rapidement dans le message suivant ou précédent dans le dossier. Un formulaire utilise un contexte de vue pour le partage des informations. Avec un objet de contexte de vue, un formulaire peut : 
  
- Inscrire avec votre client pour les notifications.
    
- Activer le message suivant ou précédent dans le dossier.
    
- Obtenir des informations sur l’impression.
    
- Obtenir l’état de votre client.
    
- Obtenir un flux qui peut être utilisé pour enregistrer la version texte d’un message.
    
Similaire aux méthodes dans le [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, les méthodes de **IMAPIViewContext** mettre en corrélation avec les fonctionnalités de client qui sont associées au contexte de l’affichage et les actions de l’utilisateur. Par exemple, un contexte de vue est impliqué dans le message suivant ou précédent d’activation, trier le contenu du dossier et le filtrage du contenu du dossier. 
  
Il n’est pas important le mécanisme de vous fournissez aux utilisateurs pour activer ces fonctionnalités, il n’est important que la sémantique de ces fonctionnalités correctement mappées sur les méthodes de l’interface **IMAPIViewContext** . 
  
Un affichage de notification récepteur est un objet qui implémente le [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) et gère les notifications à partir des serveurs de formulaire qui affectent vos formulaires de visionneuse et aide et les visionneuses de formulaire de travailler ensemble. Pour plus d’informations, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md). 
  

