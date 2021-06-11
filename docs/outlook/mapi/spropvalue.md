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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c7f4e8835831af6277cef134bf3961e9928cba33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433527"
---
# <a name="spropvalue"></a><span data-ttu-id="c6ff7-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c6ff7-103">SPropValue</span></span>

  
  
<span data-ttu-id="c6ff7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6ff7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6ff7-105">Décrit une propriété MAPI.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c6ff7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c6ff7-106">Header file:</span></span>  <br/> |<span data-ttu-id="c6ff7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c6ff7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c6ff7-108">Macros associées :</span><span class="sxs-lookup"><span data-stu-id="c6ff7-108">Related macros:</span></span>  <br/> |<span data-ttu-id="c6ff7-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="c6ff7-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="c6ff7-110">Members</span><span class="sxs-lookup"><span data-stu-id="c6ff7-110">Members</span></span>

 <span data-ttu-id="c6ff7-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="c6ff7-112">Balise de propriété de la propriété.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-112">Property tag for the property.</span></span> <span data-ttu-id="c6ff7-113">Les balises de propriété sont des nombres droits non signés 32 bits constitués de l’identificateur unique de la propriété dans l’ordre élevé de 16 bits et du type de la propriété dans l’ordre faible de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="c6ff7-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="c6ff7-115">Réservé à MAPI ; ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="c6ff7-116">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-116">**Value**</span></span>
  
> <span data-ttu-id="c6ff7-117">Union des valeurs de données, valeur spécifique dictée par le type de propriété.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="c6ff7-118">Le tableau suivant répertorie chaque type de propriété, le membre de l’union à utiliser et son type de données associé.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="c6ff7-119">**Type de propriété**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-119">**Property type**</span></span>|<span data-ttu-id="c6ff7-120">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-120">**Value**</span></span>|<span data-ttu-id="c6ff7-121">**Type de données de valeur**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c6ff7-122">PT_I2 ou PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="c6ff7-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="c6ff7-123">**i**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-123">**i**</span></span> <br/> |<span data-ttu-id="c6ff7-124">short int</span><span class="sxs-lookup"><span data-stu-id="c6ff7-124">short int</span></span>  <br/> |
|<span data-ttu-id="c6ff7-125">PT_I4 ou PT_LONG (signé)</span><span class="sxs-lookup"><span data-stu-id="c6ff7-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="c6ff7-126">**l**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-126">**l**</span></span> <br/> |<span data-ttu-id="c6ff7-127">LONG</span><span class="sxs-lookup"><span data-stu-id="c6ff7-127">LONG</span></span>  <br/> |
|<span data-ttu-id="c6ff7-128">PT_I4 ou PT_LONG (non signé)</span><span class="sxs-lookup"><span data-stu-id="c6ff7-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="c6ff7-129">**ul**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-129">**ul**</span></span> <br/> |<span data-ttu-id="c6ff7-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="c6ff7-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="c6ff7-131">PT_R4 ou PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="c6ff7-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="c6ff7-132">**flt**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-132">**flt**</span></span> <br/> |<span data-ttu-id="c6ff7-133">float</span><span class="sxs-lookup"><span data-stu-id="c6ff7-133">float</span></span>  <br/> |
|<span data-ttu-id="c6ff7-134">PT_R8 ou PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="c6ff7-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="c6ff7-135">**dbl**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-135">**dbl**</span></span> <br/> |<span data-ttu-id="c6ff7-136">double</span><span class="sxs-lookup"><span data-stu-id="c6ff7-136">double</span></span>  <br/> |
|<span data-ttu-id="c6ff7-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c6ff7-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="c6ff7-138">**b**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-138">**b**</span></span> <br/> |<span data-ttu-id="c6ff7-139">unsigned short int</span><span class="sxs-lookup"><span data-stu-id="c6ff7-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="c6ff7-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="c6ff7-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="c6ff7-141">**cur**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-141">**cur**</span></span> <br/> |[<span data-ttu-id="c6ff7-142">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="c6ff7-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="c6ff7-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="c6ff7-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="c6ff7-144">**at**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-144">**at**</span></span> <br/> |<span data-ttu-id="c6ff7-145">double</span><span class="sxs-lookup"><span data-stu-id="c6ff7-145">double</span></span>  <br/> |
|<span data-ttu-id="c6ff7-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c6ff7-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="c6ff7-147">**ft**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-147">**ft**</span></span> <br/> |[<span data-ttu-id="c6ff7-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="c6ff7-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="c6ff7-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c6ff7-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="c6ff7-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-150">**lpszA**</span></span> <br/> |<span data-ttu-id="c6ff7-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="c6ff7-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="c6ff7-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c6ff7-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="c6ff7-153">**bin**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-153">**bin**</span></span> <br/> |<span data-ttu-id="c6ff7-154">BYTE [tableau]</span><span class="sxs-lookup"><span data-stu-id="c6ff7-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="c6ff7-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c6ff7-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="c6ff7-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-156">**lpszW**</span></span> <br/> |<span data-ttu-id="c6ff7-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="c6ff7-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="c6ff7-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="c6ff7-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="c6ff7-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-159">**lpguid**</span></span> <br/> |<span data-ttu-id="c6ff7-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="c6ff7-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="c6ff7-161">PT_I8 ou PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="c6ff7-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="c6ff7-162">**li**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-162">**li**</span></span> <br/> |<span data-ttu-id="c6ff7-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="c6ff7-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="c6ff7-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="c6ff7-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-165">**MVi**</span></span> <br/> |[<span data-ttu-id="c6ff7-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="c6ff7-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="c6ff7-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="c6ff7-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="c6ff7-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-168">**MVI**</span></span> <br/> |[<span data-ttu-id="c6ff7-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="c6ff7-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="c6ff7-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="c6ff7-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="c6ff7-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="c6ff7-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="c6ff7-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="c6ff7-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="c6ff7-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="c6ff7-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="c6ff7-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="c6ff7-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="c6ff7-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="c6ff7-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="c6ff7-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="c6ff7-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="c6ff7-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="c6ff7-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="c6ff7-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="c6ff7-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-180">**MVat**</span></span> <br/> |[<span data-ttu-id="c6ff7-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="c6ff7-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="c6ff7-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c6ff7-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="c6ff7-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-183">**MVft**</span></span> <br/> |[<span data-ttu-id="c6ff7-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="c6ff7-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="c6ff7-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="c6ff7-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="c6ff7-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="c6ff7-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="c6ff7-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="c6ff7-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="c6ff7-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="c6ff7-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="c6ff7-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="c6ff7-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="c6ff7-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c6ff7-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="c6ff7-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="c6ff7-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="c6ff7-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="c6ff7-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="c6ff7-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="c6ff7-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="c6ff7-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="c6ff7-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="c6ff7-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="c6ff7-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="c6ff7-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-198">**MVli**</span></span> <br/> |[<span data-ttu-id="c6ff7-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="c6ff7-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="c6ff7-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="c6ff7-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="c6ff7-201">**err**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-201">**err**</span></span> <br/> |[<span data-ttu-id="c6ff7-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="c6ff7-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="c6ff7-203">PT_NULL ou PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="c6ff7-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="c6ff7-204">**x**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-204">**x**</span></span> <br/> |<span data-ttu-id="c6ff7-205">LONG</span><span class="sxs-lookup"><span data-stu-id="c6ff7-205">LONG</span></span>  <br/> |
|<span data-ttu-id="c6ff7-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="c6ff7-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="c6ff7-207">**lpv**</span><span class="sxs-lookup"><span data-stu-id="c6ff7-207">**lpv**</span></span> <br/> |<span data-ttu-id="c6ff7-208">VOID \*</span><span class="sxs-lookup"><span data-stu-id="c6ff7-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6ff7-209">Remarques</span><span class="sxs-lookup"><span data-stu-id="c6ff7-209">Remarks</span></span>

<span data-ttu-id="c6ff7-210">Le **membre ulPropTag** est composé de deux parties :</span><span class="sxs-lookup"><span data-stu-id="c6ff7-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="c6ff7-211">Identificateur de l’ordre élevé de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="c6ff7-212">Type de 16 bits de bas ordre.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="c6ff7-213">L’identificateur est une valeur numérique dans une plage particulière.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="c6ff7-214">MAPI définit des plages pour les identificateurs afin de décrire l’utilisation de la propriété et la personne responsable de sa maintenance.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="c6ff7-215">MAPI définit des contraintes pour chacune des balises de propriété qu’il prend en charge dans le fichier d’en-tête Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="c6ff7-216">Le type indique le format de la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="c6ff7-217">MAPI définit des constantes pour chacun des types de propriétés qu’il prend en charge dans le fichier d’en-tête Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="c6ff7-218">Pour obtenir la liste complète des plages de propriétés valides pour les identificateurs et les types de propriétés, voir l’annexe Identificateurs et [types de](property-identifiers-and-types.md) propriétés.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="c6ff7-219">Le **membre dwAlignPad** est utilisé comme remplissage pour assurer un alignement correct sur les ordinateurs qui nécessitent un alignement de 8 byte pour les valeurs de 8 byte.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="c6ff7-220">Les développeurs qui écrivent du code sur ces ordinateurs doivent utiliser des routines d’allocation de mémoire qui allouent les tableaux **SPropValue** aux limites de 8 byte.</span><span class="sxs-lookup"><span data-stu-id="c6ff7-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="c6ff7-221">Pour plus d’informations, voir [Vue d’ensemble](mapi-property-type-overview.md) du type de propriété MAPI et [mise à jour des propriétés MAPI.](updating-mapi-properties.md)</span><span class="sxs-lookup"><span data-stu-id="c6ff7-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c6ff7-222">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6ff7-222">See also</span></span>



[<span data-ttu-id="c6ff7-223">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="c6ff7-223">MAPI Structures</span></span>](mapi-structures.md)

