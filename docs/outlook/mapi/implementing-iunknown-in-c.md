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
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="8ca7b-103">Implémentation d’IUnknown dans C</span><span class="sxs-lookup"><span data-stu-id="8ca7b-103">Implementing IUnknown in C</span></span>

<span data-ttu-id="8ca7b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ca7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ca7b-105">Les implémentations de la méthode [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) dans C sont très similaires aux implémentations C++.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-105">Implementations of the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method in C are very similar to C++ implementations.</span></span> <span data-ttu-id="8ca7b-106">L'implémentation comporte deux étapes de base:</span><span class="sxs-lookup"><span data-stu-id="8ca7b-106">There are two basic steps to the implementation:</span></span> 
  
1. <span data-ttu-id="8ca7b-107">Validation des paramètres.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-107">Validating parameters.</span></span>
    
2. <span data-ttu-id="8ca7b-108">Vérification de l'identificateur de l'interface demandée par rapport à la liste des interfaces prises en charge par l'objet et renvoi de la valeur E_NO_INTERFACE ou d'un pointeur d'interface valide.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-108">Checking the identifier of the requested interface against the list of interfaces supported by the object and returning either the E_NO_INTERFACE value or a valid interface pointer.</span></span> <span data-ttu-id="8ca7b-109">Si un pointeur d'interface est renvoyé, l'implémentation doit également appeler la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour incrémenter le décompte de référence.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-109">If an interface pointer is returned, the implementation should also call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment the reference count.</span></span> 
    
<span data-ttu-id="8ca7b-110">La principale différence entre une implémentation de **QueryInterface** dans c et C++ est le premier paramètre supplémentaire dans la version c.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-110">The main difference between an implementation of **QueryInterface** in C and C++ is the additional first parameter in the C version.</span></span> <span data-ttu-id="8ca7b-111">Étant donné que le pointeur d'objet est ajouté à la liste de paramètres, une implémentation C de **QueryInterface** doit avoir davantage de validation de paramètres qu'une implémentation C++.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-111">Because the object pointer is added to the parameter list, a C implementation of **QueryInterface** must have more parameter validation than a C++ implementation.</span></span> <span data-ttu-id="8ca7b-112">La logique de vérification de l'identificateur d'interface, d'incrémentation du nombre de références et de renvoi d'un pointeur d'objet doit être identique dans les deux langages.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-112">The logic for checking the interface identifier, incrementing the reference count, and returning an object pointer should be identical in both languages.</span></span> 
  
<span data-ttu-id="8ca7b-113">L'exemple de code suivant montre comment implémenter **QueryInterface** dans C pour un objet d'État.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-113">The following code example shows how to implement **QueryInterface** in C for a status object.</span></span> 
  
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

<span data-ttu-id="8ca7b-114">Tandis que l'implémentation de la méthode **AddRef** dans C est identique à celle d'une implémentation c++, une implémentation C de la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) peut obtenir une plus grande élaborée qu'une version c++.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-114">Whereas the implementation of the **AddRef** method in C is similar to a C++ implementation, a C implementation of the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method can get more elaborate than a C++ version.</span></span> <span data-ttu-id="8ca7b-115">En effet, une grande partie de la fonctionnalité de libération d'un objet peut être incorporée dans le destructeur et le constructeur C++, et C n'a pas de mécanisme de ce type.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-115">This is because much of the functionality involved with freeing an object can be incorporated into the C++ constructor and destructor, and C has no such mechanism.</span></span> <span data-ttu-id="8ca7b-116">Toutes ces fonctionnalités doivent être incluses dans la méthode **Release** .</span><span class="sxs-lookup"><span data-stu-id="8ca7b-116">All of this functionality must be included in the **Release** method.</span></span> <span data-ttu-id="8ca7b-117">En outre, en raison du paramètre supplémentaire et de sa vtable explicite, une validation supplémentaire est requise.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-117">Also, because of the additional parameter and its explicit vtable, more validation is required.</span></span> 
  
<span data-ttu-id="8ca7b-118">L'appel de la méthode **AddRef** suivant illustre une implémentation C standard pour un objet Status.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-118">The following **AddRef** method call illustrates a typical C implementation for a status object.</span></span> 
  
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

<span data-ttu-id="8ca7b-119">L'exemple de code suivant montre une implémentation classique de **Release** pour un objet d'État C.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-119">The following code example shows a typical implementation of **Release** for a C status object.</span></span> <span data-ttu-id="8ca7b-120">Si le nombre de références est 0 après sa décrémentation, l'implémentation d'un objet d'État C doit effectuer les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="8ca7b-120">If the reference count is 0 after it is decremented, a C status object implementation should perform the following tasks:</span></span> 
  
- <span data-ttu-id="8ca7b-121">Libérez tous les pointeurs détenus vers des objets.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-121">Release any held pointers to objects.</span></span> 
    
- <span data-ttu-id="8ca7b-122">Définissez la valeur de vtable sur NULL, ce qui facilite le débogage dans le cas où l'utilisateur d'un objet appelé **Release** , mais qui a continué à essayer d'utiliser l'objet.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-122">Set the vtable to NULL, facilitating debugging in the case where an object's user called **Release** yet continued to try to use the object.</span></span> 
    
- <span data-ttu-id="8ca7b-123">Appelez **MAPIFreeBuffer** pour libérer l'objet.</span><span class="sxs-lookup"><span data-stu-id="8ca7b-123">Call **MAPIFreeBuffer** to free the object.</span></span> 
    
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

## <a name="see-also"></a><span data-ttu-id="8ca7b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ca7b-124">See also</span></span>

- [<span data-ttu-id="8ca7b-125">Implémentation d'objets MAPI</span><span class="sxs-lookup"><span data-stu-id="8ca7b-125">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="8ca7b-126">Implémentation de l'interface IUnknown</span><span class="sxs-lookup"><span data-stu-id="8ca7b-126">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

