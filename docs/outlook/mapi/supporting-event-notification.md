---
title: Notification d'événement de prise en charge
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1e3e49c-8d1d-4f7e-ba5a-be441f0f10ae
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 83c102c25b17b6769c0c676bbadd874224f75cf6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327425"
---
# <a name="supporting-event-notification"></a>Notification d'événement de prise en charge

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Étant donné que la notification d'événement de prise en charge peut être compliquée, MAPI fournit trois méthodes d'objet de prise en charge qui implémentent les composants les plus difficiles du processus. Ces méthodes fonctionnent comme une unité, et un fournisseur doit utiliser les trois ou aucun d'entre eux.
  
Les méthodes de prise en charge MAPI utilisent des clés de notification pour gérer les connexions entre les récepteurs de notification et les objets qui génèrent les notifications. Une clé de notification est une structure [NOTIFKEY](notifkey.md) qui contient des données binaires qui identifient un objet parmi les processus. Une clé de notification est généralement copiée à partir de l'identificateur d'entrée à long terme de l'objet de source Advise. Si le client a fourni un identificateur d'entrée dans l'appel à **conseiller**, vous pouvez l'utiliser pour la clé de notification. Si le paramètre _lpEntryID_ à **conseiller** a la valeur null, utilisez l'identificateur d'entrée de l'objet conteneur éventuellement le plus à l'extérieur, comme la Banque de messages. 
  
Pour utiliser les méthodes de prise en charge, appelez [IMAPISupport:: subscribe](imapisupport-subscribe.md) chaque fois **** qu'un client appelle votre méthode Advise pour s'inscrire pour une notification. AlLouez une structure [NOTIFKEY](notifkey.md) et créez une clé de notification unique pour votre objet de source de notification. Par exemple, un fournisseur de banque de messages qui est invité à informer un client lors de la réception d'un message dans un dossier particulier crée une clé de notification pour ce dossier. TransMettez un pointeur vers la structure **NOTIFKEY** dans l'appel pour **s'abonner** , ainsi qu'un pointeur vers le récepteur de notification du client. **Subscribe** appelle la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) du récepteur de notification pour incrémenter son décompte de référence et MAPI conserve le pointeur jusqu'à l'annulation de l'inscription. 
  
Vous pouvez transmettre l'indicateur NOTIFY_SYNC pour **vous abonner** afin **** de demander que les notifications se comportent de manière synchrone et ne soient pas renvoyées jusqu'à ce qu'il ait effectué tous les appels aux méthodes [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) des récepteurs de notifications enregistrés. Définissez cet indicateur uniquement pour votre usage interne. Ne la définissez pas lorsque vous répondez à un appel de **Conseil** client. La notification d'événement entre les clients et les fournisseurs est toujours asynchrone. En d'autres conditions, MAPI garantit que l'appel pendant lequel un événement se produit renverra au client avant d'effectuer les appels **OnNotify** . 
  
Si vous définissez l'indicateur NOTIFY_SYNC, n'effectuez aucune modification dans les objets de récepteur de notifications et ne transmettez pas de récepteur de notification de wrapper créé par [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour **s'abonner**. **HrThisThreadAdviseSink** crée une version thread-safe d'un récepteur de notifications à utiliser uniquement avec la notification asynchrone. 
  
Si un récepteur de notifications inscrit pour une notification synchrone est renvoyé à partir de **OnNotify** avec l'indicateur CALLBACK_DISCONTINUE défini, [IMAPISupport:: Notify](imapisupport-notify.md) définit l'indicateur NOTIFY_CANCELED et retourne sans effectuer d'appels à **OnNotify**. 
  
Une fois que **subscribe** a été renvoyé, vous n'avez plus besoin de conserver votre copie du récepteur de notification du client. Appelez sa méthode [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) pour le libérer. **Subscribe** renvoie un numéro de connexion différent de zéro que vous devez retourner au client. Le numéro de connexion représente le lien entre la source de notification et le récepteur de notifications. Il reste valide jusqu'à ce que le client ait réussi **** à déconseiller. 
  
Lorsque le client est prêt à annuler une inscription, il appelle votre **** méthode Unadvise. TransMettez le numéro de connexion **** de l'appel Unadvise à [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md). **Unsubscribe** appelle la méthode **IUnknown:: Release** du récepteur de notification. Comme avec **Advise** et Unadvise, les appels à **subscribe** et unsubscribe doivent être couplés. **** **** Vous devez passer un appel pour annuler l' **abonnement** pour chaque appel effectué pour **s'abonner**. Toutefois, vous n'avez pas besoin d'appeler **subscribe** à chaque appel de la méthode Advise. **** À l'inverse, vous pouvez l'appeler pour configurer des notifications internes. 
  
Lorsqu'un événement se produit, allouez une ou plusieurs structures de [notification](notification.md) du type approprié pour l'événement et appelez [IMAPISupport:: Notify](imapisupport-notify.md). **Notify** génère une notification pour chaque récepteur d'avis enregistré. Vous devez affecter la valeur zéro à tous les membres inutilisés de la structure de [notification](notification.md) . Cette technique d'initialisation de la structure de **notification** peut aider les clients à créer des implémentations **OnNotify** plus petites, plus rapides et moins sujettes aux erreurs. 
  
Notez qu'une structure de **notification** distincte est nécessaire pour chaque événement, même pour plusieurs événements du même type. Par exemple, si trois clients sont inscrits pour la notification de table sur une table particulière et que cinq lignes sont ajoutées à la table, vous devez créer cinq structures **OBJECT_NOTIFICATION** pour votre appel **Notify** . Une notification par lots telle que celle-ci génère de meilleures performances que l'appel de **notification** cinq fois. Pour chaque appel **Notify** , MAPI appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) de chaque récepteur de notifications enregistrées. Si aucun récepteur de notification n'est enregistré, MAPI ignore l'appel. 
  
Les fournisseurs de services qui envoient des notifications par lots doivent les ordonner afin qu'ils puissent être interprétés de la première notification au dernier. Ce classement est particulièrement nécessaire lorsqu'un lot de notifications contient une série d'événements, tels que TABLE_ROW_ADDED, avec un événement qui fait référence à une ligne précédente ajoutée à un autre événement dans le même lot.
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

