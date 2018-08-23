---
title: Envoi et réception de notifications de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7148383c92b59adb9d3783e079e7c5f28c038eac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588992"
---
# <a name="sending-and-receiving-form-notifications"></a>Envoi et réception de notifications de formulaire

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Notifications de formulaire sont utilisées dans MAPI pour faciliter la communication à partir du formulaire à votre afficheur ainsi qu’à partir de votre visionneuse au formulaire.
  
Formulaires envoyer des notifications à votre visionneuse lorsqu’un des événements suivants se produisent :
  
- Le formulaire est fermé.
    
- Un nouveau message est chargé dans le formulaire.
    
- Une opération d’enregistrement est terminée.
    
- Un message est envoyé.
    
Chacun de ces types d’événement correspondent à une méthode particulière dans [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), un des visionneuse de votre formulaire doit implémenter les interfaces. Lorsqu’un événement se produit, le form appelle la méthode **IMAPIViewAdviseSink** correspondante dans l’Afficheur de notification récepteur. Par exemple, lorsqu’un nouveau message arrive que votre afficheur doit inclure dans l’affichage, le formulaire appelle votre méthode [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) . 
  
Implémenter l’affichage de notification récepteur d’une manière qui convient pour votre visionneuse ; Il n’existe aucune mise en œuvre standard. Par exemple, dans **OnNewMessage** vous pouvez mettre à jour l’affichage du tableau de contenu du dossier en cours d’inclure le message qui vient d’arriver. Dans [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), la méthode est appelée lorsque vous recevez un événement de message envoyé, vous pouvez copier le message envoyé à un dossier éléments envoyés.
  
Formulaires de recevoir une notification à partir de votre visionneuse lors d’un changement qui affecte le formulaire et lors du chargement d’un nouveau message. Pour signaler un formulaire, appelez l’une des méthodes de **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) ou [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md). **OnChange** pour communiquer l’état d’appel. Par exemple, si le formulaire affiche le dernier élément dans un dossier lorsqu’un nouveau message arrive, appelez **OnChange** avec l’indicateur VCSTATUS_NEXT pour indiquer le formulaire qu’il est désormais un élément suivant. 
  
Appelez **OnActivateNext** pour le formulaire à l’arrivée d’un nouveau message d’alerte qu’il peut ou ne peut pas être en mesure d’afficher. Passez la classe de message du message à **OnActivateNext**. 
  
Notifications par un objet de formulaire à l’application cliente sont gérées par l’interface de **IMAPIViewAdviseSink** de l’application cliente. Pour plus d’informations, voir [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).
  

