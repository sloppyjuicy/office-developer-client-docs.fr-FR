---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: a57a72b413ba412154a27a08244e86b117cbea7d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357196"
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
  
> L'appel a réussi à arrêter le fournisseur de transport.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPProvider:: Shutdown** juste avant de publier un objet de fournisseur de transport. Avant d'appeler **Shutdown**, MAPI libère tous les objets d'ouverture de session pour un fournisseur.
  
## <a name="see-also"></a>Voir aussi



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

