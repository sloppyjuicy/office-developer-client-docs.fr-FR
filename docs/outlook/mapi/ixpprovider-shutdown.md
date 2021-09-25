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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 54e587ef23c9b121d4b9dc57bd68ebdad5ec38f3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584198"
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

Lepooler MAPI appelle la méthode **IXPProvider::Shutdown** juste avant de libérer un objet fournisseur de transport. Avant **d’appeler l’arrêt,** MAPI libère tous les objets d’accès pour un fournisseur.
  
## <a name="see-also"></a>Voir aussi



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

