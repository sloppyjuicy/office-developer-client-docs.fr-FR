---
title: Initialisation de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 5fde3e7eda8d98eb5080fff360616649b1eb96a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309729"
---
# <a name="initializing-mapi"></a>Initialisation de MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Toutes les applications clientes qui utilisent les bibliothèques MAPI doivent appeler la fonction **MAPIInitialize** . Pour plus d'informations, consultez la rubrique [MAPIInitialize](mapiinitialize.md). **MAPIInitialize** initialise les données globales pour la session et prépare les bibliothèques MAPI pour accepter les appels. Certains indicateurs doivent être définis dans certaines situations: 
  
- MAPI_NT_SERVICE
    
    Définissez l'indicateur MAPI_NT_SERVICE si votre client est implémenté en tant que service Windows. Si votre client est un service Windows et que vous ne définissez pas cet indicateur, MAPI ne le reconnaîtra pas en tant que service. 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    L'indicateur MAPI_MULTITHREAD_NOTIFICATIONS est lié à la façon dont MAPI gère les notifications. MAPI crée une fenêtre masquée qui reçoit les messages de fenêtre lorsque des modifications sont apportées à un objet générant des notifications. Les messages de fenêtre sont traités à un certain moment, ce qui entraîne l'envoi des notifications et l'appel des méthodes [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) appropriées. 
    
- MAPI_NO_COINIT
    
    Définissez l'indicateur MAPI_NO_COINT afin que **MAPIInitialize** n'essaie pas d'initialiser com avec un appel à [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx). Si une structure **MAPIINIT_0** est transmise à **MAPIInitialize** avec _ULFLAGS_ définie sur MAPI_NO_COINIT, MAPI part du principe que com a déjà été initialisé et ignore l'appel à CoInitialize. ****
    
Si l'indicateur MAPI_MULTITHREAD_NOTIFICATIONS n'est pas passé, MAPI crée la fenêtre de notification sur le thread utilisé pour votre premier appel **MAPIInitialize** . MAPI crée la fenêtre de notification sur un thread distinct si MAPI_MULTITHREAD_NOTIFICATIONS est passé, un thread dédié au traitement des notifications. MAPI attend le thread qui est utilisé pour créer la fenêtre de notification masquée pour: 
  
- Disposer d'une boucle de messages.
    
- Rester débloqué tout au long de la durée de vie de la session.
    
- La durée de vie est plus longue que celle de n'importe quel autre thread créé par votre client. 
    
Vous pouvez choisir le thread utilisé en définissant un indicateur dans le premier appel **MAPIInitialize** . Le danger pour l'un de vos threads de gérer les notifications est que si le thread disparaît, la fenêtre de notification est détruite et les notifications ne peuvent plus être envoyées à l'un de vos autres threads. De plus, un traitement spécial peut être nécessaire pour contrôler la distribution des messages de notification qui sont publiés dans la file d'attente de messages de la fenêtre masquée. 
  
Si vous utilisez une fenêtre distincte pour gérer les notifications, assurez-vous que les notifications s'affichent à l'heure appropriée sur un thread approprié. Vous n'aurez pas besoin de code spécial pour vérifier et traiter les messages Windows qui sont publiés dans la fenêtre de notification. 
  
MAPI recommande que les types d'applications clientes suivants utilisent un thread distinct pour créer la fenêtre masquée pour la prise en charge des notifications:
  
- Tous les clients multithread.
    
- Les services Windows à thread unique et les applications console Win32.
    
- Les clients à thread unique qui n'ont pas besoin d'utiliser leur thread principale pour la notification.
    
Pour utiliser l'approche de thread distincte, appelez **MAPIInitialize** sur chaque thread, en définissant l'indicateur MAPI_MULTITHREAD_NOTIFICATIONS. 
  
> [!NOTE]
> Seul le premier appel d'un client vers **MAPIInitialize** entraîne la création d'une fenêtre masquée pour prendre en charge les notifications. Les appels suivants entraînent uniquement l'incrémentation d'un décompte de référence. 
  

