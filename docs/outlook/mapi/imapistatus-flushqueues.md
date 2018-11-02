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
ms.openlocfilehash: 30aaaaa250155215149a941da7f7e528d65b8dc3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592198"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Force tous les messages en attente d’être envoyés ou reçus pour être immédiatement téléchargé ou téléchargé. Les objets de statut qui implémentent des fournisseurs de transport et de l’objet état spouleur MAPI prennent en charge cette méthode.
  
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
  
> [in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows qui affiche cette méthode.
    
 _cbTargetTransport_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpTargetTransport_ . Le paramètre _cbTargetTransport_ est défini uniquement sur les appels à l’objet d’état du spouleur MAPI. Pour les appels à un fournisseur de transport, le paramètre _cbTargetTransport_ est défini sur 0. 
    
 _lpTargetTransport_
  
> [in] Pointeur vers l’identificateur d’entrée du fournisseur de transport consiste à vider les files d’attente. Le paramètre _lpTargetTransport_ est défini uniquement sur les appels à l’objet d’état du spouleur MAPI. Pour les appels à un fournisseur de transport, le paramètre _lpTargetTransport_ est défini sur NULL. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’opération de vidage. Les indicateurs suivants peuvent être définis :
    
FLUSH_ASYNC_OK 
  
> L’opération de vidage peut se produire de manière asynchrone. Cet indicateur s’applique uniquement à l’objet d’état du spouleur MAPI. 
    
FLUSH_DOWNLOAD 
  
> Les files d’attente de messages entrants doivent être vidés.
    
FLUSH_FORCE 
  
> L’opération de vidage doit se produire malgré tout, malgré le risque d’une baisse des performances. Cet indicateur doit être défini lors de la cible d’un fournisseur de transport asynchrone.
    
FLUSH_NO_UI 
  
> L’objet de l’état ne doit pas afficher un indicateur de progression.
    
FLUSH_UPLOAD 
  
> Les files d’attente de messages sortants doivent être vidés.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de vidage a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours ; Il doit être autorisé pour effectuer, ou il doit être arrêté, avant cette opération peut être lancée.
    
MAPI_E_NO_SUPPORT 
  
> L’objet état ne gère pas cette opération, comme indiqué par l’absence de l’indicateur STATUS_FLUSH_QUEUES dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) de l’objet d’état.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIStatus::FlushQueues** demande le spouleur MAPI ou un fournisseur de transport immédiatement envoyer tous les messages dans la file d’attente sortante ou reçoivent tous les messages à partir de la file d’attente entrant. **FlushQueues** est implémentée uniquement par l’objet d’état spouleur MAPI et par les objets d’état qui offre des fournisseurs de transport. 
  
MAPI_E_BUSY doit être retournée pour les demandes asynchrones afin que les clients peuvent continuer de travail. 
  
Par défaut, **FlushQueues** est une opération synchrone ; contrôle ne retourne pas à l’appelant jusqu'à ce que le vidage est terminée. Uniquement l’opération de vidage effectuée par le spouleur MAPI peut être asynchrone ; les clients demandent ce comportement en définissant l’indicateur FLUSH_ASYNC_OK. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Implémentation d’un fournisseur de transport à distance de **FlushQueues** définit des bits dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) dans la ligne d’état de l’objet d’ouverture de session pour contrôler la façon dont les files d’attente sont vidés. Si l’indicateur FLUSH_UPLOAD passe une visionneuse à distance, la méthode **FlushQueues** doit définir les bits STATUS_INBOUND_ENABLED et STATUS_INBOUND_ACTIVE. Si l’indicateur FLUSH_DOWNLOAD passe une visionneuse à distance, la méthode **FlushQueues** doit définir les bits STATUS_OUTBOUND_ENABLED et STATUS_OUTBOUND_ACTIVE. **FlushQueues** doit renvoyer puis S_OK. Le spouleur MAPI lance les actions appropriées pour charger et télécharger des messages. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Un appel à l’objet de l’état du spouleur MAPI est une directive pour transférer tous les messages vers ou à partir du fournisseur de transport approprié. Lorsque vous appelez objet d’état d’un fournisseur de transport individuels, seuls les messages de ce fournisseur sont affectés.
  
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[Propriété canonique PidTagStatusCode](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

