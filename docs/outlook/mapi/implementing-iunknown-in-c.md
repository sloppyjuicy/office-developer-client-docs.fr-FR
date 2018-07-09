---
title: L’implémentation de IUnknown dans C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 807b6dc4-cdb7-40a4-87d7-ebc1ad5fab76
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d12201d8476d15021e896a44797ae5fc21178802
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784192"
---
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="56341-103">L’implémentation de IUnknown dans C</span><span class="sxs-lookup"><span data-stu-id="56341-103">Implementing IUnknown in C</span></span>

<span data-ttu-id="56341-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56341-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56341-105">Implémentations de la méthode [IUnknown::QueryInterface](http://msdn.microsoft.com/fr-fr/library/ms682521%28v=VS.85%29.aspx) dans C sont très similaires aux implémentations C++.</span><span class="sxs-lookup"><span data-stu-id="56341-105">Implementations of the [IUnknown::QueryInterface](http://msdn.microsoft.com/fr-fr/library/ms682521%28v=VS.85%29.aspx) method in C are very similar to C++ implementations.</span></span> <span data-ttu-id="56341-106">Il existe deux étapes de base pour l’implémentation :</span><span class="sxs-lookup"><span data-stu-id="56341-106">There are two basic steps to the implementation:</span></span> 
  
1. <span data-ttu-id="56341-107">Validation des paramètres.</span><span class="sxs-lookup"><span data-stu-id="56341-107">Validating parameters.</span></span>
    
2. <span data-ttu-id="56341-108">Vérification de l’identificateur de l’interface demandée par rapport à la liste des interfaces prises en charge par l’objet et renvoie la valeur E_NO_INTERFACE ou un pointeur d’interface valide.</span><span class="sxs-lookup"><span data-stu-id="56341-108">Checking the identifier of the requested interface against the list of interfaces supported by the object and returning either the E_NO_INTERFACE value or a valid interface pointer.</span></span> <span data-ttu-id="56341-109">Si un pointeur d’interface est renvoyé, l’implémentation doit également appeler la méthode [IUnknown::AddRef](http://msdn.microsoft.com/fr-fr/library/ms691379%28v=VS.85%29.aspx) pour incrémenter le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="56341-109">If an interface pointer is returned, the implementation should also call the [IUnknown::AddRef](http://msdn.microsoft.com/fr-fr/library/ms691379%28v=VS.85%29.aspx) method to increment the reference count.</span></span> 
    
<span data-ttu-id="56341-110">La principale différence entre une implémentation de **QueryInterface** dans C et C++ est le premier paramètre supplémentaire dans la version C.</span><span class="sxs-lookup"><span data-stu-id="56341-110">The main difference between an implementation of **QueryInterface** in C and C++ is the additional first parameter in the C version.</span></span> <span data-ttu-id="56341-111">Étant donné que le pointeur de l’objet est ajouté à la liste des paramètres, une implémentation C de **QueryInterface** doit avoir plus de validation de paramètre qu’une implémentation C++.</span><span class="sxs-lookup"><span data-stu-id="56341-111">Because the object pointer is added to the parameter list, a C implementation of **QueryInterface** must have more parameter validation than a C++ implementation.</span></span> <span data-ttu-id="56341-112">La logique pour la vérification de l’identificateur d’interface, s’incrémentant le décompte de références et le renvoi d’un pointeur d’objet doit être identique dans les deux langues.</span><span class="sxs-lookup"><span data-stu-id="56341-112">The logic for checking the interface identifier, incrementing the reference count, and returning an object pointer should be identical in both languages.</span></span> 
  
<span data-ttu-id="56341-113">L’exemple de code suivant montre comment implémenter **QueryInterface** dans C pour un objet d’état.</span><span class="sxs-lookup"><span data-stu-id="56341-113">The following code example shows how to implement **QueryInterface** in C for a status object.</span></span> 
  
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

<span data-ttu-id="56341-114">Tandis que l’implémentation de la méthode **AddRef** dans C est similaire à une implémentation C++, une implémentation C de la méthode [IUnknown::Release](http://msdn.microsoft.com/fr-fr/library/ms682317%28v=VS.85%29.aspx) peut obtenir plus complexe qu’une version C++.</span><span class="sxs-lookup"><span data-stu-id="56341-114">Whereas the implementation of the **AddRef** method in C is similar to a C++ implementation, a C implementation of the [IUnknown::Release](http://msdn.microsoft.com/fr-fr/library/ms682317%28v=VS.85%29.aspx) method can get more elaborate than a C++ version.</span></span> <span data-ttu-id="56341-115">Il s’agit, car la plupart des fonctionnalités concernées par la libération d’un objet peut être incorporée dans le constructeur C++ et le destructeur et C ne possède pas de mécanisme.</span><span class="sxs-lookup"><span data-stu-id="56341-115">This is because much of the functionality involved with freeing an object can be incorporated into the C++ constructor and destructor, and C has no such mechanism.</span></span> <span data-ttu-id="56341-116">Toutes ces fonctionnalités doivent être inclus dans la méthode de **publication** .</span><span class="sxs-lookup"><span data-stu-id="56341-116">All of this functionality must be included in the **Release** method.</span></span> <span data-ttu-id="56341-117">En outre, en raison du paramètre supplémentaire et ses vtable explicite, plus la validation est requise.</span><span class="sxs-lookup"><span data-stu-id="56341-117">Also, because of the additional parameter and its explicit vtable, more validation is required.</span></span> 
  
<span data-ttu-id="56341-118">L’appel de méthode **AddRef** suivant illustre une implémentation C typique pour un objet d’état.</span><span class="sxs-lookup"><span data-stu-id="56341-118">The following **AddRef** method call illustrates a typical C implementation for a status object.</span></span> 
  
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

<span data-ttu-id="56341-119">L’exemple de code suivant illustre une implémentation standard de **version** pour un objet d’état C.</span><span class="sxs-lookup"><span data-stu-id="56341-119">The following code example shows a typical implementation of **Release** for a C status object.</span></span> <span data-ttu-id="56341-120">Si le décompte de références est 0 après diminue, une implémentation d’objet état C doit effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="56341-120">If the reference count is 0 after it is decremented, a C status object implementation should perform the following tasks:</span></span> 
  
- <span data-ttu-id="56341-121">Version des pointeurs vers des objets en attente.</span><span class="sxs-lookup"><span data-stu-id="56341-121">Release any held pointers to objects.</span></span> 
    
- <span data-ttu-id="56341-122">Vtable la valeur NULL, faciliter le débogage dans le cas où les utilisateurs d’un objet appelé **version** suite encore pour essayer d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="56341-122">Set the vtable to NULL, facilitating debugging in the case where an object's user called **Release** yet continued to try to use the object.</span></span> 
    
- <span data-ttu-id="56341-123">Appelez **MAPIFreeBuffer** pour libérer de l’objet.</span><span class="sxs-lookup"><span data-stu-id="56341-123">Call **MAPIFreeBuffer** to free the object.</span></span> 
    
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

## <a name="see-also"></a><span data-ttu-id="56341-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56341-124">See also</span></span>

- [<span data-ttu-id="56341-125">Implémentation d’objets MAPI</span><span class="sxs-lookup"><span data-stu-id="56341-125">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="56341-126">Implémentation de l’Interface IUnknown</span><span class="sxs-lookup"><span data-stu-id="56341-126">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

