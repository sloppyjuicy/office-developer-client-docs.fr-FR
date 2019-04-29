---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Crée une copie de l'énumérateur à l'aide de la même restriction temporelle, mais en définissant le curseur au début de l'énumérateur.
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413401"
---
# <a name="ienumfbblockclone"></a>IEnumFBBlock::Clone

Crée une copie de l'énumérateur à l'aide de la même restriction temporelle, mais en définissant le curseur au début de l'énumérateur.
  
## <a name="quick-info"></a>Informations rapides

Voir [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a>Paramètres

_ppClone_
  
> remarquer Pointeur vers un pointeur vers la copie de l'interface [IEnumFBBlock](ienumfbblock.md) . 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|STANDARD  <br/> |Mémoire insuffisante pour la copie.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (API de disponibilité)](constants-free-busy-api.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

