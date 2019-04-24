---
title: Implémentation d’IUnknown dans C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68519f6c-fba8-47f5-9401-316e276f770e
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 08f3f3f937320d8a986b2002c761a37f0f749227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330176"
---
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="85a51-103">Implémentation d’IUnknown dans C++</span><span class="sxs-lookup"><span data-stu-id="85a51-103">Implementing IUnknown in C++</span></span>

<span data-ttu-id="85a51-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85a51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85a51-105">L'implémentation des méthodes [IUnknown](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx):: QueryInterface, [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)et [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) de l'interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) en C++ est assez simple.</span><span class="sxs-lookup"><span data-stu-id="85a51-105">Implementing the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface in C++ is fairly simple.</span></span> <span data-ttu-id="85a51-106">Après une validation standard des paramètres passés, une implémentation de **QueryInterface** vérifie l'identificateur de l'interface demandée par rapport à la liste des interfaces prises en charge.</span><span class="sxs-lookup"><span data-stu-id="85a51-106">After some standard validation of the parameters that are passed in, an implementation of **QueryInterface** checks the identifier of the requested interface against the list of supported interfaces.</span></span> <span data-ttu-id="85a51-107">Si l'identificateur demandé fait partie des personnes prises en charge, **AddRef** est appelé et le pointeur **This** est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="85a51-107">If the requested identifier is among those supported, **AddRef** is called and the **this** pointer is returned.</span></span> <span data-ttu-id="85a51-108">Si l'identificateur demandé ne figure pas dans la liste prise en charge, le pointeur de sortie a la valeur NULL et la valeur MAPI_E_INTERFACE_NOT_SUPPORTED est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="85a51-108">If the requested identifier is not on the supported list, the output pointer is set to NULL and the MAPI_E_INTERFACE_NOT_SUPPORTED value is returned.</span></span> 
  
<span data-ttu-id="85a51-109">L'exemple de code suivant montre comment vous pouvez implémenter **QueryInterface** en C++ pour un objet Status, un objet qui est une sous-classe de l'interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="85a51-109">The following code example shows how you can implement **QueryInterface** in C++ for a status object, an object that is a subclass of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="85a51-110">**IMAPIStatus** hérite de **IUnknown** via [IMAPIProp: IUnknown](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="85a51-110">**IMAPIStatus** inherits from **IUnknown** through [IMAPIProp : IUnknown](imapipropiunknown.md).</span></span> <span data-ttu-id="85a51-111">Par conséquent, si un appelant demande l'une de ces interfaces, le pointeur **This** peut être renvoyé car les interfaces sont liées par héritage.</span><span class="sxs-lookup"><span data-stu-id="85a51-111">Therefore, if a caller asks for any of these interfaces, the **this** pointer can be returned because the interfaces are related through inheritance.</span></span> 
  
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

<span data-ttu-id="85a51-112">L'exemple de code suivant montre comment implémenter les méthodes **AddRef** et **Release** pour `CMyMAPIObject` l'objet.</span><span class="sxs-lookup"><span data-stu-id="85a51-112">The following code example shows how to implement the **AddRef** and **Release** methods for the  `CMyMAPIObject` object.</span></span> <span data-ttu-id="85a51-113">Étant donné que l'implémentation de **AddRef** et de **Release** est simple, de nombreux fournisseurs de services choisissent de les implémenter en ligne.</span><span class="sxs-lookup"><span data-stu-id="85a51-113">Because implementing **AddRef** and **Release** is straightforward, many service providers choose to implement them inline.</span></span> <span data-ttu-id="85a51-114">Les appels aux fonctions Win32 **InterlockedIncrement** et **InterlockedDecrement** garantissent la sécurité des threads.</span><span class="sxs-lookup"><span data-stu-id="85a51-114">The calls to the Win32 functions **InterlockedIncrement** and **InterlockedDecrement** ensure thread safety.</span></span> <span data-ttu-id="85a51-115">La mémoire de l'objet est libérée par le destructeur, qui est appelée lorsque la méthode **Release** supprime l'objet.</span><span class="sxs-lookup"><span data-stu-id="85a51-115">The memory for the object is freed by the destructor, which is called when the **Release** method deletes the object.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="85a51-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85a51-116">See also</span></span>

- [<span data-ttu-id="85a51-117">Implémentation d'objets MAPI</span><span class="sxs-lookup"><span data-stu-id="85a51-117">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="85a51-118">Implémentation de l'interface IUnknown</span><span class="sxs-lookup"><span data-stu-id="85a51-118">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

