---
title: IMsgStoreStoreLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.StoreLogoff
api_type:
- COM
ms.assetid: 3773c98e-531e-4bdc-a39a-2c3bb7378cd3
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: be11c536804682d1baec8188b6d7487c71d411e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424335"
---
# <a name="imsgstorestorelogoff"></a>IMsgStore::StoreLogoff

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Active la ff de logo dans l’ordre de la boutique de messages.
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [in, out] Masque de bits d’indicateurs qui contrôle la ff de logo à partir de la boutique de messages. Lors de l’entrée, tous les indicateurs définies pour ce paramètre s’excluent mutuellement ; Un appelant ne doit spécifier qu’un seul indicateur par appel. Les indicateurs suivants sont valides lors de l’entrée :
    
LOGOFF_ABORT 
  
> Toute activité de fournisseur de transport pour cette magasin de messages doit être arrêtée avant la ff. Le contrôle est renvoyé à l’appelant après l’arrêt de l’activité. Si une activité de fournisseur de transport a lieu, la ffage de logo ne se produit pas et aucun changement de comportement du fournisseur de transport ou dupooler MAPI ne se produit. Si l’activité du fournisseur de transport est inactive, lepooler MAPI libère le magasin. 
    
LOGOFF_NO_WAIT 
  
> La magasin de messages ne doit pas attendre les messages des fournisseurs de transport avant de se fermer. Les messages sortants prêts à être envoyés sont envoyés. Si cette boutique contient la boîte de réception par défaut, tous les messages in-process sont reçus, puis la réception est désactivée. Une fois l’activité terminée, lepooler MAPI libère le magasin et le contrôle est immédiatement renvoyé à l’appelant. 
    
LOGOFF_ORDERLY 
  
> La magasin de messages ne doit pas attendre les informations des fournisseurs de transport avant de fermer. Les messages en cours de traitement sont terminés, mais aucun nouveau message n’est traitée. Une fois toutes les activités terminées, lepooler MAPI libère le magasin et le contrôle est immédiatement renvoyé au fournisseur du magasin. 
    
LOGOFF_PURGE 
  
> La logoff doit fonctionner de la même manière que si l’indicateur LOGOFF_NO_WAIT est définie, mais la méthode [IXPLogon::FlushQueues ou](ixplogon-flushqueues.md) [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) pour les fournisseurs de transport appropriés doit être appelée. L’LOGOFF_PURGE de contrôle renvoie le contrôle à l’appelant une fois l’exécution terminée. 
    
LOGOFF_QUIET 
  
> Si une activité de fournisseur de transport a lieu, la logoff ne doit pas se produire.
    
    The following flags are valid on output:
    
LOGOFF_INBOUND 
  
> Les messages entrants arrivent actuellement.
    
LOGOFF_OUTBOUND 
  
> Les messages sortants sont en cours d’envoi.
    
LOGOFF_OUTBOUND_QUEUE 
  
> Les messages sortants sont en attente (c’est-à-dire qu’ils sont dans la boîte d’envoi).
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La ff de logo s’est terminée correctement.
    
## <a name="remarks"></a>Remarques

La **méthode IMsgStore::StoreLogoff** exerce le contrôle sur l’interaction entre la boutique de messages et les fournisseurs de transport pendant le processus de ffage de la logo. **L’appel de StoreLogoff est** valide uniquement pour les magasins de messages utilisés uniquement par l’appelant. Par exemple, lorsque deux clients utilisent la même magasin de messages et que l’un d’eux appelle **StoreLogoff,** la magasin de messages est immédiatement libérée et le contrôle est renvoyé au client appelant.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Enregistrez les indicateurs transmis à **StoreLogoff** et passez-les lorsque vous appelez la méthode [IMAPISupport::StoreLogoffTransports.](imapisupport-storelogofftransports.md) N’appelez **pas StoreLogoffTransports tant** que le nombre de références de la boutique de messages n’est pas nul. Plusieurs appels **à StoreLogoffTransports** écrivent simplement les indicateurs enregistrés. 
  
Si aucun appel n’a été effectué à **StoreLogoff** avant que le nombre de références de la boutique de messages n’atteigne zéro, définissez l’indicateur LOGOFF_ABORT dans le paramètre _ulFlags_ que vous passez à **StoreLogoffTransports.**
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

