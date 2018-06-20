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
ms.openlocfilehash: 5247ca71c88b9c0f8591a732746a17204265741c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783906"
---
# <a name="imapipropgetidsfromnames"></a><span data-ttu-id="8bf35-103">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="8bf35-103">IMAPIProp::GetIDsFromNames</span></span>

  
  
<span data-ttu-id="8bf35-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8bf35-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8bf35-105">Fournit les identificateurs de propriété qui correspondent à un ou plusieurs noms de propriété.</span><span class="sxs-lookup"><span data-stu-id="8bf35-105">Provides the property identifiers that correspond to one or more property names.</span></span>
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a><span data-ttu-id="8bf35-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bf35-106">Parameters</span></span>

 <span data-ttu-id="8bf35-107">_cPropNames_</span><span class="sxs-lookup"><span data-stu-id="8bf35-107">_cPropNames_</span></span>
  
> <span data-ttu-id="8bf35-108">[in] Le nombre de noms de propriété indiqué par le paramètre _lppPropNames_ .</span><span class="sxs-lookup"><span data-stu-id="8bf35-108">[in] The count of property names pointed to by the  _lppPropNames_ parameter.</span></span> <span data-ttu-id="8bf35-109">Si _lppPropNames_ est NULL, le paramètre _cPropNames_ doit être 0.</span><span class="sxs-lookup"><span data-stu-id="8bf35-109">If  _lppPropNames_ is NULL, the  _cPropNames_ parameter must be 0.</span></span> 
    
 <span data-ttu-id="8bf35-110">_lppPropNames_</span><span class="sxs-lookup"><span data-stu-id="8bf35-110">_lppPropNames_</span></span>
  
> <span data-ttu-id="8bf35-111">[in] Pointeur vers un tableau de noms de propriété, ou NULL.</span><span class="sxs-lookup"><span data-stu-id="8bf35-111">[in] A pointer to an array of property names, or NULL.</span></span> <span data-ttu-id="8bf35-112">Transmission NULL demande des identificateurs de propriété pour tous les noms de propriété dans tous les jeux de propriétés sur laquelle l’objet comporte des informations.</span><span class="sxs-lookup"><span data-stu-id="8bf35-112">Passing NULL requests property identifiers for all property names in all property sets about which the object has information.</span></span> <span data-ttu-id="8bf35-113">Le paramètre _lppPropNames_ ne doit pas être NULL si l’indicateur MAPI_CREATE est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="8bf35-113">The  _lppPropNames_ parameter must not be NULL if the MAPI_CREATE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="8bf35-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8bf35-114">_ulFlags_</span></span>
  
> <span data-ttu-id="8bf35-115">[in] Masque de bits d’indicateurs qui indique la façon dont les identificateurs de propriété doivent être retournés.</span><span class="sxs-lookup"><span data-stu-id="8bf35-115">[in] A bitmask of flags that indicates how the property identifiers should be returned.</span></span> <span data-ttu-id="8bf35-116">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="8bf35-116">The following flag can be set:</span></span>
    
<span data-ttu-id="8bf35-117">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="8bf35-117">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="8bf35-118">Affecte un identificateur de propriété, si une n’a encore été attribuée, à un ou plusieurs noms inclus dans le tableau de noms de propriété désigné par _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="8bf35-118">Assigns a property identifier, if one has not yet been assigned, to one or more of the names included in the property name array pointed to by  _lppPropNames_.</span></span> <span data-ttu-id="8bf35-119">Cet indicateur enregistre en interne l’identificateur dans la table de mappage de nom-à-identificateur.</span><span class="sxs-lookup"><span data-stu-id="8bf35-119">This flag internally registers the identifier in the name-to-identifier mapping table.</span></span>
    
 <span data-ttu-id="8bf35-120">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="8bf35-120">_lppPropTags_</span></span>
  
> <span data-ttu-id="8bf35-121">[out] Pointeur vers un pointeur vers un tableau de balises de propriété qui contient les identificateurs de propriété existant ou nouvellement affecté.</span><span class="sxs-lookup"><span data-stu-id="8bf35-121">[out] A pointer to a pointer to an array of property tags that contains existing or newly assigned property identifiers.</span></span> <span data-ttu-id="8bf35-122">Les types de propriétés pour les balises de propriété dans ce tableau sont définis sur **PT_UNSPECIFIED**.</span><span class="sxs-lookup"><span data-stu-id="8bf35-122">The property types for the property tags in this array are set to **PT_UNSPECIFIED**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8bf35-123">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8bf35-123">Return value</span></span>

<span data-ttu-id="8bf35-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="8bf35-124">S_OK</span></span> 
  
> <span data-ttu-id="8bf35-125">Les identificateurs des noms de propriétés spécifié a été correctement retournés.</span><span class="sxs-lookup"><span data-stu-id="8bf35-125">The identifiers for the specified property names were successfully returned.</span></span>
    
<span data-ttu-id="8bf35-126">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8bf35-126">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8bf35-127">L’objet ne gère pas les propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="8bf35-127">The object does not support named properties.</span></span>
    
<span data-ttu-id="8bf35-128">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="8bf35-128">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="8bf35-129">Mémoire insuffisante n’était disponible pour récupérer les identificateurs.</span><span class="sxs-lookup"><span data-stu-id="8bf35-129">Insufficient memory was available to retrieve the identifiers.</span></span>
    
<span data-ttu-id="8bf35-130">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="8bf35-130">MAPI_E_TOO_BIG</span></span> 
  
> <span data-ttu-id="8bf35-131">Impossible d’effectuer l’opération car elle requiert trop de balises de propriété à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="8bf35-131">The operation cannot be performed because it requires too many property tags to be returned.</span></span>
    
<span data-ttu-id="8bf35-132">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="8bf35-132">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="8bf35-133">L’appel a réussi, mais un ou plusieurs identificateurs de propriété n’a pas peuvent être retournés.</span><span class="sxs-lookup"><span data-stu-id="8bf35-133">The call succeeded overall, but one or more property identifiers could not be returned.</span></span> <span data-ttu-id="8bf35-134">Le type de propriété correspondante pour chaque propriété non disponible est égale à **PT_ERROR** et son identificateur à zéro.</span><span class="sxs-lookup"><span data-stu-id="8bf35-134">The corresponding property type for each unavailable property is set to **PT_ERROR** and its identifier to zero.</span></span> <span data-ttu-id="8bf35-135">Lorsque cet avertissement est renvoyé, gérer l’appel comme réussie.</span><span class="sxs-lookup"><span data-stu-id="8bf35-135">When this warning is returned, handle the call as successful.</span></span> <span data-ttu-id="8bf35-136">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="8bf35-136">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="8bf35-137">Consultez [utilisation de Macros pour la gestion des erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="8bf35-137">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8bf35-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="8bf35-138">Remarks</span></span>

<span data-ttu-id="8bf35-139">La méthode **IMAPIProp::GetIDsFromNames** récupère un tableau de balises de propriété qui contiennent les identificateurs de propriété pour un ou plusieurs des propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="8bf35-139">The **IMAPIProp::GetIDsFromNames** method retrieves an array of property tags that hold the property identifiers for one or more named properties.</span></span> <span data-ttu-id="8bf35-140">**IMAPIProp::GetIDsFromNames** peut être appelée pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8bf35-140">**IMAPIProp::GetIDsFromNames** can be called to do the following:</span></span> 
  
- <span data-ttu-id="8bf35-141">Créer des identificateurs pour les nouveaux noms.</span><span class="sxs-lookup"><span data-stu-id="8bf35-141">Create identifiers for new names.</span></span>
    
- <span data-ttu-id="8bf35-142">Récupérer les identificateurs de noms spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8bf35-142">Retrieve identifiers for specific names.</span></span>
    
- <span data-ttu-id="8bf35-143">Récupérer les identificateurs de toutes les propriétés nommées qui sont incluses dans le mappage de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8bf35-143">Retrieve identifiers for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="8bf35-144">Propriétés nommées sont généralement utilisées par les fournisseurs de banque de messages pour les dossiers et messages.</span><span class="sxs-lookup"><span data-stu-id="8bf35-144">Named properties are typically used by message store providers for folders and messages.</span></span> <span data-ttu-id="8bf35-145">Autres objets, tels que les utilisateurs et aux sections de profil de messagerie ne peuvent pas prendre en charge l’association des noms pour les identificateurs de propriété et peuvent retourner des MAPI_E_NO_SUPPORT de **GetIDsFromNames**.</span><span class="sxs-lookup"><span data-stu-id="8bf35-145">Other objects, such as messaging users and profile sections, might not support the association of names to property identifiers and might return MAPI_E_NO_SUPPORT from **GetIDsFromNames**.</span></span>
  
<span data-ttu-id="8bf35-146">S’il existe une erreur qui renvoie un identificateur pour un nom donné, **GetIDsFromNames** renvoie MAPI_W_ERRORS_RETURNED et définit le type de propriété dans l’entrée de tableau de balise de propriété qui correspond au nom **PT_ERROR** et l’identificateur de zéro.</span><span class="sxs-lookup"><span data-stu-id="8bf35-146">If there is an error that returns an identifier for a particular name, **GetIDsFromNames** returns MAPI_W_ERRORS_RETURNED and sets the property type in the property tag array entry that corresponds to the name to **PT_ERROR** and the identifier to zero.</span></span> 
  
<span data-ttu-id="8bf35-147">Mappage de nom à identificateur est représenté par la propriété **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) d’un objet.</span><span class="sxs-lookup"><span data-stu-id="8bf35-147">Name-to-identifier mapping is represented by an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="8bf35-148">**PR_MAPPING_SIGNATURE** contient une structure [MAPIUID](mapiuid.md) qui indique le responsable de l’objet de fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="8bf35-148">**PR_MAPPING_SIGNATURE** contains a [MAPIUID](mapiuid.md) structure that indicates the service provider responsible for the object.</span></span> <span data-ttu-id="8bf35-149">Si la propriété **PR_MAPPING_SIGNATURE** est le même pour les deux objets, supposent que ces objets utilisent le même mappage à-identificateur de nom.</span><span class="sxs-lookup"><span data-stu-id="8bf35-149">If the **PR_MAPPING_SIGNATURE** property is the same for two objects, assume that these objects use the same name-to-identifier mapping.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8bf35-150">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="8bf35-150">Notes to implementers</span></span>

<span data-ttu-id="8bf35-151">Les identificateurs que vous passez dans le tableau de balise de propriété indiqué par le paramètre _lppPropNames_ doivent être dans la plage 0 x 8000 à 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="8bf35-151">The identifiers that you pass back in the property tag array pointed to by the  _lppPropNames_ parameter must be in the 0x8000 to 0xFFFE range.</span></span> <span data-ttu-id="8bf35-152">Les entrées de ce tableau doivent être dans le même ordre que les noms transmis dans le tableau de la propriété nom désignées par _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="8bf35-152">The entries in this array must be in the same order as the names passed in the property name array pointed to by  _lppPropNames_.</span></span> 
  
<span data-ttu-id="8bf35-153">Si vous prenez en charge les propriétés nommées dans un conteneur, utilisez le mappage de nom-identificateur de même pour tous les objets dans le conteneur (autrement dit, n’utilisez pas un autre mappage pour chaque dossier de la banque de messages ou de chaque message dans le dossier).</span><span class="sxs-lookup"><span data-stu-id="8bf35-153">If you support named properties on a container, use the same name-to-identifier mapping for all objects in your container (that is, do not use a different mapping for each folder in your message store or each message in your folder).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="8bf35-154">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="8bf35-154">Notes to callers</span></span>

<span data-ttu-id="8bf35-155">Étant donné que les types de propriétés pour les identificateurs de tableau de la propriété tag désignés par _lppPropTags_ renvoyées sont définis sur **PT_UNSPECIFIED**, vous devez appeler la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour récupérer les types précis.</span><span class="sxs-lookup"><span data-stu-id="8bf35-155">Because the property types for the returned identifiers in the property tag array pointed to by  _lppPropTags_ are set to **PT_UNSPECIFIED**, you will have to call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to retrieve the accurate types.</span></span> 
  
<span data-ttu-id="8bf35-156">Si vous déplacez ou copier des objets avec des propriétés nommées et les objets source et de destination ont des signatures différentes mappage telle qu’indiquée par les valeurs de leurs propriétés **PR_MAPPING_SIGNATURE** , vous devez conserver les noms pendant ces opérations.</span><span class="sxs-lookup"><span data-stu-id="8bf35-156">If you move or copy objects with named properties, and the source and destination objects have different mapping signatures as indicated by the values of their **PR_MAPPING_SIGNATURE** properties, you must preserve the names during these operations.</span></span> <span data-ttu-id="8bf35-157">Pour conserver les noms de propriété, ajustez les identificateurs de propriété correspondante pour correspondre au mappage à-identificateur de nom de l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="8bf35-157">To preserve property names, adjust the corresponding property identifiers to match the name-to-identifier mapping of the destination object.</span></span> 
  
<span data-ttu-id="8bf35-158">Certains objets ont une limite pour le nombre d’identificateurs de propriété que peuvent de nom.</span><span class="sxs-lookup"><span data-stu-id="8bf35-158">Some objects have a limit as to the number of property identifiers they can name.</span></span> <span data-ttu-id="8bf35-159">Si un appel à **GetIDsFromNames** provoque le dépassement de cette limite, la méthode renvoie MAPI_E_TOO_BIG.</span><span class="sxs-lookup"><span data-stu-id="8bf35-159">If a call to **GetIDsFromNames** causes this limit to be exceeded, the method returns MAPI_E_TOO_BIG.</span></span> <span data-ttu-id="8bf35-160">Dans ce cas, des requêtes par identificateur.</span><span class="sxs-lookup"><span data-stu-id="8bf35-160">In this case, query by identifier.</span></span> 
  
<span data-ttu-id="8bf35-161">Pour plus d’informations, voir [Les propriétés MAPI nommée](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="8bf35-161">For more information, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8bf35-162">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8bf35-162">MFCMAPI reference</span></span>

<span data-ttu-id="8bf35-163">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8bf35-163">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8bf35-164">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="8bf35-164">**File**</span></span>|<span data-ttu-id="8bf35-165">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="8bf35-165">**Function**</span></span>|<span data-ttu-id="8bf35-166">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="8bf35-166">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8bf35-167">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="8bf35-167">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="8bf35-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span><span class="sxs-lookup"><span data-stu-id="8bf35-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span></span>  <br/> |<span data-ttu-id="8bf35-169">MFCMAPI utilise la méthode **IMAPIProp::GetIDsFromNames** pour obtenir les balises de propriété pour toutes les propriétés nommées qui ont été mappées.</span><span class="sxs-lookup"><span data-stu-id="8bf35-169">MFCMAPI uses the **IMAPIProp::GetIDsFromNames** method to obtain property tags for all named properties that have been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8bf35-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bf35-170">See also</span></span>



[<span data-ttu-id="8bf35-171">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="8bf35-171">IMAPIProp::GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md)
  
[<span data-ttu-id="8bf35-172">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="8bf35-172">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="8bf35-173">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="8bf35-173">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="8bf35-174">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="8bf35-174">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="8bf35-175">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8bf35-175">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="8bf35-176">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="8bf35-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="8bf35-177">MAPI des propri�t�s nomm�e</span><span class="sxs-lookup"><span data-stu-id="8bf35-177">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="8bf35-178">Utilisation de Macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="8bf35-178">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

