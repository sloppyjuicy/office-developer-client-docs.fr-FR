---
title: IMAPISupportSpoolerYield
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.SpoolerYield
api_type:
- COM
ms.assetid: f5c6ba8f-4ef5-4d60-b4e6-5b9160ec4e99
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6cc11912b721a624b065c6d21169056843ceac0e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575728"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Donne le contrôle de l’UC aupooler MAPI afin qu’il puisse effectuer les tâches qu’il considère nécessaires.
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> Réservé ; doit être zéro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le fournisseur de transport a réussi à libérer l’UC.
    
MAPI_W_CANCEL_MESSAGE 
  
> Demande au fournisseur de transport d’arrêter la remise du message à tous les destinataires qui ne l’ont pas encore reçu.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::SpoolerYield** est implémentée pour les objets de prise en charge du fournisseur de transport. Les fournisseurs de transport **appellent SpoolerYield** pour permettre aupooler MAPI d’effectuer tout traitement nécessaire. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez **SpoolerYield** lorsque vous effectuez des opérations longues qui peuvent être suspendues. Cela permet aux applications au premier plan de s’exécuter pendant une longue opération, telle que la remise à une liste de destinataires importante sur un réseau occupé. 
  
Si **SpoolerYield** est renvoyé avec MAPI_W_CANCEL_MESSAGE, lepooler MAPI a déterminé que le message ne doit plus être envoyé. Renvoyez MAPI_E_USER_CANCEL processus d’appel et quittez, si possible. 
  
Pour plus d’informations sur le rendement aupooler MAPI, voir Interaction avec le [spooler MAPI](interacting-with-the-mapi-spooler.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

