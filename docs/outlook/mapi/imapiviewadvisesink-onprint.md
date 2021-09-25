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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 69f560903ef0fa1430007818cc364752fd9eaeae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556481"
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

Si le travail d’impression implique plusieurs pages, vous pouvez appeler **OnPrint** après l’impression de chaque page. Définissez  _dwPageNumber_ sur la page en cours d’impression et  _hrStatus_ sur S_OK. Une fois la tâche d’impression terminée, appelez **OnPrint** avec  _dwPageNumber_ définie sur la dernière page imprimée et  _hrStatus_ sur S_FALSE. 
  
Pour plus d’informations sur les notifications de formulaire, voir [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

