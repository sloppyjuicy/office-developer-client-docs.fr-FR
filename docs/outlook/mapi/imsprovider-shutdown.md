---
title: IMSProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 77688f8a09c1d990201a247a3c4e3a11ba0963b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317261"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ferme un fournisseur de banque de messages de manière ordonnée.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> dans MSR doit être un pointeur vers zéro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

MAPI appelle la méthode **IMSProvider:: Shutdown** juste avant de libérer l'objet fournisseur de la Banque de messages. MAPI libère tous les objets d'ouverture de session pour un fournisseur avant d'appeler l' **arrêt** pour ce fournisseur. 
  
## <a name="see-also"></a>Voir aussi



[IMSProvider : IUnknown](imsprovideriunknown.md)

