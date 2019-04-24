---
title: Envoi et réception de notifications de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 4ee47b51a98cf732f4e9af2a87fa1734a7250208
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339710"
---
# <a name="sending-and-receiving-form-notifications"></a>Envoi et réception de notifications de formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les notifications de formulaire sont utilisées dans MAPI pour faciliter la communication à partir du formulaire vers votre afficheur, ainsi que de votre visionneuse vers le formulaire.
  
Les formulaires envoient des notifications à votre visionneuse lorsque l'un des événements suivants se produit:
  
- Le formulaire est fermé.
    
- Un nouveau message est chargé dans le formulaire.
    
- Une opération d'enregistrement est terminée.
    
- Un message est envoyé.
    
Chacun de ces types d'événements correspond à une méthode particulière dans [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), l'une des interfaces que votre visionneuse de formulaire doit implémenter. Lorsqu'un événement se produit, le formulaire appelle la méthode **IMAPIViewAdviseSink** correspondante dans le récepteur d'avertissement de votre visionneuse. Par exemple, lorsqu'un nouveau message arrive que votre visionneuse doit inclure dans son affichage, le formulaire appelle votre méthode [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) . 
  
Implémentez votre récepteur d'avis d'affichage d'une manière adaptée à votre visionneuse; Il n'existe pas d'implémentation standard. Par exemple, dans **OnNewMessage** , vous pouvez mettre à jour l'affichage de la table des matières du dossier actif pour inclure le message nouvellement arrivé. Dans [IMAPIViewAdviseSink:: OnSubmitted](imapiviewadvisesink-onsubmitted.md), la méthode qui est appelée lorsque vous recevez un événement de message envoyé, vous pouvez copier le message envoyé dans un dossier éléments envoyés.
  
Les formulaires reçoivent une notification à partir de votre visionneuse lorsqu'une modification se produit et que vous chargez un nouveau message. Pour avertir un formulaire, appelez l'une des méthodes de **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink:: OnChange](imapiformadvisesink-onchange.md) ou [IMAPIFormAdviseSink:: OnActivateNext](imapiformadvisesink-onactivatenext.md). Appelez **OnChange** pour communiquer le statut. Par exemple, si le formulaire affiche le dernier élément dans un dossier lors de l'arrivée d'un nouveau message, appelez la fonction **OnChange** avec l'indicateur VCSTATUS_NEXT défini pour indiquer au formulaire qu'il existe maintenant un élément suivant. 
  
Appelez **OnActivateNext** pour alerter le formulaire à l'arrivée d'un nouveau message qu'il peut ou ne peut pas afficher. TransMettez la classe de message du message à **OnActivateNext**. 
  
Les notifications d'un objet Form à l'application client sont gérées par l'interface **IMAPIViewAdviseSink** de l'application cliente. Pour plus d'informations, consultez la rubrique [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md).
  

