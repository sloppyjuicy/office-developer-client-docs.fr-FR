---
title: IMAPIPropGetIDsFromNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 28880b818bc80e31cae0c695d4aac92eb9555cac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314839"
---
# <a name="imapipropgetidsfromnames"></a><span data-ttu-id="79d27-103">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="79d27-103">IMAPIProp::GetIDsFromNames</span></span>

  
  
<span data-ttu-id="79d27-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79d27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79d27-105">Fournit les identificateurs de propriété qui correspondent à un ou plusieurs noms de propriétés.</span><span class="sxs-lookup"><span data-stu-id="79d27-105">Provides the property identifiers that correspond to one or more property names.</span></span>
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a><span data-ttu-id="79d27-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79d27-106">Parameters</span></span>

 <span data-ttu-id="79d27-107">_cPropNames_</span><span class="sxs-lookup"><span data-stu-id="79d27-107">_cPropNames_</span></span>
  
> <span data-ttu-id="79d27-108">dans Nombre de noms de propriétés vers lesquels pointe le paramètre _lppPropNames_ .</span><span class="sxs-lookup"><span data-stu-id="79d27-108">[in] The count of property names pointed to by the  _lppPropNames_ parameter.</span></span> <span data-ttu-id="79d27-109">Si _lppPropNames_ a la valeur null, le paramètre _cPropNames_ doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="79d27-109">If  _lppPropNames_ is NULL, the  _cPropNames_ parameter must be 0.</span></span> 
    
 <span data-ttu-id="79d27-110">_lppPropNames_</span><span class="sxs-lookup"><span data-stu-id="79d27-110">_lppPropNames_</span></span>
  
> <span data-ttu-id="79d27-111">dans Pointeur vers un tableau de noms de propriétés, ou NULL.</span><span class="sxs-lookup"><span data-stu-id="79d27-111">[in] A pointer to an array of property names, or NULL.</span></span> <span data-ttu-id="79d27-112">Transmission des identificateurs de propriété de tous les noms de propriétés de tous les jeux de propriétés dont l'objet dispose d'informations.</span><span class="sxs-lookup"><span data-stu-id="79d27-112">Passing NULL requests property identifiers for all property names in all property sets about which the object has information.</span></span> <span data-ttu-id="79d27-113">Le paramètre _lppPropNames_ ne doit pas être null si l'indicateur MAPI_CREATE est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="79d27-113">The  _lppPropNames_ parameter must not be NULL if the MAPI_CREATE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="79d27-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="79d27-114">_ulFlags_</span></span>
  
> <span data-ttu-id="79d27-115">dans Masque de des indicateurs qui indique comment les identificateurs de propriété doivent être retournés.</span><span class="sxs-lookup"><span data-stu-id="79d27-115">[in] A bitmask of flags that indicates how the property identifiers should be returned.</span></span> <span data-ttu-id="79d27-116">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="79d27-116">The following flag can be set:</span></span>
    
<span data-ttu-id="79d27-117">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="79d27-117">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="79d27-118">Affecte un identificateur de propriété, s'il n'a pas encore été assigné, à un ou plusieurs des noms inclus dans le tableau de noms de propriétés pointé par _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="79d27-118">Assigns a property identifier, if one has not yet been assigned, to one or more of the names included in the property name array pointed to by  _lppPropNames_.</span></span> <span data-ttu-id="79d27-119">Cet indicateur inscrit en interne l'identificateur dans la table de mappage name-to-identifier.</span><span class="sxs-lookup"><span data-stu-id="79d27-119">This flag internally registers the identifier in the name-to-identifier mapping table.</span></span>
    
 <span data-ttu-id="79d27-120">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="79d27-120">_lppPropTags_</span></span>
  
> <span data-ttu-id="79d27-121">remarquer Pointeur vers un pointeur vers un tableau de balises de propriété qui contient des identificateurs de propriété existants ou nouvellement attribués.</span><span class="sxs-lookup"><span data-stu-id="79d27-121">[out] A pointer to a pointer to an array of property tags that contains existing or newly assigned property identifiers.</span></span> <span data-ttu-id="79d27-122">Les types de propriétés des balises de propriété dans ce tableau sont définis sur **PT_UNSPECIFIED**.</span><span class="sxs-lookup"><span data-stu-id="79d27-122">The property types for the property tags in this array are set to **PT_UNSPECIFIED**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="79d27-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="79d27-123">Return value</span></span>

<span data-ttu-id="79d27-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="79d27-124">S_OK</span></span> 
  
> <span data-ttu-id="79d27-125">Les identificateurs des noms de propriétés spécifiés ont été correctement renvoyés.</span><span class="sxs-lookup"><span data-stu-id="79d27-125">The identifiers for the specified property names were successfully returned.</span></span>
    
<span data-ttu-id="79d27-126">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="79d27-126">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="79d27-127">L'objet ne prend pas en charge les propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="79d27-127">The object does not support named properties.</span></span>
    
<span data-ttu-id="79d27-128">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="79d27-128">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="79d27-129">Mémoire inSuffisante pour récupérer les identificateurs.</span><span class="sxs-lookup"><span data-stu-id="79d27-129">Insufficient memory was available to retrieve the identifiers.</span></span>
    
<span data-ttu-id="79d27-130">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="79d27-130">MAPI_E_TOO_BIG</span></span> 
  
> <span data-ttu-id="79d27-131">L'opération ne peut pas être effectuée, car elle nécessite le renvoi d'un trop grand nombre de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="79d27-131">The operation cannot be performed because it requires too many property tags to be returned.</span></span>
    
<span data-ttu-id="79d27-132">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="79d27-132">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="79d27-133">L'appel a réussi globalement, mais un ou plusieurs identificateurs de propriété n'ont pas pu être renvoyés.</span><span class="sxs-lookup"><span data-stu-id="79d27-133">The call succeeded overall, but one or more property identifiers could not be returned.</span></span> <span data-ttu-id="79d27-134">Le type de propriété correspondant à chaque propriété indisponible est défini sur **PT_ERROR** et son identificateur sur zéro.</span><span class="sxs-lookup"><span data-stu-id="79d27-134">The corresponding property type for each unavailable property is set to **PT_ERROR** and its identifier to zero.</span></span> <span data-ttu-id="79d27-135">Lorsque cet avertissement est renvoyé, gérez l'appel comme réussi.</span><span class="sxs-lookup"><span data-stu-id="79d27-135">When this warning is returned, handle the call as successful.</span></span> <span data-ttu-id="79d27-136">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="79d27-136">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="79d27-137">Consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="79d27-137">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="79d27-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="79d27-138">Remarks</span></span>

<span data-ttu-id="79d27-139">La méthode **IMAPIProp:: GetIDsFromNames** extrait un tableau de balises de propriété qui contiennent les identificateurs de propriété pour une ou plusieurs propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="79d27-139">The **IMAPIProp::GetIDsFromNames** method retrieves an array of property tags that hold the property identifiers for one or more named properties.</span></span> <span data-ttu-id="79d27-140">**IMAPIProp:: GetIDsFromNames** peut être appelé pour effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="79d27-140">**IMAPIProp::GetIDsFromNames** can be called to do the following:</span></span> 
  
- <span data-ttu-id="79d27-141">Créez des identificateurs pour les nouveaux noms.</span><span class="sxs-lookup"><span data-stu-id="79d27-141">Create identifiers for new names.</span></span>
    
- <span data-ttu-id="79d27-142">Récupérez des identificateurs pour des noms spécifiques.</span><span class="sxs-lookup"><span data-stu-id="79d27-142">Retrieve identifiers for specific names.</span></span>
    
- <span data-ttu-id="79d27-143">Récupérez les identificateurs de toutes les propriétés nommées incluses dans le mappage de l'objet.</span><span class="sxs-lookup"><span data-stu-id="79d27-143">Retrieve identifiers for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="79d27-144">Les propriétés nommées sont généralement utilisées par les fournisseurs de banques de messages pour les dossiers et les messages.</span><span class="sxs-lookup"><span data-stu-id="79d27-144">Named properties are typically used by message store providers for folders and messages.</span></span> <span data-ttu-id="79d27-145">D'autres objets, tels que les utilisateurs de messagerie et les sections de profil, peuvent ne pas prendre en charge l'Association de noms à des identificateurs de propriétés et renvoyer MAPI_E_NO_SUPPORT à partir de **GetIDsFromNames**.</span><span class="sxs-lookup"><span data-stu-id="79d27-145">Other objects, such as messaging users and profile sections, might not support the association of names to property identifiers and might return MAPI_E_NO_SUPPORT from **GetIDsFromNames**.</span></span>
  
<span data-ttu-id="79d27-146">Si une erreur renvoie un identificateur pour un nom particulier, **GetIDsFromNames** renvoie MAPI_W_ERRORS_RETURNED et définit le type de propriété dans l'entrée de tableau de la balise de propriété correspondant au nom de **PT_ERROR** et l'identificateur à zéro.</span><span class="sxs-lookup"><span data-stu-id="79d27-146">If there is an error that returns an identifier for a particular name, **GetIDsFromNames** returns MAPI_W_ERRORS_RETURNED and sets the property type in the property tag array entry that corresponds to the name to **PT_ERROR** and the identifier to zero.</span></span> 
  
<span data-ttu-id="79d27-147">Le mappage nom-identificateur est représenté par la propriété **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) d'un objet.</span><span class="sxs-lookup"><span data-stu-id="79d27-147">Name-to-identifier mapping is represented by an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="79d27-148">**PR_MAPPING_SIGNATURE** contient une structure [MAPIUID](mapiuid.md) qui indique le fournisseur de services responsable de l'objet.</span><span class="sxs-lookup"><span data-stu-id="79d27-148">**PR_MAPPING_SIGNATURE** contains a [MAPIUID](mapiuid.md) structure that indicates the service provider responsible for the object.</span></span> <span data-ttu-id="79d27-149">Si la propriété **PR_MAPPING_SIGNATURE** est identique pour deux objets, partez du principe que ces objets utilisent le même mappage de nom-à-identificateur.</span><span class="sxs-lookup"><span data-stu-id="79d27-149">If the **PR_MAPPING_SIGNATURE** property is the same for two objects, assume that these objects use the same name-to-identifier mapping.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="79d27-150">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="79d27-150">Notes to implementers</span></span>

<span data-ttu-id="79d27-151">Les identificateurs que vous transférez dans le tableau de balises de propriété vers lequel pointe le paramètre _lppPropNames_ doivent être compris dans la plage 0X8000 to 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="79d27-151">The identifiers that you pass back in the property tag array pointed to by the  _lppPropNames_ parameter must be in the 0x8000 to 0xFFFE range.</span></span> <span data-ttu-id="79d27-152">Les entrées de ce tableau doivent être dans le même ordre que les noms transmis dans le tableau des noms de propriétés pointé par _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="79d27-152">The entries in this array must be in the same order as the names passed in the property name array pointed to by  _lppPropNames_.</span></span> 
  
<span data-ttu-id="79d27-153">Si vous prenez en charge les propriétés nommées sur un conteneur, utilisez le même mappage de nom à identificateur pour tous les objets de votre conteneur (autrement dit, n'utilisez pas un mappage différent pour chaque dossier de votre banque de messages ou chaque message de votre dossier).</span><span class="sxs-lookup"><span data-stu-id="79d27-153">If you support named properties on a container, use the same name-to-identifier mapping for all objects in your container (that is, do not use a different mapping for each folder in your message store or each message in your folder).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="79d27-154">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="79d27-154">Notes to callers</span></span>

<span data-ttu-id="79d27-155">Étant donné que les types de propriétés des identificateurs renvoyés dans le tableau de balises de propriété vers lequel pointe _lppPropTags_ sont définis sur **PT_UNSPECIFIED**, vous devrez appeler la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) pour récupérer les types précis.</span><span class="sxs-lookup"><span data-stu-id="79d27-155">Because the property types for the returned identifiers in the property tag array pointed to by  _lppPropTags_ are set to **PT_UNSPECIFIED**, you will have to call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to retrieve the accurate types.</span></span> 
  
<span data-ttu-id="79d27-156">Si vous déplacez ou copiez des objets avec des propriétés nommées et que les objets source et de destination ont des signatures de mappage différentes comme indiqué par les valeurs de leurs propriétés **PR_MAPPING_SIGNATURE** , vous devez conserver les noms lors de ces opérations.</span><span class="sxs-lookup"><span data-stu-id="79d27-156">If you move or copy objects with named properties, and the source and destination objects have different mapping signatures as indicated by the values of their **PR_MAPPING_SIGNATURE** properties, you must preserve the names during these operations.</span></span> <span data-ttu-id="79d27-157">Pour conserver les noms de propriété, ajustez les identificateurs de propriétés correspondants pour qu'ils correspondent au mappage nom-identificateur de l'objet de destination.</span><span class="sxs-lookup"><span data-stu-id="79d27-157">To preserve property names, adjust the corresponding property identifiers to match the name-to-identifier mapping of the destination object.</span></span> 
  
<span data-ttu-id="79d27-158">Certains objets ont une limite pour le nombre d'identificateurs de propriétés qu'ils peuvent nommer.</span><span class="sxs-lookup"><span data-stu-id="79d27-158">Some objects have a limit as to the number of property identifiers they can name.</span></span> <span data-ttu-id="79d27-159">Si un appel à **GetIDsFromNames** entraîne le dépassement de cette limite, la méthode renvoie MAPI_E_TOO_BIG.</span><span class="sxs-lookup"><span data-stu-id="79d27-159">If a call to **GetIDsFromNames** causes this limit to be exceeded, the method returns MAPI_E_TOO_BIG.</span></span> <span data-ttu-id="79d27-160">Dans ce cas, interrogez l'identificateur.</span><span class="sxs-lookup"><span data-stu-id="79d27-160">In this case, query by identifier.</span></span> 
  
<span data-ttu-id="79d27-161">Pour plus d'informations, consultez la rubrique [MAPI named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="79d27-161">For more information, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="79d27-162">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="79d27-162">MFCMAPI reference</span></span>

<span data-ttu-id="79d27-163">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="79d27-163">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="79d27-164">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="79d27-164">**File**</span></span>|<span data-ttu-id="79d27-165">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="79d27-165">**Function**</span></span>|<span data-ttu-id="79d27-166">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="79d27-166">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="79d27-167">SingleMAPIPropListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="79d27-167">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="79d27-168">CSingleMAPIPropListCtrl:: FindAllNamedPropsUsed</span><span class="sxs-lookup"><span data-stu-id="79d27-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span></span>  <br/> |<span data-ttu-id="79d27-169">MFCMAPI utilise la méthode **IMAPIProp:: GetIDsFromNames** pour obtenir les balises de propriété pour toutes les propriétés nommées qui ont été mappées.</span><span class="sxs-lookup"><span data-stu-id="79d27-169">MFCMAPI uses the **IMAPIProp::GetIDsFromNames** method to obtain property tags for all named properties that have been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="79d27-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79d27-170">See also</span></span>



[<span data-ttu-id="79d27-171">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="79d27-171">IMAPIProp::GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md)
  
[<span data-ttu-id="79d27-172">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="79d27-172">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="79d27-173">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="79d27-173">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="79d27-174">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="79d27-174">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="79d27-175">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="79d27-175">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="79d27-176">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="79d27-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="79d27-177">MAPI des propri�t�s nomm�e</span><span class="sxs-lookup"><span data-stu-id="79d27-177">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="79d27-178">Utilisation de macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="79d27-178">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

