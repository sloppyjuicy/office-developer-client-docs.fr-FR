---
title: IXPLogonTransportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportNotify
api_type:
- COM
ms.assetid: c712fc17-f436-41cf-9aa3-186c9a86d56e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f0c5cd70595ea43a0957e764150ee4d5153e32c6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589685"
---
# <a name="ixplogontransportnotify"></a>IXPLogon::TransportNotify

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique l’occurrence d’un événement demandé une notification sur lequel le fournisseur de transport.
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [entrée, sortie] Masque de bits d’indicateurs qui signale les événements de notification. Les indicateurs suivants peuvent être définies par le spouleur MAPI à l’entrée et doivent être renvoyés inchangées sortie :
    
NOTIFY_ABORT_DEFERRED 
  
> Notifie le fournisseur de transport qu’un message pour lequel il accepté de responsabilité est différé. Uniquement les fournisseurs de transport qui prennent en charge report doivent prendre en charge cet indicateur. Le paramètre _lppvData_ pointe vers l’identificateur d’entrée du message annulé. Messages le spouleur MAPI n’a pas traité peuvent toujours être différés en appelant la méthode [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) . 
    
NOTIFY_BEGIN_INBOUND 
  
> Le spouleur MAPI peut désormais accepter les messages entrants pour cette session de fournisseur de transport. Le spouleur MAPI appelle régulièrement la méthode [IXPLogon::Poll](ixplogon-poll.md) si le fournisseur de transport définie l’indicateur LOGON_SP_POLL avec l’appel [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) à l’ouverture de session. Une fois que l’indicateur NOTIFY_BEGIN_INBOUND est défini, le spouleur MAPI respecte l’indicateur NOTIFY_NEWMAIL transmis dans l’appel à la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) . La ligne de table d’état pour la session de fournisseur de transport doit être mis à jour avant de retourner en appelant la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . Les indicateurs NOTIFY_BEGIN_INBOUND et NOTIFY_END_INBOUND s’excluent mutuellement. 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> Indique le fournisseur de transport pour passer en revue les messages entrants aussi rapidement que possible. Pour se conformer à cette notification, le fournisseur de transport doit définir l’indicateur STATUS_INBOUND_FLUSH dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de ligne de tableau son état dès que possible, à l’aide de **ModifyStatusRow**. Un cycle de messagerie entrant est terminé lorsque le fournisseur détermine qu’il a téléchargé il peut ou lorsqu’il a reçu un appel de méthode **TransportNotify** avec l’indicateur NOTIFY_END_INBOUND_FLUSH. Jusqu'à la fin du cycle de messagerie entrant, le fournisseur ne doit pas appeler la méthode [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) ou renoncer à cycles pour le système d’exploitation pour la remise des messages entrants vitesse dans le cas contraire. Cela est acceptable, car le spouleur MAPI utilise généralement NOTIFY_BEGIN_INBOUND_FLUSH uniquement en réponse à une demande d’un utilisateur, par le biais d’une application cliente, pour remettre tous les messages maintenant. À la fin de l’opération de vidage entrante, le fournisseur doit utiliser **SpoolerNotify** pour effacer l’indicateur STATUS_INBOUND_FLUSH dans la propriété **PR_STATUS_CODE** de la ligne d’état. 
    
NOTIFY_BEGIN_OUTBOUND 
  
> Opérations sortantes peuvent se produire maintenant pour cette session de fournisseur de transport. S’il existe des messages envoyés à ce fournisseur, un appel à la méthode [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) suit. La ligne de table d’état pour cette session doit être mis à jour avant de retourner. Les indicateurs NOTIFY_BEGIN_OUTBOUND et NOTIFY_END_OUTBOUND s’excluent mutuellement. 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> Fonctionne comme l’indicateur NOTIFY_BEGIN_INBOUND_FLUSH, mais fait référence à des messages sortants. L’indicateur d’état appropriée est STATUS_OUTBOUND_FLUSH.
    
NOTIFY_CANCEL_MESSAGE 
  
> Le spouleur MAPI doit annuler le transfert du message dont le paramètre _lppvData_ pointe vers la valeur 32 bits à partir de la méthode **IXPLogon::SubmitMessage** appel. L’indicateur NOTIFY_CANCEL_MESSAGE peut être défini sans le fournisseur de transport ayant renvoyé à partir de la **SubmitMessage**, **IXPLogon::StartMessage**ou appel de la méthode **IXPLogon::EndMessage** qui est associé au message. Le fournisseur de transport doit renvoyer dès que possible à partir du point d’entrée qui gère le message annulé. Pour un message entrant est actuellement en cours de traitement, le fournisseur de transport enregistrez le message entrant partout où il est stocké actuellement et transmettre à la prochaine fois pratique. Les données d’objet message déjà enregistrées pour le message entrant sont ignorées. Si le fournisseur de transport ne pas cette valeur 32 bits en temps **StartMessage** ou **SubmitMessage** , la valeur est 0 pour les messages sortants et 1 pour les messages entrants. 
    
NOTIFY_END_INBOUND 
  
> Opérations entrantes doivent cesser pour cette session de fournisseur de transport. Le spouleur MAPI cesse d’utiliser la méthode **sondage** et ignore NOTIFY_NEWMAIL pour cette session. De traiter les messages doivent être effectuées. La ligne de table d’état pour la session de transport doit être mis à jour en appelant [ModifyStatusRow](imapisupport-modifystatusrow.md) avant de retourner. Les indicateurs NOTIFY_END_INBOUND et NOTIFY_BEGIN_INBOUND s’excluent mutuellement. 
    
NOTIFY_END_INBOUND_FLUSH 
  
> Notifie le fournisseur de transport à venir en dehors du mode de vidage entrants. Le fournisseur de transport ne doit pas arrêter le téléchargement, mais téléchargement doit être effectué en arrière-plan. La ligne de table d’état pour la session de transport doit être mis à jour en appelant **ModifyStatusRow** lorsque le fournisseur de transport peut être conformes à cette notification. 
    
NOTIFY_END_OUTBOUND 
  
> Opérations sortantes doivent cesser pour cette session de fournisseur de transport. Le spouleur MAPI cesse d’appeler **SubmitMessage** et ignore l’indicateur NOTIFY_READYTOSEND **SpoolerNotify** . S’il existe un message sortant en cours d’envoi, il ne doit pas être arrêté ; Pour arrêter la remise d’un message, utilisez l’indicateur NOTIFY_CANCEL_MESSAGE. La ligne de table d’état pour cette session doit être mis à jour en appelant **ModifyStatusRow** avant de retourner. Les indicateurs NOTIFY_END_INBOUND et NOTIFY_BEGIN_OUTBOUND s’excluent mutuellement. 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> Fonctionne de la même façon à NOTIFY_END_INBOUND_FLUSH, mais fait référence aux messages sortants. L’indicateur d’état appropriée est STATUS_OUTBOUND_FLUSH.
    
 _lppvData_
  
> [out] Pointeur vers un pointeur vers les données spécifiques à l’événement. Pour plus d’informations sur les _lppvData_ Spécifie, voir la description pour le paramètre _lpulFlags_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPLogon::TransportNotify** pour signaler le fournisseur de transport sur les événements pour lequel la notification a été demandée. Ces événements sont notamment une demande de spouleur MAPI pour annuler le transfert d’un message, le début ou la fin des opérations de transport entrants ou sortants et le début ou la fin d’une opération pour effacer une file d’attente de messages entrants ou sortants. 
  
Lorsque l’utilisateur tente d’annuler un message indiquant que le fournisseur de transport a différé précédemment, le spouleur MAPI appelle **TransportNotify**, en passant les indicateurs NOTIFY_CANCEL_MESSAGE et NOTIFY_ABORT_DEFERRED dans _ulFlags_. Si le spouleur MAPI se déconnecte et a encore des messages dans la file d’attente, il passe uniquement NOTIFY_ABORT_DEFERRED _ulFlags_ lorsqu’il appelle **TransportNotify**.
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Le fournisseur doit synchroniser l’accès à ses données à cet appel, car le spouleur MAPI peut appeler cette méthode à partir d’un autre thread d’exécution ou d’une procédure d’une autre fenêtre. Cela se produira probablement lorsque le spouleur MAPI signale l’annulation d’un message que le fournisseur de transport a commencé à envoyer.
  
## <a name="see-also"></a>Voir aussi

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) 
- [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) 
- [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) 
- [IXPLogon::EndMessage](ixplogon-endmessage.md) 
- [IXPLogon::Poll](ixplogon-poll.md)
- [IXPLogon::StartMessage](ixplogon-startmessage.md)
- [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [IXPLogon : IUnknown](ixplogoniunknown.md)

