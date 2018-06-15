---
title: Modèle de réception de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: cecdb2c30d6c9df2aafbeed43714269b863ebc48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19784880"
---
# <a name="message-reception-model"></a>Modèle de réception de message

  
  
**S’applique à**: Outlook 
  
Le fournisseur de transport détermine si le spouleur MAPI doit interrogent pour le courrier entrant ou s’il effectue un appel sur le spouleur MAPI lors de l’arrivée de nouveau courrier. Le fournisseur de transport définit l’indicateur SP_LOGON_POLL lorsqu’il retourne [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) pour demander d’interrogation. Sinon, le fournisseur de transport utilise [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) lorsque le courrier entrant n’est disponible. Après la formation que le courrier entrant est disponible, le spouleur MAPI ouvre un nouveau message et demande le fournisseur de transport pour stocker les propriétés de message reçu dans le message. 
  
Ce processus fonctionne comme suit :
  
1. Messages disponibles sont indiqués par le fournisseur de transport appelant **IMAPISupport::SpoolerNotify** ou par le spouleur MAPI [IXPLogon::Poll](ixplogon-poll.md)l’appel.
    
2. Le spouleur MAPI appelle [IXPLogon::StartMessage](ixplogon-startmessage.md) pour lancer le processus. 
    
3. Le fournisseur de transport place une valeur de référence à l’emplacement référencé dans **StartMessage**. Ces valeurs de référence autoriser le fournisseur de transport et le spouleur MAPI pour effectuer le suivi des messages est en cours de traitement quand il y a plusieurs messages à remettre.
    
4. Le fournisseur de transport stocke les données du message dans le passé [IMessage : IMAPIProp](imessageimapiprop.md) instance. 
    
5. Le fournisseur de transport appelle la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) sur l’instance de **IMessage** et renvoie à partir de **StartMessage**.
    
6. Le spouleur MAPI appelle [IXPLogon::TransportNotify](ixplogon-transportnotify.md) si elle doit s’arrêter la remise des messages. 
    
> [!NOTE]
> Si un fournisseur de transport doit fournir un grand nombre de messages et le fournisseur de transport à l’aide **IMAPISupport::SpoolerNotify** au lieu de **IXPLogon::Poll**, il convient ne pas à appeler des **SpoolerNotify** trop souvent ne pas le faire dans l’ordre priver les autres fournisseurs de transport de temps processeur. Le spouleur MAPI n’a pas logique pour éviter ce problème, mais en général l’intervalle entre les appels **SpoolerNotify** doit être plus longue que la durée de votre fournisseur de transport pour traiter un message. > En outre, le spouleur MAPI peut traiter pas immédiatement un message entrant. Le spouleur MAPI peut demander le fournisseur de transport pour effectuer d’autres tâches avant de recevoir le message entrant. 
  

