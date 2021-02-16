---
title: Inscription à une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 45625387-dbd2-4ca8-926b-ef87998d01d7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ccc2758b59a9227afbc50360102e793892bbdc52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424902"
---
# <a name="registering-for-a-notification"></a>Inscription à une notification

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un client peut s’inscrire aux notifications de carnet d’adresses ou de magasin de messages dans le cadre de son processus d’initialisation.
  
MAPI prend en charge les notifications sur le carnet d’adresses, que l’un des fournisseurs de carnets d’adresses la prend en charge ou non. La prise en charge des notifications sur les magasins de messages dépend du fournisseur de magasins de messages particulier. Pour déterminer si un fournisseur de magasin de messages particulier prend en charge les notifications, vérifiez sa propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Si la boutique de messages prend en charge les notifications, STORE_NOTIFY_OK bits seront définies. 
  
Inscrivez-vous aux notifications en appelant la méthode Advise d’un objet source **de** conseil. De nombreux objets **implémentent Advise** et les clients peuvent s’inscrire avec ces objets de différentes manières. 
  
 **Pour vous inscrire à une notification**
  
1. Créez un objet de sink MAPI advise et incrémentez son nombre de références.
    
2. Le cas échéant, appelez [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour créer un objet de sink de conseil qui enveloppe votre sink de conseil d’origine, puis relâchez le sink de conseil d’origine. 
    
3. Appelez l’une des méthodes **Advise** suivantes pour terminer l’inscription : 
    
  - Appelez [IMAPISession::Advise](imapisession-advise.md) to register for session notifications or for notifications on an address book or message store object. 
    
  - Appelez [IAddrBook::Advise](iaddrbook-advise.md) to register for address book notifications or for notifications on a messaging user, container, or distribution list. 
    
  - Appelez [IABLogon::Advise](iablogon-advise.md) to register directly with an address book provider for notifications on a messaging user, container, or distribution list. 
    
  - Appelez [IMsgStore::Advise](imsgstore-advise.md) to register for message store notifications or for notifications on a folder or message. 
    
  - Appelez [IMSLogon::Advise](imslogon-advise.md) pour vous inscrire directement auprès d’un fournisseur de magasins de messages pour les notifications sur un dossier ou un message. 
    
  - Appelez [IMAPITable::Advise](imapitable-advise.md) pour vous inscrire aux notifications de table. 
    
4. Mettre en cache le numéro de connexion renvoyé par **Advise**.
    
5. Si vous utilisez un sink de conseil wrapped, relâchez-le. Une fois que le sink de conseil wrapped est inscrit, vous n’en avez plus besoin.
    
L’appel de ** IMAPISession::Advise ** vous permet de vous inscrire aux notifications d’erreur critiques sur la session globale ou pour diverses notifications sur des objets individuels. Les sessions envoient des notifications d’erreur critiques aux clients connectés à des sessions partagées lorsqu’un autre client utilisant la session partagée appelle la méthode [IMAPISession::Logoff.](imapisession-logoff.md) Pour vous inscrire aux notifications de session, passez null pour le paramètre d’identificateur d’entrée. Pour vous inscrire aux notifications sur un objet individuel, passez l’identificateur d’entrée de l’objet. La **méthode IMAPISession** permet de forwarder l’appel au fournisseur de services approprié, tel que déterminé par la partie **MAPIUID** de l’identificateur d’entrée. Appeler **IMAPISession::Advise** pour s’inscrire aux notifications d’objet est plus simple que d’appeler la méthode Advise d’un fournisseur **de** services. 
  
L’inscription avec le carnet d’adresses est similaire à l’inscription à la session. Pour vous inscrire à la notification d’erreur critique à partir du carnet d’adresses, passez NULL pour l’identificateur d’entrée. Pour vous inscrire aux notifications sur un objet de carnet d’adresses particulier, spécifiez l’identificateur d’entrée et les événements d’intérêt appropriés. N’ignorez pas que de nombreux fournisseurs de carnet d’adresses ne peuvent pas prendre en charge les notifications sur des objets individuels. Au lieu de cela, ils supportent les notifications de tableau sur leur contenu et leurs tables hiérarchiques. 
  
Il est conseillé de libérer le reçu de conseil que vous implémentez ou créez avec [HrAllocAdviseSink](hrallocadvisesink.md) immédiatement après un retour réussi **d’un appel de** conseil. En effet, il est possible pour les fournisseurs de services de libérer votre sink de conseil après l’appel **Advise,** mais avant qu’un appel **Unadvise** ne soit effectué. Une fois que vous avez donné à la source de conseil un pointeur vers votre sink de conseil et que le nombre de références a été incrémenté sur ce sink de conseil, il est judicieux de le libérer, sauf si vous avez une utilisation à long terme pour celui-ci. 
  
> [!NOTE]
> Tous les numéros de connexion qui représentent des inscriptions d’avis valides ne seront pas publiés tant que l’appel **Unadvise** n’aura pas été effectué. 
  

