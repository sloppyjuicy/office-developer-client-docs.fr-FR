---
title: IMAPISupportIStorageFromStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.IStorageFromStream
api_type:
- COM
ms.assetid: da9e8fdc-dfc5-4ecc-9f9b-b76921b92d7c
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a73c87f172b4c97379bb9cd117679d3947c188af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783999"
---
# <a name="imapisupportistoragefromstream"></a><span data-ttu-id="e5350-103">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="e5350-103">IMAPISupport::IStorageFromStream</span></span>

  
  
<span data-ttu-id="e5350-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e5350-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e5350-105">Implémente un objet de stockage pour accéder à un objet stream.</span><span class="sxs-lookup"><span data-stu-id="e5350-105">Implements a storage object to access a stream.</span></span>
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="e5350-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5350-106">Parameters</span></span>

 <span data-ttu-id="e5350-107">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="e5350-107">_lpUnkIn_</span></span>
  
> <span data-ttu-id="e5350-108">[in] Pointeur vers un objet stream.</span><span class="sxs-lookup"><span data-stu-id="e5350-108">[in] A pointer to a stream object.</span></span>
    
 <span data-ttu-id="e5350-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="e5350-109">_lpInterface_</span></span>
  
> <span data-ttu-id="e5350-110">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au flux désigné par _lpUnkIn_.</span><span class="sxs-lookup"><span data-stu-id="e5350-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the stream pointed to by  _lpUnkIn_.</span></span> <span data-ttu-id="e5350-111">Une des valeurs suivantes sont valide : IID_IStream, IID_ILockBytes, ou **valeur null**, ce qui indique que l’interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) doit être utilisé pour accéder au flux.</span><span class="sxs-lookup"><span data-stu-id="e5350-111">Any of the following values are valid: IID_IStream, IID_ILockBytes, or **null**, which indicates that the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface should be used to access the stream.</span></span> 
    
 <span data-ttu-id="e5350-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e5350-112">_ulFlags_</span></span>
  
> <span data-ttu-id="e5350-113">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet de stockage doit être créé par rapport à l’objet stream.</span><span class="sxs-lookup"><span data-stu-id="e5350-113">[in] A bitmask of flags that controls how the storage object is to be created relative to the stream object.</span></span> <span data-ttu-id="e5350-114">Par défaut, le stockage est créé avec un accès en lecture seule et le flux démarre à la position zéro dans le stockage.</span><span class="sxs-lookup"><span data-stu-id="e5350-114">By default, the storage is created with read-only access and the stream starts at position zero in the storage.</span></span> <span data-ttu-id="e5350-115">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="e5350-115">The following flags can be set:</span></span>
    
<span data-ttu-id="e5350-116">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="e5350-116">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="e5350-117">Un nouvel objet de stockage doit être créé pour l’objet stream.</span><span class="sxs-lookup"><span data-stu-id="e5350-117">A new storage object should be created for the stream object.</span></span>
    
<span data-ttu-id="e5350-118">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="e5350-118">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="e5350-119">L’objet de stockage doit commencer à la position actuelle du flux.</span><span class="sxs-lookup"><span data-stu-id="e5350-119">The storage object should start at the current position of the stream.</span></span>
    
<span data-ttu-id="e5350-120">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="e5350-120">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="e5350-121">L’appelant doit avoir l’autorisation de lecture/écriture à l’objet de stockage renvoyé.</span><span class="sxs-lookup"><span data-stu-id="e5350-121">The caller should have read/write permission to the returned storage object.</span></span>
    
<span data-ttu-id="e5350-122">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="e5350-122">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="e5350-123">L’objet de stockage doit commencer à la position zéro.</span><span class="sxs-lookup"><span data-stu-id="e5350-123">The storage object should start at position zero.</span></span>
    
 <span data-ttu-id="e5350-124">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="e5350-124">_lppStorageOut_</span></span>
  
> <span data-ttu-id="e5350-125">[out] Pointeur vers un pointeur vers l’objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="e5350-125">[out] A pointer to a pointer to the storage object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e5350-126">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e5350-126">Return value</span></span>

<span data-ttu-id="e5350-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5350-127">S_OK</span></span> 
  
> <span data-ttu-id="e5350-128">L’objet de stockage a été créé avec succès.</span><span class="sxs-lookup"><span data-stu-id="e5350-128">The storage object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e5350-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="e5350-129">Remarks</span></span>

<span data-ttu-id="e5350-130">La méthode **IMAPISupport::IStorageFromStream** est implémentée pour tous les objets de prise en charge de fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="e5350-130">The **IMAPISupport::IStorageFromStream** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="e5350-131">Fournisseurs de services d’appel **IStorageFromStream** pour créer un objet de stockage à utiliser pour ouvrir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="e5350-131">Service providers call **IStorageFromStream** to create a storage object to use for opening particular properties.</span></span> <span data-ttu-id="e5350-132">Fournisseurs de services qui ont leur propre implémentation de l’interface [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) est inutile d’appeler **IStorageFromStream**.</span><span class="sxs-lookup"><span data-stu-id="e5350-132">Service providers that have their own implementation of the [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) interface do not need to call **IStorageFromStream**.</span></span> 
  
<span data-ttu-id="e5350-133">L’objet de stockage créé par **IStorageFromStream** appelle la méthode du flux [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) pour incrémenter son décompte de références, puis le décrémente le décompte lorsque l’utilisateur relâche le stockage.</span><span class="sxs-lookup"><span data-stu-id="e5350-133">The storage object created by **IStorageFromStream** calls the stream's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) method to increment its reference count and then decrements the count when the storage is released.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e5350-134">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="e5350-134">Notes to callers</span></span>

<span data-ttu-id="e5350-135">Lorsque la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de l’un de vos objets est appelée à le pour ouverture d’une propriété avec l’interface **IStorage** , effectuez les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="e5350-135">When the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method of one of your objects is called to open a property with the **IStorage** interface, perform the following tasks:</span></span> 
  
1. <span data-ttu-id="e5350-136">Ouvrir un objet stream avec l’autorisation de lecture/écriture de la propriété.</span><span class="sxs-lookup"><span data-stu-id="e5350-136">Open a stream object with read/write permission for the property.</span></span>
    
2. <span data-ttu-id="e5350-137">En interne, sélectionnez le flux de propriétés en tant qu’un objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="e5350-137">Internally mark the property stream as a storage object.</span></span>
    
3. <span data-ttu-id="e5350-138">Appelez **IStorageFromStream** pour générer un objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="e5350-138">Call **IStorageFromStream** to generate a storage object.</span></span> 
    
4. <span data-ttu-id="e5350-139">Retourne un pointeur vers cet objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="e5350-139">Return a pointer to this storage object.</span></span>
    
<span data-ttu-id="e5350-140">Si vous implémentez des interfaces supplémentaires qui utilisent l’objet de stockage, créez un objet qui encapsule l’objet de stockage et implémenter un méthode [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="e5350-140">If you implement additional interfaces that use the storage object, create an object that wraps the storage object and implement a higher level [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) method.</span></span> 
  
<span data-ttu-id="e5350-141">Ne pas autoriser une propriété à ouvrir avec l’interface **IStream** si elle a été créée avec **IStorage**.</span><span class="sxs-lookup"><span data-stu-id="e5350-141">Do not allow a property to be opened with the **IStream** interface if it was created with **IStorage**.</span></span> <span data-ttu-id="e5350-142">Inversement, ne pas autoriser une propriété à ouvrir avec l’interface **IStorage** si elle a été créée avec **IStream**.</span><span class="sxs-lookup"><span data-stu-id="e5350-142">Conversely, do not allow a property to be opened with the **IStorage** interface if it was created with **IStream**.</span></span> 
  
<span data-ttu-id="e5350-143">Avec une exception, il est possible d’utiliser l’interface **IStreamDocfile** pour l’acheminement d’un objet de stockage d’un conteneur à un autre, mais l’identificateur d’interface IID_IStreamDocfile doit être transmis dans _de la méthode **OpenProperty** lpInterface _paramètre.</span><span class="sxs-lookup"><span data-stu-id="e5350-143">With one exception, it is acceptable to use the **IStreamDocfile** interface to stream a storage object from one container to another, but the IID_IStreamDocfile interface identifier must be passed in the **OpenProperty** method's  _lpInterface_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e5350-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5350-144">See also</span></span>



[<span data-ttu-id="e5350-145">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="e5350-145">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="e5350-146">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5350-146">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

