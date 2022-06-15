---
title: Déterminer si un élément Outlook a été modifié mais pas enregistré (Outlook référence auxiliaire)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: Cette rubrique indique comment utiliser l'ID de dispatch dispidFDirty pour appeler la propriété correspondante sur un élément Outlook, si l'élément a été modifié et n'a pas été enregistré.
ms.openlocfilehash: ac6e4a38a68a52c83d957fab10aa46502ddd0dc5
ms.sourcegitcommit: a6d13fdae7eb2e503236c1b629a59b36a4fb76f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "66084052"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a>Déterminer si un élément Outlook a été modifié mais pas enregistré (Outlook référence auxiliaire)

Cette rubrique indique comment utiliser l'ID de dispatch **dispidFDirty** pour appeler la propriété correspondante sur un élément Outlook, si l'élément a été modifié et n'a pas été enregistré.
  
Étant donné un objet de l'élément, vous pouvez utiliser la méthode [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir un pointeur d'interface [IDispatch](/windows/win32/api/oaidl/nn-oaidl-idispatch) . La fonction de la rubrique `FIsItemDirty` accepte un pointeur **IDispatch** , _pdisp_, comme paramètre d’entrée. `FIsItemDirty` appelle la méthode [IDispatch::Invoke](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) , en spécifiant **dispidFDirty** comme argument pour le paramètre _dispIdMember_ et les indicateurs `DISPATCH_METHOD | DISPATCH_PROPERTYGET` pour _wFlags_, pour vérifier si l’élément a été modifié. `FIsItemDirty` retourne une valeur booléenne (**True** pour indiquer que l’élément a des modifications non enregistrées ; sinon, **False**).
  
```cpp
bool FIsItemDirty(IDispatch *pdisp)
{
    DISPPARAMS dispparams;
    UINT uArgErr;
    HRESULT hr = S_OK;
    CComVariant varDirty;
    dispparams.rgvarg = 0;
    dispparams.cArgs = 0;
    dispparams.cNamedArgs = 0;
    dispparams.rgdispidNamedArgs = NULL;
    hr = pdisp->Invoke(dispidFDirty,
        IID_NULL,
        LOCALE_SYSTEM_DEFAULT,
        DISPATCH_METHOD | DISPATCH_PROPERTYGET,
        &amp;dispparams,
        &amp;varDirty,
        NULL,
        &amp;uArgErr);
    return SUCCEEDED(hr) &amp;&amp; varDirty.bVal;
}

```

## <a name="see-also"></a>Voir aussi

- [Constantes (Outlook des API exportées)](constants-outlook-exported-apis.md)
