---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Obtient le compte suivant dans l’énumérateur.
ms.openlocfilehash: 496a4d787916d051c051b3a19a7113d9d50c6fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782753"
---
# <a name="iolkenumgetnext"></a>IOlkEnum::GetNext

Obtient le compte suivant dans l’énumérateur.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a>Paramètres

_ppunk_
  
> [in] Pointeur vers une interface **IUnknown** que les clients peuvent interroger pour obtenir une interface [IOlkAccount](iolkaccount.md) . 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|S_FALSE  <br/> |L’énumérateur a atteint la fin.  <br/> |
   
## <a name="remarks"></a>Remarques

L’interface spécifiée par *ppunk* hérite de **IUnknown**. Le client peut interroger cette interface (à l’aide de **IUnknown::QueryInterface**) pour obtenir un pointeur vers une interface **IOlkAccount** et obtenir ou définir les informations de ce compte. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md) 
- [IOlkEnum::GetCount](iolkenum-getcount.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

