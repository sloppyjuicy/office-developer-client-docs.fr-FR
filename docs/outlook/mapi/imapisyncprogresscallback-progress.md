---
title: IMAPISyncProgressCallbackProgress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISyncProgressCallback.Progress
api_type:
- COM
ms.assetid: 6797cd1c-8a0b-4f42-ba56-6162d8e7b058
ms.openlocfilehash: 733301a2c63d2809c8260d8db56adb73fe11eb54
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372625"
---
# <a name="imapisyncprogresscallbackprogress"></a>IMAPISyncProgressCallback::Progress

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Met à jour l’état dans la boîte de dialogue d’envoi/réception. Le fournisseur de magasin appelle périodiquement cette fonction.
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a>Paramètres

 **pwczsProgress**
  
> Pointeur vers une chaîne qui affiche l’étape de progression actuelle. Il peut être NULL pour mettre à jour la progression.
    
 **ulIndex**
  
> Position actuelle en cours.
    
 **ulIndexMax**
  
> Index indiquant la progression complète.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="see-also"></a>Voir aussi



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

