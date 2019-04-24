---
title: Déterminer si un élément Outlook a été modifié mais pas enregistré (référence auxiliaire d'Outlook)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: Cette rubrique indique comment utiliser l'ID de dispatch dispidFDirty pour appeler la propriété correspondante sur un élément Outlook, si l'élément a été modifié et n'a pas été enregistré.
ms.openlocfilehash: e66a23983a3cc19a7cb51d4b4c3b2c1cee58a793
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317639"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a>Déterminer si un élément Outlook a été modifié mais pas enregistré (référence auxiliaire d'Outlook)

Cette rubrique indique comment utiliser l'ID de dispatch **dispidFDirty** pour appeler la propriété correspondante sur un élément Outlook, si l'élément a été modifié et n'a pas été enregistré. 
  
Étant donné un objet de l'élément, vous pouvez utiliser la méthode [IUnknown::QueryInterface](https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)) pour obtenir un pointeur d'interface [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) . La fonction dans la rubrique `FIsItemDirty` accepte un pointeur **IDispatch** , _pDISP_, comme paramètre d'entrée.  `FIsItemDirty` appelle la méthode [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) , en spécifiant **dispidFDirty** comme argument pour le paramètre  _dispIdMember_ et les indicateurs  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` de  _wFlags_, pour vérifier si l'élément a été modifié.  `FIsItemDirty`Renvoie une valeur de type Boolean (**true** ) pour indiquer que l'élément a des modifications non enregistrées ****, false dans le cas contraire.
  
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

