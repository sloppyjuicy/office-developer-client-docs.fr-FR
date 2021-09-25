---
title: Modèle de réception des messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 48cd642cf72a04764c17be5480b10036f61142d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592038"
---
# <a name="message-reception-model"></a>Modèle de réception des messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le fournisseur de transport contrôle si lepooler MAPI doit l’sonder pour le courrier entrant ou s’il effectue un appel aupooler MAPI lorsque de nouveaux messages arrivent. Le fournisseur de transport définit l’SP_LOGON_POLL lorsqu’il retourne à partir [d’IXPProvider::TransportLogon](ixpprovider-transportlogon.md) pour demander l’interrogation. Dans le cas contraire, le fournisseur de transport utilise [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) lorsque le courrier entrant est disponible. Une fois que vous avez appris que le courrier entrant est disponible, lepooler MAPI ouvre un nouveau message et demande au fournisseur de transport de stocker les propriétés du message reçu dans le message. 
  
Ce processus fonctionne comme suit :
  
1. Les messages disponibles sont indiqués par le fournisseur de transport appelant **IMAPISupport::SpoolerNotify** ou par lepooler MAPI appelant [IXPLogon::P.](ixplogon-poll.md)
    
2. Lepooler MAPI appelle [IXPLogon::StartMessage](ixplogon-startmessage.md) pour lancer le processus. 
    
3. Le fournisseur de transport place une valeur de référence à l’emplacement référencé dans **StartMessage**. Ces valeurs de référence permettent au fournisseur de transport et aupooler MAPI d’assurer le suivi du message en cours de traitement lorsqu’il y a plusieurs messages à remettre.
    
4. Le fournisseur de transport stocke les données de message dans l’instance [IMessage : IMAPIProp](imessageimapiprop.md) transmise. 
    
5. Le fournisseur de transport appelle [la méthode IMAPIProp::SaveChanges](imapiprop-savechanges.md) sur l’instance **IMessage** et retourne à partir de **StartMessage**.
    
6. Lepooler MAPI appelle [IXPLogon::TransportNotify](ixplogon-transportnotify.md) s’il doit arrêter la remise du message. 
    
> [!NOTE]
> Si un fournisseur de transport doit remettre un grand nombre de messages et qu’il utilise **IMAPISupport::SpoolerNotify** au lieu d’IXPLogon::P le, il est important de ne pas appeler trop souvent **SpoolerNotify** afin de ne pas inconfidifier d’autres fournisseurs de transport de temps processeur.  Lepooler MAPI a une logique pour empêcher cela, mais en général l’intervalle entre les appels **SpoolerNotify** doit être plus long que le temps qu’il faut à votre fournisseur de transport pour traiter un message. > également, lepooler MAPI peut ne pas traiter immédiatement un message entrant. Lepooler MAPI peut demander au fournisseur de transport d’effectuer d’autres tâches avant de recevoir le message entrant. 
  

