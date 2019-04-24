---
title: IMAPISupportOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenTemplateID
api_type:
- COM
ms.assetid: 532f7af0-b2cc-49dd-b1de-e3ec1dc9a3e7
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 07aa508b473f4a87d5b4909f83771549c301a600
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326361"
---
# <a name="imapisupportopentemplateid"></a><span data-ttu-id="93202-103">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="93202-103">IMAPISupport::OpenTemplateID</span></span>

  
  
<span data-ttu-id="93202-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93202-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93202-105">Ouvre une entrée de destinataire dans un fournisseur de carnets d'adresses étrangers.</span><span class="sxs-lookup"><span data-stu-id="93202-105">Opens a recipient entry in a foreign address book provider.</span></span>
  
```cpp
HRESULT OpenTemplateID(
ULONG cbTemplateID,
LPENTRYID lpTemplateID,
ULONG ulTemplateFlags,
LPMAPIPROP lpMAPIPropData,
LPCIID lpInterface,
LPMAPIPROP FAR * lppMAPIPropNew,
LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a><span data-ttu-id="93202-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93202-106">Parameters</span></span>

 <span data-ttu-id="93202-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="93202-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="93202-108">dans Nombre d'octets dans l'identificateur de modèle pointé par _lpTemplateID_.</span><span class="sxs-lookup"><span data-stu-id="93202-108">[in] The byte count in the template identifier pointed to by  _lpTemplateID_.</span></span> 
    
 <span data-ttu-id="93202-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="93202-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="93202-110">dans Pointeur vers la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de l'identificateur de modèle de l'entrée de destinataire à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="93202-110">[in] A pointer to the template identifier **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="93202-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="93202-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="93202-112">dans Masque de des indicateurs utilisés pour décrire l'ouverture de l'entrée.</span><span class="sxs-lookup"><span data-stu-id="93202-112">[in] A bitmask of flags used to describe how to open the entry.</span></span> <span data-ttu-id="93202-113">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="93202-113">The following flag can be set:</span></span>
    
<span data-ttu-id="93202-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="93202-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="93202-115">Une nouvelle entrée est créée.</span><span class="sxs-lookup"><span data-stu-id="93202-115">A new entry is being created.</span></span> <span data-ttu-id="93202-116">Lorsque le fournisseur étranger reçoit l'appel [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) à partir de MAPI, il peut contrôler la manière dont l'entrée est créée en modifiant les propriétés pointées par le paramètre _lpMAPIPropData_ ou en renvoyant une interface spécifique. implémentation dans _lppMAPIPropNew_ pour contrôler la définition des propriétés de la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="93202-116">When the foreign provider receives the subsequent [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) call from MAPI, it can control how the entry is created by modifying properties pointed to by the  _lpMAPIPropData_ parameter or by returning a specific interface implementation in  _lppMAPIPropNew_ to control how properties for the new entry are set.</span></span> 
    
 <span data-ttu-id="93202-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="93202-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="93202-118">dans Pointeur vers l'implémentation de l'interface que l'appelant utilise pour accéder à l'entrée.</span><span class="sxs-lookup"><span data-stu-id="93202-118">[in] A pointer to the interface implementation that the caller uses to access the entry.</span></span> <span data-ttu-id="93202-119">Il s'agit de l'implémentation que le fournisseur étranger peut encapsuler avec sa propre implémentation et renvoyer le paramètre _lppMAPIPropNew_ .</span><span class="sxs-lookup"><span data-stu-id="93202-119">This is the implementation that the foreign provider can wrap with its own implementation and return in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="93202-120">Le paramètre _lpMAPIPropData_ doit pointer vers une implémentation d'interface en lecture/écriture qui dérive de [IMAPIProp: IUnknown](imapipropiunknown.md) et prend en charge l'interface demandée dans le paramètre _lpInterface_ .</span><span class="sxs-lookup"><span data-stu-id="93202-120">The  _lpMAPIPropData_ parameter must point to a read/write interface implementation that derives from [IMAPIProp : IUnknown](imapipropiunknown.md) and supports the interface being requested in the  _lpInterface_ parameter.</span></span> 
    
 <span data-ttu-id="93202-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="93202-121">_lpInterface_</span></span>
  
> <span data-ttu-id="93202-122">dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à l'entrée.</span><span class="sxs-lookup"><span data-stu-id="93202-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the entry.</span></span> <span data-ttu-id="93202-123">Le paramètre _lppMAPIPropNew_ pointe vers une interface du type spécifié par _lpInterface_.</span><span class="sxs-lookup"><span data-stu-id="93202-123">The  _lppMAPIPropNew_ parameter points to an interface of the type specified by  _lpInterface_.</span></span> <span data-ttu-id="93202-124">Le passage de NULL renvoie l'interface standard pour un utilisateur de messagerie, IID_IMailUser.</span><span class="sxs-lookup"><span data-stu-id="93202-124">Passing NULL returns the standard interface for a messaging user, IID_IMailUser.</span></span> 
    
 <span data-ttu-id="93202-125">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="93202-125">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="93202-126">remarquer Pointeur vers l'implémentation de l'interface que le fournisseur étranger fournit pour accéder à l'entrée.</span><span class="sxs-lookup"><span data-stu-id="93202-126">[out] A pointer to the interface implementation that the foreign provider supplies for accessing the entry.</span></span>
    
 <span data-ttu-id="93202-127">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="93202-127">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="93202-128">MSR doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="93202-128">Reserved; must be NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="93202-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="93202-129">Return value</span></span>

<span data-ttu-id="93202-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="93202-130">S_OK</span></span> 
  
> <span data-ttu-id="93202-131">Le processus de liaison a réussi.</span><span class="sxs-lookup"><span data-stu-id="93202-131">The binding process was successful.</span></span>
    
<span data-ttu-id="93202-132">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="93202-132">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="93202-133">Le fournisseur de carnets d'adresses étrangers n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="93202-133">The foreign address book provider doesn't exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93202-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="93202-134">Remarks</span></span>

<span data-ttu-id="93202-135">La méthode **IMAPISupport:: OpenTemplateID** est implémentée uniquement pour les objets de prise en charge du fournisseur de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="93202-135">The **IMAPISupport::OpenTemplateID** method is implemented only for address book provider support objects.</span></span> <span data-ttu-id="93202-136">**OpenTemplateID** est appelé uniquement par les fournisseurs de carnet d'adresses qui peuvent agir comme des hôtes pour les entrées appartenant à d'autres fournisseurs de carnet d'adresses, également appelés fournisseurs étrangers.</span><span class="sxs-lookup"><span data-stu-id="93202-136">**OpenTemplateID** is called only by address book providers that can act as hosts for entries that belong to other address book providers, also known as foreign providers.</span></span> <span data-ttu-id="93202-137">Les fournisseurs d'hôtes appellent **OpenTemplateID** pour ouvrir une entrée étrangère, qui se produit lorsque les données du fournisseur hôte sont liées au code dans le fournisseur étranger.</span><span class="sxs-lookup"><span data-stu-id="93202-137">Host providers call **OpenTemplateID** to open a foreign entry, which occurs when data in the host provider is bound to code in the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="93202-138">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="93202-138">Notes to callers</span></span>

<span data-ttu-id="93202-139">Appelez **OpenTemplateID** uniquement si vous prenez en charge le stockage des entrées avec des identificateurs de modèle provenant de fournisseurs de carnet d'adresses étrangers.</span><span class="sxs-lookup"><span data-stu-id="93202-139">Call **OpenTemplateID** only if you support the storage of entries with template identifiers from foreign address book providers.</span></span> <span data-ttu-id="93202-140">Cette prise en charge impose des exigences supplémentaires sur vos implémentations de [IABContainer:: CreateEntry](iabcontainer-createentry.md) et [IABLogon:: OpenEntry](iablogon-openentry.md) .</span><span class="sxs-lookup"><span data-stu-id="93202-140">Such support places additional requirements on your [IABContainer::CreateEntry](iabcontainer-createentry.md) and [IABLogon::OpenEntry](iablogon-openentry.md) implementations.</span></span> <span data-ttu-id="93202-141">Pour plus d'informations, consultez les descriptions de ces méthodes et [agir en tant que fournisseur de carnets d'adresses hôte](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="93202-141">For more information, see the descriptions of these methods and [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
<span data-ttu-id="93202-142">Si l'appel **OpenTemplateID** est renvoyé en tant qu'interface liée à la même implémentation d'objet de propriété que celle que vous avez passée, vous pouvez libérer votre référence à votre objet Property.</span><span class="sxs-lookup"><span data-stu-id="93202-142">If the **OpenTemplateID** call returns as the bound interface the same property object implementation that you passed in, you can release your reference to your property object.</span></span> <span data-ttu-id="93202-143">Cela est dû au fait que le fournisseur étranger a appelé la méthode **AddRef** de l'objet pour conserver sa propre référence.</span><span class="sxs-lookup"><span data-stu-id="93202-143">This is because the foreign provider has called the object's **AddRef** method to keep its own reference.</span></span> <span data-ttu-id="93202-144">Si le fournisseur étranger n'a pas besoin de conserver une référence à l'objet Property, **OpenTemplateID** renverra l'objet de propriété indépendant.</span><span class="sxs-lookup"><span data-stu-id="93202-144">If the foreign provider does not need to keep a reference to the property object, then **OpenTemplateID** will return the unbound property object.</span></span> 
  
<span data-ttu-id="93202-145">Si **OpenTemplateID** échoue avec MAPI_E_UNKNOWN_ENTRYID, essayez de continuer en traitant l'entrée comme étant en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="93202-145">If **OpenTemplateID** fails with MAPI_E_UNKNOWN_ENTRYID, try to continue by treating the entry as read-only.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="93202-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93202-146">See also</span></span>



[<span data-ttu-id="93202-147">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="93202-147">IABLogon::OpenTemplateID</span></span>](iablogon-opentemplateid.md)
  
[<span data-ttu-id="93202-148">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="93202-148">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="93202-149">Propriété canonique PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="93202-149">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="93202-150">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="93202-150">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

