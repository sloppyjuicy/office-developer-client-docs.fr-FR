---
title: Composition d’un nouveau message à l’aide d’un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412799"
---
# <a name="composing-a-new-message-by-using-a-form"></a>Composition d’un nouveau message à l’aide d’un formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour utiliser un formulaire pour composer un nouveau message, créez d’abord un objet de message personnalisé.
  
 **Pour composer un nouveau message à l’aide d’un formulaire**
  
1. Appelez la méthode [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) du gestionnaire de formulaires pour récupérer un pointeur vers un objet d’informations de formulaire , un objet qui implémente l’interface [IMAPIFormInfo : IMAPIProp.](imapiforminfoimapiprop.md) 
    
2. Passez le pointeur à l’objet d’informations du formulaire dans un appel [à IMAPIFormMgr::CreateForm](imapiformmgr-createform.md). **CreateForm charge** le serveur de formulaire approprié. En outre, passez un identificateur d’interface à **CreateForm** pour spécifier l’interface à utiliser pour accéder au nouveau message. En règle générale, vous [demandez IPersistMessage : IUnknown](ipersistmessageiunknown.md) en IID_IPersistMessage **à CreateForm**.
    
3. Enregistrez le nouveau message en appelant sa [méthode IPersistMessage::Save.](ipersistmessage-save.md) Le serveur de formulaire doit définir des valeurs pour les propriétés requises du message lors de sa création. 
    
4. Chargez le message à l’aide de l’une des deux stratégies : [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) ou [IMAPISession::P repareForm](imapisession-prepareform.md) suivi de [IMAPISession::ShowForm](imapisession-showform.md). Pour plus d’informations sur ces stratégies, voir [Chargement d’un message dans un formulaire.](loading-a-message-into-a-form.md)
    
> [!NOTE]
> Il existe des opportunités de gains de performances lors du chargement d’un nouveau message personnalisé dans un serveur de formulaires, car vous aurez déjà eu la possibilité d’obtenir des informations sur le message, telles que sa classe de message, pendant le traitement requis pour les appels **ResolveMessageClass** et **CreateForm.** Pour cette raison, vous serez en mesure de simplifier le traitement requis avant d’appeler **LoadForm** sur celui décrit dans la rubrique Chargement d’un [message dans un formulaire](loading-a-message-into-a-form.md). 
  

