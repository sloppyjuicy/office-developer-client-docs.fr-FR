---
title: Prise en charge des notifications d’événement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a1e3e49c-8d1d-4f7e-ba5a-be441f0f10ae
ms.openlocfilehash: 047548092a94ad14afe2eb536c46877ccfd1dc51
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378526"
---
# <a name="supporting-event-notification"></a>Prise en charge des notifications d’événement

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Étant donné que la prise en charge des notifications d’événements peut être compliquée, MAPI fournit trois méthodes d’objet de prise en charge qui implémentent les parties les plus difficiles du processus. Ces méthodes fonctionnent en tant qu’unité et un fournisseur doit utiliser les trois méthodes ou aucune d’entre elles.
  
Les méthodes de prise en charge MAPI utilisent des clés de notification pour gérer les connexions entre les réceptions de notification et les objets qui génèrent les notifications. Une clé de notification est [une structure NOTIFKEY](notifkey.md) qui contient des données binaires qui identifient un objet parmi les processus. Une clé de notification est généralement copiée à partir de l’identificateur d’entrée à long terme de l’objet source de notification. Si le client a fourni un identificateur d’entrée dans l’appel au service **Conseil, vous** pouvez l’utiliser pour la clé de notification. Si le  _paramètre lpEntryID_ à **Advise** est NULL, utilisez l’identificateur d’entrée de l’objet conteneur le plus à l’extérieur possible, tel que la magasin de messages. 
  
Pour utiliser les méthodes de support, appelez [IMAPISupport::Subscribe](imapisupport-subscribe.md) chaque fois qu’un client appelle votre méthode **Advise** pour s’inscrire à une notification. Allouez [une structure NOTIFKEY](notifkey.md) et créez une clé de notification unique pour votre objet source de conseil. Par exemple, un fournisseur de magasins de messages qui est invité à avertir un client lorsqu’un message est reçu dans un dossier particulier crée une clé de notification pour ce dossier. Passez un pointeur vers la structure **NOTIFKEY** dans l’appel à **s’abonner** , ainsi qu’un pointeur vers le sink de conseil du client. **Subscribe** calls the advise sink’s [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method to increment its reference count and MAPI retains the pointer until the registration is canceled. 
  
Vous pouvez transmettre l’indicateur NOTIFY_SYNC s’abonner pour  demander que **Notify** se comporte de manière synchrone et ne retourne pas tant qu’il n’a pas effectué tous les appels aux méthodes [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) des sinks de notification inscrits. Définissez cet indicateur uniquement pour votre propre utilisation interne. Ne la définissez pas lorsque vous répondez à **un appel de** conseil client. La notification d’événement entre les clients et les fournisseurs est toujours asynchrone. Autrement dit, MAPI garantit que l’appel au cours duquel un événement se produit sera de retour au client avant que les appels **OnNotify** ne soient effectués. 
  
Si vous définissez l’indicateur NOTIFY_SYNC, n’abonnez aucune modification aux objets de sink de conseil et ne passez pas un wrapper advise sink créé par [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour s’abonner **.** **HrThisThreadAdviseSink** crée une version thread-safe d’un réception de conseil à utiliser uniquement avec une notification asynchrone. 
  
Si un réception de notification inscrit pour une notification synchrone renvoie à partir de **OnNotify** avec l’indicateur CALLBACK_DISCONTINUE définie, [IMAPISupport::Notify](imapisupport-notify.md) définit l’indicateur NOTIFY_CANCELED et renvoie sans effectuer d’appels à **OnNotify**. 
  
Une **fois l’abonnement** renvoyé, vous n’aurez plus besoin de conserver votre copie du reçu de conseil du client. Appelez sa [méthode IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) pour la libérer. **L’abonnement** renvoie un numéro de connexion autre que zéro que vous devez renvoyer au client. Le numéro de connexion représente le lien entre la source de conseil et le sink de conseil. Il reste valide jusqu’à ce que le client effectue un appel réussi à **Unadvise**. 
  
Lorsque le client est prêt à annuler une inscription, il appelle votre **méthode Unadvise** . Passez le numéro de connexion de **l’appel Unadvise** à [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md). **Unsubscribe** calls the advise sink’s **IUnknown::Release** method. Comme avec **Advise** et **Unadvise**, les appels à **Subscribe** et **Unsubscribe** doivent être associés. Vous devez effectuer un appel pour **vous désabonner** pour chaque appel effectué pour **s’abonner**. Toutefois, vous n’avez pas besoin d’appeler **Subscribe** chaque fois que votre **méthode Advise** est appelée. À l’inverse, vous pouvez l’appeler pour la configuration des notifications internes. 
  
Lorsqu’un événement se produit, allouez une ou plusieurs structures [de NOTIFICATION](notification.md) du type approprié à l’événement et appelez [IMAPISupport::Notify](imapisupport-notify.md). **Notify** génère une notification pour chaque réception de notification inscrit. Vous devez définir tous les membres inutilisés de la structure [NOTIFICATION](notification.md) sur zéro. Cette technique d’initialisation de la structure **NOTIFICATION** peut aider les clients à créer des implémentations **OnNotify** plus petites, plus rapides et moins sujettes aux erreurs. 
  
Notez qu’une structure **de NOTIFICATION** distincte est nécessaire pour chaque événement, même pour plusieurs événements du même type. Par exemple, si trois clients sont inscrits pour la notification de table sur une table particulière et que cinq lignes sont ajoutées à la table, vous devez créer cinq structures **OBJECT_NOTIFICATION** pour votre appel **Notify** . Une notification par lot comme celle-ci se traduit par de meilleures performances que l’appel **de Notification** cinq fois. Pour chaque **appel Notify** , MAPI appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de chaque reçu de notification inscrit. S’il n’existe aucun reçu de conseil inscrit, MAPI ignore l’appel. 
  
Les fournisseurs de services qui envoient des notifications par lots doivent les commander afin qu’ils soient interprétés de la première notification à la dernière. Ce traitement est particulièrement nécessaire lorsqu’un lot de notifications contient une série d’événements, tels que TABLE_ROW_ADDED avec un événement qui fait référence à une ligne précédente qui a été ajoutée dans un autre événement dans le même lot.
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

