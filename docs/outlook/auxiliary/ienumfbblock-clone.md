---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Crée une copie de l’éumérateur, en utilisant la même restriction de temps, mais en fixant le curseur au début de l’éumérateur.
ms.openlocfilehash: 248b65ccc493f574c8485d228c3e8f853df2a1fa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567997"
---
# <a name="ienumfbblockclone"></a>IEnumFBBlock::Clone

Crée une copie de l’éumérateur, en utilisant la même restriction de temps, mais en fixant le curseur au début de l’éumérateur.
  
## <a name="quick-info"></a>Informations rapides

Voir [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a>Paramètres

_ccplone_
  
> [out] Pointeur vers le pointeur vers la copie de [l’interface IEnumFBBlock.](ienumfbblock.md) 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_OUTOFMEMORY  <br/> |Mémoire insuffisante pour effectuer la copie.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (API de libre/occupé)](constants-free-busy-api.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

