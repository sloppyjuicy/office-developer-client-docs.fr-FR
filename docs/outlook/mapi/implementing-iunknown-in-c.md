---
title: Implémentation d’IUnknown dans C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 807b6dc4-cdb7-40a4-87d7-ebc1ad5fab76
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3c634defcad76755fc6604a23d2091bb21e15111
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391443"
---
# <a name="implementing-iunknown-in-c"></a>Implémentation d’IUnknown dans C

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Implémentations de la méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) dans C sont très similaires aux implémentations C++. Il existe deux étapes de base pour l’implémentation : 
  
1. Validation des paramètres.
    
2. Vérification de l’identificateur de l’interface demandée par rapport à la liste des interfaces prises en charge par l’objet et renvoie la valeur E_NO_INTERFACE ou un pointeur d’interface valide. Si un pointeur d’interface est renvoyé, l’implémentation doit également appeler la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour incrémenter le décompte de références. 
    
La principale différence entre une implémentation de **QueryInterface** dans C et C++ est le premier paramètre supplémentaire dans la version C. Étant donné que le pointeur de l’objet est ajouté à la liste des paramètres, une implémentation C de **QueryInterface** doit avoir plus de validation de paramètre qu’une implémentation C++. La logique pour la vérification de l’identificateur d’interface, s’incrémentant le décompte de références et le renvoi d’un pointeur d’objet doit être identique dans les deux langues. 
  
L’exemple de code suivant montre comment implémenter **QueryInterface** dans C pour un objet d’état. 
  
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

Tandis que l’implémentation de la méthode **AddRef** dans C est similaire à une implémentation C++, une implémentation C de la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) peut obtenir plus complexe qu’une version C++. Il s’agit, car la plupart des fonctionnalités concernées par la libération d’un objet peut être incorporée dans le constructeur C++ et le destructeur et C ne possède pas de mécanisme. Toutes ces fonctionnalités doivent être inclus dans la méthode de **publication** . En outre, en raison du paramètre supplémentaire et ses vtable explicite, plus la validation est requise. 
  
L’appel de méthode **AddRef** suivant illustre une implémentation C typique pour un objet d’état. 
  
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

L’exemple de code suivant illustre une implémentation standard de **version** pour un objet d’état C. Si le décompte de références est 0 après diminue, une implémentation d’objet état C doit effectuer les tâches suivantes : 
  
- Version des pointeurs vers des objets en attente. 
    
- Vtable la valeur NULL, faciliter le débogage dans le cas où les utilisateurs d’un objet appelé **version** suite encore pour essayer d’utiliser l’objet. 
    
- Appelez **MAPIFreeBuffer** pour libérer de l’objet. 
    
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

- [Implémentation d’objets MAPI](implementing-mapi-objects.md)
- [Implémentation de l’interface IUnknown](implementing-the-iunknown-interface.md)

