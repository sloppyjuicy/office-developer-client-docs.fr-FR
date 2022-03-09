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
ms.openlocfilehash: e752e3a9bf2804db81cc2e7b1c02cbf4364a7bd9
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373934"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Donne le contrôle de l’UC aupooler MAPI afin qu’il puisse effectuer toutes les tâches qu’il considère nécessaires.
  
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

**Appelez SpoolerYield** lorsque vous effectuez des opérations longues qui peuvent être suspendues. Cela permet aux applications au premier plan de s’exécuter pendant une longue opération, telles que la remise à une liste de destinataires importante sur un réseau occupé. 
  
Si **SpoolerYield** est renvoyé avec MAPI_W_CANCEL_MESSAGE, lepooler MAPI a déterminé que le message ne doit plus être envoyé. Renvoyez MAPI_E_USER_CANCEL processus d’appel et quittez, si possible. 
  
Pour plus d’informations sur le rendement aupooler MAPI, voir [Interaction avec le spooler MAPI](interacting-with-the-mapi-spooler.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

