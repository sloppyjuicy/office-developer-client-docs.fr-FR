---
title: Implémentation d'une visionneuse de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: bbd0792b0e3e3f274797fabd7f5d5eb49cfc73fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332892"
---
# <a name="implementing-a-form-viewer"></a>Implémentation d'une visionneuse de formulaires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une visionneuse de formulaires comprend trois objets: un site de messagerie, un récepteur de notification d'affichage et un contexte d'affichage. Chacun de ces objets vous permet d'interagir avec un serveur de formulaires et ses formulaires.
  
Un site de messagerie est un objet qui implémente l'interface [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) et qui assiste les serveurs de formulaire avec des tâches telles que le mouvement, l'enregistrement ou la suppression de messages, la création de nouveaux messages ou le lancement de nouveaux serveurs de formulaires. Les sites de messagerie sont utilisés par les formulaires pour obtenir des informations sur l'état de votre client par rapport à différents fournisseurs de services. Par exemple, un formulaire peut utiliser votre site de messagerie pour obtenir un pointeur vers votre banque de messages actuelle, un message ou un dossier. 
  
Il existe deux types de méthodes dans l'interface **IMAPIMessageSite** : 
  
- Méthodes qui fournissent des informations pour former des objets.
    
- Méthodes qui manipulent les messages.
    
Les méthodes qui fournissent des informations aux objets de formulaire sont faciles à mettre en œuvre. Dans tous les cas, à l'exception de [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md), vous devez déjà disposer des informations requises par chaque méthode.
  
Les méthodes qui manipulent les messages doivent agir comme si elles avaient été déclenchées via votre interface utilisateur normale. Par exemple, si un objet Form appelle votre méthode [IMAPIMessageSite:: newMessage,](imapimessagesite-newmessage.md) , se comporte comme si l'utilisateur avait choisi de composer un nouveau message personnalisé avec votre interface utilisateur normale. Les commandes qui génèrent généralement ce comportement sont **composer**, **ouvrir**, **répondre**, **répondre à tous les destinataires**et **transférer**. 
  
Un contexte de vue est un objet qui implémente l'interface [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) et fournit aux serveurs de formulaires un contexte pour le message en cours, ce qui permet aux serveurs de basculer facilement vers le message suivant ou précédent dans le dossier. Un formulaire utilise un contexte d'affichage pour partager des informations. Avec un objet Context View, un formulaire peut: 
  
- Inscrivez-vous avec votre client pour les notifications.
    
- Activer le message suivant ou précédent dans le dossier.
    
- Obtenir des informations sur l'impression.
    
- Obtenir l'état de votre client.
    
- Obtenir un flux qui peut être utilisé pour enregistrer la version texte d'un message.
    
À l'inStar des méthodes de l'interface [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) , les méthodes de **IMAPIViewContext** correspondent aux actions de l'utilisateur et aux fonctionnalités clientes qui sont liées au contexte d'affichage. Par exemple, un contexte d'affichage implique l'activation du message suivant ou précédent, le tri du contenu du dossier et le filtrage du contenu du dossier. 
  
Il n'est pas important de déterminer le mécanisme que vous fournissez aux utilisateurs pour activer ces fonctionnalités, il est uniquement important que la sémantique de ces fonctionnalités mappe bien aux méthodes de l'interface **IMAPIViewContext** . 
  
Un récepteur de notification d'affichage est un objet qui implémente l'interface [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) et gère les notifications à partir de serveurs de formulaires qui affectent votre visionneuse et les formulaires d'aide et les visionneuses de formulaire pour fonctionner ensemble. Pour plus d'informations, consultez la rubrique [envoi et réception](sending-and-receiving-form-notifications.md)de notifications de formulaire. 
  

