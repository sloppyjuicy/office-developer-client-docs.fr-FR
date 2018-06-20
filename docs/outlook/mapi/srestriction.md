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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9748229799641d62b1649491c432f10164b49192
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787244"
---
# <a name="srestriction"></a><span data-ttu-id="2a8e7-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-103">SRestriction</span></span>

  
  
<span data-ttu-id="2a8e7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2a8e7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2a8e7-105">Décrit un filtre pour limiter l’affichage d’une table aux lignes particuliers.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2a8e7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2a8e7-106">Header file:</span></span>  <br/> |<span data-ttu-id="2a8e7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2a8e7-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="2a8e7-108">Membres</span><span class="sxs-lookup"><span data-stu-id="2a8e7-108">Members</span></span>

 <span data-ttu-id="2a8e7-109">**RT**</span><span class="sxs-lookup"><span data-stu-id="2a8e7-109">**rt**</span></span>
  
> <span data-ttu-id="2a8e7-110">Le type de restriction.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-110">The restriction type.</span></span> <span data-ttu-id="2a8e7-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a8e7-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="2a8e7-112">RES_AND</span><span class="sxs-lookup"><span data-stu-id="2a8e7-112">RES_AND</span></span> 
  
> <span data-ttu-id="2a8e7-113">Une restriction **et** , qui applique une opération de bits **AND** à une restriction.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="2a8e7-114">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="2a8e7-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="2a8e7-115">Une restriction de masque de bits, qui applique un masque de bits pour une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="2a8e7-116">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="2a8e7-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="2a8e7-117">Une restriction de commentaire, qui associe un commentaire à une restriction.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="2a8e7-118">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="2a8e7-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="2a8e7-119">Restriction de comparaison de propriété, qui permet de comparer deux valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="2a8e7-120">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="2a8e7-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="2a8e7-121">Une restriction de contenu, qui recherche une valeur de propriété pour un contenu spécifique.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="2a8e7-122">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="2a8e7-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="2a8e7-123">Une restriction existe, qui détermine si une propriété est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="2a8e7-124">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="2a8e7-124">RES_NOT</span></span> 
  
> <span data-ttu-id="2a8e7-125">**Pas** restriction, qui applique une opération **NOT** logique à une restriction.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="2a8e7-126">RES_OR</span><span class="sxs-lookup"><span data-stu-id="2a8e7-126">RES_OR</span></span> 
  
> <span data-ttu-id="2a8e7-127">Une restriction **ou** , qui applique une opération **ou** logique à une restriction.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="2a8e7-128">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="2a8e7-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="2a8e7-129">Une restriction de propriété, qui détermine si une valeur de propriété correspond à une valeur particulière.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="2a8e7-130">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="2a8e7-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="2a8e7-131">Une restriction de taille, qui détermine si une valeur de propriété est une taille spécifique.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="2a8e7-132">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="2a8e7-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="2a8e7-133">Une restriction objet secondaire, qui applique une restriction aux pièces jointes d’un message ou des destinataires.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="2a8e7-134">**res**</span><span class="sxs-lookup"><span data-stu-id="2a8e7-134">**res**</span></span>
  
> <span data-ttu-id="2a8e7-135">Union de structures de restriction décrivant le filtre à appliquer.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="2a8e7-136">La structure spécifique incluse dans le membre **res** dépend de la valeur du membre **rt** .</span><span class="sxs-lookup"><span data-stu-id="2a8e7-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="2a8e7-137">Le mappage entre le type de restriction et la structure est répertorié dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="2a8e7-138">**Type de restriction**</span><span class="sxs-lookup"><span data-stu-id="2a8e7-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="2a8e7-139">**Structure de restriction**</span><span class="sxs-lookup"><span data-stu-id="2a8e7-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="2a8e7-140">RES_AND</span><span class="sxs-lookup"><span data-stu-id="2a8e7-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="2a8e7-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="2a8e7-142">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="2a8e7-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="2a8e7-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="2a8e7-144">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="2a8e7-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="2a8e7-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="2a8e7-146">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="2a8e7-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="2a8e7-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="2a8e7-148">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="2a8e7-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="2a8e7-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="2a8e7-150">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="2a8e7-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="2a8e7-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="2a8e7-152">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="2a8e7-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="2a8e7-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="2a8e7-154">RES_OR</span><span class="sxs-lookup"><span data-stu-id="2a8e7-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="2a8e7-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="2a8e7-156">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="2a8e7-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="2a8e7-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="2a8e7-158">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="2a8e7-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="2a8e7-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="2a8e7-160">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="2a8e7-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="2a8e7-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a8e7-162">Remarques</span><span class="sxs-lookup"><span data-stu-id="2a8e7-162">Remarks</span></span>

<span data-ttu-id="2a8e7-163">Clients utilisent une structure **SRestriction** pour limiter le nombre et le type de lignes dans leur vue d’une table et pour rechercher des messages spécifiques dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="2a8e7-164">Pour imposer la limitation sur une table, les clients appellent [IMAPITable](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="2a8e7-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="2a8e7-165">Pour imposer la limite d’un dossier, les clients appellent [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) méthode du dossier.</span><span class="sxs-lookup"><span data-stu-id="2a8e7-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="2a8e7-166">Pour plus d’informations sur l’utilisation des restrictions des tableaux, voir [à propos des Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="2a8e7-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2a8e7-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a8e7-167">See also</span></span>



[<span data-ttu-id="2a8e7-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="2a8e7-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="2a8e7-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="2a8e7-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="2a8e7-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="2a8e7-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="2a8e7-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="2a8e7-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="2a8e7-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="2a8e7-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="2a8e7-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="2a8e7-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="2a8e7-179">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="2a8e7-179">MAPI Structures</span></span>](mapi-structures.md)

