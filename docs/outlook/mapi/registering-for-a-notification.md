---
title: Inscription à une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 45625387-dbd2-4ca8-926b-ef87998d01d7
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: ccc2758b59a9227afbc50360102e793892bbdc52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328405"
---
# <a name="registering-for-a-notification"></a>Inscription à une notification

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un client peut s'inscrire pour les notifications de carnet d'adresses ou de banque de messages dans le cadre de son processus d'initialisation.
  
MAPI prend en charge la notification dans le carnet d'adresses, quel que soit le fournisseur de carnet d'adresses qui le prend en charge. La prise en charge de la notification sur les banques de messages dépend du fournisseur de banque de messages particulier. Pour déterminer si un fournisseur de banque de messages particulier prend en charge les notifications, vérifiez sa propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Si le magasin de messages prend en charge les notifications, le bit STORE_NOTIFY_OK est défini. 
  
Inscrivez-vous pour les notifications en appelant la **** méthode Advise de l'objet source Advise. De nombreux objets **** implémentEnt Advise et les clients peuvent s'enregistrer avec ces objets de différentes façons. 
  
 **Pour vous inscrire pour une notification**
  
1. Créer un objet récepteur MAPI Advise et incrémenter son décompte de références.
    
2. Si nécessaire, appelez [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour créer un objet de récepteur de notification qui encapsule votre récepteur de notification d'origine, puis relâchez le récepteur de Conseil d'origine.. 
    
3. Appelez l'une des méthodes **Advise** suivantes pour terminer l'inscription: 
    
  - Appelez [IMAPISession:: Advise](imapisession-advise.md) pour enregistrer les notifications de session ou les notifications sur un objet de carnet d'adresses ou de banque de messages. 
    
  - Appelez [IAddrBook:: Advise](iaddrbook-advise.md) pour inscrire les notifications de carnet d'adresses ou les notifications sur un utilisateur de messagerie, un conteneur ou une liste de distribution. 
    
  - Appelez [IABLogon:: Advise](iablogon-advise.md) pour enregistrer directement auprès d'un fournisseur de carnets d'adresses pour les notifications sur un utilisateur de messagerie, un conteneur ou une liste de distribution. 
    
  - Appelez [IMsgStore:: Advise](imsgstore-advise.md) pour inscrire les notifications de banque de messages ou pour les notifications d'un dossier ou d'un message. 
    
  - Appelez [IMSLogon:: Advise](imslogon-advise.md) pour enregistrer directement auprès d'un fournisseur de banque de messages pour les notifications d'un dossier ou d'un message. 
    
  - Appeler [IMAPITable:: conseille](imapitable-advise.md) de s'inscrire aux notifications de table. 
    
4. Mettre en cache le numéro de **** connexion renvoyé par Advise.
    
5. Si vous utilisez un récepteur de notifications encapsulées, libérez-le. Une fois que le récepteur de notifications a été inscrit, vous n'en avez plus besoin.
    
L'appel de * * IMAPISession:: adVise * * vous permet d'enregistrer les notifications d'erreur critique sur la session globale ou pour diverses notifications sur des objets individuels. Les sessions envoient des notifications d'erreur critiques aux clients connectés à des sessions partagées lorsqu'un autre client utilisant la session partagée appelle la méthode [IMAPISession:: Logoff](imapisession-logoff.md) . Pour vous inscrire aux notifications de session, transmettez la valeur NULL pour le paramètre d'identificateur d'entrée. Pour vous inscrire aux notifications sur un objet individuel, transmettez l'identificateur d'entrée de l'objet. La méthode **IMAPISession** transfère l'appel au fournisseur de services approprié, tel que déterminé par la partie **MAPIUID** de l'identificateur d'entrée. L'appel de **IMAPISession:: Advise** to Register for Object notifications est plus simple que l'appel de la méthode Advise d'un fournisseur de services. **** 
  
L'enregistrement avec le carnet d'adresses est similaire à celui de la session. Pour vous inscrire à une notification d'erreur critique à partir du carnet d'adresses, transmettez la valeur NULL pour l'identificateur d'entrée. Pour vous inscrire aux notifications sur un objet de carnet d'adresses particulier, spécifiez l'identificateur d'entrée et l'événement ou les événements intéressants appropriés. N'oubliez pas que de nombreux fournisseurs de carnets d'adresses ne prennent pas en charge les notifications sur les objets individuels. Elles prennent en charge les notifications de table sur leurs tables de contenu et de hiérarchie. 
  
Il est recommandé de libérer le récepteur de notification que vous implémentez ou créez avec [HrAllocAdviseSink](hrallocadvisesink.md) immédiatement après un retour réussi d'un appel de **notification** . En effet, il est possible pour les fournisseurs de services de libérer votre récepteur de notifications après l'appel de la **notification** , mais avant qu'un appel Unadvise ne soit effectué. **** Une fois que vous avez attribué à la source de notification un pointeur vers votre récepteur de notification et que le nombre de références a été incrémenté sur ce récepteur de notifications, il est recommandé de le libérer à moins que vous n'utilisiez à long terme. 
  
> [!NOTE]
> Tous les numéros de connexion qui représentent des enregistrements d'avis valides ne seront **** pas libérés tant que l'appel Unadvise n'est pas effectué. 
  

