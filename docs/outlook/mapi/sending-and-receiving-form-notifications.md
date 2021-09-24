---
title: Envoi et réception de notifications de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 57a4e4d1a39130e666b786f51c0ea48c7966c656
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550063"
---
# <a name="sending-and-receiving-form-notifications"></a>Envoi et réception de notifications de formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les notifications de formulaire sont utilisées dans MAPI pour faciliter la communication du formulaire à votre visionneuse, ainsi qu’à partir de votre visionneuse vers le formulaire.
  
Les formulaires envoient des notifications à votre visionneuse lorsque l’un des événements suivants se produit :
  
- Le formulaire est fermé.
    
- Un nouveau message est chargé dans le formulaire.
    
- Une opération d’enregistrer est terminée.
    
- Un message est envoyé.
    
Chacun de ces types d’événements correspond à une méthode particulière dans [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), l’une des interfaces que votre visionneuse de formulaire doit implémenter. Lorsqu’un événement se produit, le formulaire appelle la méthode **IMAPIViewAdviseSink** correspondante dans le sink de conseil de votre visionneuse. Par exemple, lorsqu’un nouveau message arrive que votre visionneuse doit inclure dans son affichage, le formulaire appelle votre méthode [IMAPIViewAdviseSink::OnNewMessage.](imapiviewadvisesink-onnewmessage.md) 
  
Implémenter votre affichage conseiller en tant que sink d’une manière qui soit logique pour votre visionneuse ; il n’existe aucune implémentation standard. Par exemple, dans **OnNewMessage,** vous pouvez mettre à jour la vue de la table des matières du dossier actuel pour inclure le message nouvellement arrivé. Dans [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), la méthode qui est appelée lorsque vous recevez un événement de message envoyé, vous pouvez copier le message envoyé dans un dossier Éléments envoyés.
  
Les formulaires reçoivent une notification de votre visionneuse lorsqu’une modification affecte le formulaire et lorsque vous chargez un nouveau message. Pour notifier un formulaire, appelez l’une des méthodes de **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) ou [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md). Appelez **OnChange pour** communiquer l’état. Par exemple, si le formulaire affiche le dernier élément d’un dossier lorsqu’un nouveau message arrive, appelez **OnChange** avec l’indicateur VCSTATUS_NEXT pour indiquer au formulaire qu’il existe désormais un élément suivant. 
  
Appelez **OnActivateNext** pour alerter le formulaire de l’arrivée d’un nouveau message qu’il peut ou non afficher. Passez la classe de message du message à **OnActivateNext**. 
  
Les notifications par un objet de formulaire à l’application cliente sont gérées par l’interface **IMAPIViewAdviseSink** de l’application cliente. Pour plus d’informations, [voir IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).
  

