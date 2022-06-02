---
title: IMAPISync SynchronizeInBackground
description: IMAPISync SynchronizeInBackground lance une synchronisation. Il est appelé par Microsoft Outlook 2010 et 2013 et implémenté par les fournisseurs de magasins de messages.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISync.SynchronizeInBackground
api_type:
- COM
ms.assetid: c4aaca65-d553-476c-8c6d-5f880b6efdc1
ms.openlocfilehash: 5e27a4f02fe711dd8e479d58162e641bf856d201
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827869"
---
# <a name="imapisync--synchronizeinbackground"></a>IMAPISync : SynchronizeInBackground

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Lance une synchronisation. Cette méthode est appelée par Microsoft Outlook 2010 et Microsoft Outlook 2013 et implémentée par les fournisseurs de magasins de messages. 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a>Paramètres

 _psibpb_
  
> Informe le fournisseur de ce qui sera synchronisé et donne accès aux interfaces qui peuvent être utilisées pendant la synchronisation. Il s’agit d’une structure [MAPISIB](mapisib.md) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="see-also"></a>Voir aussi



[IMAPISync : IUnknown](imapisynciunknown.md)
  
[MAPISIB](mapisib.md)

