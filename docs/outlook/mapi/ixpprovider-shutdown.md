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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2d9a58ff05bb0da07762b9eafddef7303e8b9bc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592604"
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
  
> L’appel a réussi à l’arrêt du fournisseur de transport.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPProvider::Shutdown** juste avant la libération d’un objet de fournisseur de transport. Avant d’appeler **l’arrêt**, MAPI libère tous les objets d’ouverture de session pour un fournisseur.
  
## <a name="see-also"></a>Voir aussi



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

