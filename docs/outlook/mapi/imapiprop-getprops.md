---
title: IMAPIPropGetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetProps
api_type:
- COM
ms.assetid: 1c7a9cd2-d765-4218-9aee-52df1a2aae6c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9b03775d495f7d1f51142eb0ed06fc9ecdf6d1a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316610"
---
# <a name="imapipropgetprops"></a><span data-ttu-id="143de-103">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="143de-103">IMAPIProp::GetProps</span></span>

  
  
<span data-ttu-id="143de-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="143de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="143de-105">Récupère la valeur de propriété d'une ou de plusieurs propriétés d'un objet.</span><span class="sxs-lookup"><span data-stu-id="143de-105">Retrieves the property value of one or more properties of an object.</span></span>
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="143de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="143de-106">Parameters</span></span>

 <span data-ttu-id="143de-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="143de-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="143de-108">dans Pointeur vers un tableau de balises de propriété qui identifient les propriétés dont les valeurs doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="143de-108">[in] A pointer to an array of property tags that identify the properties whose values are to be retrieved.</span></span> <span data-ttu-id="143de-109">Le paramètre _lpPropTagArray_ doit être null, ce qui indique que les valeurs de toutes les propriétés de l'objet doivent être renvoyées ou pointer vers une structure [SPropTagArray](sproptagarray.md) qui contient une ou plusieurs balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="143de-109">The  _lpPropTagArray_ parameter must be either NULL, indicating that values for all properties of the object should be returned, or point to an [SPropTagArray](sproptagarray.md) structure that contains one or more property tags.</span></span> 
    
 <span data-ttu-id="143de-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="143de-110">_ulFlags_</span></span>
  
> <span data-ttu-id="143de-111">dans Masque de des indicateurs qui indique le format des propriétés ayant le type PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="143de-111">[in] A bitmask of flags that indicates the format for properties that have the type PT_UNSPECIFIED.</span></span> <span data-ttu-id="143de-112">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="143de-112">The following flag can be set:</span></span>
    
<span data-ttu-id="143de-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="143de-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="143de-114">Les valeurs de chaîne de ces propriétés doivent être renvoyées au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="143de-114">The string values for these properties should be returned in the Unicode format.</span></span> <span data-ttu-id="143de-115">Si l'indicateur MAPI_UNICODE n'est pas défini, les valeurs de chaîne doivent être renvoyées au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="143de-115">If the MAPI_UNICODE flag is not set, the string values should be returned in the ANSI format.</span></span>
    
 <span data-ttu-id="143de-116">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="143de-116">_lpcValues_</span></span>
  
> <span data-ttu-id="143de-117">remarquer Pointeur vers le nombre de valeurs de propriété vers lesquelles pointe le paramètre _lppPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="143de-117">[out] A pointer to a count of property values pointed to by the  _lppPropArray_ parameter.</span></span> <span data-ttu-id="143de-118">Si _lppPropArray_ est null, le contenu du paramètre _lpcValues_ est zéro.</span><span class="sxs-lookup"><span data-stu-id="143de-118">If  _lppPropArray_ is NULL, the content of the  _lpcValues_ parameter is zero.</span></span> 
    
 <span data-ttu-id="143de-119">_lppPropArray_</span><span class="sxs-lookup"><span data-stu-id="143de-119">_lppPropArray_</span></span>
  
> <span data-ttu-id="143de-120">remarquer Pointeur vers un pointeur vers les valeurs de propriété récupérées.</span><span class="sxs-lookup"><span data-stu-id="143de-120">[out] A pointer to a pointer to the retrieved property values.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="143de-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="143de-121">Return value</span></span>

<span data-ttu-id="143de-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="143de-122">S_OK</span></span> 
  
> <span data-ttu-id="143de-123">Les valeurs de propriété ont été correctement récupérées.</span><span class="sxs-lookup"><span data-stu-id="143de-123">The property values were successfully retrieved.</span></span>
    
<span data-ttu-id="143de-124">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="143de-124">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="143de-125">L'appel a réussi globalement, mais une ou plusieurs propriétés sont inaccessibles.</span><span class="sxs-lookup"><span data-stu-id="143de-125">The call succeeded overall, but one or more properties could not be accessed.</span></span> <span data-ttu-id="143de-126">Le membre **aulPropTag** de la valeur de propriété pour chaque propriété indisponible a un type de propriété PT_ERROR et un identificateur de zéro.</span><span class="sxs-lookup"><span data-stu-id="143de-126">The **aulPropTag** member of the property value for each unavailable property has a property type of PT_ERROR and an identifier of zero.</span></span> <span data-ttu-id="143de-127">Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi.</span><span class="sxs-lookup"><span data-stu-id="143de-127">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="143de-128">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="143de-128">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="143de-129">Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="143de-129">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
<span data-ttu-id="143de-130">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="143de-130">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="143de-131">Zéro a été transmis dans le membre **cValues** de la structure **SPropTagArray** vers laquelle pointe _lpPropTagArray_.</span><span class="sxs-lookup"><span data-stu-id="143de-131">Zero was passed in the **cValues** member of the **SPropTagArray** structure pointed to by  _lpPropTagArray_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="143de-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="143de-132">Remarks</span></span>

<span data-ttu-id="143de-133">La méthode **IMAPIProp:: GetProps** obtient les valeurs de propriété d'une ou de plusieurs propriétés d'un objet.</span><span class="sxs-lookup"><span data-stu-id="143de-133">The **IMAPIProp::GetProps** method obtains the property values of one or more properties of an object.</span></span> 
  
<span data-ttu-id="143de-134">Les valeurs de propriété sont renvoyées dans le même ordre que celui demandé (c'est-à-dire, l'ordre des propriétés dans le tableau de balises de propriété vers lequel pointe _lpPropTagArray_ correspond à l'ordre dans le tableau de structures de valeurs de propriétés pointé par _lppPropArray _).</span><span class="sxs-lookup"><span data-stu-id="143de-134">The property values are returned in the same order as they were requested (that is, the order of properties in the property tag array pointed to by  _lpPropTagArray_ matches the order in the array of property value structures pointed to by  _lppPropArray_).</span></span> 
  
<span data-ttu-id="143de-135">Les types de propriétés spécifiés dans les membres **aulPropTag** du tableau de balises de propriété indiquent le type de valeur à renvoyer dans le membre de **valeur** de chaque structure de valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="143de-135">The property types specified in the **aulPropTag** members of the property tag array indicate the type of value that should be returned in the **Value** member of each property value structure.</span></span> <span data-ttu-id="143de-136">Toutefois, si l'appelant ne connaît pas le type d'une propriété, le type dans le membre **aulPropTag** peut être défini à la place de PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="143de-136">However, if the caller does not know the type of a property, the type in the **aulPropTag** member can be set instead to PT_UNSPECIFIED.</span></span> <span data-ttu-id="143de-137">Lors de la récupération de la valeur, **GetProps** définit le type correct dans le membre **aulPropTag** de la structure de valeur de la propriété pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="143de-137">In retrieving the value, **GetProps** sets the correct type in the **aulPropTag** member of the property value structure for the property.</span></span> 
  
<span data-ttu-id="143de-138">Si les types de propriété sont spécifiés dans le **SPropTagArray** dans _lpPropTagArray_, les valeurs de propriété dans les **SPropValue** renvoyées dans _lppPropArray_ ont des types qui correspondent exactement aux types demandés, sauf si une valeur d'erreur est renvoyée. cas.</span><span class="sxs-lookup"><span data-stu-id="143de-138">If property types are specified in the **SPropTagArray** in  _lpPropTagArray_, the property values in the **SPropValue** returned in  _lppPropArray_ have types that exactly match the requested types, unless an error value is returned instead.</span></span> 
  
<span data-ttu-id="143de-139">Les propriétés de chaîne peuvent avoir l'un des deux types de propriété suivants: PT_UNICODE pour représenter le format Unicode et PT_STRING8 pour représenter le format ANSI.</span><span class="sxs-lookup"><span data-stu-id="143de-139">String properties can have one of two property types: PT_UNICODE to represent the Unicode format and PT_STRING8 to represent the ANSI format.</span></span> <span data-ttu-id="143de-140">Si l'indicateur MAPI_UNICODE est défini dans le paramètre _ulFlags_ , chaque fois que **GetProps** ne peut pas déterminer le format approprié pour une propriété de chaîne, il renvoie sa valeur au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="143de-140">If the MAPI_UNICODE flag is set in the  _ulFlags_ parameter, whenever **GetProps** cannot determine the appropriate format for a string property, it returns its value in the Unicode format.</span></span> <span data-ttu-id="143de-141">**GetProps** ne peut pas déterminer un type de propriété de chaîne exact dans les situations suivantes:</span><span class="sxs-lookup"><span data-stu-id="143de-141">**GetProps** cannot determine an exact string property type in the following situations:</span></span> 
  
- <span data-ttu-id="143de-142">Le paramètre _lpPropTagArray_ est défini sur null pour demander toutes les propriétés.</span><span class="sxs-lookup"><span data-stu-id="143de-142">The  _lpPropTagArray_ parameter is set to NULL to request all properties.</span></span> 
    
- <span data-ttu-id="143de-143">Le membre **aulPropTag** inclut la valeur PT_UNSPECIFIED comme type de propriété dans le tableau de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="143de-143">The **aulPropTag** member includes the value PT_UNSPECIFIED as its property type in the property tag array.</span></span> 
    
<span data-ttu-id="143de-144">Si le paramètre _lpPropTagArray_ est défini sur null pour récupérer toutes les propriétés de l'objet et qu'aucune propriété n'existe, **GetProps** effectue les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="143de-144">If the  _lpPropTagArray_ parameter is set to NULL to retrieve all of the properties of the object and no properties exist, **GetProps** does the following:</span></span> 
  
- <span data-ttu-id="143de-145">Renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="143de-145">Returns S_OK.</span></span>
    
- <span data-ttu-id="143de-146">Affecte la valeur 0 à la valeur Count dans le membre **cValues** de la structure de la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="143de-146">Sets the count value in the **cValues** member of the property value structure to 0.</span></span> 
    
- <span data-ttu-id="143de-147">Définit le contenu de _lpcValues_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="143de-147">Sets the contents of  _lpcValues_ to 0.</span></span> 
    
- <span data-ttu-id="143de-148">Définit _lppPropArray_ sur null.</span><span class="sxs-lookup"><span data-stu-id="143de-148">Sets  _lppPropArray_ to NULL.</span></span> 
    
 <span data-ttu-id="143de-149">**GetProps** ne doit pas renvoyer les propriétés à valeurs multiples avec **cValues** défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="143de-149">**GetProps** must not return multiple-value properties with **cValues** set to 0.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="143de-150">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="143de-150">Notes to implementers</span></span>

<span data-ttu-id="143de-151">Appelez la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) pour allouer initialement de la mémoire pour la structure [SPropValue](spropvalue.md) vers laquelle pointe _lpPropTagArray_; Appelez [MAPIAllocateMore](mapiallocatemore.md) pour allouer toute mémoire supplémentaire nécessaire pour les membres de la structure.</span><span class="sxs-lookup"><span data-stu-id="143de-151">Call the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate memory initially for the [SPropValue](spropvalue.md) structure pointed to by  _lpPropTagArray_; call [MAPIAllocateMore](mapiallocatemore.md) to allocate any additional memory needed for the structure's members.</span></span> 
  
<span data-ttu-id="143de-152">Renvoie MAPI_W_ERRORS_RETURNED si vous ne pouvez pas récupérer la valeur d'une ou plusieurs des propriétés demandées.</span><span class="sxs-lookup"><span data-stu-id="143de-152">Return MAPI_W_ERRORS_RETURNED if you cannot retrieve the value for one or more of the requested properties.</span></span> <span data-ttu-id="143de-153">Dans la structure de la valeur de la propriété, définissez le type dans le membre **aulPropTag** sur PT_ERROR et le membre **value** sur un code d'État qui décrit l'erreur.</span><span class="sxs-lookup"><span data-stu-id="143de-153">In the property value structure, set the type in the **aulPropTag** member to PT_ERROR and the **Value** member to a status code that describes the error.</span></span> <span data-ttu-id="143de-154">Par exemple, si vous devez convertir une chaîne au format Unicode et ne pas prendre en charge Unicode, définissez le membre **value** sur MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="143de-154">For example, if you have to convert a string to Unicode and do not support Unicode, set the **Value** member to MAPI_E_BAD_CHARWIDTH.</span></span> <span data-ttu-id="143de-155">Si la propriété est trop volumineuse, définissez-la sur MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="143de-155">If the property is too large, set it to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="143de-156">Si l'objet ne prend pas en charge la propriété, affectez-lui la valeur MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="143de-156">If the object does not support the property, set it to MAPI_E_NOT_FOUND.</span></span> 
  
<span data-ttu-id="143de-157">L'implémentation d'un fournisseur de transport distant de la méthode **GetProps** doit renvoyer les valeurs de propriété du dossier pour les propriétés demandées par l'appelant.</span><span class="sxs-lookup"><span data-stu-id="143de-157">A remote transport provider's implementation of the **GetProps** method must return the folder's property values for properties requested by the caller.</span></span> <span data-ttu-id="143de-158">Votre implémentation doit effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="143de-158">Your implementation must do the following:</span></span> 
  
- <span data-ttu-id="143de-159">AlLouez un tableau de valeurs de propriété à renvoyer à l'appelant et stockez son adresse dans le paramètre de pointeur de valeur de propriété transmis à cet effet.</span><span class="sxs-lookup"><span data-stu-id="143de-159">Allocate a property value array to return to the caller and store its address in the property value pointer parameter passed in for that purpose.</span></span>
    
- <span data-ttu-id="143de-160">Copiez les balises de propriété des propriétés du dossier dans les balises de propriété du tableau de valeurs de propriété en fonction du tableau de balises de propriété transmises à **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="143de-160">Copy the property tags from the folder's properties into the property tags in the property value array according to the array of property tags passed to **GetProps**.</span></span>
    
- <span data-ttu-id="143de-161">Assurez-vous que le type de propriété est défini pour toutes les balises de propriété transmises à **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="143de-161">Ensure that the property type is set for all property tags passed to **GetProps**.</span></span> <span data-ttu-id="143de-162">L'appelant peut transmettre un type de propriété PT_UNSPECIFIED, auquel cas **GetProps** doit définir le type de propriété approprié pour cette balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="143de-162">The caller can pass in a property type of PT_UNSPECIFIED, in which case **GetProps** must set the correct property type for that property tag.</span></span> 
    
- <span data-ttu-id="143de-163">Définissez la valeur de chaque propriété dans le tableau de valeurs de la propriété en fonction de sa balise.</span><span class="sxs-lookup"><span data-stu-id="143de-163">Set the value of each property in the property value array according to its tag.</span></span> <span data-ttu-id="143de-164">Par exemple, si la balise de propriété demandée par l'appelant est **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** pouvez définir la valeur sur MAPI_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="143de-164">For example, if the property tag requested by the caller is **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** can set the value to MAPI_FOLDER.</span></span> 
    
- <span data-ttu-id="143de-165">Si l'appelant transmet les balises de propriété que votre implémentation ne gère pas, vous pouvez définir la balise de propriété sur PT_ERROR pour ces propriétés et définir la valeur de la propriété sur MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="143de-165">If the caller passes in any property tags that your implementation does not handle, you can set the property tag to PT_ERROR for those properties, and set the property value to MAPI_E_NOT_FOUND.</span></span>
    
- <span data-ttu-id="143de-166">Renvoie S_OK si aucune erreur ne s'est produite ou MAPI_W_ERRORS_RETURNED s'il y a eu des erreurs.</span><span class="sxs-lookup"><span data-stu-id="143de-166">Return S_OK if no errors occurred or MAPI_W_ERRORS_RETURNED if there were errors.</span></span>
    
<span data-ttu-id="143de-167">L'implémentation d'un fournisseur de transport distant de la méthode **GetProps** doit au minimum prendre en charge les propriétés suivantes:</span><span class="sxs-lookup"><span data-stu-id="143de-167">A remote transport provider's implementation of the **GetProps** method must support the following properties at a minimum:</span></span> 
  
- <span data-ttu-id="143de-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="143de-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span></span>
    
- <span data-ttu-id="143de-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="143de-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span></span>
    
- <span data-ttu-id="143de-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="143de-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="143de-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="143de-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="143de-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="143de-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="143de-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="143de-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="143de-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="143de-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="143de-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="143de-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="143de-176">**PR_OBJECT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="143de-176">**PR_OBJECT_TYPE**</span></span>
    
- <span data-ttu-id="143de-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="143de-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="143de-178">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="143de-178">Notes to callers</span></span>

<span data-ttu-id="143de-179">Pour les propriétés de type PT_OBJECT, appelez la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) au lieu de **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="143de-179">For properties of type PT_OBJECT, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method instead of **GetProps**.</span></span> 
  
<span data-ttu-id="143de-180">Pour les propriétés sécurisées, ne prévoyez pas de les récupérer en appelant **GetProps** avec le paramètre _LPPPROPTAGARRAY_ défini sur null.</span><span class="sxs-lookup"><span data-stu-id="143de-180">For secure properties, do not expect to retrieve them by calling **GetProps** with the  _lppPropTagArray_ parameter set to NULL.</span></span> <span data-ttu-id="143de-181">Vous devez définir explicitement l'identificateur d'une propriété sécurisée dans le membre **aulPropTag** de son tableau de balises de propriété lorsque vous appelez **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="143de-181">You must explicitly set a secure property's identifier in the **aulPropTag** member of its property tag array when you call **GetProps**.</span></span> <span data-ttu-id="143de-182">Le fournisseur de services indique quand et comment une propriété sécurisée est disponible.</span><span class="sxs-lookup"><span data-stu-id="143de-182">When and how a secure property is available is up to the service provider.</span></span> 
  
<span data-ttu-id="143de-183">Libérez la structure **SPropValue** renvoyée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) uniquement si **GetProps** renvoie S_OK ou MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="143de-183">Free the returned **SPropValue** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **GetProps** returns S_OK or MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="143de-184">Si **GetProps** renvoie MAPI_W_ERRORS_RETURNED car il n'a pas accès à une ou plusieurs propriétés, vérifiez les balises de propriété des propriétés renvoyées.</span><span class="sxs-lookup"><span data-stu-id="143de-184">If **GetProps** returns MAPI_W_ERRORS_RETURNED because it could not access one or more properties, check the property tags of the returned properties.</span></span> <span data-ttu-id="143de-185">Les valeurs suivantes sont définies dans la structure de la valeur de la propriété des propriétés ayant échoué:</span><span class="sxs-lookup"><span data-stu-id="143de-185">The failed properties will have the following values set in their property value structure:</span></span> 
  
- <span data-ttu-id="143de-186">Type de propriété dans le membre **aulPropTag** défini sur PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="143de-186">The property type in the **aulPropTag** member set to PT_ERROR.</span></span> 
    
- <span data-ttu-id="143de-187">La valeur de la propriété dans le membre de la **valeur** est définie sur un code d'État pour l'erreur, par exemple MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="143de-187">The property value in the **Value** member set to a status code for the error, such as MAPI_E_NOT_FOUND.</span></span> 
    
<span data-ttu-id="143de-188">Les propriétés qui échouent, car elles sont trop volumineuses pour être renvoyées dans la structure de la valeur de la propriété, leur membre de **valeur** est défini sur MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="143de-188">Properties that fail because they are too large to conveniently be returned in the property value structure have their **Value** member set to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="143de-189">En règle générale, cela se produit avec les propriétés de chaîne ou binaires de type PT_STRING8, PT_UNICODE ou PT_BINARY lorsque la valeur de la propriété est supérieure ou égale à 4 Ko.</span><span class="sxs-lookup"><span data-stu-id="143de-189">Typically, this occurs with string or binary properties of type PT_STRING8, PT_UNICODE, or PT_BINARY when the value of the property is 4 KB or larger.</span></span> <span data-ttu-id="143de-190">Appelez **IMAPIProp:: OpenProperty** pour récupérer les propriétés volumineuses.</span><span class="sxs-lookup"><span data-stu-id="143de-190">Call **IMAPIProp::OpenProperty** to retrieve large properties.</span></span> 
  
<span data-ttu-id="143de-191">Toutes les implémentations de **GetProps** prennent en charge les formats Unicode et ANSI pour les chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="143de-191">Not all implementations of **GetProps** support both the Unicode and ANSI formats for character strings.</span></span> <span data-ttu-id="143de-192">Lorsqu'une propriété particulière requiert une conversion de format de chaîne et que **GetProps** ne peut pas la prendre en charge, le membre de **valeur** de la propriété est défini sur MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="143de-192">When a particular property requires string format conversion and **GetProps** cannot support it, the **Value** member for the property is set to MAPI_E_BAD_CHARWIDTH.</span></span> 
  
<span data-ttu-id="143de-193">Pour vérifier s'il s'agit d'un fichier PST SharePoint, montez-le à l'aide de [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md), puis appelez **GetProps** sur l'objet de banque de messages pour demander cette propriété.</span><span class="sxs-lookup"><span data-stu-id="143de-193">To check if a PST is a SharePoint PST, mount the PST using [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), then call **GetProps** on the message store object requesting this property.</span></span> <span data-ttu-id="143de-194">S'il existe, vous pouvez supposer que le fichier PST a été configuré pour SharePoint; Si ce n'est pas le cas, le fichier PST n'a pas été configuré en tant que fichier PST SharePoint.</span><span class="sxs-lookup"><span data-stu-id="143de-194">If it exists, you can assume the PST has been configured for SharePoint; if not, the PST has not been configured as a SharePoint PST.</span></span> 
  
<span data-ttu-id="143de-195">Pour plus d'informations sur l'utilisation de **GetProps** pour accéder aux propriétés, consultez la rubrique [extraction de propriétés MAPI](retrieving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="143de-195">For more information about how to use **GetProps** to access properties, see [Retrieving MAPI Properties](retrieving-mapi-properties.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="143de-196">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="143de-196">MFCMAPI reference</span></span>

<span data-ttu-id="143de-197">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="143de-197">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="143de-198">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="143de-198">**File**</span></span>|<span data-ttu-id="143de-199">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="143de-199">**Function**</span></span>|<span data-ttu-id="143de-200">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="143de-200">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="143de-201">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="143de-201">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="143de-202">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="143de-202">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="143de-203">MFCMAPI utilise la méthode **IMAPIProp:: GetProps** pour obtenir toutes les propriétés d'un objet en passant null ou le tableau renvoyé par la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) dans le paramètre _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="143de-203">MFCMAPI uses the **IMAPIProp::GetProps** method to obtain all properties for an object by passing either NULL or the array returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method in the  _lpPropTagArray_ parameter.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="143de-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="143de-204">See also</span></span>



[<span data-ttu-id="143de-205">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="143de-205">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="143de-206">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="143de-206">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="143de-207">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="143de-207">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="143de-208">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="143de-208">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="143de-209">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="143de-209">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="143de-210">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="143de-210">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="143de-211">SPropValue</span><span class="sxs-lookup"><span data-stu-id="143de-211">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="143de-212">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="143de-212">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="143de-213">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="143de-213">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="143de-214">Récupération des propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="143de-214">Retrieving MAPI Properties</span></span>](retrieving-mapi-properties.md)
  
[<span data-ttu-id="143de-215">Utilisation de macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="143de-215">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

