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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 334ec8dd0c683cf9b765f387281c624b20520098
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784298"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**S’applique à**: Outlook 
  
Ferme un fournisseur de magasin de message de manière ordonnée.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> [in] Réservé ; doit être un pointeur vers zéro.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

MAPI appelle la méthode **IMSProvider::Shutdown** juste avant de libérer l’objet de fournisseur de magasin de message. MAPI libère tous les objets d’ouverture de session pour un fournisseur avant l’appel de **l’arrêt** de ce fournisseur. 
  
## <a name="see-also"></a>Voir aussi



[IMSProvider : IUnknown](imsprovideriunknown.md)

