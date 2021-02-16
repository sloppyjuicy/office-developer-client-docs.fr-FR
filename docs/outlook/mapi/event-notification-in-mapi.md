---
title: Notification d’événement dans MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b3b625b-6dea-4b12-99a9-152935bdfe39
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 30d4ad5e0fc1ecdc4c8eb06f75d39e38dd481269
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321394"
---
# <a name="event-notification-in-mapi"></a>Notification d’événement dans MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La notification d’événement est la communication d’informations entre deux objets MAPI. Via l’un des objets, un client ou un fournisseur de services s’inscrit pour la notification d’une modification ou d’une erreur, appelée événement, qui peut avoir lieu dans l’autre objet. Une fois l’événement se produit, le premier objet est averti de la modification ou de l’erreur. L’objet qui reçoit la notification est appelé le sink de notification ; L’objet responsable de la notification est appelé source de notification.
  
Il existe trois types d’objets de type sink de conseil (tous les types sont des objets MAPI standard) :
  
- Conseillez les objets de sink.   
- Les objets de sink de conseil de formulaire.  
- Afficher les objets de sink de conseil.
    
Les objets de type sink de conseil sont le type le plus courant. Les réceptions de notification sont généralement implémentées par les applications clientes pour recevoir des notifications de carnet d’adresses et de magasin de messages et prendre en charge l’interface [IMAPIAdviseSink : IUnknown.](imapiadvisesinkiunknown.md) **IMAPIAdviseSink** contient une seule méthode, [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md). Les sinks de conseil de formulaire et d’affichage sont moins courants ; ils sont implémentés pour recevoir des notifications concernant les modifications apportées aux formulaires personnalisés. Les sinks de conseil de formulaires supportent l’interface [IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) et les sinks de conseil d’affichage la prise en charge de l’interface [IMAPIViewAdviseSink : IUnknown.](imapiviewadvisesinkiunknown.md) Étant donné que la plupart des clients implémentent des objets de réception de notification standard, supposons que les discussions sur les notifications concernent les notifications de carnet d’adresses et de magasin de messages plutôt que les notifications par formulaires. Pour plus d’informations sur les notifications de formulaires, voir [MAPI Forms Notifications](mapi-forms-notifications.md) et [Writing Form Server Code](writing-form-server-code.md).
  
Les objets source de conseil sont implémentés par les fournisseurs de services et par MAPI. Tous les fournisseurs de services ne supportent pas la notification d’événement ; Il est facultatif, mais fortement recommandé. Les fournisseurs de magasins de messages et de carnets d’adresses prend généralement en charge les notifications d’objet sur plusieurs de leurs objets et les notifications de tableau sur leur contenu et leurs tables hiérarchiques. Les fournisseurs de transport ne supportent pas les notifications directement ; ils s’appuient sur d’autres méthodes de communication avec les clients.
  
Contrairement aux sinks de conseil, les objets source de conseil ne sont pas un type unique d’objet MAPI. De nombreux objets MAPI, tels que les magasins de messages et les tables, peuvent prendre le rôle de source de conseil. Une source de conseil est tout objet MAPI qui fait les choses suivantes :
  
- Implémente une **méthode Advise** pour recevoir des inscriptions de notification. 
    
- Implémente **une méthode Unadvise** pour recevoir des annulations de notification. 
    
- Génère des notifications du type approprié aux objets de réception de notification appropriés qui ont été inscrits en appelant leurs méthodes **IMAPIAdviseSink::OnNotify.** 
    
Les clients qui implémentent des objets de réception de notification appellent **Advise** lorsqu’ils souhaitent s’inscrire pour une notification, dans la plupart des cas en passant l’identificateur d’entrée de l’objet avec lequel l’inscription doit avoir lieu, et **Unadvise** lorsqu’ils souhaitent annuler l’inscription. Les clients passent un paramètre **à Advise** qui indique lequel des différents types d’événements qu’ils souhaitent surveiller. **L’avis** renvoie un nombre autre que zéro qui représente une connexion réussie entre le sink de conseil et la source de conseil. 
  
Avant d’appeler **Advise,** les clients peuvent déterminer si un fournisseur de magasins de messages prend en charge la notification en vérifiant que l’indicateur STORE_NOTIFY_OK est définie dans la propriété **PR_STORE_SUPPORT_MASK (** [PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)de la boutique de messages. Les clients ne peuvent pas déterminer à l’avance si un fournisseur de carnet d’adresses prend en charge les notifications. Les clients doivent tenter de s’inscrire et, si la tentative échoue, ils peuvent supposer que les notifications ne sont pas pris en compte.
  
Lorsqu’un événement pour lequel un client s’est inscrit se produit, la source de notification avertit le recevoir en appelant sa méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) avec une structure de données de notification qui contient des informations sur l’événement. L’implémentation **d’OnNotify** par un réception de conseil peut effectuer des tâches en réponse à la notification, telles que la mise à jour des données en mémoire ou l’actualisation d’un écran. 
  
Les fournisseurs de services peuvent implémenter la prise en charge des notifications manuellement ou tirer parti de l’aide fournie dans trois méthodes **IMAPISupport** : [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)et [IMAPISupport::Notify](imapisupport-notify.md). Les **méthodes Subscribe** et **Unsubscribe** gèrent l’inscription et l’enregistrement des notifications pour les fournisseurs ; La **méthode Notify** gère l’envoi de notifications, le cas échéant. 
  
Pour utiliser les méthodes d’objet de support pour l’inscription des notifications, les fournisseurs de services appellent [IMAPISupport::Subscribe](imapisupport-subscribe.md) in their **Advise** methods and pass to **Subscribe** the advise sink pointer that clients pass to **Advise**. Si un identificateur d’entrée est transmis en tant que paramètre d’entrée pour spécifier une source de conseil, les fournisseurs de services le convertissent en clé binaire. **S’abonner** crée un numéro de connexion unique et c’est ce numéro que les fournisseurs de services retournent aux clients. Les fournisseurs de services peuvent libérer le pointeur d’objet de sink du client à tout moment une fois **l’appel** de conseil terminé. 
  
Lorsque les clients appellent **Unadvise** pour annuler une inscription, les fournisseurs de services décrémentent le nombre de références sur le pointeur de sink de conseil du client ou appellent **Unsubscribe** pour en faire de même. 
  
Lorsqu’il est temps de générer une notification, les fournisseurs de services effectuent tout traitement interne lié à la notification et initialisent une structure de [notification](notification.md) en lui fixant la valeur zéro pour tous ses membres inutilisés. Cette technique d’initialisation de la structure **NOTIFICATION** peut aider les clients à créer des implémentations **OnNotify** plus petites, plus rapides et moins sujettes aux erreurs. 
  
L’illustration suivante montre la communication entre les objets de sink de conseil, les objets source de conseil et MAPI. MAPI est impliqué uniquement lorsque la source de notification appelle les méthodes **IMAPISupport** pour la prise en charge des notifications. 
  
**Appels de notification d’événement**
  
![Appels de notification d’événements appels](media/amapi_51.gif "de notification d’événement")
  
La classe MFCMAPI **CAdviseSink** (à l’aide des fichiers AdviseSink.h et AdviseSink.cpp) implémente l’objet de sink de conseil pour tous les appels à **Advise**. Pour plus d’informations sur MFCMAPI, voir [MFCMAPI en](mfcmapi-as-a-code-sample.md) tant qu’exemple de code et [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154).
  

