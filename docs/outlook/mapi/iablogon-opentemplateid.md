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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f2fedd98fe84d7359aebaca8d03a20f392dae2b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783603"
---
# <a name="iablogonopentemplateid"></a><span data-ttu-id="73c69-103">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="73c69-103">IABLogon::OpenTemplateID</span></span>

  
  
<span data-ttu-id="73c69-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73c69-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73c69-105">Ouvre une entrée du destinataire qui comporte des données qui résident dans un fournisseur de carnet d’adresses hôte.</span><span class="sxs-lookup"><span data-stu-id="73c69-105">Opens a recipient entry that has data residing in a host address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="73c69-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73c69-106">Parameters</span></span>

 <span data-ttu-id="73c69-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="73c69-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="73c69-108">[in] Le nombre d’octets dans l’identificateur de modèle indiqué par le paramètre _lpTemplateID_ .</span><span class="sxs-lookup"><span data-stu-id="73c69-108">[in] The byte count in the template identifier pointed to by the  _lpTemplateID_ parameter.</span></span> 
    
 <span data-ttu-id="73c69-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="73c69-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="73c69-110">[in] Pointeur vers l’identificateur du modèle, ou la propriété de **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), de l’entrée de destinataire à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="73c69-110">[in] A pointer to the template identifier, or **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="73c69-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="73c69-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="73c69-112">[in] Un masque binaire composé des indicateurs utilisés pour indiquer comment ouvrir l’entrée représentée par l’identificateur de modèle.</span><span class="sxs-lookup"><span data-stu-id="73c69-112">[in] A bitmask of flags used to indicate how to open the entry represented by the template identifier.</span></span> <span data-ttu-id="73c69-113">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="73c69-113">The following flag can be set:</span></span>
    
<span data-ttu-id="73c69-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="73c69-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="73c69-115">Le fournisseur d’hébergement crée une nouvelle entrée dans le conteneur en fonction de l’entrée représentée par l’identificateur de modèle.</span><span class="sxs-lookup"><span data-stu-id="73c69-115">The host provider is creating a new entry in its container based on the entry represented by the template identifier.</span></span> <span data-ttu-id="73c69-116">La méthode **IABLogon::OpenTemplateID** doit exécuter spécifique d’initialisation de l’entrée du fournisseur de l’hôte à l’aide de la [IMAPIProp : IUnknown](imapipropiunknown.md) implémentation dans le paramètre _lpMAPIPropData_ ou retour **IMAPIProp personnalisé **implémentation dans le paramètre _lppMAPIPropNew_ de l’interface.</span><span class="sxs-lookup"><span data-stu-id="73c69-116">The **IABLogon::OpenTemplateID** method should either perform specific initialization of the host provider's entry by using the [IMAPIProp : IUnknown](imapipropiunknown.md) implementation in the  _lpMAPIPropData_ parameter, or return a custom **IMAPIProp** interface implementation in the  _lppMAPIPropNew_ parameter.</span></span> 
    
 <span data-ttu-id="73c69-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="73c69-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="73c69-118">[in] Un pointeur vers l’objet property du fournisseur d’hébergement et l’implémentation d’une interface dérivé **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="73c69-118">[in] A pointer to the host provider's property object and implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="73c69-119">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="73c69-119">_lpInterface_</span></span>
  
> <span data-ttu-id="73c69-120">[in] Pointeur vers l’identificateur d’interface (IID) qui représente le type de pointeur de l’interface à retourner dans le paramètre _lppMAPIPropNew_ .</span><span class="sxs-lookup"><span data-stu-id="73c69-120">[in] A pointer to the interface identifier (IID) that represents the type of interface pointer to be returned in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="73c69-121">Le passage de **null** renvoie la norme d’interface utilisateur, la messagerie [IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="73c69-121">Passing **null** returns the standard messaging user interface, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span>
    
 <span data-ttu-id="73c69-122">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="73c69-122">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="73c69-123">[out] Un pointeur vers l’objet de la propriété liée et une implémentation d’une interface dérivé **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="73c69-123">[out] A pointer to the bound property object and an implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="73c69-124">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="73c69-124">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="73c69-125">[out] Réservé ; doit être **null**.</span><span class="sxs-lookup"><span data-stu-id="73c69-125">[out] Reserved; must be **null**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="73c69-126">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="73c69-126">Return value</span></span>

<span data-ttu-id="73c69-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="73c69-127">S_OK</span></span> 
  
> <span data-ttu-id="73c69-128">Le code a été correctement lié à des données liées dans le fournisseur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="73c69-128">The appropriate code was successfully bound to related data in the host provider.</span></span>
    
<span data-ttu-id="73c69-129">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="73c69-129">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="73c69-130">L’objet ne prend pas en charge les ID de modèle.</span><span class="sxs-lookup"><span data-stu-id="73c69-130">The object does not support template IDs.</span></span>
    
<span data-ttu-id="73c69-131">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="73c69-131">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="73c69-132">L’identificateur de modèle passé dans le paramètre _lpTemplateID_ n’est pas reconnue par le fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="73c69-132">The template identifier passed in the  _lpTemplateID_ parameter is not recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="73c69-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="73c69-133">Remarks</span></span>

<span data-ttu-id="73c69-134">La méthode **IABLogon::OpenTemplateID** est implémentée uniquement par les fournisseurs de carnet d’adresses qui doivent contrôler les copies de leurs données qui sont trouvent dans les conteneurs de fournisseurs d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="73c69-134">The **IABLogon::OpenTemplateID** method is implemented only by address book providers that need to maintain control over copies of their entries that are located in the containers of host providers.</span></span> <span data-ttu-id="73c69-135">Fournisseurs qui implémentent **OpenTemplateID** sont appelés fournisseurs de carnet d’adresse étrangère.</span><span class="sxs-lookup"><span data-stu-id="73c69-135">Providers that implement **OpenTemplateID** are known as foreign address book providers.</span></span> <span data-ttu-id="73c69-136">Fournisseurs d’hébergement appeler [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) pour créer une entrée copiée ou ouvrir l’entrée copiée et MAPI passe à l’appel de **IABLogon::OpenTemplateID**.</span><span class="sxs-lookup"><span data-stu-id="73c69-136">Host providers call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to create a copied entry or open the copied entry, and MAPI passes on the call to **IABLogon::OpenTemplateID**.</span></span> <span data-ttu-id="73c69-137">**IABLogon::OpenTemplateID** ouvre l’entrée et lie le code qui le contrôle à des données dans le fournisseur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="73c69-137">**IABLogon::OpenTemplateID** opens the entry and binds the code that controls it to data in the host provider.</span></span> 
  
<span data-ttu-id="73c69-138">Au lieu d’utiliser un identificateur d’entrée, **IABLogon::OpenTemplateID** utilise une autre propriété, identificateur du modèle de l’entrée, **PR_TEMPLATEID**.</span><span class="sxs-lookup"><span data-stu-id="73c69-138">Rather than use an entry identifier, **IABLogon::OpenTemplateID** uses another property, the entry's template identifier, **PR_TEMPLATEID**.</span></span> <span data-ttu-id="73c69-139">Identificateurs de modèle doivent être pris en charge pour les écritures dont le code doit être lié à des données dans un fournisseur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="73c69-139">Template identifiers should be supported for entries whose code must be bound to data in a host provider.</span></span>
  
<span data-ttu-id="73c69-140">Certains exemples de lorsqu’un fournisseur de carnet d’adresses doit implémenter **IABLogon::OpenTemplateID** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="73c69-140">Some examples of when an address book provider should implement **IABLogon::OpenTemplateID** are as follows:</span></span> 
  
- <span data-ttu-id="73c69-141">Pour mettre à jour régulièrement les données d’une entrée copiée afin qu’il reste synchronisé avec l’original.</span><span class="sxs-lookup"><span data-stu-id="73c69-141">To periodically update the data for a copied entry so that it stays synchronized with the original.</span></span>
    
- <span data-ttu-id="73c69-142">Pour implémenter les fonctionnalités que le fournisseur d’hébergement ne peut pas implémenter, telles que le remplissage dynamique d’une liste qui s’affiche dans la table des détails de l’entrée de données sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="73c69-142">To implement functionality that the host provider cannot implement, such as dynamically populating a list that appears in the entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="73c69-143">Pour contrôler l’interaction entre les propriétés de l’entrée du fournisseur d’hébergement et l’entrée d’origine, telles que l’informatique **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) à partir des valeurs des contrôles modifier dans l’affichage des détails qui contiennent des différentes composants de l’adresse.</span><span class="sxs-lookup"><span data-stu-id="73c69-143">To control the interaction between properties in the host provider's entry and the original entry, such as computing the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) from the values of the edit controls in the details display that contain different components of the address.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="73c69-144">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="73c69-144">Notes to implementers</span></span>

<span data-ttu-id="73c69-145">Lorsqu’un fournisseur d’hébergement copie ou crée une entrée de votre fournisseur et que vous fournissez une implémentation d’objet de propriété via **IABLogon::OpenTemplateID**, vous gérez la plupart des appels à mettre à jour de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="73c69-145">When a host provider copies or creates an entry from your provider and you supply a property object implementation through **IABLogon::OpenTemplateID**, you handle most of the calls to maintain the entry.</span></span> <span data-ttu-id="73c69-146">Toutefois, car il est le fournisseur d’hébergement pour transférer les appels vers vous, le fournisseur d’hébergement peut intercepter des appels et exécuter le traitement personnalisé avant de transférer l’appel.</span><span class="sxs-lookup"><span data-stu-id="73c69-146">However, because it is up to the host provider to forward these calls to you, the host provider can intercept any call and perform custom processing before forwarding the call.</span></span>
  
<span data-ttu-id="73c69-147">Vous devez utiliser les instructions suivantes votre propriété implémentations d’objets :</span><span class="sxs-lookup"><span data-stu-id="73c69-147">You should use the following guidelines in your property object implementations:</span></span>
  
- <span data-ttu-id="73c69-148">Lorsque [IMAPIProp::GetProps](imapiprop-getprops.md) est appelé, déterminez si la demande est une propriété calculée et, s’il s’agit, gérer.</span><span class="sxs-lookup"><span data-stu-id="73c69-148">When [IMAPIProp::GetProps](imapiprop-getprops.md) is called, determine whether the request is for a computed property and, if it is, handle it.</span></span> <span data-ttu-id="73c69-149">Transférer toutes les demandes pour les propriétés non calculées pour le fournisseur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="73c69-149">Transfer all requests for noncomputed properties to the host provider.</span></span> 
    
- <span data-ttu-id="73c69-150">Lorsque [IMAPIProp::OpenProperty](imapiprop-openproperty.md) est appelée pour ouvrir une table à l’exception des détails afficher le tableau, traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="73c69-150">When [IMAPIProp::OpenProperty](imapiprop-openproperty.md) is called to open any table except the details display table, handle the request.</span></span> <span data-ttu-id="73c69-151">La plupart des tables ne peut pas être copié avec précision pour le fournisseur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="73c69-151">Most tables cannot be copied accurately to the host provider.</span></span> <span data-ttu-id="73c69-152">Vous devez générer l’implémentation **IMAPITable** pour ces tables demandés.</span><span class="sxs-lookup"><span data-stu-id="73c69-152">You must generate the **IMAPITable** implementation for these requested tables.</span></span> <span data-ttu-id="73c69-153">La propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) du tableau Détails doit être copiée vers le fournisseur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="73c69-153">The details table **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property must be copied to the host provider.</span></span> <span data-ttu-id="73c69-154">Cela permet à ce fournisseur générer la table localement.</span><span class="sxs-lookup"><span data-stu-id="73c69-154">This allows this provider to generate the table locally.</span></span> <span data-ttu-id="73c69-155">Vous voudrez peut-être enveloppe l’implémentation de table complet pour générer des notifications d’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="73c69-155">You might want to wrap the display table implementation to generate display table notifications.</span></span> 
    
- <span data-ttu-id="73c69-156">Lorsque [IMAPIProp::SetProps](imapiprop-setprops.md) est appelé, le fournisseur d’hébergement peut valider les données avant de vous permettant de définir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="73c69-156">When [IMAPIProp::SetProps](imapiprop-setprops.md) is called, the host provider can validate the data before letting you set the properties.</span></span> <span data-ttu-id="73c69-157">Vous pouvez vérifier que toutes les propriétés nécessaires ont été définies ou calculées.</span><span class="sxs-lookup"><span data-stu-id="73c69-157">You can verify that all of the necessary properties were set or computed.</span></span> <span data-ttu-id="73c69-158">Si une erreur est détectée, retourne la valeur d’erreur approprié et, si possible, des explications supplémentaires par le biais de [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="73c69-158">If an error is detected, return the appropriate error value and, if you can, any additional explanation through [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span>
    
- <span data-ttu-id="73c69-159">Lorsque [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelé, le fournisseur d’hébergement souhaiterez peut-être effectuer un traitement avant d’enregistrer l’entrée.</span><span class="sxs-lookup"><span data-stu-id="73c69-159">When [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called, the host provider might want to perform processing before you save the entry.</span></span> <span data-ttu-id="73c69-160">Vous devez enregistrer toutes les données qui sont affectées par les propriétés modifiées, par exemple une nouvelle adresse, dans l’entrée du fournisseur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="73c69-160">You should save any data that is affected by the changed properties, such as a new address, in the host provider's entry.</span></span> 
    
<span data-ttu-id="73c69-161">En général, rendre votre implémentation de l’entrée que vous passez au fournisseur hôte intercepter toutes les méthodes pour manipuler des contextuelle des propriétés pertinentes.</span><span class="sxs-lookup"><span data-stu-id="73c69-161">In general, make your implementation of the entry that you pass back to the host provider intercept all of the methods to perform context-specific manipulation of the relevant properties.</span></span> <span data-ttu-id="73c69-162">Si l’indicateur FILL_ENTRY est passé dans le paramètre _ulTemplateFlags_ , définissez toutes les propriétés de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="73c69-162">If the FILL_ENTRY flag is passed in the  _ulTemplateFlags_ parameter, set all properties for the entry.</span></span> 
  
<span data-ttu-id="73c69-163">Si vous renvoyez un nouvel objet property dans le paramètre _lppMAPIPropNew_ , appeler la méthode [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) d’objet de propriété du fournisseur d’hébergement de maintenir une référence.</span><span class="sxs-lookup"><span data-stu-id="73c69-163">If you return a new property object in the  _lppMAPIPropNew_ parameter, call the [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method of the host provider's property object to maintain a reference.</span></span> <span data-ttu-id="73c69-164">Une fois qu’ils sont traités par l’objet lié, tous les appels par le biais de l’objet lié l’implémentation **IMAPIProp** renvoyée dans _lppMAPIPropNew_ doivent être acheminés vers leur méthode correspondante dans l’objet de la propriété hôte.</span><span class="sxs-lookup"><span data-stu-id="73c69-164">All calls through the bound object that the **IMAPIProp** implementation returned in  _lppMAPIPropNew_ should be routed to their corresponding method in the host property object after they are dealt with by the bound object.</span></span> 
  
<span data-ttu-id="73c69-165">Les identificateurs de propriété de toute propriété nommée qui est transmise par le biais de l’objet de la propriété liée se trouvent dans l’espace de noms de votre fournisseur identificateur.</span><span class="sxs-lookup"><span data-stu-id="73c69-165">The property identifiers of any named properties that are passed through your bound property object are in your provider's identifier namespace.</span></span> <span data-ttu-id="73c69-166">Votre implémentation de la méthode [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) doit déterminer les noms des propriétés afin qu’elle puisse exécuter des tâches spécifiques d’un modèle.</span><span class="sxs-lookup"><span data-stu-id="73c69-166">Your implementation of the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method should determine the names of the properties so that it can perform any template-specific tasks.</span></span> <span data-ttu-id="73c69-167">De même, les propriétés votre fournisseur transmet au fournisseur hôte doivent également être dans votre espace de noms.</span><span class="sxs-lookup"><span data-stu-id="73c69-167">Similarly, properties that your provider passes on to the host provider must also be in your namespace.</span></span> <span data-ttu-id="73c69-168">Par exemple, si vous définissez une propriété nommée dans **OpenTemplateID**, vous devez utiliser un des identificateurs de votre pour le nom — sa création, le cas échéant, en appelant la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="73c69-168">For example, if you set a named property in **OpenTemplateID**, you should use one of your identifiers for the name—creating it, if necessary, by calling the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="73c69-169">Si vous ne connaissez pas l’identificateur d’entrée passé _lpTemplateID_, retourne MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="73c69-169">If you do not recognize the entry identifier passed in  _lpTemplateID_, return MAPI_E_UNKNOWN_ENTRYID.</span></span>
  
<span data-ttu-id="73c69-170">Pour plus d’informations sur l’utilisation des identificateurs de modèle carnet d’adresse, voir [agissant comme un fournisseur de carnet d’adresses étrangère](acting-as-a-foreign-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="73c69-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="73c69-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73c69-171">See also</span></span>



[<span data-ttu-id="73c69-172">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="73c69-172">IMAPISupport::OpenTemplateID</span></span>](imapisupport-opentemplateid.md)
  
[<span data-ttu-id="73c69-173">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="73c69-173">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="73c69-174">Propriété canonique PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="73c69-174">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="73c69-175">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="73c69-175">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

