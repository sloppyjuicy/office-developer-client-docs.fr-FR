---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 8b2190f77c7575d3d4f5e25fa0863bec844158bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348901"
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
  
> Dans MSR doit être un pointeur vers zéro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La connexion a été annulée.
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Dans votre implémentation de la méthode **Shutdown** , effectuez toutes les tâches que vous jugez nécessaires. MAPI appelle votre méthode d' **arrêt** uniquement une fois que vous avez publié tous vos objets d'ouverture de session. 
  
## <a name="see-also"></a>Voir aussi



[IABProvider : IUnknown](iabprovideriunknown.md)

