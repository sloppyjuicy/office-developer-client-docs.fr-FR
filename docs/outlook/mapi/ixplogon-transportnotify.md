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
ms.openlocfilehash: 2482dc39d3f1d1568b45dd3de88358e08d190be4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428857"
---
# <a name="ixplogontransportnotify"></a>IXPLogon::TransportNotify

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Signale l'occurrence d'un événement sur lequel le fournisseur de transport a demandé une notification.
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [in, out] Masque de réindicateur qui signale les événements de notification. Les indicateurs suivants peuvent être définis par le spouleur MAPI en entrée et doivent être renvoyés inchangés lors de la sortie:
    
NOTIFY_ABORT_DEFERRED 
  
> Informe le fournisseur de transport qu'un message pour lequel il a accepté la responsabilité est différé. Seuls les fournisseurs de transport qui prennent en charge le report doivent prendre en charge cet indicateur. Le paramètre _lppvData_ pointe vers l'identificateur d'entrée du message annulé. Les messages que le spouleur MAPI n'a pas traités peuvent toujours être différés en appelant la méthode [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) . 
    
NOTIFY_BEGIN_INBOUND 
  
> Le spouleur MAPI peut désormais accepter les messages entrants pour cette session de fournisseur de transport. Le spouleur MAPI appelle régulièrement la méthode [IXPLogon::P oll](ixplogon-poll.md) si le fournisseur de transport définit l'indicateur LOGON_SP_POLL avec l'appel [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) à l'ouverture de session. Une fois l'indicateur NOTIFY_BEGIN_INBOUND défini, le spouleur MAPI honore l'indicateur NOTIFY_NEWMAIL transmis dans l'appel à la méthode [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) . La ligne du fournisseur de transport doit être mise à jour avant de renvoyer en appelant la méthode [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) . Les indicateurs NOTIFY_BEGIN_INBOUND et NOTIFY_END_INBOUND s'excluent mutuellement. 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> Indique au fournisseur de transport de passer en revue les messages entrants aussi rapidement que possible. Pour se conformer à cette notification, le fournisseur de transport doit définir l'indicateur STATUS_INBOUND_FLUSH dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de sa ligne de table d'État dès qu'il le peut, à l'aide de **ModifyStatusRow**. Un cycle de messagerie entrante est terminé lorsque le fournisseur détermine qu'il a téléchargé le tout ou lorsqu'il a reçu un appel de méthode **TransportNotify** avec l'indicateur NOTIFY_END_INBOUND_FLUSH défini. Jusqu'à la fin du cycle de messagerie entrante, le fournisseur ne doit pas appeler la méthode [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) , ni passer des cycles au système d'exploitation pour accélérer la remise des messages entrants. Cela est acceptable car le spouleur MAPI utilise généralement NOTIFY_BEGIN_INBOUND_FLUSH uniquement en réponse à la demande d'un utilisateur, via une application cliente, pour fournir tous les messages maintenant. À la fin de l'opération de vidage entrant, le fournisseur doit utiliser **SpoolerNotify** pour effacer l'indicateur STATUS_INBOUND_FLUSH dans la propriété **PR_STATUS_CODE** de sa ligne d'État. 
    
NOTIFY_BEGIN_OUTBOUND 
  
> Les opérations sortantes peuvent maintenant se produire pour cette session de fournisseur de transport. S'il existe des messages à envoyer pour ce fournisseur, un appel à la méthode [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) suit. La ligne de la table d'état de cette session doit être mise à jour avant de renvoyer. Les indicateurs NOTIFY_BEGIN_OUTBOUND et NOTIFY_END_OUTBOUND s'excluent mutuellement. 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> Fonctionne de la même manière que l'indicateur NOTIFY_BEGIN_INBOUND_FLUSH, mais fait référence aux messages sortants. L'indicateur d'état approprié est STATUS_OUTBOUND_FLUSH.
    
NOTIFY_CANCEL_MESSAGE 
  
> Le spouleur MAPI doit annuler le transfert du message pour lequel le paramètre _lppvData_ pointe vers la valeur 32 bits à partir de l'appel de méthode **IXPLogon:: SubmitMessage** . L'indicateur NOTIFY_CANCEL_MESSAGE peut être défini sans que le fournisseur de transport retournée à partir de l'appel de méthode **SubmitMessage**, **IXPLogon:: StartMessage**ou **IXPLogon:: EndMessage** associé au message. Le fournisseur de transport doit renvoyer dès que possible à partir du point d'entrée qui gère le message annulé. Pour un message entrant en cours de traitement, le fournisseur de transport doit enregistrer le message entrant où qu'il était actuellement stocké et le remet à un moment opportun. Les données de l'objet message déjà stockées pour le message entrant sont ignorées. Si le fournisseur de transport n'a pas mis à jour cette valeur 32 bits au **StartMessage** ou **SubmitMessage** , la valeur est 0 pour les messages sortants et 1 pour les messages entrants. 
    
NOTIFY_END_INBOUND 
  
> Les opérations entrantes doivent cesser de s'arrêter pour cette session de fournisseur de transport. Le spouleur MAPI cesse d'utiliser la méthode de **sondage** et ignore NOTIFY_NEWMAIL pour cette session. Les messages en cours de traitement doivent être terminés. La ligne de la table d'état de la session de transport doit être mise à jour en appelant [ModifyStatusRow](imapisupport-modifystatusrow.md) avant de renvoyer. Les indicateurs NOTIFY_END_INBOUND et NOTIFY_BEGIN_INBOUND s'excluent mutuellement. 
    
NOTIFY_END_INBOUND_FLUSH 
  
> Indique au fournisseur de transport de sortir du mode de vidage du trafic entrant. Le fournisseur de transport ne doit pas arrêter le téléchargement, mais le téléchargement doit être réalisé en arrière-plan. La ligne de la table d'état de la session de transport doit être mise à jour en appelant **ModifyStatusRow** lorsque le fournisseur de transport peut se conformer à cette notification. 
    
NOTIFY_END_OUTBOUND 
  
> Les opérations sortantes doivent cesser de s'arrêter pour cette session de fournisseur de transport. Le spouleur MAPI cesse d'appeler **SubmitMessage** et ignore l'indicateur **SpoolerNotify** NOTIFY_READYTOSEND. S'il existe un message sortant en cours d'envoi, il ne doit pas être arrêté; pour arrêter la remise d'un message, utilisez l'indicateur NOTIFY_CANCEL_MESSAGE. La ligne de la table d'État pour cette session doit être mise à jour en appelant **ModifyStatusRow** avant de renvoyer. Les indicateurs NOTIFY_END_INBOUND et NOTIFY_BEGIN_OUTBOUND s'excluent mutuellement. 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> Fonctionne de la même manière que NOTIFY_END_INBOUND_FLUSH, mais fait référence aux messages sortants. L'indicateur d'état approprié est STATUS_OUTBOUND_FLUSH.
    
 _lppvData_
  
> remarquer Pointeur vers un pointeur vers des données spécifiques à l'événement. Pour plus d'informations sur ce que _lppvData_ spécifie, voir la description du paramètre _lpulFlags_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPLogon:: TransportNotify** pour signaler au fournisseur de transport les événements pour lesquels la notification a été demandée. Ces événements incluent une demande de spouleur MAPI permettant d'annuler le transfert d'un message, le début ou la fin des opérations de transport entrantes ou sortantes, ainsi que le début ou la fin d'une opération pour effacer une file d'attente de messages entrants ou sortants. 
  
Lorsque l'utilisateur tente d'annuler un message que le fournisseur de transport a précédemment différé, le spouleur MAPI appelle **TransportNotify**, en transmettant les indicateurs NOTIFY_ABORT_DEFERRED et NOTIFY_CANCEL_MESSAGE dans _ulFlags_. Si le spouleur MAPI se déconnecte et dispose toujours de messages dans la file d'attente, il passe uniquement NOTIFY_ABORT_DEFERRED dans _ulFlags_ lorsqu'il appelle **TransportNotify**.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Le fournisseur doit synchroniser l'accès à ses données lors de cet appel, car le spouleur MAPI peut appeler cette méthode à partir d'un autre thread d'exécution ou d'une procédure pour une autre fenêtre. Cela se produit très probablement lorsque le spouleur MAPI signale l'annulation d'un message que le fournisseur de transport a commencé à envoyer.
  
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

