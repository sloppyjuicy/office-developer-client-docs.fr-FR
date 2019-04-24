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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: e66315042f8b5cd5aff0e4aa076588c9f312376a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328783"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avertit la visionneuse de formulaires de l'état d'impression d'un formulaire.
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a>Paramètres

 _dwPageNumber_
  
> dans Numéro de la dernière page imprimée.
    
 _hrStatus_
  
> dans Valeur HRESULT indiquant l'état du travail d'impression. Les valeurs possibles sont les suivantes :
    
S_FALSE 
  
> La tâche d'impression s'est terminée correctement.
    
S_OK 
  
> La tâche d'impression est en cours d'exécution.
    
Echec 
  
> Le travail d'impression a été terminé en raison d'un échec.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi.
    
MAPI_E_USER_CANCEL 
  
> L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton Annuler d'une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Les objets de formulaire appellent la méthode **IMAPIViewAdviseSink:: OnPrint** lors de l'impression pour informer la visionneuse de la progression de l'impression. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si la tâche d'impression implique plusieurs pages, vous pouvez appeler **OnPrint** une fois que chaque page est imprimée. Définissez _dwPageNumber_ sur la page actuellement imprimée et _hrStatus_ à S_OK. Une fois le travail d'impression terminé, appelez **OnPrint** avec _dwPageNumber_ défini sur la dernière page imprimée et _hrStatus_ définie sur S_FALSE. 
  
Pour plus d'informations sur les notifications de formulaire, consultez la rubrique [envoi et réception de notifications de formulaire](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

