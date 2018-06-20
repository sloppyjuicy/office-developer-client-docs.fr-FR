---
title: SPropValue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropValue
api_type:
- COM
ms.assetid: faf795a2-84db-432d-a05f-082f25a5cab5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f378bdd473410b846328cbe1f911eba9401f88cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787249"
---
# <a name="spropvalue"></a><span data-ttu-id="c9115-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c9115-103">SPropValue</span></span>

  
  
<span data-ttu-id="c9115-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9115-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9115-105">Décrit une propriété MAPI.</span><span class="sxs-lookup"><span data-stu-id="c9115-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9115-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c9115-106">Header file:</span></span>  <br/> |<span data-ttu-id="c9115-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9115-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c9115-108">Macros connexes :</span><span class="sxs-lookup"><span data-stu-id="c9115-108">Related macros:</span></span>  <br/> |<span data-ttu-id="c9115-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="c9115-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="c9115-110">Membres</span><span class="sxs-lookup"><span data-stu-id="c9115-110">Members</span></span>

 <span data-ttu-id="c9115-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="c9115-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="c9115-112">Balise de propriété pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="c9115-112">Property tag for the property.</span></span> <span data-ttu-id="c9115-113">Balises de propriété sont des entiers non signés 32 bits constituée de l’identificateur unique de la propriété dans l’ordre de haut niveau 16 bits et le type de propriété dans les 16 bits de poids faible.</span><span class="sxs-lookup"><span data-stu-id="c9115-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="c9115-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="c9115-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="c9115-115">Réservé pour MAPI ; n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="c9115-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="c9115-116">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c9115-116">**Value**</span></span>
  
> <span data-ttu-id="c9115-117">Union des valeurs de données, la valeur spécifique dictée par le type de propriété.</span><span class="sxs-lookup"><span data-stu-id="c9115-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="c9115-118">Le tableau suivant répertorie pour chaque type de propriété, le membre de l’union qui doit être utilisé et son type de données associé.</span><span class="sxs-lookup"><span data-stu-id="c9115-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="c9115-119">**Type de propriété**</span><span class="sxs-lookup"><span data-stu-id="c9115-119">**Property type**</span></span>|<span data-ttu-id="c9115-120">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c9115-120">**Value**</span></span>|<span data-ttu-id="c9115-121">**Type de données de valeur**</span><span class="sxs-lookup"><span data-stu-id="c9115-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9115-122">PT_I2 ou PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="c9115-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="c9115-123">**J’ai**</span><span class="sxs-lookup"><span data-stu-id="c9115-123">**i**</span></span> <br/> |<span data-ttu-id="c9115-124">int court</span><span class="sxs-lookup"><span data-stu-id="c9115-124">short int</span></span>  <br/> |
|<span data-ttu-id="c9115-125">PT_I4 ou PT_LONG (connecté)</span><span class="sxs-lookup"><span data-stu-id="c9115-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="c9115-126">**l**</span><span class="sxs-lookup"><span data-stu-id="c9115-126">**l**</span></span> <br/> |<span data-ttu-id="c9115-127">LONG</span><span class="sxs-lookup"><span data-stu-id="c9115-127">LONG</span></span>  <br/> |
|<span data-ttu-id="c9115-128">PT_I4 ou PT_LONG (non signé)</span><span class="sxs-lookup"><span data-stu-id="c9115-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="c9115-129">**UL**</span><span class="sxs-lookup"><span data-stu-id="c9115-129">**ul**</span></span> <br/> |<span data-ttu-id="c9115-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="c9115-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="c9115-131">PT_R4 ou PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="c9115-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="c9115-132">**flt**</span><span class="sxs-lookup"><span data-stu-id="c9115-132">**flt**</span></span> <br/> |<span data-ttu-id="c9115-133">flottant</span><span class="sxs-lookup"><span data-stu-id="c9115-133">float</span></span>  <br/> |
|<span data-ttu-id="c9115-134">PT_R8 ou PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="c9115-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="c9115-135">**Double**</span><span class="sxs-lookup"><span data-stu-id="c9115-135">**dbl**</span></span> <br/> |<span data-ttu-id="c9115-136">double</span><span class="sxs-lookup"><span data-stu-id="c9115-136">double</span></span>  <br/> |
|<span data-ttu-id="c9115-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c9115-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="c9115-138">**b**</span><span class="sxs-lookup"><span data-stu-id="c9115-138">**b**</span></span> <br/> |<span data-ttu-id="c9115-139">entier court</span><span class="sxs-lookup"><span data-stu-id="c9115-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="c9115-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="c9115-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="c9115-141">**cur**</span><span class="sxs-lookup"><span data-stu-id="c9115-141">**cur**</span></span> <br/> |[<span data-ttu-id="c9115-142">DEVISE</span><span class="sxs-lookup"><span data-stu-id="c9115-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="c9115-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="c9115-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="c9115-144">**à**</span><span class="sxs-lookup"><span data-stu-id="c9115-144">**at**</span></span> <br/> |<span data-ttu-id="c9115-145">double</span><span class="sxs-lookup"><span data-stu-id="c9115-145">double</span></span>  <br/> |
|<span data-ttu-id="c9115-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c9115-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="c9115-147">**FT**</span><span class="sxs-lookup"><span data-stu-id="c9115-147">**ft**</span></span> <br/> |[<span data-ttu-id="c9115-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="c9115-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="c9115-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c9115-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="c9115-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="c9115-150">**lpszA**</span></span> <br/> |<span data-ttu-id="c9115-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="c9115-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="c9115-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c9115-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="c9115-153">**Corbeille**</span><span class="sxs-lookup"><span data-stu-id="c9115-153">**bin**</span></span> <br/> |<span data-ttu-id="c9115-154">OCTETS [array]</span><span class="sxs-lookup"><span data-stu-id="c9115-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="c9115-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c9115-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="c9115-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="c9115-156">**lpszW**</span></span> <br/> |<span data-ttu-id="c9115-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="c9115-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="c9115-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="c9115-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="c9115-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="c9115-159">**lpguid**</span></span> <br/> |<span data-ttu-id="c9115-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="c9115-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="c9115-161">PT_I8 ou PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="c9115-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="c9115-162">**li**</span><span class="sxs-lookup"><span data-stu-id="c9115-162">**li**</span></span> <br/> |<span data-ttu-id="c9115-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="c9115-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="c9115-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="c9115-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="c9115-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="c9115-165">**MVi**</span></span> <br/> |[<span data-ttu-id="c9115-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="c9115-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="c9115-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="c9115-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="c9115-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="c9115-168">**MVI**</span></span> <br/> |[<span data-ttu-id="c9115-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="c9115-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="c9115-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="c9115-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="c9115-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="c9115-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="c9115-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="c9115-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="c9115-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="c9115-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="c9115-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="c9115-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="c9115-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="c9115-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="c9115-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="c9115-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="c9115-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="c9115-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="c9115-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="c9115-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="c9115-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="c9115-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="c9115-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="c9115-180">**MVat**</span></span> <br/> |[<span data-ttu-id="c9115-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="c9115-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="c9115-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c9115-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="c9115-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="c9115-183">**MVft**</span></span> <br/> |[<span data-ttu-id="c9115-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="c9115-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="c9115-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="c9115-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="c9115-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="c9115-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="c9115-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="c9115-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="c9115-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="c9115-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="c9115-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="c9115-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="c9115-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="c9115-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="c9115-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c9115-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="c9115-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="c9115-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="c9115-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="c9115-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="c9115-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="c9115-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="c9115-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="c9115-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="c9115-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="c9115-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="c9115-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="c9115-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="c9115-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="c9115-198">**MVli**</span></span> <br/> |[<span data-ttu-id="c9115-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="c9115-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="c9115-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="c9115-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="c9115-201">**message d’erreur**</span><span class="sxs-lookup"><span data-stu-id="c9115-201">**err**</span></span> <br/> |[<span data-ttu-id="c9115-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="c9115-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="c9115-203">PT_NULL ou PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="c9115-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="c9115-204">**x**</span><span class="sxs-lookup"><span data-stu-id="c9115-204">**x**</span></span> <br/> |<span data-ttu-id="c9115-205">LONG</span><span class="sxs-lookup"><span data-stu-id="c9115-205">LONG</span></span>  <br/> |
|<span data-ttu-id="c9115-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="c9115-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="c9115-207">**LPV**</span><span class="sxs-lookup"><span data-stu-id="c9115-207">**lpv**</span></span> <br/> |<span data-ttu-id="c9115-208">VOID\*</span><span class="sxs-lookup"><span data-stu-id="c9115-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9115-209">Remarques</span><span class="sxs-lookup"><span data-stu-id="c9115-209">Remarks</span></span>

<span data-ttu-id="c9115-210">Le membre **ulPropTag** est composé de deux parties :</span><span class="sxs-lookup"><span data-stu-id="c9115-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="c9115-211">Un identificateur dans l’ordre de haut niveau 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c9115-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="c9115-212">Un type dans les 16 bits de poids faible.</span><span class="sxs-lookup"><span data-stu-id="c9115-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="c9115-213">L’identificateur est une valeur numérique dans une plage spécifique.</span><span class="sxs-lookup"><span data-stu-id="c9115-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="c9115-214">MAPI définit les plages pour les identificateurs décrire la propriété qui est utilisée pour et qui est chargé de maintenance.</span><span class="sxs-lookup"><span data-stu-id="c9115-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="c9115-215">MAPI définit des contraintes pour chacune des balises de propriété pris en charge dans le fichier d’en-tête Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="c9115-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="c9115-216">Le type indique le format de la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="c9115-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="c9115-217">MAPI définit des constantes pour chacun des types de propriété pris en charge dans le fichier d’en-tête Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="c9115-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="c9115-218">Pour une liste complète des plages de propriété valide pour les identificateurs et les types de propriété, voir l’annexe [les Types et les identificateurs de propriété](property-identifiers-and-types.md) .</span><span class="sxs-lookup"><span data-stu-id="c9115-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="c9115-219">Le membre **dwAlignPad** est utilisé comme remplissage pour effectuer un alignement correct que sur les ordinateurs qui nécessitent l’alignement de 8 octets pour les valeurs de 8 octets.</span><span class="sxs-lookup"><span data-stu-id="c9115-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="c9115-220">Développeurs, écrire du code sur ces ordinateurs doivent utiliser des routines d’allocation de mémoire qui affectent les tableaux **SPropValue** sur les limites de 8 octets.</span><span class="sxs-lookup"><span data-stu-id="c9115-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="c9115-221">Pour plus d’informations, voir [Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md) et [Mise à jour des propriétés MAPI](updating-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="c9115-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c9115-222">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9115-222">See also</span></span>



[<span data-ttu-id="c9115-223">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="c9115-223">MAPI Structures</span></span>](mapi-structures.md)

