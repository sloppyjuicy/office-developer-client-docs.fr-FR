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
# <a name="srestriction"></a><span data-ttu-id="1a62e-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-103">SRestriction</span></span>

  
  
<span data-ttu-id="1a62e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a62e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a62e-105">Décrit un filtre pour limiter l’affichage d’un tableau à des lignes particulières.</span><span class="sxs-lookup"><span data-stu-id="1a62e-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a62e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="1a62e-106">Header file:</span></span>  <br/> |<span data-ttu-id="1a62e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a62e-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="1a62e-108">Members</span><span class="sxs-lookup"><span data-stu-id="1a62e-108">Members</span></span>

 <span data-ttu-id="1a62e-109">**rt**</span><span class="sxs-lookup"><span data-stu-id="1a62e-109">**rt**</span></span>
  
> <span data-ttu-id="1a62e-110">Type de restriction.</span><span class="sxs-lookup"><span data-stu-id="1a62e-110">The restriction type.</span></span> <span data-ttu-id="1a62e-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a62e-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="1a62e-112">RES_AND</span><span class="sxs-lookup"><span data-stu-id="1a62e-112">RES_AND</span></span> 
  
> <span data-ttu-id="1a62e-113">Une restriction **AND,** qui applique une opération **AND** au bit à une restriction.</span><span class="sxs-lookup"><span data-stu-id="1a62e-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="1a62e-114">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="1a62e-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="1a62e-115">Restriction de masque de bits, qui applique un masque de bits à une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="1a62e-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="1a62e-116">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="1a62e-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="1a62e-117">Restriction de commentaire, qui associe un commentaire à une restriction.</span><span class="sxs-lookup"><span data-stu-id="1a62e-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="1a62e-118">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="1a62e-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="1a62e-119">Restriction de comparaison de propriété, qui compare deux valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="1a62e-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="1a62e-120">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="1a62e-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="1a62e-121">Restriction de contenu qui recherche une valeur de propriété pour un contenu spécifique.</span><span class="sxs-lookup"><span data-stu-id="1a62e-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="1a62e-122">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="1a62e-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="1a62e-123">Restriction existante, qui détermine si une propriété est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1a62e-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="1a62e-124">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="1a62e-124">RES_NOT</span></span> 
  
> <span data-ttu-id="1a62e-125">Une restriction **NOT,** qui applique une opération **LOGIQUE NOT** à une restriction.</span><span class="sxs-lookup"><span data-stu-id="1a62e-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="1a62e-126">RES_OR</span><span class="sxs-lookup"><span data-stu-id="1a62e-126">RES_OR</span></span> 
  
> <span data-ttu-id="1a62e-127">Une restriction **OR,** qui applique une opération **LOGIQUE OR** à une restriction.</span><span class="sxs-lookup"><span data-stu-id="1a62e-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="1a62e-128">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="1a62e-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="1a62e-129">Restriction de propriété, qui détermine si une valeur de propriété correspond à une valeur particulière.</span><span class="sxs-lookup"><span data-stu-id="1a62e-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="1a62e-130">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="1a62e-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="1a62e-131">Restriction de taille, qui détermine si une valeur de propriété est une taille particulière.</span><span class="sxs-lookup"><span data-stu-id="1a62e-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="1a62e-132">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="1a62e-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="1a62e-133">Restriction de sous-objet, qui applique une restriction aux pièces jointes ou aux destinataires d’un message.</span><span class="sxs-lookup"><span data-stu-id="1a62e-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="1a62e-134">**res**</span><span class="sxs-lookup"><span data-stu-id="1a62e-134">**res**</span></span>
  
> <span data-ttu-id="1a62e-135">Union des structures de restriction décrivant le filtre à appliquer.</span><span class="sxs-lookup"><span data-stu-id="1a62e-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="1a62e-136">La structure spécifique incluse dans le **membre res** dépend de la valeur du membre **rt.**</span><span class="sxs-lookup"><span data-stu-id="1a62e-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="1a62e-137">Le mappage entre le type de restriction et la structure est répertorié dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1a62e-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="1a62e-138">**Type de restriction**</span><span class="sxs-lookup"><span data-stu-id="1a62e-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="1a62e-139">**Structure des restrictions**</span><span class="sxs-lookup"><span data-stu-id="1a62e-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="1a62e-140">RES_AND</span><span class="sxs-lookup"><span data-stu-id="1a62e-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="1a62e-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="1a62e-142">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="1a62e-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="1a62e-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="1a62e-144">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="1a62e-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="1a62e-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="1a62e-146">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="1a62e-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="1a62e-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="1a62e-148">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="1a62e-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="1a62e-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="1a62e-150">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="1a62e-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="1a62e-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="1a62e-152">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="1a62e-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="1a62e-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="1a62e-154">RES_OR</span><span class="sxs-lookup"><span data-stu-id="1a62e-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="1a62e-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="1a62e-156">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="1a62e-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="1a62e-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="1a62e-158">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="1a62e-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="1a62e-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="1a62e-160">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="1a62e-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="1a62e-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a62e-162">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a62e-162">Remarks</span></span>

<span data-ttu-id="1a62e-163">Les clients utilisent une structure **SRestriction** pour limiter le nombre et le type de lignes dans leur vue d’une table et pour rechercher des messages spécifiques dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="1a62e-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="1a62e-164">Pour imposer la limitation à une table, les clients appellent [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="1a62e-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="1a62e-165">Pour imposer la limitation à un dossier, les clients appellent la méthode [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) du dossier.</span><span class="sxs-lookup"><span data-stu-id="1a62e-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="1a62e-166">Pour plus d’informations sur l’utilisation des restrictions avec des tableaux, voir [À propos des restrictions.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="1a62e-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a62e-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a62e-167">See also</span></span>



[<span data-ttu-id="1a62e-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="1a62e-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="1a62e-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="1a62e-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="1a62e-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="1a62e-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="1a62e-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="1a62e-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="1a62e-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="1a62e-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="1a62e-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="1a62e-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="1a62e-179">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="1a62e-179">MAPI Structures</span></span>](mapi-structures.md)

