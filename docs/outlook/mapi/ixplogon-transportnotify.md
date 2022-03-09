---
title: IXPLogonTransportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.TransportNotify
api_type:
- COM
ms.assetid: c712fc17-f436-41cf-9aa3-186c9a86d56e
ms.openlocfilehash: a59e1b9946a9d8beb929fc2ed3d6d34c7176f378
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63377469"
---
# <a name="ixplogontransportnotify"></a>IXPLogon::TransportNotify

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Signale l’occurrence d’un événement sur lequel le fournisseur de transport a demandé une notification.
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [in, out] Masque de bits d’indicateurs signalant les événements de notification. Les indicateurs suivants peuvent être définies par lepooler MAPI lors de l’entrée et doivent être renvoyés inchangés lors de la sortie :
    
NOTIFY_ABORT_DEFERRED 
  
> Avertit le fournisseur de transport qu’un message pour lequel il a accepté la responsabilité est différé. Seuls les fournisseurs de transport qui supportent le report doivent prendre en charge cet indicateur. Le  _paramètre lppvData_ pointe vers l’identificateur d’entrée du message annulé. Les messages que lepooler MAPI n’a pas traitées peuvent toujours être différés en appelant la méthode [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) . 
    
NOTIFY_BEGIN_INBOUND 
  
> Lepooler MAPI peut désormais accepter les messages entrants pour cette session de fournisseur de transport. Lepooler MAPI appelle régulièrement la méthode [IXPLogon::P élément](ixplogon-poll.md) si le fournisseur de transport a pour effet de définir l’indicateur LOGON_SP_POLL avec l’appel [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) lors de l’logonation. Une fois l’indicateur NOTIFY_BEGIN_INBOUND est définie, lepooler MAPI honore l’indicateur NOTIFY_NEWMAIL passé dans l’appel à la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) . La ligne de tableau d’état de la session du fournisseur de transport doit être mise à jour avant d’être retourné en appelant la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . Les indicateurs NOTIFY_BEGIN_INBOUND et NOTIFY_END_INBOUND sont mutuellement exclusifs. 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> Indique au fournisseur de transport de passer les messages entrants aussi rapidement que possible. Pour se conformer à cette notification, le fournisseur de transport doit définir l’indicateur STATUS_INBOUND_FLUSH dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de sa ligne de table d’état dès que possible, à l’aide de **ModifyStatusRow**. Un cycle de messagerie entrant est terminé lorsque le fournisseur détermine qu’il a téléchargé tout ce qu’il peut, ou lorsqu’il a reçu un appel de méthode **TransportNotify** avec l’indicateur NOTIFY_END_INBOUND_FLUSH définie. Jusqu’à la fin du cycle de messagerie entrante, le fournisseur ne doit pas appeler la méthode [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) ou abandonner les cycles vers le système d’exploitation pour accélérer la remise des messages entrants. Cela est acceptable, car lepooler MAPI utilise généralement NOTIFY_BEGIN_INBOUND_FLUSH uniquement en réponse à la demande d’un utilisateur, via une application cliente, pour remettre tous les messages maintenant. À la fin de l’opération de purge entrante, le fournisseur doit utiliser **SpoolerNotify** pour effacer l’indicateur STATUS_INBOUND_FLUSH dans la propriété **PR_STATUS_CODE** de sa ligne d’état. 
    
NOTIFY_BEGIN_OUTBOUND 
  
> Les opérations sortantes peuvent maintenant se produire pour cette session de fournisseur de transport. S’il existe des messages à envoyer pour ce fournisseur, un appel à la méthode [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) suit. La ligne de tableau d’état de cette session doit être mise à jour avant de revenir. Les indicateurs NOTIFY_BEGIN_OUTBOUND et NOTIFY_END_OUTBOUND sont mutuellement exclusifs. 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> Fonctionne de la même façon que l’NOTIFY_BEGIN_INBOUND_FLUSH, mais fait référence aux messages sortants. L’indicateur d’état approprié est STATUS_OUTBOUND_FLUSH.
    
NOTIFY_CANCEL_MESSAGE 
  
> Lepooler MAPI doit annuler le transfert du message pour lequel le paramètre  _lppvData_ pointe vers la valeur 32 bits à partir de l’appel de méthode **IXPLogon::SubmitMessage** . L’indicateur NOTIFY_CANCEL_MESSAGE peut être définie sans que le fournisseur de transport soit retourné à partir de l’appel de méthode **SubmitMessage**, **IXPLogon::StartMessage** ou **IXPLogon::EndMessage** associé au message. Le fournisseur de transport doit retourner dès que possible à partir du point d’entrée qui gère le message annulé. Pour un message entrant en cours de traitement, le fournisseur de transport doit enregistrer le message entrant là où il est actuellement stocké et le remettre à nouveau au moment opportun suivant. Les données d’objet de message déjà stockées pour le message entrant sont ignorées. Si le fournisseur de transport n’a pas mis à jour cette valeur 32 bits au moment de **StartMessage** ou **SubmitMessage** , la valeur est 0 pour les messages sortants et 1 pour les messages entrants. 
    
NOTIFY_END_INBOUND 
  
> Les opérations entrantes doivent cesser pour cette session de fournisseur de transport. Lepooler MAPI cesse d’utiliser la méthode **Poll** et ignore NOTIFY_NEWMAIL pour cette session. Les messages in-process doivent être terminés. La ligne de tableau d’état de la session de transport doit être mise à jour en appelant [ModifyStatusRow](imapisupport-modifystatusrow.md) avant de la renvoyer. Les indicateurs NOTIFY_END_INBOUND et NOTIFY_BEGIN_INBOUND sont mutuellement exclusifs. 
    
NOTIFY_END_INBOUND_FLUSH 
  
> Avertit le fournisseur de transport de sorte qu’il sorte du mode de  purge entrant. Le fournisseur de transport ne doit pas arrêter le téléchargement, mais le téléchargement doit être effectué en arrière-plan. La ligne de table d’état de la session de transport doit être mise à jour en appelant **ModifyStatusRow** lorsque le fournisseur de transport peut se conformer à cette notification. 
    
NOTIFY_END_OUTBOUND 
  
> Les opérations sortantes doivent cesser pour cette session de fournisseur de transport. Lepooler MAPI cesse d’appeler **SubmitMessage** et ignore l’indicateur **NOTIFY_READYTOSEND SpoolerNotify** . S’il existe un message sortant en cours d’envoi, il ne doit pas être arrêté ; pour arrêter la remise d’un message, utilisez l’indicateur NOTIFY_CANCEL_MESSAGE message. La ligne de tableau d’état de cette session doit être mise à jour en appelant **ModifyStatusRow** avant de la renvoyer. Les indicateurs NOTIFY_END_INBOUND et NOTIFY_BEGIN_OUTBOUND sont mutuellement exclusifs. 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> Fonctionne de la même NOTIFY_END_INBOUND_FLUSH, mais fait référence aux messages sortants. L’indicateur d’état approprié est STATUS_OUTBOUND_FLUSH.
    
 _lppvData_
  
> [out] Pointeur vers un pointeur vers des données spécifiques à un événement. Pour plus d’informations sur ce  _que lppvData_ spécifie, voir la description du  _paramètre lpulFlags_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Lepooler MAPI appelle la méthode **IXPLogon::TransportNotify** pour signaler au fournisseur de transport les événements pour lesquels une notification a été demandée. Ces événements incluent une demande depooler MAPI pour annuler un transfert de messages, le début ou la fin des opérations de transport entrantes ou sortantes, ainsi que le début ou la fin d’une opération pour effacer une file d’attente de messages entrants ou sortants. 
  
Lorsque l’utilisateur tente d’annuler un message que le fournisseur de transport a différé précédemment, lepooler MAPI appelle **TransportNotify**, en passant les indicateurs NOTIFY_ABORT_DEFERRED et NOTIFY_CANCEL_MESSAGE dans  _ulFlags_. Si lepooler MAPI se dé connecte et qu’il a toujours des messages dans la file d’attente, il passe uniquement NOTIFY_ABORT_DEFERRED dans  _ulFlags_ lorsqu’il appelle **TransportNotify**.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Le fournisseur doit synchroniser l’accès à ses données lors de cet appel, car lepooler MAPI peut appeler cette méthode à partir d’un autre thread d’exécution ou d’une procédure pour une autre fenêtre. Cela se produit très probablement lorsque lepooler MAPI signale l’annulation d’un message que le fournisseur de transport a commencé à envoyer.
  
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

