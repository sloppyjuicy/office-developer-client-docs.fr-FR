---
title: Déterminer si un élément Outlook a été modifié mais ne pas enregistré (autre référence Outlook)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: Cette rubrique indique comment utiliser l'ID de dispatch dispidFDirty pour appeler la propriété correspondante sur un élément Outlook, si l'élément a été modifié et n'a pas été enregistré.
ms.openlocfilehash: ece6ede368cf2ffb3b18575161fef4b3f132fdf0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782561"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a><span data-ttu-id="3e369-103">Déterminer si un élément Outlook a été modifié mais ne pas enregistré (autre référence Outlook)</span><span class="sxs-lookup"><span data-stu-id="3e369-103">Determine if an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>

<span data-ttu-id="3e369-104">Cette rubrique indique comment utiliser l'ID de dispatch **dispidFDirty** pour appeler la propriété correspondante sur un élément Outlook, si l'élément a été modifié et n'a pas été enregistré.</span><span class="sxs-lookup"><span data-stu-id="3e369-104">This topic shows how to use the **dispidFDirty** dispatch ID to invoke the corresponding property on an Outlook item, to see whether the item has been modified and has not been saved.</span></span> 
  
<span data-ttu-id="3e369-105">Étant donné un objet de l'élément, vous pouvez utiliser la méthode [IUnknown::QueryInterface](http://msdn.microsoft.com/library/com.iunknown_queryinterface.aspx) pour obtenir un pointeur d'interface [IDispatch](http://msdn.microsoft.com/library/ebbff4bc-36b2-4861-9efa-ffa45e013eb5%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3e369-105">Given an item object, you can use the [IUnknown::QueryInterface](http://msdn.microsoft.com/library/com.iunknown_queryinterface.aspx) method to obtain an [IDispatch](http://msdn.microsoft.com/library/ebbff4bc-36b2-4861-9efa-ffa45e013eb5%28Office.15%29.aspx) interface pointer.</span></span> <span data-ttu-id="3e369-106">La fonction dans la rubrique `FIsItemDirty` accepte un pointeur **IDispatch** , _argument pdisp_, comme paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3e369-106">The function in the topic `FIsItemDirty` accepts an **IDispatch** pointer,  _pdisp_, as an input parameter.</span></span>  <span data-ttu-id="3e369-107">`FIsItemDirty` appelle la méthode [IDispatch::Invoke](http://msdn.microsoft.com/library/964ade8e-9d8a-4d32-bd47-aa678912a54d%28Office.15%29.aspx) , en spécifiant **dispidFDirty** comme argument pour le paramètre  _dispIdMember_ et les indicateurs  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` de  _wFlags_, pour vérifier si l'élément a été modifié.</span><span class="sxs-lookup"><span data-stu-id="3e369-107">`FIsItemDirty` calls the [IDispatch::Invoke](http://msdn.microsoft.com/library/964ade8e-9d8a-4d32-bd47-aa678912a54d%28Office.15%29.aspx) method, specifying **dispidFDirty** as the argument for the  _dispIdMember_ parameter, and the flags  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` for  _wFlags_, to verify whether the item has been modified.</span></span>  <span data-ttu-id="3e369-108">`FIsItemDirty`Renvoie une valeur booléenne (**True** pour indiquer que l’élément a des modifications non enregistrées ; sinon, **False**).</span><span class="sxs-lookup"><span data-stu-id="3e369-108">`FIsItemDirty` returns a Boolean value (**True** to indicate that the item has unsaved changes; otherwise, **False**).</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="3e369-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e369-109">See also</span></span>

- [<span data-ttu-id="3e369-110">Constantes (Outlook des API exportées)</span><span class="sxs-lookup"><span data-stu-id="3e369-110">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)

