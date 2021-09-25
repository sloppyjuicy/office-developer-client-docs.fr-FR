---
title: Initialisation de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7efde83b40ca62fcd19d430f9b261789bac55e18
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556349"
---
# <a name="initializing-mapi"></a>Initialisation de MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Toutes les applications clientes qui utilisent les bibliothèques MAPI doivent appeler la **fonction MAPIInitialize.** Pour plus d’informations, [voir MAPIInitialize](mapiinitialize.md). **MAPIInitialize** initialise les données globales de la session et prépare les bibliothèques MAPI à accepter les appels. Quelques indicateurs sont importants à définir dans certaines situations : 
  
- MAPI_NT_SERVICE
    
    Définissez l MAPI_NT_SERVICE si votre client est implémenté en tant que service Windows client. Si votre client est un service Windows et que vous ne définissez pas cet indicateur, MAPI ne le reconnaîtra pas en tant que service. 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    L MAPI_MULTITHREAD_NOTIFICATIONS de gestion des notifications est lié à la façon dont MAPI gère les notifications. MAPI crée une fenêtre masquée qui reçoit des messages de fenêtre lorsque des modifications sont apportées à un objet générant des notifications. Les messages de fenêtre sont traitées à un moment donné, ce qui entraîne l’envoi des notifications et l’appel des méthodes [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) appropriées. 
    
- MAPI_NO_COINIT
    
    Définissez l MAPI_NO_COINT de sorte que **MAPIInitialize** n’essaie pas d’initialiser COM avec un appel à [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx). Si une structure MAPIINIT_0 est transmise à **MAPIInitialize** avec _ulFlags_ définie sur MAPI_NO_COINIT, MAPI suppose que COM **a** déjà été initialisé et ignore l’appel à **CoInitialize**.
    
Si MAPI_MULTITHREAD_NOTIFICATIONS’indicateur n’est pas passé, MAPI crée la fenêtre de notification sur le thread qui a été utilisé pour votre premier appel **MAPIInitialize.** MAPI crée la fenêtre de notification sur un thread distinct si MAPI_MULTITHREAD_NOTIFICATIONS est transmis , un thread dédié à la gestion des notifications. MAPI attend du thread utilisé pour créer la fenêtre de notification masquée : 
  
- Avoir une boucle de message.
    
- Restez débloqué tout au long de la durée de vie de la session.
    
- Avoir une durée de vie plus longue que tout autre thread créé par votre client. 
    
Vous pouvez choisir le fil de discussion utilisé en fixant un indicateur dans le premier **appel MAPIInitialize.** Le risque de permettre à l’un de vos threads de gérer les notifications est que si le thread disparaît, la fenêtre de notification est détruite et les notifications ne peuvent plus être envoyées à aucun de vos autres threads. En outre, un traitement spécial peut être nécessaire pour contrôler la distribution des messages de notification publiés dans la file d’attente de messages de la fenêtre masquée. 
  
Si vous utilisez une fenêtre distincte pour gérer les notifications, soyez certain que les notifications apparaîtront au moment approprié sur un thread approprié. Vous n’aurez pas besoin de code spécial pour vérifier et traiter les messages Windows publiés dans la fenêtre de notification. 
  
MAPI recommande que les types d’applications clientes suivants utilisent un thread distinct pour créer la fenêtre masquée pour la prise en charge des notifications :
  
- Tous les clients multithread.
    
- Les services de Windows thread unique et les applications console Win32.
    
- Clients à thread unique qui n’ont pas besoin d’utiliser leur thread principal pour la notification.
    
Pour utiliser l’approche de thread distincte, appelez **MAPIInitialize** sur chaque thread, en MAPI_MULTITHREAD_NOTIFICATIONS’indicateur. 
  
> [!NOTE]
> Seul le premier appel d’un client à **MAPIInitialize** entraîne la création d’une fenêtre masquée pour prendre en charge les notifications. Les appels suivants entraînent uniquement l’incrémentation d’un nombre de références. 
  

