---
title: L’implémentation de IUnknown en langage C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68519f6c-fba8-47f5-9401-316e276f770e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: c899eb0afd123b26e12081f5157be3bae7917813
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784190"
---
# <a name="implementing-iunknown-in-c"></a>L’implémentation de IUnknown en langage C++

**S’applique à**: Outlook 
  
L’implémentation des méthodes de l’interface [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)and [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) en langage C++ est relativement simple. Après une validation standard des paramètres qui sont passés, une implémentation de **QueryInterface** vérifie l’identificateur de l’interface demandée par rapport à la liste des interfaces prises en charge. Si l’identificateur demandé est parmi ceux pris en charge, **AddRef** est appelé et le pointeur **this** est renvoyé. Si l’identificateur demandé n’est pas dans la liste pris en charge, le pointeur de la sortie est défini sur NULL et la valeur MAPI_E_INTERFACE_NOT_SUPPORTED est renvoyée. 
  
L’exemple de code suivant montre comment vous pouvez implémenter **QueryInterface** en langage C++ pour un objet d’état, un objet qui est une sous-classe de la [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface. **IMAPIStatus** hérite **IUnknown** via [IMAPIProp : IUnknown](imapipropiunknown.md). Par conséquent, si un appelant demande une de ces interfaces, le pointeur **this** peut être obtenue, car les interfaces liées par le biais de l’héritage des autorisations. 
  
```cpp
HRESULT CMyMAPIObject::QueryInterface (REFIID   riid,
                                       LPVOID * ppvObj)
{
    // Always set out parameter to NULL, validating it first.
    if (!ppvObj)
        return E_INVALIDARG;
    *ppvObj = NULL;
    if (riid == IID_IUnknown || riid == IID_IMAPIProp ||
        riid == IID_IMAPIStatus)
    {
        // Increment the reference count and return the pointer.
        *ppvObj = (LPVOID)this;
        AddRef();
        return NOERROR;
    }
    return E_NOINTERFACE;
}

```

L’exemple de code suivant montre comment implémenter les méthodes **AddRef** et **Release** pour le `CMyMAPIObject` objet. Étant donné que l’implémentation **AddRef** et **Release** est simple, nombreux fournisseurs de services choisissent les implémenter en ligne. Les appels aux fonctions Win32 **InterlockedIncrement** et **InterlockedDecrement** assurer la sécurité de thread. La mémoire pour l’objet est libérée par le destructeur, qui est appelé lorsque la méthode **Release** supprime l’objet. 
  
```cpp
ULONG CMyMAPIObject::AddRef()
{
    InterlockedIncrement(m_cRef);
    return m_cRef;
}
ULONG CMyMAPIObject::Release()
{
    // Decrement the object's internal counter.
    ULONG ulRefCount = InterlockedDecrement(m_cRef);
    if (0 == m_cRef)
    {
        delete this;
    }
    return ulRefCount;
}
 
```

## <a name="see-also"></a>Voir aussi

- [Implémentation d’objets MAPI](implementing-mapi-objects.md)
- [Implémentation de l’Interface IUnknown](implementing-the-iunknown-interface.md)

