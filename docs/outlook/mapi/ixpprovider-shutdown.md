---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
ms.openlocfilehash: 1e5305e1ca0247440de9eaf65940c0addf2353df
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374683"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ferme un fournisseur de transport de manière ordonnée.
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi à arrêter le fournisseur de transport.
    
## <a name="remarks"></a>Remarques

Lepooler MAPI appelle la méthode **IXPProvider::Shutdown** juste avant de libérer un objet fournisseur de transport. Avant d’appeler **l’arrêt**, MAPI libère tous les objets d’accès pour un fournisseur.
  
## <a name="see-also"></a>Voir aussi



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

