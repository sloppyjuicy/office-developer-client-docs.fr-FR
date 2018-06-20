---
title: Enregistrement d’une Notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 45625387-dbd2-4ca8-926b-ef87998d01d7
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2d01527bb3c5176087aabeb69dbc8d99738df772
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786995"
---
# <a name="registering-for-a-notification"></a>Enregistrement d’une Notification

  
  
**S’applique à**: Outlook 
  
Un client peut inscrire pour les notifications de magasin de message ou de carnet d’adresses dans le cadre du processus d’initialisation.
  
MAPI prend en charge la notification sur le carnet d’adresses quel que soit ou non des fournisseurs de carnet d’adresses prend en charge. Prise en charge des notifications sur les banques de messages varie selon le fournisseur de banque de message particulier. Pour déterminer si un fournisseur de magasin de message particulier prend en charge les notifications, vérifiez sa propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Si la banque de messages prend en charge les notifications, définit le bit STORE_NOTIFY_OK. 
  
Inscription des notifications en appelant la méthode **Advise** d’un objet source advise. Nombre d’objets implémenter **Advise** et les clients peuvent s’inscrire avec les objets de diverses manières. 
  
 **Pour vous inscrire à une notification**
  
1. Créer une MAPI objet récepteur de notification et incrémente le décompte de références.
    
2. Le cas échéant, appelez [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour créer un objet récepteur advise qui encapsule votre récepteur de notifications d’origine, puis relâchez le récepteur de conseils d’origine... 
    
3. Appelez l’une des méthodes suivantes **Advise** pour terminer l’enregistrement : 
    
  - Appelez [IMAPISession::Advise](imapisession-advise.md) pour enregistrer les notifications de session ou pour les notifications sur un objet de magasin de message ou de carnet d’adresses. 
    
  - Appelez [IAddrBook::Advise](iaddrbook-advise.md) pour enregistrer les notifications de carnet d’adresse ou pour les notifications sur une messagerie utilisateur, conteneur ou liste de distribution. 
    
  - Appelez [IABLogon::Advise](iablogon-advise.md) pour inscrire directement avec un fournisseur de carnet d’adresses pour les notifications sur une messagerie utilisateur, conteneur ou liste de distribution. 
    
  - Appelez [IMsgStore::Advise](imsgstore-advise.md) pour inscrire pour les notifications de banque de messages ou des notifications sur un dossier ou un message. 
    
  - Appelez [IMSLogon::Advise](imslogon-advise.md) pour inscrire directement avec un fournisseur de magasin de message pour les notifications sur un dossier ou un message. 
    
  - Appelez [IMAPITable::Advise](imapitable-advise.md) pour s’inscrire pour les notifications de table. 
    
4. Mettre en cache le numéro de connexion renvoyé depuis **Advise**.
    
5. Si vous utilisez un récepteur de notifications encapsulé, libérer. Une fois le récepteur de notifications encapsulé est enregistré, vous n’avez plus besoin.
    
Appel ** IMAPISession::Advise ** permet de vous inscrire pour les notifications d’erreur critique sur la session globale ou pour différentes notifications sur des objets individuels. Sessions envoyer des notifications d’erreur critique aux clients connectés à des sessions partagées lorsqu’un autre client à l’aide de la session partagée appelle la méthode [IMAPISession::Logoff](imapisession-logoff.md) . Pour vous inscrire pour les notifications de session, passez la valeur NULL pour le paramètre identificateur de l’entrée. Pour vous inscrire pour les notifications sur un objet individuel, passez l’identificateur d’entrée de l’objet. La méthode **IMAPISession** transfère l’appel vers le fournisseur de services approprié, tel que déterminé par la partie **MAPIUID** de l’identificateur d’entrée. L’appel **IMAPISession::Advise** pour inscrire les notifications de l’objet est plus simple que l’appel de méthode de **notification** d’un fournisseur de services. 
  
Inscription avec le carnet d’adresses est similaire à l’enregistrement de la session. Pour vous inscrire pour la notification d’erreur critique du carnet d’adresses, passez la valeur NULL pour l’identificateur d’entrée. Pour vous inscrire pour les notifications sur un objet de carnet d’adresses spécifique, spécifiez l’identificateur d’entrée approprié et ou les événements d’intérêt. Sachez que plusieurs fournisseurs de carnet d’adresses ne permettent pas de notifications sur des objets individuels. Au lieu de cela, elles prennent en charge les notifications de table de leur contenu et les tables de hiérarchie. 
  
Il est conseillé de libérer le récepteur de notifications créés avec [HrAllocAdviseSink](hrallocadvisesink.md) immédiatement après un retour réussi à partir d’un appel **Advise** ou implémenter. C’est pourquoi il est possible, pour les fournisseurs de services de publication de votre récepteur de notifications après l’appel **Advise** , mais avant un **Unadvise** appel est effectué. Une fois que vous avez accordé la source advise un pointeur à votre récepteur de notifications et le décompte de références a été incrémenté sur ce récepteur de notifications, il est judicieux de libérer sauf si vous avez un long terme utiliser pour celle-ci. 
  
> [!NOTE]
> Tous les numéros de connexion qui représentent les enregistrements advisory valides ne seront pas libérées jusqu'à ce que l’appel **Unadvise** est effectué. 
  

