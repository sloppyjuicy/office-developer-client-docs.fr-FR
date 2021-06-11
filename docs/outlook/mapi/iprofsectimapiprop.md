---
title: IProfSect IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfSect
api_type:
- COM
ms.assetid: 4e704044-5230-4521-a0d2-b7c2f981c954
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 99ce944bec94a1e832f77fa8b0916ac1c76f6dc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406597"
---
# <a name="iprofsect--imapiprop"></a><span data-ttu-id="8058f-103">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8058f-103">IProfSect : IMAPIProp</span></span>

  
  
<span data-ttu-id="8058f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8058f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8058f-105">Fonctionne avec les propriétés des objets de section de profil.</span><span class="sxs-lookup"><span data-stu-id="8058f-105">Works with the properties of profile section objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8058f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8058f-106">Header file:</span></span>  <br/> |<span data-ttu-id="8058f-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="8058f-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="8058f-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="8058f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8058f-109">Objets de section de profil</span><span class="sxs-lookup"><span data-stu-id="8058f-109">Profile section objects</span></span>  <br/> |
|<span data-ttu-id="8058f-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="8058f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8058f-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="8058f-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="8058f-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="8058f-112">Called by:</span></span>  <br/> |<span data-ttu-id="8058f-113">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="8058f-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="8058f-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="8058f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8058f-115">IID_IProfSect</span><span class="sxs-lookup"><span data-stu-id="8058f-115">IID_IProfSect</span></span>  <br/> |
|<span data-ttu-id="8058f-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="8058f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="8058f-117">LPPROFSECT</span><span class="sxs-lookup"><span data-stu-id="8058f-117">LPPROFSECT</span></span>  <br/> |
|<span data-ttu-id="8058f-118">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="8058f-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="8058f-119">Non traduit</span><span class="sxs-lookup"><span data-stu-id="8058f-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8058f-120">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="8058f-120">Vtable order</span></span>

<span data-ttu-id="8058f-121">Cette interface n’a pas de méthode unique.</span><span class="sxs-lookup"><span data-stu-id="8058f-121">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="8058f-122">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="8058f-122">**Required properties**</span></span>|<span data-ttu-id="8058f-123">**Access**</span><span class="sxs-lookup"><span data-stu-id="8058f-123">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8058f-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8058f-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8058f-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8058f-125">Read-only</span></span>  <br/> |
|<span data-ttu-id="8058f-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8058f-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8058f-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8058f-127">Read-only</span></span>  <br/> |
   
## <a name="notes-to-callers"></a><span data-ttu-id="8058f-128">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="8058f-128">Notes to callers</span></span>

<span data-ttu-id="8058f-129">**L’interface IProfSect** ne possède aucune méthode unique, mais vous pouvez appeler les méthodes [IMAPIProp](imapipropiunknown.md) de la section de profil.</span><span class="sxs-lookup"><span data-stu-id="8058f-129">The **IProfSect** interface does not have any unique methods of its own, but you can call the profile section's [IMAPIProp](imapipropiunknown.md) methods.</span></span> <span data-ttu-id="8058f-130">Il existe certaines différences entre l’implémentation **IProfSect** et d’autres implémentations **d’IMAPIProp**:</span><span class="sxs-lookup"><span data-stu-id="8058f-130">There are some differences between the **IProfSect** implementation and other implementations of **IMAPIProp**:</span></span>
  
- <span data-ttu-id="8058f-131">**IProfSect ne** prend pas en charge un modèle de transaction.</span><span class="sxs-lookup"><span data-stu-id="8058f-131">**IProfSect** does not support a transaction model.</span></span> 
    
- <span data-ttu-id="8058f-132">**IProfSect ne** prend pas en charge les propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="8058f-132">**IProfSect** does not support named properties.</span></span> 
    
- <span data-ttu-id="8058f-133">**IProfSect** réserve la plage d’identificateurs 0x67F0 à 0x67ff pour les propriétés sécurisées.</span><span class="sxs-lookup"><span data-stu-id="8058f-133">**IProfSect** reserves the identifier range 0x67F0 to 0x67ff for secure properties.</span></span> 
    
<span data-ttu-id="8058f-134">La non-prise en charge d’un modèle de transaction signifie que toutes les modifications apportées à une section de profil à la suite d’appels aux méthodes [IMAPIProp::CopyProps](imapiprop-copyprops.md) et [IMAPIProp::CopyTo](imapiprop-copyto.md) se produisent immédiatement.</span><span class="sxs-lookup"><span data-stu-id="8058f-134">Not supporting a transaction model means that all changes that were made to a profile section following calls to the [IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md) methods occur immediately.</span></span> <span data-ttu-id="8058f-135">Les appels à [la méthode IMAPIProp::SaveChanges](imapiprop-savechanges.md) réussissent, mais n’enregistrent pas réellement les modifications.</span><span class="sxs-lookup"><span data-stu-id="8058f-135">Calls to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method succeed but do not actually save any changes.</span></span> 
  
<span data-ttu-id="8058f-136">Pour être protégés contre les modifications qui se produisent prématurément, les fournisseurs de services doivent effectuer des copies de leurs sections de profil qui sont affichées aux utilisateurs par le biais de feuilles de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8058f-136">To be protected from changes that occur prematurely, service providers need to make copies of their profile sections that are displayed to users through property sheets.</span></span> <span data-ttu-id="8058f-137">Les feuilles de propriétés doivent fonctionner avec la copie, au lieu de la section de profil réelle.</span><span class="sxs-lookup"><span data-stu-id="8058f-137">The property sheets should work with the copy, instead of the real profile section.</span></span> <span data-ttu-id="8058f-138">Lorsque l’utilisateur clique sur le bouton **OK** pour vérifier que les modifications sont exactes, les modifications peuvent être enregistrées dans la section profil réel.</span><span class="sxs-lookup"><span data-stu-id="8058f-138">When the user clicks the **OK** button to verify that the changes are accurate, the changes can be saved to the real profile section.</span></span> 
  
<span data-ttu-id="8058f-139">Pour implémenter une feuille de propriétés à l’aide d’une section de profil copiée, utilisez la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="8058f-139">To implement a property sheet by using a copied profile section, use the following procedure:</span></span>
  
1. <span data-ttu-id="8058f-140">Ouvrez la section profil en appelant la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) ou [IProviderAdmin::OpenProfileSection.](iprovideradmin-openprofilesection.md)</span><span class="sxs-lookup"><span data-stu-id="8058f-140">Open the profile section by calling the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> 
    
2. <span data-ttu-id="8058f-141">Appelez la [fonction CreateIProp](createiprop.md) pour récupérer un objet de données de propriété , un objet qui prend en charge l’interface **IPropData.**</span><span class="sxs-lookup"><span data-stu-id="8058f-141">Call the [CreateIProp](createiprop.md) function to retrieve a property data object — an object that supports the **IPropData** interface.</span></span> 
    
3. <span data-ttu-id="8058f-142">Appelez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) de la section de profil pour copier les propriétés qui apparaîtront dans la feuille des propriétés de la section profil vers l’objet de données de propriété.</span><span class="sxs-lookup"><span data-stu-id="8058f-142">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties that will appear on the property sheet from the profile section to the property data object.</span></span> 
    
4. <span data-ttu-id="8058f-143">Appelez la méthode [IMAPISupport::D oConfigPropSheet](imapisupport-doconfigpropsheet.md) pour demander au fournisseur de services d’afficher une feuille de propriétés et passez un pointeur vers l’objet de données de propriété dans le paramètre _lpConfigData._</span><span class="sxs-lookup"><span data-stu-id="8058f-143">Call the [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) method to request that the service provider display a property sheet, and pass a pointer to the property data object in the  _lpConfigData_ parameter.</span></span> 
    
5. <span data-ttu-id="8058f-144">Lorsque l’utilisateur enregistre les modifications apportées aux propriétés de configuration dans la feuille des propriétés, appelez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) pour copier les propriétés de l’objet de données de propriété dans la section de profil.</span><span class="sxs-lookup"><span data-stu-id="8058f-144">When the user saves changes to configuration properties in the property sheet, call the [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties from the property data object back to the profile section.</span></span> 
    
<span data-ttu-id="8058f-145">Les sections de profil, contrairement aux autres objets, ne sont pas en charge les propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="8058f-145">Profile sections, unlike other objects, do not support named properties.</span></span> <span data-ttu-id="8058f-146">Les méthodes [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) retournent MAPI_E_NO_SUPPORT si elles sont appelées sur un objet de section de profil.</span><span class="sxs-lookup"><span data-stu-id="8058f-146">The [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) methods return MAPI_E_NO_SUPPORT if they are called on a profile section object.</span></span> <span data-ttu-id="8058f-147">Si vous utilisez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour définir les identificateurs de propriété dans la plage ci-dessus 0x8000, le type de propriété PT_ERROR est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="8058f-147">If you use the [IMAPIProp::SetProps](imapiprop-setprops.md) method to set property identifiers in the range above 0x8000, the PT_ERROR property type will be returned.</span></span> 
  
<span data-ttu-id="8058f-148">Les sections de profil réservent la plage d'0x67F0 à 0x67FF pour les propriétés sécurisées.</span><span class="sxs-lookup"><span data-stu-id="8058f-148">Profile sections reserve the identifier range 0x67F0 to 0x67FF for secure properties.</span></span> <span data-ttu-id="8058f-149">Les fournisseurs de services peuvent utiliser cette plage pour stocker des mots de passe et d’autres informations d’identification spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8058f-149">Service providers can use this range to store passwords and other provider-specific credentials.</span></span> <span data-ttu-id="8058f-150">Les propriétés de cette plage ne sont pas renvoyées dans la liste complète des propriétés lorsque NULL est transmis dans le paramètre _lpPropTag_ de la méthode [IMAPIProp::GetProps,](imapiprop-getprops.md) ni dans le paramètre _lppPropTagArray_ de la méthode [IMAPIProp::GetPropList.](imapiprop-getproplist.md)</span><span class="sxs-lookup"><span data-stu-id="8058f-150">Properties in this range are not returned in the complete list of properties when NULL is passed in the  _lpPropTag_ parameter of the [IMAPIProp::GetProps](imapiprop-getprops.md) method, nor are they returned in the  _lppPropTagArray_ parameter of the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> <span data-ttu-id="8058f-151">Les propriétés sécurisées doivent être demandées spécifiquement par leurs identificateurs.</span><span class="sxs-lookup"><span data-stu-id="8058f-151">Secure properties must be requested specifically by their identifiers.</span></span> 
  
<span data-ttu-id="8058f-152">MAPI fournit une section de profil avec la constante codée en dur MUID_PROFILE_INSTANCE comme identificateur et PR_SEARCH_KEY **(** [PidTagSearchKey](pidtagsearchkey-canonical-property.md)) comme propriété unique.</span><span class="sxs-lookup"><span data-stu-id="8058f-152">MAPI furnishes a profile section with the hard-coded constant MUID_PROFILE_INSTANCE as its identifier and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) as its single property.</span></span> <span data-ttu-id="8058f-153">MAPI garantit que la **valeur PR_SEARCH_KEY** propriété sera unique parmi tous les profils créés.</span><span class="sxs-lookup"><span data-stu-id="8058f-153">MAPI ensures that the **PR_SEARCH_KEY** property value will be unique among all created profiles.</span></span> <span data-ttu-id="8058f-154">Utilisez **PR_SEARCH_KEY** au lieu  de PR_PROFILE_NAME lorsque l’unicité est importante, car il est possible qu’un profil supprimé soit suivi d’un autre profil du même nom.</span><span class="sxs-lookup"><span data-stu-id="8058f-154">Use **PR_SEARCH_KEY** instead of **PR_PROFILE_NAME** when uniqueness is important, because it is possible for a deleted profile to be followed by another profile with the same name.</span></span> 
  
<span data-ttu-id="8058f-155">Pour plus d’informations sur l’utilisation des sections de profil, voir [Administering Profiles and Message Services](administering-profiles-and-message-services.md).</span><span class="sxs-lookup"><span data-stu-id="8058f-155">For more information about how to use profile sections, see [Administering Profiles and Message Services](administering-profiles-and-message-services.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8058f-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8058f-156">See also</span></span>



[<span data-ttu-id="8058f-157">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="8058f-157">MAPI Interfaces</span></span>](mapi-interfaces.md)

