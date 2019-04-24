---
title: IABLogonOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenTemplateID
api_type:
- COM
ms.assetid: 751c36d3-c39e-4357-a60a-88685a378de0
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: bc68878a25873533162df7e1671e483c3bb77865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334747"
---
# <a name="iablogonopentemplateid"></a><span data-ttu-id="06e26-103">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="06e26-103">IABLogon::OpenTemplateID</span></span>

  
  
<span data-ttu-id="06e26-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06e26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06e26-105">Ouvre une entrée de destinataire dont les données résident dans un fournisseur de carnet d'adresses hôte.</span><span class="sxs-lookup"><span data-stu-id="06e26-105">Opens a recipient entry that has data residing in a host address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="06e26-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06e26-106">Parameters</span></span>

 <span data-ttu-id="06e26-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="06e26-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="06e26-108">dans Nombre d'octets dans l'identificateur de modèle pointé par le paramètre _lpTemplateID_ .</span><span class="sxs-lookup"><span data-stu-id="06e26-108">[in] The byte count in the template identifier pointed to by the  _lpTemplateID_ parameter.</span></span> 
    
 <span data-ttu-id="06e26-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="06e26-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="06e26-110">dans Pointeur vers l'identificateur de modèle, ou propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), de l'entrée de destinataire à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="06e26-110">[in] A pointer to the template identifier, or **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="06e26-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="06e26-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="06e26-112">dans Masque de des indicateurs utilisé pour indiquer comment ouvrir l'entrée représentée par l'identificateur de modèle.</span><span class="sxs-lookup"><span data-stu-id="06e26-112">[in] A bitmask of flags used to indicate how to open the entry represented by the template identifier.</span></span> <span data-ttu-id="06e26-113">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="06e26-113">The following flag can be set:</span></span>
    
<span data-ttu-id="06e26-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="06e26-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="06e26-115">Le fournisseur hôte crée une entrée dans son conteneur en fonction de l'entrée représentée par l'identificateur de modèle.</span><span class="sxs-lookup"><span data-stu-id="06e26-115">The host provider is creating a new entry in its container based on the entry represented by the template identifier.</span></span> <span data-ttu-id="06e26-116">La méthode **IABLogon:: OpenTemplateID** doit effectuer une initialisation spécifique de l'entrée du fournisseur hôte à l'aide de l'implémentation [IMAPIProp: IUnknown](imapipropiunknown.md) dans le paramètre _LpMAPIPropData_ , ou renvoyer une \*\*IMAPIProp personnalisée. \*\*implémentation de l'interface dans le paramètre _lppMAPIPropNew_ .</span><span class="sxs-lookup"><span data-stu-id="06e26-116">The **IABLogon::OpenTemplateID** method should either perform specific initialization of the host provider's entry by using the [IMAPIProp : IUnknown](imapipropiunknown.md) implementation in the  _lpMAPIPropData_ parameter, or return a custom **IMAPIProp** interface implementation in the  _lppMAPIPropNew_ parameter.</span></span> 
    
 <span data-ttu-id="06e26-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="06e26-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="06e26-118">dans Pointeur vers l'objet Property du fournisseur hôte et l'implémentation d'une interface dérivée de **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="06e26-118">[in] A pointer to the host provider's property object and implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="06e26-119">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="06e26-119">_lpInterface_</span></span>
  
> <span data-ttu-id="06e26-120">dans Pointeur vers l'identificateur d'interface (IID) qui représente le type de pointeur d'interface à renvoyer dans le paramètre _lppMAPIPropNew_ .</span><span class="sxs-lookup"><span data-stu-id="06e26-120">[in] A pointer to the interface identifier (IID) that represents the type of interface pointer to be returned in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="06e26-121">Le passage de la **valeur null** renvoie l'interface utilisateur de messagerie standard, [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="06e26-121">Passing **null** returns the standard messaging user interface, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span>
    
 <span data-ttu-id="06e26-122">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="06e26-122">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="06e26-123">remarquer Pointeur vers l'objet de propriété liée et implémentation d'une interface dérivée de **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="06e26-123">[out] A pointer to the bound property object and an implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="06e26-124">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="06e26-124">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="06e26-125">remarquer MSR doit être **null**.</span><span class="sxs-lookup"><span data-stu-id="06e26-125">[out] Reserved; must be **null**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="06e26-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="06e26-126">Return value</span></span>

<span data-ttu-id="06e26-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="06e26-127">S_OK</span></span> 
  
> <span data-ttu-id="06e26-128">Le code approprié a été correctement lié aux données connexes dans le fournisseur d'hôte.</span><span class="sxs-lookup"><span data-stu-id="06e26-128">The appropriate code was successfully bound to related data in the host provider.</span></span>
    
<span data-ttu-id="06e26-129">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="06e26-129">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="06e26-130">L'objet ne prend pas en charge les ID de modèle.</span><span class="sxs-lookup"><span data-stu-id="06e26-130">The object does not support template IDs.</span></span>
    
<span data-ttu-id="06e26-131">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="06e26-131">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="06e26-132">L'identificateur de modèle passé dans le paramètre _lpTemplateID_ n'est pas reconnu par le fournisseur de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="06e26-132">The template identifier passed in the  _lpTemplateID_ parameter is not recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="06e26-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="06e26-133">Remarks</span></span>

<span data-ttu-id="06e26-134">La méthode **IABLogon:: OpenTemplateID** est implémentée uniquement par les fournisseurs de carnet d'adresses qui doivent conserver le contrôle des copies de leurs entrées qui se trouvent dans les conteneurs des fournisseurs hôtes.</span><span class="sxs-lookup"><span data-stu-id="06e26-134">The **IABLogon::OpenTemplateID** method is implemented only by address book providers that need to maintain control over copies of their entries that are located in the containers of host providers.</span></span> <span data-ttu-id="06e26-135">Les fournisseurs qui implémentent **OpenTemplateID** sont appelés fournisseurs de carnets d'adresses étrangers.</span><span class="sxs-lookup"><span data-stu-id="06e26-135">Providers that implement **OpenTemplateID** are known as foreign address book providers.</span></span> <span data-ttu-id="06e26-136">Les fournisseurs d'hôtes appellent [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) pour créer une entrée copiée ou ouvrir l'entrée copiée, et MAPI transmet l'appel à **IABLogon:: OpenTemplateID**.</span><span class="sxs-lookup"><span data-stu-id="06e26-136">Host providers call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to create a copied entry or open the copied entry, and MAPI passes on the call to **IABLogon::OpenTemplateID**.</span></span> <span data-ttu-id="06e26-137">**IABLogon:: OpenTemplateID** ouvre l'entrée et lie le code qui le contrôle aux données du fournisseur hôte.</span><span class="sxs-lookup"><span data-stu-id="06e26-137">**IABLogon::OpenTemplateID** opens the entry and binds the code that controls it to data in the host provider.</span></span> 
  
<span data-ttu-id="06e26-138">Au lieu d'utiliser un identificateur d'entrée, **IABLogon:: OpenTemplateID** utilise une autre propriété, l'identificateur de modèle de l'entrée, **PR_TEMPLATEID**.</span><span class="sxs-lookup"><span data-stu-id="06e26-138">Rather than use an entry identifier, **IABLogon::OpenTemplateID** uses another property, the entry's template identifier, **PR_TEMPLATEID**.</span></span> <span data-ttu-id="06e26-139">Les identificateurs de modèle doivent être pris en charge pour les entrées dont le code doit être lié aux données dans un fournisseur d'hôte.</span><span class="sxs-lookup"><span data-stu-id="06e26-139">Template identifiers should be supported for entries whose code must be bound to data in a host provider.</span></span>
  
<span data-ttu-id="06e26-140">Voici quelques exemples de cas où un fournisseur de carnets d'adresses doit implémenter **IABLogon:: OpenTemplateID** sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="06e26-140">Some examples of when an address book provider should implement **IABLogon::OpenTemplateID** are as follows:</span></span> 
  
- <span data-ttu-id="06e26-141">Mettre à jour régulièrement les données d'une entrée copiée de sorte qu'elles restent synchronisées avec l'original.</span><span class="sxs-lookup"><span data-stu-id="06e26-141">To periodically update the data for a copied entry so that it stays synchronized with the original.</span></span>
    
- <span data-ttu-id="06e26-142">Implémenter les fonctionnalités que le fournisseur d'hôtes ne peut pas implémenter, telles que le remplissage dynamique d'une liste qui apparaît dans la table des détails de l'entrée à partir de données sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="06e26-142">To implement functionality that the host provider cannot implement, such as dynamically populating a list that appears in the entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="06e26-143">Pour contrôler l'interaction entre les propriétés dans l'entrée du fournisseur de l'hôte et l'entrée d'origine, telles que le calcul de la **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) à partir des valeurs des contrôles d'édition dans l'affichage des détails qui contiennent différentes composants de l'adresse.</span><span class="sxs-lookup"><span data-stu-id="06e26-143">To control the interaction between properties in the host provider's entry and the original entry, such as computing the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) from the values of the edit controls in the details display that contain different components of the address.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="06e26-144">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="06e26-144">Notes to implementers</span></span>

<span data-ttu-id="06e26-145">Lorsqu'un fournisseur d'hôtes copie ou crée une entrée à partir de votre fournisseur et que vous fournissez une implémentation d'objet de propriété via **IABLogon:: OpenTemplateID**, vous gérez la plupart des appels pour maintenir l'entrée.</span><span class="sxs-lookup"><span data-stu-id="06e26-145">When a host provider copies or creates an entry from your provider and you supply a property object implementation through **IABLogon::OpenTemplateID**, you handle most of the calls to maintain the entry.</span></span> <span data-ttu-id="06e26-146">Toutefois, étant donné qu'il revient au fournisseur hôte de transférer ces appels à vous, le fournisseur hôte peut intercepter tout appel et effectuer un traitement personnalisé avant de transférer l'appel.</span><span class="sxs-lookup"><span data-stu-id="06e26-146">However, because it is up to the host provider to forward these calls to you, the host provider can intercept any call and perform custom processing before forwarding the call.</span></span>
  
<span data-ttu-id="06e26-147">Vous devez utiliser les instructions suivantes dans les implémentations de l'objet Property:</span><span class="sxs-lookup"><span data-stu-id="06e26-147">You should use the following guidelines in your property object implementations:</span></span>
  
- <span data-ttu-id="06e26-148">Lorsque [IMAPIProp:: GetProps](imapiprop-getprops.md) est appelé, déterminez si la demande concerne une propriété calculée et, si c'est le cas, gérez-la.</span><span class="sxs-lookup"><span data-stu-id="06e26-148">When [IMAPIProp::GetProps](imapiprop-getprops.md) is called, determine whether the request is for a computed property and, if it is, handle it.</span></span> <span data-ttu-id="06e26-149">Transférez toutes les demandes pour les propriétés qui ne sont pas calculées vers le fournisseur hôte.</span><span class="sxs-lookup"><span data-stu-id="06e26-149">Transfer all requests for noncomputed properties to the host provider.</span></span> 
    
- <span data-ttu-id="06e26-150">Lorsque [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) est appelé pour ouvrir une table à l'exception de la table d'affichage des détails, gérez la demande.</span><span class="sxs-lookup"><span data-stu-id="06e26-150">When [IMAPIProp::OpenProperty](imapiprop-openproperty.md) is called to open any table except the details display table, handle the request.</span></span> <span data-ttu-id="06e26-151">La plupart des tables ne peuvent pas être copiées correctement sur le fournisseur hôte.</span><span class="sxs-lookup"><span data-stu-id="06e26-151">Most tables cannot be copied accurately to the host provider.</span></span> <span data-ttu-id="06e26-152">Vous devez générer l'implémentation de l' **IMAPITable** pour ces tables demandées.</span><span class="sxs-lookup"><span data-stu-id="06e26-152">You must generate the **IMAPITable** implementation for these requested tables.</span></span> <span data-ttu-id="06e26-153">La propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) de la table des détails doit être copiée sur le fournisseur hôte.</span><span class="sxs-lookup"><span data-stu-id="06e26-153">The details table **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property must be copied to the host provider.</span></span> <span data-ttu-id="06e26-154">Cela permet à ce fournisseur de générer la table localement.</span><span class="sxs-lookup"><span data-stu-id="06e26-154">This allows this provider to generate the table locally.</span></span> <span data-ttu-id="06e26-155">Vous souhaiterez peut-être encapsuler l'implémentation de la table d'affichage pour générer des notifications de table d'affichage.</span><span class="sxs-lookup"><span data-stu-id="06e26-155">You might want to wrap the display table implementation to generate display table notifications.</span></span> 
    
- <span data-ttu-id="06e26-156">Lorsque [IMAPIProp:: SetProps](imapiprop-setprops.md) est appelé, le fournisseur d'hôtes peut valider les données avant de vous permettre de définir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="06e26-156">When [IMAPIProp::SetProps](imapiprop-setprops.md) is called, the host provider can validate the data before letting you set the properties.</span></span> <span data-ttu-id="06e26-157">Vous pouvez vérifier que toutes les propriétés nécessaires ont été définies ou calculées.</span><span class="sxs-lookup"><span data-stu-id="06e26-157">You can verify that all of the necessary properties were set or computed.</span></span> <span data-ttu-id="06e26-158">Si une erreur est détectée, renvoyer la valeur d'erreur appropriée et, si possible, une explication supplémentaire via [IMAPIProp:: GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="06e26-158">If an error is detected, return the appropriate error value and, if you can, any additional explanation through [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span>
    
- <span data-ttu-id="06e26-159">Lorsque [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) est appelé, le fournisseur hôte peut souhaiter effectuer un traitement avant l'enregistrement de l'entrée.</span><span class="sxs-lookup"><span data-stu-id="06e26-159">When [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called, the host provider might want to perform processing before you save the entry.</span></span> <span data-ttu-id="06e26-160">Vous devez enregistrer toutes les données affectées par les propriétés modifiées, telles qu'une nouvelle adresse, dans l'entrée du fournisseur de l'hôte.</span><span class="sxs-lookup"><span data-stu-id="06e26-160">You should save any data that is affected by the changed properties, such as a new address, in the host provider's entry.</span></span> 
    
<span data-ttu-id="06e26-161">En règle générale, votre implémentation de l'entrée que vous transmettez au fournisseur hôte interceptez toutes les méthodes pour effectuer une manipulation propre au contexte des propriétés pertinentes.</span><span class="sxs-lookup"><span data-stu-id="06e26-161">In general, make your implementation of the entry that you pass back to the host provider intercept all of the methods to perform context-specific manipulation of the relevant properties.</span></span> <span data-ttu-id="06e26-162">Si l'indicateur FILL_ENTRY est transmis dans le paramètre _ulTemplateFlags_ , définissez toutes les propriétés de l'entrée.</span><span class="sxs-lookup"><span data-stu-id="06e26-162">If the FILL_ENTRY flag is passed in the  _ulTemplateFlags_ parameter, set all properties for the entry.</span></span> 
  
<span data-ttu-id="06e26-163">Si vous renvoyez un nouvel objet Property dans le paramètre _lppMAPIPropNew_ , appelez la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) de l'objet Property du fournisseur hôte pour maintenir une référence.</span><span class="sxs-lookup"><span data-stu-id="06e26-163">If you return a new property object in the  _lppMAPIPropNew_ parameter, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method of the host provider's property object to maintain a reference.</span></span> <span data-ttu-id="06e26-164">Tous les appels par le biais de l'objet lié que l'implémentation **IMAPIProp** a renvoyé dans _lppMAPIPropNew_ doivent être routés vers leur méthode correspondante dans l'objet de propriété hôte après qu'ils ont été traités par l'objet lié.</span><span class="sxs-lookup"><span data-stu-id="06e26-164">All calls through the bound object that the **IMAPIProp** implementation returned in  _lppMAPIPropNew_ should be routed to their corresponding method in the host property object after they are dealt with by the bound object.</span></span> 
  
<span data-ttu-id="06e26-165">Les identificateurs de propriété de toutes les propriétés nommées transmises via votre objet de propriété liée se trouvent dans l'espace de noms de l'identificateur de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="06e26-165">The property identifiers of any named properties that are passed through your bound property object are in your provider's identifier namespace.</span></span> <span data-ttu-id="06e26-166">Votre implémentation de la méthode [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) doit déterminer les noms des propriétés afin qu'elle puisse effectuer des tâches spécifiques au modèle.</span><span class="sxs-lookup"><span data-stu-id="06e26-166">Your implementation of the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method should determine the names of the properties so that it can perform any template-specific tasks.</span></span> <span data-ttu-id="06e26-167">De même, les propriétés que votre fournisseur transmet au fournisseur hôte doivent également figurer dans votre espace de noms.</span><span class="sxs-lookup"><span data-stu-id="06e26-167">Similarly, properties that your provider passes on to the host provider must also be in your namespace.</span></span> <span data-ttu-id="06e26-168">Par exemple, si vous définissez une propriété nommée dans **OpenTemplateID**, vous devez utiliser l'un de vos identificateurs pour le nom — en le créant, le cas échéant, en appelant la méthode [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="06e26-168">For example, if you set a named property in **OpenTemplateID**, you should use one of your identifiers for the name—creating it, if necessary, by calling the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="06e26-169">Si vous ne connaissez pas l'identificateur d'entrée passé dans _lpTemplateID_, renvoyez MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="06e26-169">If you do not recognize the entry identifier passed in  _lpTemplateID_, return MAPI_E_UNKNOWN_ENTRYID.</span></span>
  
<span data-ttu-id="06e26-170">Pour plus d'informations sur l'utilisation des identificateurs de modèle de carnet d'adresses, consultez la rubrique [agir en tant que fournisseur de carnet d'adresses étranger](acting-as-a-foreign-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="06e26-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06e26-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06e26-171">See also</span></span>



[<span data-ttu-id="06e26-172">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="06e26-172">IMAPISupport::OpenTemplateID</span></span>](imapisupport-opentemplateid.md)
  
[<span data-ttu-id="06e26-173">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="06e26-173">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="06e26-174">Propriété canonique PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="06e26-174">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="06e26-175">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="06e26-175">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

