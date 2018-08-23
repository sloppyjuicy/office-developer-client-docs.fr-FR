---
title: Déterminer si un élément Outlook a été modifié mais ne pas enregistré (autre référence Outlook)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: Cette rubrique indique comment utiliser l'ID de dispatch dispidFDirty pour appeler la propriété correspondante sur un élément Outlook, si l'élément a été modifié et n'a pas été enregistré.
ms.openlocfilehash: adaa0f72d427a5cfc98b93e8aa4403d5a76ecd9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588096"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a><span data-ttu-id="c4360-103">Déterminer si un élément Outlook a été modifié mais ne pas enregistré (autre référence Outlook)</span><span class="sxs-lookup"><span data-stu-id="c4360-103">Determine if an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>

<span data-ttu-id="c4360-104">Cette rubrique indique comment utiliser l'ID de dispatch **dispidFDirty** pour appeler la propriété correspondante sur un élément Outlook, si l'élément a été modifié et n'a pas été enregistré.</span><span class="sxs-lookup"><span data-stu-id="c4360-104">This topic shows how to use the **dispidFDirty** dispatch ID to invoke the corresponding property on an Outlook item, to see whether the item has been modified and has not been saved.</span></span> 
  
<span data-ttu-id="c4360-105">Étant donné un objet de l'élément, vous pouvez utiliser la méthode [IUnknown::QueryInterface](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)) pour obtenir un pointeur d'interface [IDispatch](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="c4360-105">Given an item object, you can use the [IUnknown::QueryInterface](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)) method to obtain an [IDispatch](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) interface pointer.</span></span> <span data-ttu-id="c4360-106">La fonction dans la rubrique `FIsItemDirty` accepte un pointeur **IDispatch** , _argument pdisp_, comme paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="c4360-106">The function in the topic `FIsItemDirty` accepts an **IDispatch** pointer,  _pdisp_, as an input parameter.</span></span>  <span data-ttu-id="c4360-107">`FIsItemDirty` appelle la méthode [IDispatch::Invoke](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) , en spécifiant **dispidFDirty** comme argument pour le paramètre  _dispIdMember_ et les indicateurs  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` de  _wFlags_, pour vérifier si l'élément a été modifié.</span><span class="sxs-lookup"><span data-stu-id="c4360-107">`FIsItemDirty` calls the [IDispatch::Invoke](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) method, specifying **dispidFDirty** as the argument for the  _dispIdMember_ parameter, and the flags  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` for  _wFlags_, to verify whether the item has been modified.</span></span>  <span data-ttu-id="c4360-108">`FIsItemDirty`Renvoie une valeur booléenne (**True** pour indiquer que l’élément a des modifications non enregistrées ; sinon, **False**).</span><span class="sxs-lookup"><span data-stu-id="c4360-108">`FIsItemDirty` returns a Boolean value (**True** to indicate that the item has unsaved changes; otherwise, **False**).</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="c4360-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4360-109">See also</span></span>

- [<span data-ttu-id="c4360-110">Constantes (Outlook des API exportées)</span><span class="sxs-lookup"><span data-stu-id="c4360-110">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)

