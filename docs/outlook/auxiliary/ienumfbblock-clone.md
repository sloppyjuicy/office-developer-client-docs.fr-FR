---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Crée une copie de l’énumérateur, à l’aide de la même restriction mais définissant le curseur au début de l’énumérateur.
ms.openlocfilehash: 51503be2091fa01da6f636bf6944274068617f05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782574"
---
# <a name="ienumfbblockclone"></a>IEnumFBBlock::Clone

Crée une copie de l’énumérateur, à l’aide de la même restriction mais définissant le curseur au début de l’énumérateur.
  
## <a name="quick-info"></a>Informations rapides

Voir [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a>Paramètres

_ppclone_
  
> [out] Un pointeur vers un pointeur vers la copie de l’interface [IEnumFBBlock](ienumfbblock.md) . 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|E_OUTOFMEMORY  <br/> |La mémoire est insuffisante pour la copie.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (disponibilité API)](constants-free-busy-api.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

