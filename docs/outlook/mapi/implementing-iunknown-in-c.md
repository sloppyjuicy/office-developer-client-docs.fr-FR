---
title: Implémentation d’IUnknown dans C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 807b6dc4-cdb7-40a4-87d7-ebc1ad5fab76
ms.openlocfilehash: fa51bb189182df23738ca1916c16dc7168181f64
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378204"
---
# <a name="implementing-iunknown-in-c"></a>Implémentation d’IUnknown dans C

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les implémentations de [la méthode IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) en C sont très similaires aux implémentations C++. Il existe deux étapes de base pour l’implémentation : 
  
1. Validation des paramètres.
    
2. Vérification de l’identificateur de l’interface demandée par rapport à la liste des interfaces pris en charge par l’objet et renvoi de la valeur E_NO_INTERFACE ou d’un pointeur d’interface valide. Si un pointeur d’interface est renvoyé, l’implémentation doit également appeler la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour incrémenter le nombre de références. 
    
La principale différence entre une implémentation de **QueryInterface** en C et C++ est le premier paramètre supplémentaire dans la version C. Étant donné que le pointeur d’objet est ajouté à la liste des paramètres, une implémentation C de **QueryInterface** doit avoir plus de validation de paramètre qu’une implémentation C++. La logique permettant de vérifier l’identificateur d’interface, d’incrémenter le nombre de références et de renvoyer un pointeur d’objet doit être identique dans les deux langues. 
  
L’exemple de code suivant montre comment **implémenter QueryInterface** en C pour un objet d’état. 
  
```cpp
STDMETHODIMP STATUS_QueryInterface(LPMYSTATUSOBJ lpMyObj, REFIID riid,
                                   LPVOID FAR * lppvObj)
{
    HRESULT hr = hrSuccess;
    // Validate the object pointer.
    if (!lpMyObj || lpMyObj->lpVtbl != &vtblSTATUS )
    {
        hr = ResultFromScode(E_INVALIDARG);
        return hr;
    }
    // Validate other parameters.
    if (!lppvObj)
    {
        hr = ResultFromScode(E_INVALIDARG);
        return hr;
    }
    // Set the output pointer to NULL.
    *lppvObj = NULL;
    // Check the interface identifier.
    if (memcmp(riid, &IID_IUnknown, sizeof(IID)) &&
        memcmp(riid, &IID_IMAPIProp, sizeof(IID)) &&
        memcmp(riid, &IID_IMAPIStatus, sizeof(IID)))
    {
        hr = ResultFromScode(E_NOINTERFACE);
        return hr;
    }
    // The interface is supported. Increment the reference count and return.
    lpMyObj->lpVtbl->AddRef(lpMyObj);
    *lppvObj = lpMyObj;
    return hr;
}

```

Alors que l’implémentation de la méthode **AddRef** en C est similaire à une implémentation C++, une implémentation C de la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) peut être plus élaborée qu’une version C++. Cela est dû au fait que la plupart des fonctionnalités impliquées dans la libération d’un objet peuvent être incorporées dans le constructeur et le destructeur C++, et C n’a pas ce mécanisme. Toutes ces fonctionnalités doivent être incluses dans la **méthode Release** . En outre, en raison du paramètre supplémentaire et de sa vtable explicite, une validation supplémentaire est requise. 
  
L’appel **de méthode AddRef** suivant illustre une implémentation C classique pour un objet d’état. 
  
```cpp
STDMETHODIMP_(ULONG) STATUS_AddRef(LPMYSTATUSOBJ lpMyObj)
{
    LONG cRef;
    // Check to see whether it has a lpVtbl object member.
    if (!lpMyObj || lpMyObj->lpVtbl != &vtblSTATUS)
    {
        return 1;
    }
    // Check the method.
    if (STATUS_AddRef != lpMyObj->lpVtbl->AddRef)
    {
        return 1;
    }
    InterlockedIncrement(lpMyObj->cRef);
    cRef = ++lpMyObj->cRef;
    InterlockedDecrement (lpMyObj->cRef);
    return cRef;
}

```

L’exemple de code suivant illustre une implémentation classique de **Release** pour un objet d’état C. Si le nombre de références est 0 après sa décrémentation, une implémentation d’objet d’état C doit effectuer les tâches suivantes : 
  
- Relâchez tous les pointeurs mis en place vers des objets. 
    
- Définissez la table vtable sur NULL, facilitant le débogage dans le cas où l’utilisateur d’un objet appelé **Release** continuait à essayer d’utiliser l’objet. 
    
- Appelez **MAPIFreeBuffer** pour libérer l’objet. 
    
```cpp
STDMETHODIMP_(ULONG) STATUS_Release(LPMYSTATUSOBJ lpMyObj)
{
    LONG cRef;
    // Check the size of the vtable.
    if (!lpMyObj)
    {
        return 1;
    }
    // Check whether the vtable is correct.
    if (lpMyObj->lpVtbl != &vtblSTATUS)
    {
        return 1;
    }
    InterlockedIncrement(lpMyObj->cRef);
    cRef = --lpMyObj->cRef;
    InterlockedIncrement (lpMyObj->cRef);
    if (cRef == 0)
    {
        lpMyObj->lpVtbl->Release(lpMyObj);
        DeleteCriticalSection(&lpMyObj->cs);
        // Release the IMAPIProp pointer.
        lpMyObj->lpProp->Release(lpMyObj->lpProp);
        lpMyObj->lpVtbl = NULL;
        lpMyObj->lpFreeBuff(lpMyObj);
        return 0;
    }
    return cRef;
}

```

## <a name="see-also"></a>Voir aussi

- [Mise en œuvre des objets MAPI](implementing-mapi-objects.md)
- [Mise en œuvre de l’interface IUnknown](implementing-the-iunknown-interface.md)

