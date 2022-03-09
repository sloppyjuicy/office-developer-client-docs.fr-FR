---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Obtient le compte suivant dans l’éumérateur.
ms.openlocfilehash: 42d7949a4fbaa1aa2e24cb1f7ddc2f24662d4cd2
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370509"
---
# <a name="iolkenumgetnext"></a>IOlkEnum::GetNext

Obtient le compte suivant dans l’éumérateur.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a>Paramètres

_ppunk_
  
> [in] Pointeur vers une interface **IUnknown** que le client peut interroger pour obtenir une interface [IOlkAccount](iolkaccount.md) .

## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi. |
|S_FALSE  <br/> |L’éumérateur a atteint la fin. |

## <a name="remarks"></a>Remarques

L’interface spécifiée *par ppunk* hérite de **IUnknown**. Le client peut interroger cette interface (à l’aide de **IUnknown::QueryInterface**) pour obtenir un pointeur vers une interface **IOlkAccount** et obtenir ou définir des informations pour ce compte.
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)
- [IOlkEnum::GetCount](iolkenum-getcount.md)  
- [IOlkEnum::Reset](iolkenum-reset.md)
- [IOlkEnum::Skip](iolkenum-skip.md)