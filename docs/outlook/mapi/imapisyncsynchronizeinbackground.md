---
title: IMAPISync SynchronizeInBackground
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
description: 'Dernière modification : 26 juin 2012'
ms.openlocfilehash: 579df1e0dd3b027e8bd4dea832154a4be46f7569
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575756"
---
# <a name="imapisync--synchronizeinbackground"></a>IMAPISync : SynchronizeInBackground

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Lance une synchronisation. Cette méthode est appelée par les Microsoft Outlook 2010 et Microsoft Outlook 2013 et implémentée par les fournisseurs de magasins de messages. 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a>Paramètres

 _psibpb_
  
> Informe le fournisseur de ce qui sera synchronisé et donne accès aux interfaces qui peuvent être utilisées pendant la synchronisation. Il s’agit [d’une structure MAPISIB.](mapisib.md) 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="see-also"></a>Voir aussi



[IMAPISync : IUnknown](imapisynciunknown.md)
  
[MAPISIB](mapisib.md)

