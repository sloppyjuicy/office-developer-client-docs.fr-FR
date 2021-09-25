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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0f01f495372122c2c2f8b2e5d1242d7a1898f62f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592339"
---
# <a name="imapisyncprogresscallbackprogress"></a>IMAPISyncProgressCallback::Progress

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Met à jour l’état dans la boîte de dialogue d’envoi/réception. Le fournisseur de magasins appelle régulièrement cette fonction.
  
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

