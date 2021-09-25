---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Obtient le compte suivant dans l’éumérateur.
ms.openlocfilehash: 7d49faa7bb6be4b0ee76eb36f47a6971dc5b1ad9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557140"
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
  
> [in] Pointeur vers une interface **IUnknown** que le client peut interroger pour obtenir une interface [IOlkAccount.](iolkaccount.md) 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L'appel a réussi.  <br/> |
|S_FALSE  <br/> |L’éumérateur a atteint la fin.  <br/> |
   
## <a name="remarks"></a>Remarques

L’interface spécifiée  *par ppunk*  hérite de **IUnknown**. Le client peut interroger cette interface (à l’aide de **IUnknown::QueryInterface**) pour obtenir un pointeur vers une interface **IOlkAccount** et obtenir ou définir des informations pour ce compte. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md) 
- [IOlkEnum::GetCount](iolkenum-getcount.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

