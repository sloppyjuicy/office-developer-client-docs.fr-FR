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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: be11c536804682d1baec8188b6d7487c71d411e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348740"
---
# <a name="imsgstorestorelogoff"></a>IMsgStore::StoreLogoff

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Active la déconnexion de la Banque de messages de façon ordonnée.
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [in, out] Masque de des indicateurs qui contrôle la fermeture de session à partir de la Banque de messages. Lors de l'entrée, tous les indicateurs définis pour ce paramètre s'excluent mutuellement; un appelant ne doit spécifier qu'un seul indicateur par appel. Les indicateurs suivants sont valides à l'entrée:
    
LOGOFF_ABORT 
  
> Toute activité de fournisseur de transport pour cette banque de messages doit être arrêtée avant la fermeture de session. Le contrôle est renvoyé à l'appelant une fois l'activité arrêtée. Si une activité de fournisseur de transport est en cours d'exécution, la déconnexion ne se produit pas et aucune modification n'est apportée au comportement du spouleur MAPI ou des fournisseurs de transport. Si l'activité du fournisseur de transport est inactive, le spouleur MAPI libère le magasin. 
    
LOGOFF_NO_WAIT 
  
> La Banque de messages ne doit pas attendre les messages provenant de fournisseurs de transport avant de se fermer. Les messages sortants prêts à être envoyés sont envoyés. Si ce magasin contient la boîte de réception par défaut, tous les messages en cours de traitement sont reçus, puis la réception supplémentaire est désactivée. Une fois toutes les activités terminées, le spouleur MAPI libère le magasin et le contrôle est immédiatement renvoyé à l'appelant. 
    
LOGOFF_ORDERLY 
  
> La Banque de messages ne doit pas attendre les informations des fournisseurs de transport avant de se fermer. Les messages en cours de traitement sont terminés, mais aucun nouveau message n'est traité. Une fois toutes les activités terminées, le spouleur MAPI libère le magasin et le contrôle est immédiatement renvoyé au fournisseur de banque. 
    
LOGOFF_PURGE 
  
> La déconnexion doit fonctionner de la même manière que si l'indicateur LOGOFF_NO_WAIT est défini, mais la méthode [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) ou [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) pour les fournisseurs de transport appropriés doit être appelée. L'indicateur LOGOFF_PURGE renvoie le contrôle à l'appelant une fois l'opération terminée. 
    
LOGOFF_QUIET 
  
> Si une activité de fournisseur de transport est en cours, la déconnexion ne doit pas avoir lieu.
    
    The following flags are valid on output:
    
LOGOFF_INBOUND 
  
> Les messages entrants arrivent actuellement.
    
LOGOFF_OUTBOUND 
  
> Les messages sortants sont en cours d'envoi.
    
LOGOFF_OUTBOUND_QUEUE 
  
> Les messages sortants sont en attente (ils se trouvent dans la boîte d'envoi).
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La déconnexion s'est déroulée correctement.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore:: StoreLogoff** exerce un contrôle sur l'interaction de la Banque de messages et des fournisseurs de transport lors du processus de fermeture de session. L'appel de **StoreLogoff** est valide uniquement pour les banques de messages qui sont utilisées uniquement par l'appelant. Par exemple, lorsque deux clients utilisent le même magasin de messages et que l'un d'entre eux appelle **StoreLogoff**, la Banque de messages est immédiatement libérée et le contrôle est renvoyé au client appelant.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Enregistrez les indicateurs transmis à **StoreLogoff** et transmettez-les lorsque vous appelez la méthode [IMAPISupport:: StoreLogoffTransports](imapisupport-storelogofftransports.md) . N'appelez pas **StoreLogoffTransports** tant que le nombre de références de la Banque de messages n'est pas inférieur à zéro. Plusieurs appels à **StoreLogoffTransports** remplacent simplement les indicateurs enregistrés. 
  
Si aucun appel n'a été passé à **StoreLogoff** avant que le nombre de références de la Banque de messages n'atteigne zéro, définissez l'indicateur LOGOFF_ABORT dans le paramètre _ulFlags_ que vous transmettez à **StoreLogoffTransports**.
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

