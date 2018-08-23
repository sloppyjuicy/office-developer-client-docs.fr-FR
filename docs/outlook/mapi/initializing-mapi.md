---
title: Initialisation de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d896d66db13b2114c1c333084d5f3b1d3a341796
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574789"
---
# <a name="initializing-mapi"></a>Initialisation de MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Toutes les applications clientes qui utilisent les bibliothèques MAPI doivent appeler la fonction **exécuter MAPIInitialize** . Pour plus d’informations, voir [exécuter MAPIInitialize](mapiinitialize.md). **Exécuter MAPIInitialize** initialise les données globales pour la session et prépare les bibliothèques d’accepter les appels MAPI. Il existe quelques indicateurs qui sont importantes pour définir dans certaines situations : 
  
- MAPI_NT_SERVICE
    
    Définir l’indicateur MAPI_NT_SERVICE si votre client est implémentée comme un service Windows. Si votre client est un service Windows et vous ne définissez pas cet indicateur, MAPI le reconnaît pas en tant que service. 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    L’indicateur MAPI_MULTITHREAD_NOTIFICATIONS se rapporte à comment MAPI gère les notifications. MAPI crée une fenêtre masquée qui reçoit les messages de fenêtre lorsque les modifications sont apportées à un objet de génération de notifications. Les messages de fenêtre sont traités à un moment donné, à l’origine de l’envoi des notifications et les méthodes de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) appropriées à appeler. 
    
- MAPI_NO_COINIT
    
    Définir l’indicateur MAPI_NO_COINT pour pouvoir **exécuter MAPIInitialize** n’essaie pas d’initialiser COM avec un appel à [CoInitialize](http://msdn.microsoft.com/en-us/library/ms886303.aspx). Si une structure **MAPIINIT_0** est passée à **exécuter MAPIInitialize** avec _ulFlags_ défini sur MAPI_NO_COINIT, MAPI part du principe que COM a déjà été initialisé et ignorer l’appel à **CoInitialize**.
    
Si l’indicateur MAPI_MULTITHREAD_NOTIFICATIONS n’est pas transmise, MAPI crée la fenêtre de notification sur le thread qui a été utilisé pour votre premier appel **exécuter MAPIInitialize** . MAPI crée la fenêtre de notification sur un thread distinct si MAPI_MULTITHREAD_NOTIFICATIONS est passé, un thread dédié à la gestion des notifications. MAPI attend le thread qui est utilisé pour créer la fenêtre de notification masqué : 
  
- Avoir une boucle de message.
    
- Ne pas bloquer pendant toute la durée de la session.
    
- Avoir une durée de vie plue que tout autre thread créé par votre client. 
    
Vous pouvez choisir de thread qui est utilisé en définissant un indicateur dans le premier appel **exécuter MAPIInitialize** . Le risque en autorisant un de vos threads pour gérer les notifications est que si le thread disparaît, la destruction de la fenêtre de notification et les notifications ne peuvent plus être envoyées à n’importe lequel de vos autres threads. En outre, un traitement spécial peut être nécessaire pour contrôler la distribution des messages de notification qui sont publiés dans la file d’attente de messages de la fenêtre masquée. 
  
Si vous utilisez une fenêtre séparée pour gérer les notifications, être assuré que les notifications seront affiche au moment opportun sur une thread approprié. Vous n’aurez pas de code spécial pour rechercher et traiter les messages Windows qui sont publiés dans la fenêtre de notification. 
  
MAPI recommande les types suivants d’applications clientes d’utiliser un thread distinct pour créer la fenêtre masquée pour la prise en charge de la notification :
  
- Tous les clients multithreads.
    
- Applications de la console Windows services seul thread et Win32.
    
- Un seul thread les clients qui n’ont pas besoin d’utiliser leur thread principale pour notification.
    
Pour utiliser l’approche de thread distinct, appelez **exécuter MAPIInitialize** sur chaque thread, l’indicateur MAPI_MULTITHREAD_NOTIFICATIONS. 
  
> [!NOTE]
> Uniquement d’un client premier appel à **exécuter MAPIInitialize** provoque une fenêtre masquée à créer pour prendre en charge les notifications. Cause uniquement les appels suivants à incrémenter un décompte de références. 
  

