---
title: Notification d’événement dans MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b3b625b-6dea-4b12-99a9-152935bdfe39
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 30d4ad5e0fc1ecdc4c8eb06f75d39e38dd481269
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321394"
---
# <a name="event-notification-in-mapi"></a>Notification d’événement dans MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La notification d'événement est la communication d'informations entre deux objets MAPI. Par le biais d'un des objets, un client ou un fournisseur de services s'inscrit à la notification d'une modification ou d'une erreur, appelé un événement, qui peut avoir lieu dans l'autre objet. Après l'événement, le premier objet est informé de la modification ou de l'erreur. L'objet qui reçoit la notification est appelé récepteur de notifications; l'objet responsable de la notification est appelé la source de l'avis.
  
Il existe trois types d'objets de récepteur de notifications (tous les types sont des objets MAPI standard):
  
- Avertir les objets récepteurs.   
- Objets de récepteur de formulaire.  
- Afficher les objets de récepteur de notifications.
    
Les objets de récepteur de notifications sont le type le plus courant. Les récepteurs de notifications sont généralement implémentés par les applications clientes pour recevoir les notifications de carnet d'adresses et de banque de messages et prendre en charge l'interface [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) . **IMAPIAdviseSink** contient une seule méthode, [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md). Les récepteurs de notifications de formulaire et d'affichage sont moins courants; elles sont implémentées pour recevoir des notifications sur les modifications apportées aux formulaires personnalisés. Les récepteurs de notifications de formulaire prennent en charge les récepteurs d'interface [IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) et d'affichage prennent en charge l'interface [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) . Étant donné que la plupart des clients implémentent des objets de récepteur standard, supposez que les discussions des notifications concernent les notifications de carnet d'adresses et de banque de messages plutôt que les notifications par formulaires. Pour plus d'informations sur les notifications de formulaires, voir [MAPI Forms notifications](mapi-forms-notifications.md) et [Writing Form Server Code](writing-form-server-code.md).
  
Les objets source de notification sont implémentés par les fournisseurs de services et par MAPI. Tous les fournisseurs de services ne prennent pas en charge la notification d'événement; Il est facultatif, mais vivement recommandé. Les fournisseurs de banques de messages et de carnets d'adresses prennent généralement en charge les notifications d'objet sur plusieurs de leurs objets et des notifications de table sur leurs tables de contenu et de hiérarchie. Les fournisseurs de transport ne prennent pas en charge les notifications directement; elles s'appuient sur d'autres méthodes de communication avec les clients.
  
Contrairement aux récepteurs de notifications, les objets source d'avis ne sont pas un type unique d'objet MAPI. De nombreux objets MAPI, tels que les banques de messages et les tables, peuvent prendre la source de l'avis. Une source de notification est un objet MAPI qui effectue les opérations suivantes:
  
- Implémente une **** méthode Advise pour recevoir des enregistrements de notification. 
    
- Implémente une **** méthode Unadvise pour recevoir des annulations de notification. 
    
- Génère des notifications du type approprié pour les objets conseillers appropriés qui ont été inscrits en appelant leurs méthodes **IMAPIAdviseSink:: OnNotify** . 
    
Les clients qui implémentent les objets de récepteur de notification appellent un **conseiller** lorsqu'ils veulent s'inscrire pour une notification, dans la plupart des cas, en transmettant l'identificateur d'entrée de l'objet avec lequel l'inscription doit avoir lieu, et Unadvise quand il souhaite annuler l'élément **** son. Les clients transmettent un paramètre à **conseiller** qui indique quels types d'événements qu'ils souhaitent surveiller. **Advise** renvoie un nombre différent de zéro qui représente une connexion réussie entre le récepteur de notification et la source de notification. 
  
Avant d' **** appeler Advise, les clients peuvent déterminer si un fournisseur de banque de messages prend en charge la notification en vérifiant que l'indicateur STORE_NOTIFY_OK est défini dans le **PR_STORE_SUPPORT_MASK** de la Banque de messages ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). inspecteur. Il n'existe aucun moyen pour les clients de déterminer à l'avance si un fournisseur de carnet d'adresses prend en charge les notifications ou non. Les clients doivent tenter de s'inscrire et si la tentative échoue, ils peuvent supposer que les notifications ne sont pas prises en charge.
  
Lorsqu'un événement pour lequel un client a enregistré se produit, la source de notification avertit le récepteur de notification en appelant sa méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) avec une structure de données de notification qui contient des informations sur l'événement. L'implémentation d'un récepteur de notifications d' **OnNotify** peut effectuer des tâches en réponse à la notification, telle que la mise à jour des données en mémoire ou l'actualisation de l'affichage de l'écran. 
  
Les fournisseurs de services peuvent implémenter la prise en charge des notifications manuellement ou tirer parti de l'aide fournie dans trois méthodes **IMAPISupport** : [IMAPISupport:: subscribe](imapisupport-subscribe.md), [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md)et [IMAPISupport:: Notify ](imapisupport-notify.md). Les méthodes **subscribe** et unsubscribe gèrent l'inscription et l'annulation de l'enregistrement des notifications pour les fournisseurs; **** la méthode **Notify** gère l'envoi de notifications lorsque cela est nécessaire. 
  
Pour utiliser les méthodes de l'objet de prise en charge pour l'enregistrement des notifications, les fournisseurs de services appellent [IMAPISupport:: subscribe](imapisupport-subscribe.md) dans leurs méthodes de **Conseil** et passent pour **abonner** le pointeur de récepteur de notifications que les clients transmettent à l' **avis**. Si un identificateur d'entrée est transmis en tant que paramètre d'entrée pour spécifier une source de notification, les fournisseurs de services le convertissent en une clé binaire. **Subscribe** crée un numéro de connexion unique et correspond à ce nombre que les fournisseurs de services renvoient aux clients. Les fournisseurs de services peuvent libérer le pointeur d'objet du récepteur de notifications du client à tout moment une fois l'appel de la **notification** terminé. 
  
Lorsque les clients **** appellent Unadvise pour annuler une inscription, les fournisseurs de services décrémentent le décompte de référence sur le pointeur du récepteur de notification du client ou appeler unsubscribe pour faire la même chose. **** 
  
Lorsqu'il est temps de générer une notification, les fournisseurs de services effectuent tout traitement interne lié à la notification et initialisent une structure de [notification](notification.md) en définissant tous ses membres inutilisés sur zéro. Cette technique d'initialisation de la structure de **notification** peut aider les clients à créer des implémentations **OnNotify** plus petites, plus rapides et moins sujettes aux erreurs. 
  
L'illustration suivante montre la communication entre les objets de récepteur de notification, les objets de source de notification et MAPI. MAPI est uniquement impliqué lorsque la source de notification appelle les méthodes **IMAPISupport** pour prendre en charge les notifications. 
  
**Appels de notification d’événement**
  
![Appels de notification d'événement] (media/amapi_51.gif "Appels de notification d'événement")
  
La classe MFCMAPI **CAdviseSink** (à l'aide des fichiers AdviseSink. h et AdviseSink. cpp) implémente l'objet de récepteur de notifications pour tous les appels à **conseiller**. Pour plus d'informations sur MFCMAPI, consultez [la rubrique MFCMAPI en tant qu'exemple de code](mfcmapi-as-a-code-sample.md) et [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154).
  

