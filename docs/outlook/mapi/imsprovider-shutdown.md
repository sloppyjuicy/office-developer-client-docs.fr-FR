---
title: IMSProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
ms.openlocfilehash: 96298673772c49784b574704a31c7dc51f93cd2e
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374088"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ferme un fournisseur de magasins de messages de manière ordonnée.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [in] Réservé ; doit être un pointeur vers zéro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

MAPI appelle la **méthode IMSProvider::Shutdown** juste avant de libérer l’objet fournisseur de la boutique de messages. MAPI libère tous les objets d’accès pour un fournisseur avant d’appeler **l’arrêt** pour ce fournisseur. 
  
## <a name="see-also"></a>Voir aussi



[IMSProvider : IUnknown](imsprovideriunknown.md)

