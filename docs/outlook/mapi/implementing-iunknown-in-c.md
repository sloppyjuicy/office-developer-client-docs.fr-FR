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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346773"
---
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="5dfd9-103">Implémentation d’IUnknown dans C</span><span class="sxs-lookup"><span data-stu-id="5dfd9-103">Implementing IUnknown in C</span></span>

<span data-ttu-id="5dfd9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5dfd9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5dfd9-105">Les implémentations de [la méthode IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) en C sont très similaires aux implémentations C++.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-105">Implementations of the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method in C are very similar to C++ implementations.</span></span> <span data-ttu-id="5dfd9-106">Il existe deux étapes de base pour l’implémentation :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-106">There are two basic steps to the implementation:</span></span> 
  
1. <span data-ttu-id="5dfd9-107">Validation des paramètres.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-107">Validating parameters.</span></span>
    
2. <span data-ttu-id="5dfd9-108">Vérification de l’identificateur de l’interface demandée par rapport à la liste des interfaces pris en charge par l’objet et renvoi de la valeur E_NO_INTERFACE ou d’un pointeur d’interface valide.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-108">Checking the identifier of the requested interface against the list of interfaces supported by the object and returning either the E_NO_INTERFACE value or a valid interface pointer.</span></span> <span data-ttu-id="5dfd9-109">Si un pointeur d’interface est renvoyé, l’implémentation doit également appeler la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour incrémenter le nombre de références.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-109">If an interface pointer is returned, the implementation should also call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment the reference count.</span></span> 
    
<span data-ttu-id="5dfd9-110">La principale différence entre une implémentation de **QueryInterface** en C et C++ est le premier paramètre supplémentaire dans la version C.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-110">The main difference between an implementation of **QueryInterface** in C and C++ is the additional first parameter in the C version.</span></span> <span data-ttu-id="5dfd9-111">Étant donné que le pointeur d’objet est ajouté à la liste des paramètres, une implémentation C de **QueryInterface** doit avoir plus de validation de paramètre qu’une implémentation C++.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-111">Because the object pointer is added to the parameter list, a C implementation of **QueryInterface** must have more parameter validation than a C++ implementation.</span></span> <span data-ttu-id="5dfd9-112">La logique permettant de vérifier l’identificateur d’interface, d’incrémenter le nombre de références et de renvoyer un pointeur d’objet doit être identique dans les deux langues.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-112">The logic for checking the interface identifier, incrementing the reference count, and returning an object pointer should be identical in both languages.</span></span> 
  
<span data-ttu-id="5dfd9-113">L’exemple de code suivant montre comment implémenter **QueryInterface** en C pour un objet d’état.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-113">The following code example shows how to implement **QueryInterface** in C for a status object.</span></span> 
  
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

<span data-ttu-id="5dfd9-114">Alors que l’implémentation de la méthode **AddRef** en C est similaire à une implémentation C++, une implémentation C de la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) peut être plus élaborée qu’une version C++.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-114">Whereas the implementation of the **AddRef** method in C is similar to a C++ implementation, a C implementation of the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method can get more elaborate than a C++ version.</span></span> <span data-ttu-id="5dfd9-115">Cela est dû au fait que la plupart des fonctionnalités impliquées dans la libération d’un objet peuvent être incorporées dans le constructeur et le destructeur C++, et C n’a pas ce mécanisme.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-115">This is because much of the functionality involved with freeing an object can be incorporated into the C++ constructor and destructor, and C has no such mechanism.</span></span> <span data-ttu-id="5dfd9-116">Toutes ces fonctionnalités doivent être incluses dans la **méthode Release.**</span><span class="sxs-lookup"><span data-stu-id="5dfd9-116">All of this functionality must be included in the **Release** method.</span></span> <span data-ttu-id="5dfd9-117">En outre, en raison du paramètre supplémentaire et de son vtable explicite, une validation supplémentaire est requise.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-117">Also, because of the additional parameter and its explicit vtable, more validation is required.</span></span> 
  
<span data-ttu-id="5dfd9-118">L’appel **de méthode AddRef** suivant illustre une implémentation C classique pour un objet d’état.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-118">The following **AddRef** method call illustrates a typical C implementation for a status object.</span></span> 
  
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

<span data-ttu-id="5dfd9-119">L’exemple de code suivant illustre une implémentation classique de **Release** pour un objet d’état C.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-119">The following code example shows a typical implementation of **Release** for a C status object.</span></span> <span data-ttu-id="5dfd9-120">Si le nombre de références est 0 après sa décrémentation, une implémentation d’objet d’état C doit effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="5dfd9-120">If the reference count is 0 after it is decremented, a C status object implementation should perform the following tasks:</span></span> 
  
- <span data-ttu-id="5dfd9-121">Relâchez tous les pointeurs mis en place vers des objets.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-121">Release any held pointers to objects.</span></span> 
    
- <span data-ttu-id="5dfd9-122">Définissez la table vtable sur NULL, facilitant le débogage dans le cas où l’utilisateur d’un objet appelé **Release** continuait à essayer d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-122">Set the vtable to NULL, facilitating debugging in the case where an object's user called **Release** yet continued to try to use the object.</span></span> 
    
- <span data-ttu-id="5dfd9-123">Appelez **MAPIFreeBuffer** pour libérer l’objet.</span><span class="sxs-lookup"><span data-stu-id="5dfd9-123">Call **MAPIFreeBuffer** to free the object.</span></span> 
    
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

## <a name="see-also"></a><span data-ttu-id="5dfd9-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dfd9-124">See also</span></span>

- [<span data-ttu-id="5dfd9-125">Mise en œuvre des objets MAPI</span><span class="sxs-lookup"><span data-stu-id="5dfd9-125">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="5dfd9-126">Mise en œuvre de l’interface IUnknown</span><span class="sxs-lookup"><span data-stu-id="5dfd9-126">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

