---
title: Modèle de réception des messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 487598374f15300cc8b899a50d74b535b5a33c91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415116"
---
# <a name="message-reception-model"></a>Modèle de réception des messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le fournisseur de transport contrôle si le spouleur MAPI doit l'interroger pour le courrier entrant ou s'il effectue un appel vers le spouleur MAPI lors de l'arrivée de nouveaux messages. Le fournisseur de transport définit l'indicateur SP_LOGON_POLL lorsqu'il revient de [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) pour demander l'interrogation. Dans le cas contraire, le fournisseur de transport utilise [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) lorsque le courrier entrant est disponible. Une fois que le courrier entrant est disponible, le spouleur MAPI ouvre un nouveau message et demande au fournisseur de transport de stocker les propriétés de message reçues dans le message. 
  
Ce processus fonctionne comme suit:
  
1. Les messages disponibles sont indiqués par le fournisseur de transport appelant **IMAPISupport:: SpoolerNotify** ou par le SPOULEur MAPI qui appelle [IXPLogon::P oll](ixplogon-poll.md).
    
2. Le spouleur MAPI appelle [IXPLogon:: StartMessage](ixplogon-startmessage.md) pour lancer le processus. 
    
3. Le fournisseur de transport place une valeur de référence à l'emplacement référencé dans **StartMessage**. Ces valeurs de référence autorisent le fournisseur de transport et le spouleur MAPI à effectuer le suivi du message en cours de traitement lorsqu'il y a plusieurs messages à livrer.
    
4. Le fournisseur de transport stocke les données de message dans l'instance [IMessage: IMAPIProp](imessageimapiprop.md) passée. 
    
5. Le fournisseur de transport appelle la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) sur l'instance **IMessage** et renvoie à partir de **StartMessage**.
    
6. Le spouleur MAPI appelle [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) s'il doit arrêter la remise des messages. 
    
> [!NOTE]
> Si un fournisseur de transport doit livrer un grand nombre de messages et que le fournisseur de transport utilise **IMAPISupport:: SpoolerNotify** au lieu de **IXPLogon::P oll**, vous devez veiller à ne pas appeler **SpoolerNotify** trop fréquemment pour ne pas priver les autres fournisseurs de transport du temps processeur. Le spouleur MAPI est doté d'une logique pour éviter ce problème, mais en général l'intervalle entre les appels **SpoolerNotify** doit être plus long que le temps nécessaire à votre fournisseur de transport pour traiter un message. > en outre, le spouleur MAPI ne peut pas traiter immédiatement un message entrant. Le spouleur MAPI peut demander au fournisseur de transport d'effectuer d'autres tâches avant de recevoir le message entrant. 
  

