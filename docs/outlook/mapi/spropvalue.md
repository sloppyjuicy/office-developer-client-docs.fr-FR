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
ms.openlocfilehash: c7f4e8835831af6277cef134bf3961e9928cba33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326585"
---
# <a name="spropvalue"></a><span data-ttu-id="b148e-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b148e-103">SPropValue</span></span>

  
  
<span data-ttu-id="b148e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b148e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b148e-105">Décrit une propriété MAPI.</span><span class="sxs-lookup"><span data-stu-id="b148e-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b148e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b148e-106">Header file:</span></span>  <br/> |<span data-ttu-id="b148e-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b148e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b148e-108">Macros connexes:</span><span class="sxs-lookup"><span data-stu-id="b148e-108">Related macros:</span></span>  <br/> |<span data-ttu-id="b148e-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="b148e-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="b148e-110">Members</span><span class="sxs-lookup"><span data-stu-id="b148e-110">Members</span></span>

 <span data-ttu-id="b148e-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="b148e-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="b148e-112">Balise de propriété de la propriété.</span><span class="sxs-lookup"><span data-stu-id="b148e-112">Property tag for the property.</span></span> <span data-ttu-id="b148e-113">Les balises de propriété sont des entiers non signés 32 bits constitués de l'identificateur unique de la propriété dans l'ordre décroissant de 16 bits et le type de la propriété dans le bas de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b148e-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="b148e-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="b148e-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="b148e-115">Réservé pour MAPI; ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="b148e-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="b148e-116">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b148e-116">**Value**</span></span>
  
> <span data-ttu-id="b148e-117">Union de valeurs de données, la valeur spécifique déterminée par le type de propriété.</span><span class="sxs-lookup"><span data-stu-id="b148e-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="b148e-118">Le tableau suivant répertorie pour chaque type de propriété, le membre de l'Union à utiliser et le type de données associé.</span><span class="sxs-lookup"><span data-stu-id="b148e-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="b148e-119">**Type de propriété**</span><span class="sxs-lookup"><span data-stu-id="b148e-119">**Property type**</span></span>|<span data-ttu-id="b148e-120">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b148e-120">**Value**</span></span>|<span data-ttu-id="b148e-121">**Type de données de la valeur**</span><span class="sxs-lookup"><span data-stu-id="b148e-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b148e-122">PT_I2 ou PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="b148e-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="b148e-123">**i**</span><span class="sxs-lookup"><span data-stu-id="b148e-123">**i**</span></span> <br/> |<span data-ttu-id="b148e-124">short int</span><span class="sxs-lookup"><span data-stu-id="b148e-124">short int</span></span>  <br/> |
|<span data-ttu-id="b148e-125">PT_I4 ou PT_LONG (signé)</span><span class="sxs-lookup"><span data-stu-id="b148e-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="b148e-126">**l**</span><span class="sxs-lookup"><span data-stu-id="b148e-126">**l**</span></span> <br/> |<span data-ttu-id="b148e-127">PLUS</span><span class="sxs-lookup"><span data-stu-id="b148e-127">LONG</span></span>  <br/> |
|<span data-ttu-id="b148e-128">PT_I4 ou PT_LONG (non signé)</span><span class="sxs-lookup"><span data-stu-id="b148e-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="b148e-129">**suffix**</span><span class="sxs-lookup"><span data-stu-id="b148e-129">**ul**</span></span> <br/> |<span data-ttu-id="b148e-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="b148e-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="b148e-131">PT_R4 ou PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="b148e-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="b148e-132">**flt**</span><span class="sxs-lookup"><span data-stu-id="b148e-132">**flt**</span></span> <br/> |<span data-ttu-id="b148e-133">flottant</span><span class="sxs-lookup"><span data-stu-id="b148e-133">float</span></span>  <br/> |
|<span data-ttu-id="b148e-134">PT_R8 ou PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="b148e-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="b148e-135">**clic**</span><span class="sxs-lookup"><span data-stu-id="b148e-135">**dbl**</span></span> <br/> |<span data-ttu-id="b148e-136">double</span><span class="sxs-lookup"><span data-stu-id="b148e-136">double</span></span>  <br/> |
|<span data-ttu-id="b148e-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b148e-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="b148e-138">**point**</span><span class="sxs-lookup"><span data-stu-id="b148e-138">**b**</span></span> <br/> |<span data-ttu-id="b148e-139">entier court non signé</span><span class="sxs-lookup"><span data-stu-id="b148e-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="b148e-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="b148e-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="b148e-141">**Tabs**</span><span class="sxs-lookup"><span data-stu-id="b148e-141">**cur**</span></span> <br/> |[<span data-ttu-id="b148e-142">CONCURRENT</span><span class="sxs-lookup"><span data-stu-id="b148e-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="b148e-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="b148e-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="b148e-144">**Regardez**</span><span class="sxs-lookup"><span data-stu-id="b148e-144">**at**</span></span> <br/> |<span data-ttu-id="b148e-145">double</span><span class="sxs-lookup"><span data-stu-id="b148e-145">double</span></span>  <br/> |
|<span data-ttu-id="b148e-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b148e-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="b148e-147">**pied**</span><span class="sxs-lookup"><span data-stu-id="b148e-147">**ft**</span></span> <br/> |[<span data-ttu-id="b148e-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="b148e-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="b148e-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="b148e-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="b148e-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="b148e-150">**lpszA**</span></span> <br/> |<span data-ttu-id="b148e-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="b148e-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="b148e-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b148e-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="b148e-153">**plateau**</span><span class="sxs-lookup"><span data-stu-id="b148e-153">**bin**</span></span> <br/> |<span data-ttu-id="b148e-154">BYTE [array]</span><span class="sxs-lookup"><span data-stu-id="b148e-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="b148e-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b148e-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="b148e-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="b148e-156">**lpszW**</span></span> <br/> |<span data-ttu-id="b148e-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="b148e-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="b148e-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="b148e-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="b148e-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="b148e-159">**lpguid**</span></span> <br/> |<span data-ttu-id="b148e-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="b148e-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="b148e-161">PT_I8 ou PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="b148e-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="b148e-162">**&**</span><span class="sxs-lookup"><span data-stu-id="b148e-162">**li**</span></span> <br/> |<span data-ttu-id="b148e-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="b148e-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="b148e-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="b148e-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="b148e-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="b148e-165">**MVi**</span></span> <br/> |[<span data-ttu-id="b148e-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="b148e-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="b148e-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="b148e-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="b148e-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="b148e-168">**MVI**</span></span> <br/> |[<span data-ttu-id="b148e-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="b148e-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="b148e-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="b148e-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="b148e-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="b148e-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="b148e-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="b148e-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="b148e-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="b148e-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="b148e-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="b148e-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="b148e-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="b148e-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="b148e-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="b148e-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="b148e-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="b148e-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="b148e-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="b148e-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="b148e-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="b148e-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="b148e-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="b148e-180">**MVat**</span></span> <br/> |[<span data-ttu-id="b148e-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="b148e-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="b148e-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b148e-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="b148e-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="b148e-183">**MVft**</span></span> <br/> |[<span data-ttu-id="b148e-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="b148e-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="b148e-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="b148e-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="b148e-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="b148e-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="b148e-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="b148e-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="b148e-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="b148e-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="b148e-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="b148e-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="b148e-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="b148e-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="b148e-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b148e-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="b148e-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="b148e-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="b148e-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="b148e-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="b148e-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="b148e-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="b148e-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="b148e-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="b148e-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="b148e-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="b148e-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="b148e-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="b148e-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="b148e-198">**MVli**</span></span> <br/> |[<span data-ttu-id="b148e-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="b148e-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="b148e-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="b148e-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="b148e-201">**err**</span><span class="sxs-lookup"><span data-stu-id="b148e-201">**err**</span></span> <br/> |[<span data-ttu-id="b148e-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="b148e-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="b148e-203">PT_NULL ou PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="b148e-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="b148e-204">**x**</span><span class="sxs-lookup"><span data-stu-id="b148e-204">**x**</span></span> <br/> |<span data-ttu-id="b148e-205">PLUS</span><span class="sxs-lookup"><span data-stu-id="b148e-205">LONG</span></span>  <br/> |
|<span data-ttu-id="b148e-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="b148e-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="b148e-207">**LPV**</span><span class="sxs-lookup"><span data-stu-id="b148e-207">**lpv**</span></span> <br/> |<span data-ttu-id="b148e-208">RÉSIDUEL\*</span><span class="sxs-lookup"><span data-stu-id="b148e-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b148e-209">Remarques</span><span class="sxs-lookup"><span data-stu-id="b148e-209">Remarks</span></span>

<span data-ttu-id="b148e-210">Le membre **ulPropTag** est composé de deux parties:</span><span class="sxs-lookup"><span data-stu-id="b148e-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="b148e-211">Identificateur dans l'ordre décroissant de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b148e-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="b148e-212">Un type dans les bits de poids faible 16.</span><span class="sxs-lookup"><span data-stu-id="b148e-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="b148e-213">L'identificateur est une valeur numérique comprise dans une plage particulière.</span><span class="sxs-lookup"><span data-stu-id="b148e-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="b148e-214">MAPI définit des plages d'identificateurs pour décrire ce à quoi la propriété est utilisée et qui est responsable de sa maintenance.</span><span class="sxs-lookup"><span data-stu-id="b148e-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="b148e-215">MAPI définit des contraintes pour chacune des balises de propriété qu'il prend en charge dans le fichier d'en-tête Mapitags. h.</span><span class="sxs-lookup"><span data-stu-id="b148e-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="b148e-216">Le type indique le format de la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="b148e-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="b148e-217">MAPI définit des constantes pour chaque type de propriété qu'il prend en charge dans le fichier d'en-tête Mapidefs. h.</span><span class="sxs-lookup"><span data-stu-id="b148e-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="b148e-218">Pour obtenir la liste complète des plages de propriétés valides pour les identificateurs et les types de propriétés, voir l'annexe relative aux [identificateurs et aux types](property-identifiers-and-types.md) de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b148e-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="b148e-219">Le membre **dwAlignPad** est utilisé comme remplissage pour garantir un alignement correct sur les ordinateurs qui nécessitent un alignement sur 8 octets pour les valeurs 8 octets.</span><span class="sxs-lookup"><span data-stu-id="b148e-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="b148e-220">Les développeurs qui écrivent du code sur ces ordinateurs doivent utiliser des routines d'allocation de mémoire qui allouent les tableaux **SPropValue** sur des limites de 8 octets.</span><span class="sxs-lookup"><span data-stu-id="b148e-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="b148e-221">Pour plus d'informations, reportez-vous à la rubrique [MAPI Property type Overview](mapi-property-type-overview.md) et [mise à jour des propriétés MAPI](updating-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="b148e-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b148e-222">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b148e-222">See also</span></span>



[<span data-ttu-id="b148e-223">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="b148e-223">MAPI Structures</span></span>](mapi-structures.md)

