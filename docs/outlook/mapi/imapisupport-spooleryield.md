---
title: IMAPISupportSpoolerYield
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerYield
api_type:
- COM
ms.assetid: f5c6ba8f-4ef5-4d60-b4e6-5b9160ec4e99
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d90f502e2cd7f97ac273ebecedbd0363097b1d60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584953"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Donne le contrôle de l’UC pour le spouleur MAPI afin qu’elle puisse exécuter toutes les tâches qu’elle estime nécessaires.
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> Réservé ; doit être égal à zéro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le fournisseur de transport a été libéré correctement l’UC.
    
MAPI_W_CANCEL_MESSAGE 
  
> Indique le fournisseur de transport pour arrêter la remise du message aux destinataires qui ne le n'avez pas encore reçu.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::SpoolerYield** est implémentée pour les objets de prise en charge de fournisseur de transport. Fournisseurs de transport appellent **SpoolerYield** pour autoriser le spouleur MAPI effectuer un traitement nécessaire. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Appelez **SpoolerYield** lorsque vous effectuez les opérations de longue durée peuvent être suspendues. Cela permet aux applications de premier plan à exécuter pendant une longue opération, par exemple remise à une liste de destinataires volumineuse sur un réseau occupé (e). 
  
Si **SpoolerYield** renvoie avec MAPI_W_CANCEL_MESSAGE, le spouleur MAPI a déterminé que le message ne doit être envoyé. Retourner MAPI_E_USER_CANCEL à vos processus appelant et de sortie, si possible. 
  
Pour plus d’informations sur les transmettre au spouleur MAPI, consultez [l’interaction avec le spouleur MAPI](interacting-with-the-mapi-spooler.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

