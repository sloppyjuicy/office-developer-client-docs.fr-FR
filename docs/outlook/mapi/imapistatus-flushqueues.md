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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 5f8396ca84192e485d33fb5a96f641361b717584
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328193"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Force tous les messages en attente d'être envoyés ou reçus pour être immédiatement téléchargés ou téléchargés. L'objet d'État du spouleur MAPI et les objets d'État que les fournisseurs de transport implémentent prennent en charge cette méthode.
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> dans Handle de la fenêtre parente des boîtes de dialogue ou des fenêtres que cette méthode affiche.
    
 _cbTargetTransport_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpTargetTransport_ . Le paramètre _cbTargetTransport_ est défini uniquement sur les appels vers l'objet d'État du spouleur MAPI. Pour les appels à un fournisseur de transport, le paramètre _cbTargetTransport_ est défini sur 0. 
    
 _lpTargetTransport_
  
> dans Pointeur vers l'identificateur d'entrée du fournisseur de transport qui doit vider ses files d'attente de messages. Le paramètre _lpTargetTransport_ est défini uniquement sur les appels vers l'objet d'État du spouleur MAPI. Pour les appels à un fournisseur de transport, le paramètre _lpTargetTransport_ est défini sur null. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle l'opération de vidage. Les indicateurs suivants peuvent être définis:
    
FLUSH_ASYNC_OK 
  
> L'opération de vidage peut être effectuée de manière asynchrone. Cet indicateur s'applique uniquement à l'objet d'État du spouleur MAPI. 
    
FLUSH_DOWNLOAD 
  
> Les files d'attente de messages entrants doivent être vidées.
    
FLUSH_FORCE 
  
> L'opération de vidage doit avoir lieu indépendamment du risque de diminution des performances. Cet indicateur doit être défini lorsqu'un fournisseur de transport asynchrone est ciblé.
    
FLUSH_NO_UI 
  
> L'objet Status ne doit pas afficher d'indicateur de progression.
    
FLUSH_UPLOAD 
  
> Les files d'attente de messages sortants doivent être vidées.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'opération de vidage a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours; il doit être autorisé à se terminer ou doit être arrêté, avant que cette opération puisse être lancée.
    
MAPI_E_NO_SUPPORT 
  
> L'objet Status ne prend pas en charge cette opération, comme indiqué par l'absence de l'indicateur STATUS_FLUSH_QUEUES dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) de l'objet Status.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIStatus:: FlushQueues** demande que le spouleur MAPI ou un fournisseur de transport envoie immédiatement tous les messages dans la file d'attente sortante ou reçoit tous les messages de la file d'attente entrante. **FlushQueues** est implémenté uniquement par l'objet d'État du spouleur MAPI et par les objets d'état fournis par les fournisseurs de transport. 
  
MAPI_E_BUSY doit être renvoyé pour les demandes asynchrones afin que les clients puissent continuer à travailler. 
  
Par défaut, **FlushQueues** est une opération synchrone; le contrôle ne retourne pas à l'appelant tant que le vidage n'est pas terminé. Seule l'opération de vidage effectuée par le spouleur MAPI peut être asynchrone; les clients demandent ce comportement en définissant l'indicateur FLUSH_ASYNC_OK. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

L'implémentation d'un fournisseur de transport distant **FlushQueues** définit les bits dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la ligne d'état de l'objet Logon pour contrôler la façon dont les files d'attente sont vidées. Si une visionneuse distante réussit l'indicateur FLUSH_UPLOAD, la méthode **FlushQueues** doit définir les bits STATUS_INBOUND_ENABLED et STATUS_INBOUND_ACTIVE. Si une visionneuse distante réussit l'indicateur FLUSH_DOWNLOAD, la méthode **FlushQueues** doit définir les bits STATUS_OUTBOUND_ENABLED et STATUS_OUTBOUND_ACTIVE. **FlushQueues** doit ensuite renvoyer S_OK. Le spouleur MAPI lance ensuite les actions appropriées pour le chargement et le téléchargement des messages. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Un appel à l'objet d'État du spouleur MAPI est une directive permettant de transférer tous les messages vers ou à partir du fournisseur de transport approprié. Lorsque vous appelez l'objet d'état d'un fournisseur de transport individuel, seuls les messages de ce fournisseur sont affectés.
  
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[Propriété canonique PidTagStatusCode](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

