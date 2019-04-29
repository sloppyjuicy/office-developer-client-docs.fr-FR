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
ms.openlocfilehash: f6cdebf82d8b84ada3d029865867c5192af90b0d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409908"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Donne le contrôle de l'UC au spouleur MAPI afin qu'il puisse effectuer toutes les tâches qu'il juge nécessaires.
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> MSR doit être égal à zéro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le fournisseur de transport a libéré le processeur.
    
MAPI_W_CANCEL_MESSAGE 
  
> Indique au fournisseur de transport d'arrêter la remise du message à tous les destinataires qui ne l'ont pas encore reçu.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: SpoolerYield** est implémentée pour les objets de prise en charge du fournisseur de transport. Les fournisseurs de transport appellent **SpoolerYield** pour permettre au spouleur MAPI d'effectuer tout traitement nécessaire. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez **SpoolerYield** lorsque vous effectuez des opérations de longue durée qui peuvent être suspendues. Cela permet aux applications de premier plan de s'exécuter pendant une longue opération, telle que la remise à une grande liste de destinataires sur un réseau occupé. 
  
Si **SpoolerYield** est renvoyé avec MAPI_W_CANCEL_MESSAGE, le spouleur MAPI a déterminé que le message ne doit plus être envoyé. Retournez MAPI_E_USER_CANCEL à votre processus d'appel et quittez, si possible. 
  
Pour plus d'informations sur la génération du spouleur MAPI, consultez [la rubrique interaction avec le spouleUR MAPI](interacting-with-the-mapi-spooler.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

