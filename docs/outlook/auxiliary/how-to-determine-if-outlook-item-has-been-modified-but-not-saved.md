---
title: Déterminer si un Outlook a été modifié mais pas enregistré (Outlook référence auxiliaire)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: Cette rubrique indique comment utiliser l'ID de dispatch dispidFDirty pour appeler la propriété correspondante sur un élément Outlook, si l'élément a été modifié et n'a pas été enregistré.
ms.openlocfilehash: 7ea75ee2a8b0fad63e31357718c936f4e7bbc1b6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592794"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a>Déterminer si un Outlook a été modifié mais pas enregistré (Outlook référence auxiliaire)

Cette rubrique indique comment utiliser l'ID de dispatch **dispidFDirty** pour appeler la propriété correspondante sur un élément Outlook, si l'élément a été modifié et n'a pas été enregistré. 
  
Étant donné un objet de l'élément, vous pouvez utiliser la méthode [IUnknown::QueryInterface](https://docs.microsoft.com/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir un pointeur d'interface [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) . La fonction dans la rubrique `FIsItemDirty` accepte un **pointeur IDispatch,**  _pdisp_, comme paramètre d’entrée.  `FIsItemDirty` appelle la méthode [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) , en spécifiant **dispidFDirty** comme argument pour le paramètre  _dispIdMember_ et les indicateurs  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` de  _wFlags_, pour vérifier si l'élément a été modifié.  `FIsItemDirty` renvoie une valeur boolé européenne (**True** pour indiquer que l’élément a des modifications non apportées ; sinon, **False**).
  
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

