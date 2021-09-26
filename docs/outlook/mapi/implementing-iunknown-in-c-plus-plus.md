---
title: Implémentation d’IUnknown dans C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 68519f6c-fba8-47f5-9401-316e276f770e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c64f29c91341209988f7980957468cd96ff70779
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630550"
---
# <a name="implementing-iunknown-in-c"></a>Implémentation d’IUnknown dans C++

**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’implémentation des méthodes [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)et [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) de l’interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) en C++ est assez simple. Après une validation standard des paramètres transmis, une implémentation de **QueryInterface** vérifie l’identificateur de l’interface demandée par rapport à la liste des interfaces pris en charge. Si l’identificateur demandé fait partie des éléments pris en charge, **AddRef** est appelé et **le** pointeur est renvoyé. Si l’identificateur demandé ne figure pas dans la liste prise en charge, le pointeur de sortie est définie sur NULL et la valeur MAPI_E_INTERFACE_NOT_SUPPORTED est renvoyée. 
  
L’exemple de code suivant montre comment implémenter **QueryInterface** en C++ pour un objet status, un objet qui est une sous-classe de l’interface [IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) **IMAPIStatus** hérite de **IUnknown** via [IMAPIProp : IUnknown](imapipropiunknown.md). Par conséquent, si un appelant demande l’une de ces interfaces, ce **pointeur** peut être renvoyé car les interfaces sont liées par héritage. 
  
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

L’exemple de code suivant montre comment implémenter les méthodes **AddRef** et **Release** pour  `CMyMAPIObject` l’objet. Étant donné que **l’implémentation d’AddRef** et **release** est simple, de nombreux fournisseurs de services choisissent de les implémenter en ligne. Les appels aux fonctions Win32 **InterlockedIncrement** et **InterlockedDecrement** garantissent la sécurité des threads. La mémoire de l’objet est libérée par le destructeur, qui est appelé lorsque la méthode **Release** supprime l’objet. 
  
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

- [Mise en œuvre des objets MAPI](implementing-mapi-objects.md)
- [Mise en œuvre de l’interface IUnknown](implementing-the-iunknown-interface.md)

