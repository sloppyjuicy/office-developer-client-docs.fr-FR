---
title: Notification d’événement MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b3b625b-6dea-4b12-99a9-152935bdfe39
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 30d4ad5e0fc1ecdc4c8eb06f75d39e38dd481269
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389973"
---
# <a name="event-notification-in-mapi"></a>Notification d’événement MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Notification d’événements est la communication des informations entre deux objets MAPI. Par le biais d’un des objets, un client ou fournisseur de services s’inscrit pour la notification d’une modification ou d’erreur, appelée un événement, qui peut-être être effectuées dans l’autre objet. Une fois que l’événement se produit, le premier objet est informé de la modification ou l’erreur. L’objet qui reçoit la notification est appelé le récepteur de notifications ; l’objet responsable de la notification est appelé source advise.
  
Il existe trois types de notifications pour les objets de récepteur (tous les types sont des objets MAPI standard) :
  
- Objets de récepteur de notification.   
- Objets de récepteur de notification de formulaire.  
- Affichage de notification objets récepteur.
    
Informez les objets récepteurs sont du type les plus courantes. Récepteurs sont généralement implémentés par les applications clientes pour recevoir le carnet d’adresses et de prise en charge et de notifications de banque de messages de notification du [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface. **IMAPIAdviseSink** contient une seule méthode, [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md). Formulaire et en mode de notification récepteurs sont moins courantes ; ils sont implémentés pour recevoir des notifications sur les modifications apportées à des formulaires personnalisés. Prise en charge des récepteurs de notification du formulaire la [IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) prise en charge des récepteurs de notification interface et afficher la [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface. Étant donné que les objets de récepteur de notification standard de mettre en œuvre la plupart des clients, supposons que discussions de notifications par rapport au carnet d’adresses et notifications de banque de messages plutôt que les notifications de formulaires. Pour plus d’informations sur les notifications de formulaires, voir [Notifications de formulaires MAPI](mapi-forms-notifications.md) et [L’écriture de Code de formulaire serveur](writing-form-server-code.md).
  
Avertir la source d’objets sont implémentés par les fournisseurs de services et MAPI. Tous les fournisseurs de service prennent en charge la notification d’événement ; Il est facultatif, mais fortement recommandé. Adresse et la banque de messages du livre fournisseurs généralement prise en charge les notifications d’objet sur plusieurs de leurs objets et les notifications de tableau sur leur contenu et les tables de hiérarchie. Fournisseurs de transport ne prennent pas en charge les notifications directement ; ils s’appuient sur les autres méthodes de communication avec les clients.
  
Contrairement aux récepteurs de notifications, conseiller objets source ne sont pas un type unique de l’objet MAPI. Plusieurs objets MAPI, tels que les banques de messages et des tableaux, peuvent prendre le rôle de source advise. Une source advise est n’importe quel objet MAPI qui effectue les opérations suivantes :
  
- Implémente une méthode **Advise** pour recevoir des inscriptions des notifications. 
    
- Implémente une méthode **Unadvise** pour recevoir des annulations de notification. 
    
- Génère des notifications de type approprié pour les objets de récepteur advise approprié qui se sont inscrits en appelant leurs méthodes **IMAPIAdviseSink::OnNotify** . 
    
Objets de récepteur d’appel **Advise** lorsqu’ils veulent s’inscrire pour une notification, dans la plupart des cas, en passant l’identificateur d’entrée de l’objet dont l’inscription doit avoir lieu et **Unadvise** lorsqu’ils souhaitent annuler de notification de clients qui implémentent le inscription. Clients passez un paramètre à **Advise** qui indique les types d’événements à contrôler. **Advise** renvoie un nombre différent de zéro qui représente une connexion entre le récepteur de notifications et advise source. 
  
Avant d’appeler **Advise**, les clients peuvent déterminer si un fournisseur de magasin de message prend en charge la notification en vérifiant que l’indicateur STORE_NOTIFY_OK est défini dans **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) du magasin message propriété. Il n’existe aucun moyen pour les clients déterminer à l’avance ou non un fournisseur de carnet d’adresses prend en charge les notifications. Les clients doivent essayez d’enregistrer et si la tentative échoue, ils peuvent supposent que les notifications sont non pris en charge.
  
Lorsque cet événement se produit un événement pour lequel un client a enregistré, la source advise avertit le récepteur de notifications en appelant la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) avec une structure de données de notification qui contient des informations sur l’événement. Implémentation d’un récepteur de notifications de **OnNotify** peut effectuer des tâches en réponse à la notification, telles que la mise à jour des données dans la mémoire ou l’actualisation d’un affichage de l’écran. 
  
Fournisseurs de services peuvent implémenter la prise en charge pour les notifications manuellement ou tirer parti de l’aide fournie dans trois méthodes **IMAPISupport** : [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)et [IMAPISupport::Notify ](imapisupport-notify.md). Les méthodes **d’abonnement** et de **désabonnement** gérer l’inscription aux notifications et annulation d’enregistrement pour les fournisseurs ; la méthode **Notify** gère l’envoi de notifications si nécessaire. 
  
Pour utiliser les méthodes de l’objet de prise en charge pour l’inscription aux notifications, les fournisseurs de services [IMAPISupport::Subscribe](imapisupport-subscribe.md) d’appel dans leurs méthodes **Advise** et passez **s’abonner** le pointeur du récepteur advise que clients passer **Advise**. Si un identificateur d’entrée est passé comme paramètre d’entrée pour spécifier une source de notification, fournisseurs de services de convertir en une clé binaire. **S’abonner** crée un numéro de connexion unique et c’est ce numéro qui renvoient des fournisseurs de services aux clients. Fournisseurs de services de diffusion du client pointeur d’objet récepteur de notification à tout moment après l’appel **Advise** est terminé. 
  
Lorsque les clients appellent **Unadvise** pour annuler un enregistrement, les fournisseurs de services soit décrémenter le décompte de références du client pointeur du récepteur de notification ou **Annuler l’abonnement** pour effectuer la même. 
  
Lorsqu’il est temps de générer une notification, fournisseurs de services exécutez tout traitement interne qui se rapporte à la notification et initialise une structure [NOTIFICATION](notification.md) en affectant à tous ses membres inutilisés à zéro. Cette technique pour l’initialisation de la structure **NOTIFICATION** peut aider les clients à créer plus petit, plus rapide et moins sujet aux erreurs **OnNotify** implémentations. 
  
L’illustration suivante montre la communication entre les objets de récepteur de notification, MAPI et les objets de la source de notification. MAPI est impliquée uniquement lorsque la source advise appelle les méthodes **IMAPISupport** pour la prise en charge de la notification. 
  
**Appels de notification d’événement**
  
![Appels de notification d’événement] (media/amapi_51.gif "Appels de notification d’événement")
  
La classe MFCMAPI **CAdviseSink** (en utilisant les fichiers AdviseSink.h et AdviseSink.cpp) implémente l’objet de récepteur advise pour tous les appels aux **notifications**. Pour plus d’informations sur MFCMAPI, voir [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md) et [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154).
  

