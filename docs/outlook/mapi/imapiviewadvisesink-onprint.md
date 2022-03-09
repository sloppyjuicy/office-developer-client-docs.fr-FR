---
title: IMAPIViewAdviseSinkOnPrint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
ms.openlocfilehash: b2b151011b65b7b1ca4bde41742284aa91d496c4
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374130"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avertit la visionneuse de formulaires de l’état d’impression d’un formulaire.
  
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
  
> [in] Valeur HRESULT indiquant l’état de la tâche d’impression. Les valeurs possibles sont les suivantes :
    
S_FALSE 
  
> Le travail d’impression s’est terminé correctement.
    
S_OK 
  
> Le travail d’impression est en cours.
    
FAILED 
  
> Le travail d’impression a été interrompu en raison d’un échec.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton Annuler dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Les objets de formulaire appellent la méthode **IMAPIViewAdviseSink::OnPrint** lors de l’impression pour informer la visionneuse de la progression de l’impression. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si le travail d’impression implique plusieurs pages, vous pouvez appeler **OnPrint** après l’impression de chaque page. _Définissez dwPageNumber_ sur la page en cours d’impression et _hrStatus_ sur S_OK. Lorsque le travail d’impression est terminé, appelez **OnPrint** avec  _dwPageNumber_ définie sur la dernière page imprimée et  _hrStatus_ sur S_FALSE. 
  
Pour plus d’informations sur les notifications de formulaire, voir [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

