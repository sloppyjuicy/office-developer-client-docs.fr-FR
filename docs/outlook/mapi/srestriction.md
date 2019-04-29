---
title: SRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRestriction
api_type:
- COM
ms.assetid: c12b4409-da6f-480b-87af-1e5baea2e8bd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a2a6d273495df52adb83393dc5549b0872c8f6f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439358"
---
# <a name="srestriction"></a><span data-ttu-id="413a6-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-103">SRestriction</span></span>

  
  
<span data-ttu-id="413a6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="413a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="413a6-105">Décrit un filtre permettant de limiter l'affichage d'un tableau à des lignes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="413a6-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="413a6-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="413a6-106">Header file:</span></span>  <br/> |<span data-ttu-id="413a6-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="413a6-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRestriction
{
  ULONG rt;
  union
  {
    SComparePropsRestriction resCompareProps;
    SAndRestriction resAnd;
    SOrRestriction resOr;
    SNotRestriction resNot;
    SContentRestriction resContent;
    SPropertyRestriction resProperty;
    SBitMaskRestriction resBitMask;
    SSizeRestriction resSize;
    SExistRestriction resExist;
    SSubRestriction resSub;
    SCommentRestriction resComment;
  } res;
} SRestriction;

```

## <a name="members"></a><span data-ttu-id="413a6-108">Members</span><span class="sxs-lookup"><span data-stu-id="413a6-108">Members</span></span>

 <span data-ttu-id="413a6-109">**transcriptase**</span><span class="sxs-lookup"><span data-stu-id="413a6-109">**rt**</span></span>
  
> <span data-ttu-id="413a6-110">Type de restriction.</span><span class="sxs-lookup"><span data-stu-id="413a6-110">The restriction type.</span></span> <span data-ttu-id="413a6-111">Les valeurs possibles sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="413a6-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="413a6-112">RES_AND</span><span class="sxs-lookup"><span data-stu-id="413a6-112">RES_AND</span></span> 
  
> <span data-ttu-id="413a6-113">Une restriction **and** , qui applique une opération \*\*\*\* and au niveau du bit à une restriction.</span><span class="sxs-lookup"><span data-stu-id="413a6-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="413a6-114">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="413a6-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="413a6-115">Une restriction de masque de masques, qui applique un masque de à une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="413a6-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="413a6-116">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="413a6-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="413a6-117">Restriction de commentaire, qui associe un commentaire à une restriction.</span><span class="sxs-lookup"><span data-stu-id="413a6-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="413a6-118">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="413a6-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="413a6-119">Une restriction de comparaison de propriétés, qui compare deux valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="413a6-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="413a6-120">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="413a6-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="413a6-121">Une restriction de contenu, qui recherche une valeur de propriété pour un contenu spécifique.</span><span class="sxs-lookup"><span data-stu-id="413a6-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="413a6-122">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="413a6-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="413a6-123">Une restriction Exists, qui détermine si une propriété est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="413a6-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="413a6-124">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="413a6-124">RES_NOT</span></span> 
  
> <span data-ttu-id="413a6-125">Aucune \*\*\*\* restriction, qui applique une opération **not** logique à une restriction.</span><span class="sxs-lookup"><span data-stu-id="413a6-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="413a6-126">RES_OR</span><span class="sxs-lookup"><span data-stu-id="413a6-126">RES_OR</span></span> 
  
> <span data-ttu-id="413a6-127">Une restriction **or** , qui applique une opération **or** logique à une restriction.</span><span class="sxs-lookup"><span data-stu-id="413a6-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="413a6-128">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="413a6-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="413a6-129">Une restriction de propriété, qui détermine si une valeur de propriété correspond à une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="413a6-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="413a6-130">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="413a6-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="413a6-131">Une restriction de taille, qui détermine si une valeur de propriété correspond à une taille particulière.</span><span class="sxs-lookup"><span data-stu-id="413a6-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="413a6-132">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="413a6-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="413a6-133">Une restriction de sous-objet, qui applique une restriction aux pièces jointes ou aux destinataires d'un message.</span><span class="sxs-lookup"><span data-stu-id="413a6-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="413a6-134">**serv**</span><span class="sxs-lookup"><span data-stu-id="413a6-134">**res**</span></span>
  
> <span data-ttu-id="413a6-135">Union des structures de restriction décrivant le filtre à appliquer.</span><span class="sxs-lookup"><span data-stu-id="413a6-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="413a6-136">La structure spécifique incluse dans le membre **res** dépend de la valeur du membre **RT** .</span><span class="sxs-lookup"><span data-stu-id="413a6-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="413a6-137">Le mappage entre le type de restriction et la structure est illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="413a6-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="413a6-138">**Type de restriction**</span><span class="sxs-lookup"><span data-stu-id="413a6-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="413a6-139">**Structure de restriction**</span><span class="sxs-lookup"><span data-stu-id="413a6-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="413a6-140">RES_AND</span><span class="sxs-lookup"><span data-stu-id="413a6-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="413a6-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="413a6-142">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="413a6-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="413a6-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="413a6-144">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="413a6-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="413a6-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="413a6-146">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="413a6-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="413a6-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="413a6-148">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="413a6-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="413a6-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="413a6-150">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="413a6-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="413a6-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="413a6-152">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="413a6-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="413a6-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="413a6-154">RES_OR</span><span class="sxs-lookup"><span data-stu-id="413a6-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="413a6-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="413a6-156">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="413a6-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="413a6-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="413a6-158">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="413a6-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="413a6-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="413a6-160">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="413a6-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="413a6-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="413a6-162">Remarques</span><span class="sxs-lookup"><span data-stu-id="413a6-162">Remarks</span></span>

<span data-ttu-id="413a6-163">Les clients utilisent une structure **SRestriction** pour limiter le nombre et le type de lignes dans leur affichage d'un tableau et Rechercher des messages spécifiques dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="413a6-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="413a6-164">Pour imposer la limitation sur une table, les clients appellent soit une fonction [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="413a6-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="413a6-165">Pour imposer la limitation sur un dossier, les clients appellent la méthode [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) du dossier.</span><span class="sxs-lookup"><span data-stu-id="413a6-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="413a6-166">Pour plus d'informations sur l'utilisation des restrictions avec des tableaux, voir [about restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="413a6-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="413a6-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="413a6-167">See also</span></span>



[<span data-ttu-id="413a6-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="413a6-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="413a6-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="413a6-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="413a6-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="413a6-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="413a6-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="413a6-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="413a6-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="413a6-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="413a6-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="413a6-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="413a6-179">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="413a6-179">MAPI Structures</span></span>](mapi-structures.md)

