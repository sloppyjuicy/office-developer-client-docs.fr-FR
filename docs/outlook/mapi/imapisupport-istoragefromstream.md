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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7200e7d226eb148fef094ab8540990644d2d4c99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316586"
---
# <a name="imapisupportistoragefromstream"></a><span data-ttu-id="8eb87-103">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="8eb87-103">IMAPISupport::IStorageFromStream</span></span>

  
  
<span data-ttu-id="8eb87-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8eb87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8eb87-105">Implémente un objet de stockage pour accéder à un flux.</span><span class="sxs-lookup"><span data-stu-id="8eb87-105">Implements a storage object to access a stream.</span></span>
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="8eb87-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8eb87-106">Parameters</span></span>

 <span data-ttu-id="8eb87-107">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="8eb87-107">_lpUnkIn_</span></span>
  
> <span data-ttu-id="8eb87-108">[in] Pointeur vers un objet stream.</span><span class="sxs-lookup"><span data-stu-id="8eb87-108">[in] A pointer to a stream object.</span></span>
    
 <span data-ttu-id="8eb87-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8eb87-109">_lpInterface_</span></span>
  
> <span data-ttu-id="8eb87-110">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au flux pointé par  _lpUnkIn_.</span><span class="sxs-lookup"><span data-stu-id="8eb87-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the stream pointed to by  _lpUnkIn_.</span></span> <span data-ttu-id="8eb87-111">L’une des valeurs suivantes est valide : IID_IStream, IID_ILockBytes ou **null,** ce qui indique que l’interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) doit être utilisée pour accéder au flux.</span><span class="sxs-lookup"><span data-stu-id="8eb87-111">Any of the following values are valid: IID_IStream, IID_ILockBytes, or **null**, which indicates that the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface should be used to access the stream.</span></span> 
    
 <span data-ttu-id="8eb87-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8eb87-112">_ulFlags_</span></span>
  
> <span data-ttu-id="8eb87-113">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet de stockage doit être créé par rapport à l’objet de flux.</span><span class="sxs-lookup"><span data-stu-id="8eb87-113">[in] A bitmask of flags that controls how the storage object is to be created relative to the stream object.</span></span> <span data-ttu-id="8eb87-114">Par défaut, le stockage est créé avec un accès en lecture seule et le flux démarre à la position zéro dans le stockage.</span><span class="sxs-lookup"><span data-stu-id="8eb87-114">By default, the storage is created with read-only access and the stream starts at position zero in the storage.</span></span> <span data-ttu-id="8eb87-115">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="8eb87-115">The following flags can be set:</span></span>
    
<span data-ttu-id="8eb87-116">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="8eb87-116">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="8eb87-117">Un nouvel objet de stockage doit être créé pour l’objet de flux.</span><span class="sxs-lookup"><span data-stu-id="8eb87-117">A new storage object should be created for the stream object.</span></span>
    
<span data-ttu-id="8eb87-118">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="8eb87-118">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="8eb87-119">L’objet de stockage doit commencer à la position actuelle du flux.</span><span class="sxs-lookup"><span data-stu-id="8eb87-119">The storage object should start at the current position of the stream.</span></span>
    
<span data-ttu-id="8eb87-120">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="8eb87-120">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="8eb87-121">L’appelant doit avoir une autorisation de lecture/écriture sur l’objet de stockage renvoyé.</span><span class="sxs-lookup"><span data-stu-id="8eb87-121">The caller should have read/write permission to the returned storage object.</span></span>
    
<span data-ttu-id="8eb87-122">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="8eb87-122">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="8eb87-123">L’objet de stockage doit commencer à la position zéro.</span><span class="sxs-lookup"><span data-stu-id="8eb87-123">The storage object should start at position zero.</span></span>
    
 <span data-ttu-id="8eb87-124">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="8eb87-124">_lppStorageOut_</span></span>
  
> <span data-ttu-id="8eb87-125">[out] Pointeur vers un pointeur vers l’objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="8eb87-125">[out] A pointer to a pointer to the storage object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8eb87-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8eb87-126">Return value</span></span>

<span data-ttu-id="8eb87-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="8eb87-127">S_OK</span></span> 
  
> <span data-ttu-id="8eb87-128">L’objet de stockage a été créé avec succès.</span><span class="sxs-lookup"><span data-stu-id="8eb87-128">The storage object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8eb87-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="8eb87-129">Remarks</span></span>

<span data-ttu-id="8eb87-130">La **méthode IMAPISupport::IStorageFromStream** est implémentée pour tous les objets de prise en charge du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="8eb87-130">The **IMAPISupport::IStorageFromStream** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="8eb87-131">Les fournisseurs de services **appellent IStorageFromStream** pour créer un objet de stockage à utiliser pour ouvrir des propriétés particulières.</span><span class="sxs-lookup"><span data-stu-id="8eb87-131">Service providers call **IStorageFromStream** to create a storage object to use for opening particular properties.</span></span> <span data-ttu-id="8eb87-132">Les fournisseurs de services qui ont leur propre implémentation de l’interface [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) n’ont pas besoin d’appeler **IStorageFromStream**.</span><span class="sxs-lookup"><span data-stu-id="8eb87-132">Service providers that have their own implementation of the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface do not need to call **IStorageFromStream**.</span></span> 
  
<span data-ttu-id="8eb87-133">L’objet de stockage créé par **IStorageFromStream** appelle la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) du flux pour incrémenter son nombre de références, puis décrémente le nombre lorsque le stockage est libéré.</span><span class="sxs-lookup"><span data-stu-id="8eb87-133">The storage object created by **IStorageFromStream** calls the stream's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment its reference count and then decrements the count when the storage is released.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8eb87-134">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="8eb87-134">Notes to callers</span></span>

<span data-ttu-id="8eb87-135">Lorsque la [méthode IMAPIProp::OpenProperty](imapiprop-openproperty.md) de l’un de vos objets est appelée pour ouvrir une propriété avec l’interface **IStorage,** effectuez les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="8eb87-135">When the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method of one of your objects is called to open a property with the **IStorage** interface, perform the following tasks:</span></span> 
  
1. <span data-ttu-id="8eb87-136">Ouvrez un objet stream avec une autorisation de lecture/écriture pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="8eb87-136">Open a stream object with read/write permission for the property.</span></span>
    
2. <span data-ttu-id="8eb87-137">Marquez en interne le flux de propriété en tant qu’objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="8eb87-137">Internally mark the property stream as a storage object.</span></span>
    
3. <span data-ttu-id="8eb87-138">Appelez **IStorageFromStream** pour générer un objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="8eb87-138">Call **IStorageFromStream** to generate a storage object.</span></span> 
    
4. <span data-ttu-id="8eb87-139">Renvoyer un pointeur vers cet objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="8eb87-139">Return a pointer to this storage object.</span></span>
    
<span data-ttu-id="8eb87-140">Si vous implémentez des interfaces supplémentaires qui utilisent l’objet de stockage, créez un objet qui enveloppe l’objet de stockage et implémentez une méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="8eb87-140">If you implement additional interfaces that use the storage object, create an object that wraps the storage object and implement a higher level [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method.</span></span> 
  
<span data-ttu-id="8eb87-141">N’autorisez pas l’ouverture d’une propriété avec l’interface **IStream** si elle a été créée avec **IStorage**.</span><span class="sxs-lookup"><span data-stu-id="8eb87-141">Do not allow a property to be opened with the **IStream** interface if it was created with **IStorage**.</span></span> <span data-ttu-id="8eb87-142">Inversement, n’autorisez pas l’ouverture d’une propriété avec l’interface **IStorage** si elle a été créée avec **IStream**.</span><span class="sxs-lookup"><span data-stu-id="8eb87-142">Conversely, do not allow a property to be opened with the **IStorage** interface if it was created with **IStream**.</span></span> 
  
<span data-ttu-id="8eb87-143">À une exception près, il est acceptable d’utiliser l’interface **IStreamDocfile** pour diffuser un objet de stockage d’un conteneur à un autre, mais l’identificateur d’interface IID_IStreamDocfile doit être transmis dans le paramètre _lpInterface_ de la méthode **OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="8eb87-143">With one exception, it is acceptable to use the **IStreamDocfile** interface to stream a storage object from one container to another, but the IID_IStreamDocfile interface identifier must be passed in the **OpenProperty** method's  _lpInterface_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8eb87-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8eb87-144">See also</span></span>



[<span data-ttu-id="8eb87-145">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="8eb87-145">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="8eb87-146">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8eb87-146">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

