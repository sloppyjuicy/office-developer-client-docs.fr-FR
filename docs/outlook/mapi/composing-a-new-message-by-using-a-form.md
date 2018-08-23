---
title: Création d’un message en utilisant un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 667d7afe1772786507ffc8eb75f901439ada61d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587866"
---
# <a name="composing-a-new-message-by-using-a-form"></a>Création d’un message en utilisant un formulaire

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Pour utiliser un formulaire pour créer un nouveau message, d’abord créer un nouvel objet de message personnalisé.
  
 **Pour composer un nouveau message à l’aide d’un formulaire**
  
1. Appelez [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) méthode du gestionnaire formulaire pour récupérer un pointeur vers un objet d’informations de formulaire, un objet qui implémente le [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface. 
    
2. Passez le pointeur à l’objet d’informations de formulaire dans un appel à [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md). **CreateForm** charge le serveur de la forme appropriée. En outre, passez un identificateur d’interface à **CreateForm** pour spécifier l’interface à utiliser pour accéder au nouveau message. En règle générale, vous demander [IPersistMessage : IUnknown](ipersistmessageiunknown.md) en transmettant IID_IPersistMessage à **CreateForm**.
    
3. Enregistrez le nouveau message en appelant la méthode [IPersistMessage::Save](ipersistmessage-save.md) . Le serveur de formulaire doit définir les valeurs des propriétés requises du message lorsqu’il crée le message. 
    
4. Charger le message à l’aide d’une des deux stratégies : [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) ou [IMAPISession::PrepareForm](imapisession-prepareform.md) suivi [IMAPISession::ShowForm](imapisession-showform.md). Pour plus d’informations sur ces stratégies, consultez [chargement d’un Message dans un formulaire](loading-a-message-into-a-form.md).
    
> [!NOTE]
> Il existe des opportunités pour les gains de performances lors du chargement d’un nouveau message personnalisé à un serveur de formulaire, car vous serez ont déjà eu permet d’obtenir des informations sur le message, telles que sa classe de message — pendant le traitement requis pour la ** ResolveMessageClass** et appels **CreateForm** . Pour cette raison, vous serez en mesure de simplifier le traitement requis avant d’appeler **LoadForm** sur qui décrit dans la rubrique [chargement d’un Message dans un formulaire](loading-a-message-into-a-form.md). 
  

