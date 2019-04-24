---
title: Composition d'un nouveau message à l'aide d'un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335125"
---
# <a name="composing-a-new-message-by-using-a-form"></a>Composition d'un nouveau message à l'aide d'un formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour utiliser un formulaire afin de composer un nouveau message, commencez par créer un objet message personnalisé.
  
 **Pour composer un nouveau message à l'aide d'un formulaire**
  
1. Appelez la méthode [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) du gestionnaire de formulaire pour extraire un pointeur vers un objet d'informations de formulaire, un objet qui implémente l'interface [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) . 
    
2. TransMettez le pointeur à l'objet d'informations de formulaire dans un appel à [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md). **CreateForm** charge le serveur de formulaires approprié. En outre, transmettez un identificateur d'interface à **CreateForm** pour spécifier l'interface à utiliser pour accéder au nouveau message. En règle générale, vous demandez [IPersistMessage: IUnknown](ipersistmessageiunknown.md) en passant IID_IPersistMessage à **CreateForm**.
    
3. Enregistrez le nouveau message en appelant sa méthode [IPersistMessage:: Save](ipersistmessage-save.md) . Le serveur de formulaire doit définir des valeurs pour les propriétés requises du message lors de la création du message. 
    
4. Chargez le message à l'aide de l'une des deux stratégies suivantes: [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) ou [IMAPISession::P Repareform](imapisession-prepareform.md) suivi par [IMAPISession:: ShowForm](imapisession-showform.md). Pour plus d'informations sur ces stratégies, consultez la rubrique [chargement d'un message dans un formulaire](loading-a-message-into-a-form.md).
    
> [!NOTE]
> Il existe des possibilités de gains de performances lors du chargement d'un nouveau message personnalisé dans un serveur de formulaire, car vous aurez déjà eu la possibilité d'obtenir des informations sur le message, telles que sa classe de message, pendant le traitement requis pour le ** Appels ResolveMessageClass** et **CreateForm** . Pour cette raison, vous serez en mesure de simplifier le traitement requis avant d'appeler **LoadForm** sur ce qui est décrit dans la rubrique [chargement d'un message dans un formulaire](loading-a-message-into-a-form.md). 
  

