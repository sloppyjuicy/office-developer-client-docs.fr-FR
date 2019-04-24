---
title: Implémentation d’IUnknown dans C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 807b6dc4-cdb7-40a4-87d7-ebc1ad5fab76
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3c634defcad76755fc6604a23d2091bb21e15111
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346773"
---
# <a name="implementing-iunknown-in-c"></a>Implémentation d’IUnknown dans C

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les implémentations de la méthode [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) dans C sont très similaires aux implémentations C++. L'implémentation comporte deux étapes de base: 
  
1. Validation des paramètres.
    
2. Vérification de l'identificateur de l'interface demandée par rapport à la liste des interfaces prises en charge par l'objet et renvoi de la valeur E_NO_INTERFACE ou d'un pointeur d'interface valide. Si un pointeur d'interface est renvoyé, l'implémentation doit également appeler la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour incrémenter le décompte de référence. 
    
La principale différence entre une implémentation de **QueryInterface** dans c et C++ est le premier paramètre supplémentaire dans la version c. Étant donné que le pointeur d'objet est ajouté à la liste de paramètres, une implémentation C de **QueryInterface** doit avoir davantage de validation de paramètres qu'une implémentation C++. La logique de vérification de l'identificateur d'interface, d'incrémentation du nombre de références et de renvoi d'un pointeur d'objet doit être identique dans les deux langages. 
  
L'exemple de code suivant montre comment implémenter **QueryInterface** dans C pour un objet d'État. 
  
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

Tandis que l'implémentation de la méthode **AddRef** dans C est identique à celle d'une implémentation c++, une implémentation C de la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) peut obtenir une plus grande élaborée qu'une version c++. En effet, une grande partie de la fonctionnalité de libération d'un objet peut être incorporée dans le destructeur et le constructeur C++, et C n'a pas de mécanisme de ce type. Toutes ces fonctionnalités doivent être incluses dans la méthode **Release** . En outre, en raison du paramètre supplémentaire et de sa vtable explicite, une validation supplémentaire est requise. 
  
L'appel de la méthode **AddRef** suivant illustre une implémentation C standard pour un objet Status. 
  
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

L'exemple de code suivant montre une implémentation classique de **Release** pour un objet d'État C. Si le nombre de références est 0 après sa décrémentation, l'implémentation d'un objet d'État C doit effectuer les tâches suivantes: 
  
- Libérez tous les pointeurs détenus vers des objets. 
    
- Définissez la valeur de vtable sur NULL, ce qui facilite le débogage dans le cas où l'utilisateur d'un objet appelé **Release** , mais qui a continué à essayer d'utiliser l'objet. 
    
- Appelez **MAPIFreeBuffer** pour libérer l'objet. 
    
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

- [Implémentation d'objets MAPI](implementing-mapi-objects.md)
- [Implémentation de l'interface IUnknown](implementing-the-iunknown-interface.md)

