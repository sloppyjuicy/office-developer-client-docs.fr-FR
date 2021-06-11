---
title: IMAPIStatusFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.FlushQueues
api_type:
- COM
ms.assetid: d6b01a91-b452-4b2c-9802-698e7b0f4169
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5f8396ca84192e485d33fb5a96f641361b717584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432603"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Force le téléchargement immédiat de tous les messages en attente d’envoi ou de réception. L’objet d’état dupooler MAPI et les objets d’état implémentés par les fournisseurs de transport la prise en charge de cette méthode.
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.
    
 _cbTargetTransport_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpTargetTransport._ Le  _paramètre cbTargetTransport_ est uniquement définie sur les appels à l’objet d’état dupooler MAPI. Pour les appels à un fournisseur de transport, le  _paramètre cbTargetTransport_ est définie sur 0. 
    
 _lpTargetTransport_
  
> [in] Pointeur vers l’identificateur d’entrée du fournisseur de transport qui doit vider ses files d’attente de messages. Le  _paramètre lpTargetTransport est_ uniquement définie sur les appels à l’objet d’état dupooler MAPI. Pour les appels à un fournisseur de transport,  _le paramètre lpTargetTransport_ est définie sur NULL. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’opération de purge. Les indicateurs suivants peuvent être définies :
    
FLUSH_ASYNC_OK 
  
> L’opération de purge peut se produire de manière asynchrone. Cet indicateur s’applique uniquement à l’objet d’état dupooler MAPI. 
    
FLUSH_DOWNLOAD 
  
> Les files d’attente de messages entrants doivent être vidées.
    
FLUSH_FORCE 
  
> L’opération de purge doit avoir lieu, malgré le risque de diminution des performances. Cet indicateur doit être définie lorsqu’un fournisseur de transport asynchrone est ciblé.
    
FLUSH_NO_UI 
  
> L’objet d’état ne doit pas afficher d’indicateur de progression.
    
FLUSH_UPLOAD 
  
> Les files d’attente de messages sortants doivent être vidées.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de purge a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours ; Il doit être autorisé à se terminer ou arrêté avant que cette opération puisse être lancée.
    
MAPI_E_NO_SUPPORT 
  
> L’objet status ne prend pas en charge cette opération, comme indiqué par l’absence de l’indicateur STATUS_FLUSH_QUEUES dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) de l’objet d’état.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIStatus::FlushQueues** demande aupooler MAPI ou à un fournisseur de transport d’envoyer immédiatement tous les messages de la file d’attente sortante ou de recevoir tous les messages de la file d’attente entrante. **FlushQueues est** implémenté uniquement par l’objet d’état dupooler MAPI et par les objets d’état que les fournisseurs de transport fournissent. 
  
MAPI_E_BUSY les demandes asynchrones doivent être renvoyées afin que les clients continuent à travailler. 
  
Par défaut, **FlushQueues est** une opération synchrone ; ne revient pas à l’appelant tant que le purgement n’est pas terminé. Seule l’opération de purge effectuée par lepooler MAPI peut être asynchrone ; les clients demandent ce comportement en FLUSH_ASYNC_OK’indicateur. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

L’implémentation de **FlushQueues** par un fournisseur de transport distant définit des bits dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la ligne d’état de l’objet d’authentification pour contrôler la façon dont les files d’attente sont vidées. Si une visionneuse distante passe dans l’indicateur FLUSH_UPLOAD, la méthode **FlushQueues** doit définir les STATUS_INBOUND_ENABLED et STATUS_INBOUND_ACTIVE bits. Si une visionneuse distante passe dans l’indicateur FLUSH_DOWNLOAD, la méthode **FlushQueues** doit définir les bits STATUS_OUTBOUND_ENABLED et STATUS_OUTBOUND_ACTIVE distants. **FlushQueues** doit ensuite renvoyer S_OK. Lepooler MAPI lance ensuite les actions appropriées pour charger et télécharger des messages. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Un appel à l’objet d’état dupooler MAPI est une directive qui consiste à transférer tous les messages vers ou depuis le fournisseur de transport approprié. Lorsque vous appelez l’objet d’état d’un fournisseur de transport individuel, seuls les messages de ce fournisseur sont affectés.
  
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[Propriété canonique PidTagStatusCode](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

