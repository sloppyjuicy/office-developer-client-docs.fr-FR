---
title: Prise en charge des notifications d’événements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1e3e49c-8d1d-4f7e-ba5a-be441f0f10ae
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 83c102c25b17b6769c0c676bbadd874224f75cf6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397141"
---
# <a name="supporting-event-notification"></a>Prise en charge des notifications d’événements

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prise en charge de la notification d’événement pouvant être complexe, MAPI fournit trois méthodes d’objet prise en charge qui implémentent la partie la plus difficile du processus. Ces méthodes fonctionnent comme une unité, et un fournisseur doit utiliser tous les trois ou aucun d'entre eux.
  
Les méthodes de prise en charge MAPI utilisent des clés de notification pour gérer les connexions entre les récepteurs de notifications et les objets qui génèrent des notifications. Une clé de notification est une structure [NOTIFKEY](notifkey.md) qui contient des données binaires qui identifie un objet entre les processus. Une clé de notification est généralement copiée à partir de l’identificateur d’entrée à long terme de l’objet source de notification. Si le client a fourni un identificateur d’entrée dans l’appel à **Advise**, vous pouvez l’utiliser pour la clé de notification. Si le paramètre _lpEntryID_ **Advise** est NULL, utilisez l’identificateur d’entrée de l’objet conteneur le plus éloigné possibles, telles que la banque de messages. 
  
Pour utiliser les méthodes de prise en charge, appelez [IMAPISupport::Subscribe](imapisupport-subscribe.md) chaque fois qu’un client appelle votre méthode **Advise** pour vous inscrire à une notification. Allouer une structure [NOTIFKEY](notifkey.md) et créer une clé de notification unique pour votre objet de source advise. Par exemple, un fournisseur de magasins de message est invité à informer un client lorsqu’un message est reçu dans un dossier spécifique crée une clé de notification pour ce dossier. Passez un pointeur vers la structure **NOTIFKEY** dans l’appel de **s’abonner** avec un pointeur vers du client récepteur de notification. **S’abonner** appelle [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) méthode du récepteur advise pour incrémenter son décompte de références et MAPI conserve le pointeur jusqu'à ce que l’enregistrement est annulée. 
  
Vous pouvez passer l’indicateur NOTIFY_SYNC à **s’abonner** à demander que **Notify** se comportent de façon synchrone et pas retour jusqu'à ce qu’il a apportées à tous les appels vers les méthodes [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) d’inscrit récepteurs de notifications. Définissez cet indicateur uniquement à votre propre usage interne. Ne le définissez pas lorsque vous répondez à un appel **Advise** client. Notification d’événement entre les clients et fournisseurs est toujours asynchrone. Autrement dit, MAPI garantit que l’appel pendant laquelle un événement se produit renverra au client avant qu’un des appels **OnNotify** soient effectué. 
  
Si vous définissez l’indicateur NOTIFY_SYNC, n’apportez aucune modification à tous les objets de récepteur advise et ne passent pas d’un récepteur de notifications wrapper créé par [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) **s’abonner**. **HrThisThreadAdviseSink** crée une version thread-safe d’un récepteur de notifications à utiliser avec la notification asynchrone. 
  
Si un récepteur de notifications enregistré pour une notification synchrone renvoie de **OnNotify** avec l’indicateur CALLBACK_DISCONTINUE, [IMAPISupport::Notify](imapisupport-notify.md) définit l’indicateur NOTIFY_CANCELED et renvoie sans apporter de tous les appels à **OnNotify**. 
  
Une fois que **l’abonnement** a renvoyé, vous n’aura plus nécessaire de conserver votre copie du récepteur de notification du client. Appelez la méthode [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) pour libérer. **S’abonner** renvoie un nombre différent de zéro connexion vous devez retourner au client. Le numéro de connexion représente la liaison entre la source des notifications et le récepteur de notifications. Il reste valide jusqu'à ce que le client effectue un appel réussi **Unadvise**. 
  
Lorsque le client est prêt à annuler un enregistrement, il appelle la méthode **Unadvise** . Passez le numéro de connexion de l’appel de **Unadvise** à [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md). **Annuler l’abonnement** appelle la méthode de **IUnknown::Release** de notification du récepteur. Comme avec **Advise** et **Unadvise**, appels **s’abonner** et **Annuler l’abonnement** doivent être associés. Vous devez apporter un appel pour **Annuler l’abonnement** pour chaque appel effectué **s’abonner**. Toutefois, vous n’êtes pas obligé d’appelé la méthode **Subscribe** chaque fois que votre méthode **Advise** est appelée. Inversement, vous pouvez l’appeler à la configuration de notifications internes. 
  
Lorsqu’un événement se produit, allouer une ou plusieurs des structures [NOTIFICATION](notification.md) du type approprié pour l’événement et appelez [IMAPISupport::Notify](imapisupport-notify.md). **Notifier** génère une notification pour chaque récepteur de notifications enregistrés. Vous devez définir tous les membres inutilisées de la structure de [NOTIFICATION](notification.md) à zéro. Cette technique pour l’initialisation de la structure **NOTIFICATION** peut aider les clients à créer plus petit, plus rapide et moins sujet aux erreurs **OnNotify** implémentations. 
  
Notez qu’une structure **NOTIFICATION** distincte est nécessaire pour chaque événement, même pour plusieurs événements du même type. Par exemple, si trois clients sont enregistrés pour la notification de table sur une table spécifique et cinq lignes sont ajoutées à la table, vous devez créer cinq structures **OBJECT_NOTIFICATION** pour votre appel **Notify** . Une notification de lot tel que cela entraîne de meilleures performances que l’appel **notifier** à cinq reprises. Pour chaque appel **Notify** , MAPI appelle la méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de chaque récepteur de notifications enregistrés. S’il y a non enregistré récepteurs, de notifications MAPI ignore l’appel. 
  
Fournisseurs de services d’envoi des notifications par lot doivent leur ordre afin qu’ils peuvent être interprétés de la première notification à la dernière. Cette commande est particulièrement nécessaire lorsqu’un lot de notifications contient une série d’événements, tel que TABLE_ROW_ADDED avec un événement qui fait référence à une ligne précédente a été ajoutée à un autre événement dans le même lot.
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

