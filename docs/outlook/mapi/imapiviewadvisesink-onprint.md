---
title: IMAPIViewAdviseSinkOnPrint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 202d461d4acefe18e69b47db9319cb328c61406e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592317"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Avertit l’utilisateur du formulaire de l’état d’impression d’un formulaire.
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a>Paramètres

 _dwPageNumber_
  
> [in] Numéro de la dernière page imprimée.
    
 _hrStatus_
  
> [in] Une valeur HRESULT indiquant l’état de l’impression. Les valeurs possibles sont les suivantes :
    
S_FALSE 
  
> Le travail d’impression est terminée et réussie.
    
S_OK 
  
> Le travail d’impression est en cours.
    
A ÉCHOUÉ 
  
> Le travail d’impression a été interrompu en raison d’une défaillance.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La notification a réussi.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton d’annulation dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Objets de formulaire appeler la méthode **IMAPIViewAdviseSink::OnPrint** lors de l’impression pour informer l’Afficheur de progression de l’impression. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Si le travail d’impression implique plusieurs pages, vous pouvez appeler **OnPrint** après que chaque page est imprimé. Valeur _dwPageNumber_ à la page en cours d’impression et _hrStatus_ S_OK. Lorsque le travail d’impression est terminé, appel **OnPrint** avec _dwPageNumber_ défini à la dernière page imprimée et _hrStatus_ valeur S_FALSE. 
  
Pour plus d’informations sur les notifications de formulaire, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

