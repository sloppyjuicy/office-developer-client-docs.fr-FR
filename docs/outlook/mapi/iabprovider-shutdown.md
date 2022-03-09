---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
ms.openlocfilehash: c986d31ae367c09eaf7623fedc24b7ea80300379
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374725"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule une connexion à une session active.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [In] Réservé ; doit être un pointeur vers zéro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La connexion a été correctement annulée.
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Dans votre implémentation de la méthode **Shutdown** , effectuez les tâches que vous jugez nécessaires. MAPI appelle votre **méthode d’arrêt** uniquement après avoir libéré tous vos objets d’logo. 
  
## <a name="see-also"></a>Voir aussi



[IABProvider : IUnknown](iabprovideriunknown.md)

