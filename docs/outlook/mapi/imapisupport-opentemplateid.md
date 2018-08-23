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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 855810f7ac3bc1bd433ddd56aba3fe1f938b9559
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575384"
---
# <a name="imapisupportopentemplateid"></a><span data-ttu-id="47185-103">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="47185-103">IMAPISupport::OpenTemplateID</span></span>

  
  
<span data-ttu-id="47185-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47185-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47185-105">Ouvre une entrée de destinataires dans un fournisseur de carnet d’adresse étrangère.</span><span class="sxs-lookup"><span data-stu-id="47185-105">Opens a recipient entry in a foreign address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="47185-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47185-106">Parameters</span></span>

 <span data-ttu-id="47185-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="47185-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="47185-108">[in] Le nombre d’octets dans l’identificateur de modèle désigné par _lpTemplateID_.</span><span class="sxs-lookup"><span data-stu-id="47185-108">[in] The byte count in the template identifier pointed to by  _lpTemplateID_.</span></span> 
    
 <span data-ttu-id="47185-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="47185-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="47185-110">[in] Pointeur vers l’identificateur du modèle propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de l’entrée de destinataire à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="47185-110">[in] A pointer to the template identifier **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="47185-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="47185-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="47185-112">[in] Un masque binaire composé des indicateurs utilisés pour décrire comment ouvrir l’entrée.</span><span class="sxs-lookup"><span data-stu-id="47185-112">[in] A bitmask of flags used to describe how to open the entry.</span></span> <span data-ttu-id="47185-113">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="47185-113">The following flag can be set:</span></span>
    
<span data-ttu-id="47185-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="47185-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="47185-115">Une nouvelle entrée est créée.</span><span class="sxs-lookup"><span data-stu-id="47185-115">A new entry is being created.</span></span> <span data-ttu-id="47185-116">Lorsque le fournisseur étranger reçoit le prochain appel [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) MAPI, il peut contrôler la création de l’entrée en modifiant les propriétés indiquées par le paramètre _lpMAPIPropData_ ou en retournant une interface spécifique mise en œuvre dans _lppMAPIPropNew_ pour contrôler la définition des propriétés de la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="47185-116">When the foreign provider receives the subsequent [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) call from MAPI, it can control how the entry is created by modifying properties pointed to by the  _lpMAPIPropData_ parameter or by returning a specific interface implementation in  _lppMAPIPropNew_ to control how properties for the new entry are set.</span></span> 
    
 <span data-ttu-id="47185-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="47185-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="47185-118">[in] Pointeur vers l’implémentation d’interface de l’appelant à accéder à l’entrée.</span><span class="sxs-lookup"><span data-stu-id="47185-118">[in] A pointer to the interface implementation that the caller uses to access the entry.</span></span> <span data-ttu-id="47185-119">Il s’agit de l’implémentation du fournisseur étranger pouvant envelopper avec sa propre implémentation et retourner dans le paramètre _lppMAPIPropNew_ .</span><span class="sxs-lookup"><span data-stu-id="47185-119">This is the implementation that the foreign provider can wrap with its own implementation and return in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="47185-120">Le paramètre _lpMAPIPropData_ doit pointer sur une implémentation d’interface en lecture/écriture qui dérive de [IMAPIProp : IUnknown](imapipropiunknown.md) et prend en charge l’interface demandée dans le paramètre _lpInterface_ .</span><span class="sxs-lookup"><span data-stu-id="47185-120">The  _lpMAPIPropData_ parameter must point to a read/write interface implementation that derives from [IMAPIProp : IUnknown](imapipropiunknown.md) and supports the interface being requested in the  _lpInterface_ parameter.</span></span> 
    
 <span data-ttu-id="47185-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="47185-121">_lpInterface_</span></span>
  
> <span data-ttu-id="47185-122">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’entrée.</span><span class="sxs-lookup"><span data-stu-id="47185-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the entry.</span></span> <span data-ttu-id="47185-123">Le paramètre _lppMAPIPropNew_ pointe vers une interface du type spécifié par _lpInterface_.</span><span class="sxs-lookup"><span data-stu-id="47185-123">The  _lppMAPIPropNew_ parameter points to an interface of the type specified by  _lpInterface_.</span></span> <span data-ttu-id="47185-124">Passage de NULL renvoie l’interface standard pour un utilisateur de messagerie, IID_IMailUser.</span><span class="sxs-lookup"><span data-stu-id="47185-124">Passing NULL returns the standard interface for a messaging user, IID_IMailUser.</span></span> 
    
 <span data-ttu-id="47185-125">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="47185-125">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="47185-126">[out] Pointeur vers l’implémentation d’interface que le fournisseur étranger donne pour accéder à l’entrée.</span><span class="sxs-lookup"><span data-stu-id="47185-126">[out] A pointer to the interface implementation that the foreign provider supplies for accessing the entry.</span></span>
    
 <span data-ttu-id="47185-127">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="47185-127">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="47185-128">Réservé ; doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="47185-128">Reserved; must be NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47185-129">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="47185-129">Return value</span></span>

<span data-ttu-id="47185-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="47185-130">S_OK</span></span> 
  
> <span data-ttu-id="47185-131">Le processus de liaison a réussi.</span><span class="sxs-lookup"><span data-stu-id="47185-131">The binding process was successful.</span></span>
    
<span data-ttu-id="47185-132">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="47185-132">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="47185-133">Le fournisseur de carnet d’adresse étrangère n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="47185-133">The foreign address book provider doesn't exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47185-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="47185-134">Remarks</span></span>

<span data-ttu-id="47185-135">La méthode **IMAPISupport::OpenTemplateID** est implémentée uniquement pour les objets de prise en charge du fournisseur adresse téléchargeable.</span><span class="sxs-lookup"><span data-stu-id="47185-135">The **IMAPISupport::OpenTemplateID** method is implemented only for address book provider support objects.</span></span> <span data-ttu-id="47185-136">**OpenTemplateID** est appelé uniquement par les fournisseurs de carnet d’adresses qui peuvent agir en tant qu’hôtes pour les entrées qui appartiennent à d’autres fournisseurs de carnet d’adresses, également appelé étrangères fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="47185-136">**OpenTemplateID** is called only by address book providers that can act as hosts for entries that belong to other address book providers, also known as foreign providers.</span></span> <span data-ttu-id="47185-137">Fournisseurs d’hébergement appellent **OpenTemplateID** pour ouvrir une entrée étrangère, ce qui se produit lorsque des données dans le fournisseur d’hébergement sont liées au code dans le fournisseur étranger.</span><span class="sxs-lookup"><span data-stu-id="47185-137">Host providers call **OpenTemplateID** to open a foreign entry, which occurs when data in the host provider is bound to code in the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="47185-138">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="47185-138">Notes to callers</span></span>

<span data-ttu-id="47185-139">Appelez **OpenTemplateID** uniquement si vous prenez en charge le stockage des entrées avec les identificateurs de modèle à partir des fournisseurs de carnet d’adresse étrangère.</span><span class="sxs-lookup"><span data-stu-id="47185-139">Call **OpenTemplateID** only if you support the storage of entries with template identifiers from foreign address book providers.</span></span> <span data-ttu-id="47185-140">Cette prise en charge impose des exigences supplémentaires sur vos implémentations [IABContainer::CreateEntry](iabcontainer-createentry.md) et [IABLogon::OpenEntry](iablogon-openentry.md) .</span><span class="sxs-lookup"><span data-stu-id="47185-140">Such support places additional requirements on your [IABContainer::CreateEntry](iabcontainer-createentry.md) and [IABLogon::OpenEntry](iablogon-openentry.md) implementations.</span></span> <span data-ttu-id="47185-141">Pour plus d’informations, consultez les descriptions de ces méthodes [agissant comme un fournisseur de carnet d’adresses hôte](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="47185-141">For more information, see the descriptions of these methods and [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
<span data-ttu-id="47185-142">Si l’appel **OpenTemplateID** renvoie l’interface liée l’implémentation d’objet même propriété que vous avez passé, vous pouvez libérer la référence à votre objet de la propriété.</span><span class="sxs-lookup"><span data-stu-id="47185-142">If the **OpenTemplateID** call returns as the bound interface the same property object implementation that you passed in, you can release your reference to your property object.</span></span> <span data-ttu-id="47185-143">Il s’agit, car le fournisseur étranger a appelé la méthode l’objet **AddRef** pour garder sa propre référence.</span><span class="sxs-lookup"><span data-stu-id="47185-143">This is because the foreign provider has called the object's **AddRef** method to keep its own reference.</span></span> <span data-ttu-id="47185-144">Si le fournisseur étranger n’a pas besoin de conserver une référence à l’objet property, **OpenTemplateID** renvoie l’objet property indépendant.</span><span class="sxs-lookup"><span data-stu-id="47185-144">If the foreign provider does not need to keep a reference to the property object, then **OpenTemplateID** will return the unbound property object.</span></span> 
  
<span data-ttu-id="47185-145">En cas d’échec de **OpenTemplateID** avec MAPI_E_UNKNOWN_ENTRYID, essayez de continuer à traiter l’entrée en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="47185-145">If **OpenTemplateID** fails with MAPI_E_UNKNOWN_ENTRYID, try to continue by treating the entry as read-only.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47185-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47185-146">See also</span></span>



[<span data-ttu-id="47185-147">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="47185-147">IABLogon::OpenTemplateID</span></span>](iablogon-opentemplateid.md)
  
[<span data-ttu-id="47185-148">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="47185-148">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="47185-149">Propriété canonique PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="47185-149">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="47185-150">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47185-150">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

