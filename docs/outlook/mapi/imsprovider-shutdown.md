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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 342b87a3a8f0349631e64600e294d4f19ab1099c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589090"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ferme un fournisseur de magasin de message de manière ordonnée.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [in] Réservé ; doit être un pointeur vers zéro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

MAPI appelle la méthode **IMSProvider::Shutdown** juste avant de libérer l’objet de fournisseur de magasin de message. MAPI libère tous les objets d’ouverture de session pour un fournisseur avant l’appel de **l’arrêt** de ce fournisseur. 
  
## <a name="see-also"></a>Voir aussi



[IMSProvider : IUnknown](imsprovideriunknown.md)

