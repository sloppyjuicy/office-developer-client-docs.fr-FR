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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2ac8fb6f4e56b6f086e6061c227120cd49fc621a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784261"
---
# <a name="imsgstorestorelogoff"></a>IMsgStore::StoreLogoff

  
  
**S’applique à**: Outlook 
  
Permet la déconnexion ordonnée de la banque de messages.
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [entrée, sortie] Masque de bits d’indicateurs qui contrôle la fermeture de session à partir de la banque de messages. À l’entrée, tous les indicateurs de ce paramètre sont mutuellement ; l’appelant doit spécifier qu’un seul indicateur par appel. Les indicateurs suivants sont valides sur ENTRÉE :
    
LOGOFF_ABORT 
  
> Toute activité du fournisseur de transport pour cette banque de messages doit être arrêtée avant la fermeture de session. Contrôle est renvoyé à l’appelant une fois que l’activité est arrêtée. Si aucune activité de fournisseur de transport a lieu, la fermeture de session ne se produit pas et aucune modification du comportement des fournisseurs de transport ou spouleur MAPI se produit. Si l’activité de fournisseur de transport est inactive, le spouleur MAPI libère le magasin. 
    
LOGOFF_NO_WAIT 
  
> La banque de messages ne doit pas attendre pour les messages de fournisseurs de transport avant la fermeture. Les messages sortants qui sont prêts à être envoyés sont envoyées. Si ce magasin contient la boîte de réception par défaut, tous les messages en cours sont reçus, puis réception supplémentaire est désactivée. Lorsque toutes les activités sont terminée, le spouleur MAPI libère le magasin et contrôle est immédiatement renvoyé à l’appelant. 
    
LOGOFF_ORDERLY 
  
> La banque de messages ne doit pas attendre pour plus d’informations à partir des fournisseurs de transport avant de se fermer. Les messages qui sont actuellement en cours de traitement sont terminées, mais aucuns nouveaux messages ne sont traités. Lorsque toutes les activités sont terminée, le spouleur MAPI libère le magasin et contrôle est immédiatement renvoyé au fournisseur de magasin. 
    
LOGOFF_PURGE 
  
> La fermeture de session doit utiliser la même comme si l’indicateur LOGOFF_NO_WAIT est défini, mais la [IXPLogon::FlushQueues](ixplogon-flushqueues.md) [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) méthode ou pour les fournisseurs de transport approprié doit être appelée. L’indicateur LOGOFF_PURGE retourne le contrôle à l’appelant après la fin. 
    
LOGOFF_QUIET 
  
> Si aucune activité de fournisseur de transport a lieu, la fermeture de session ne doit pas se produire.
    
    The following flags are valid on output:
    
LOGOFF_INBOUND 
  
> Les messages entrants arrivent actuellement.
    
LOGOFF_OUTBOUND 
  
> Les messages sortants sont en cours d’envoi.
    
LOGOFF_OUTBOUND_QUEUE 
  
> Les messages sortants sont en attente (autrement dit, ils sont dans la boîte d’envoi).
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La fermeture de session s’est terminée correctement.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::StoreLogoff** exerce de contrôle sur l’interaction du message stocker et fournisseurs de transport au cours du processus de fermeture de session. L’appel **StoreLogoff** est valide uniquement pour les banques de messages qui sont utilisés uniquement par l’appelant. Par exemple, lorsque deux clients utilisent le même magasin de message et un d'entre eux appelle **StoreLogoff**, la banque de messages est immédiatement publiée et le contrôle est retourné au client appelant.
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Enregistrez les indicateurs qui sont passés à **StoreLogoff** et transmettez-les lorsque vous appelez la méthode [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) . N’appelez pas **StoreLogoffTransports** jusqu'à ce que le décompte de références de la banque de messages tombe à zéro. Plusieurs appels à **StoreLogoffTransports** remplacent simplement les indicateurs enregistrés. 
  
Si aucun appel n’a été apporté à **StoreLogoff** avant le message décompte de références du magasin est égal à zéro, définir l’indicateur LOGOFF_ABORT dans le paramètre _ulFlags_ que vous passez à **StoreLogoffTransports**.
  
## <a name="see-also"></a>Voir aussi



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

