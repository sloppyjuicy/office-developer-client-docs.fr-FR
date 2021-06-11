---
title: IMAPIPropDeleteProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.DeleteProps
api_type:
- COM
ms.assetid: 5cc642de-21f0-4826-bf21-aac4bcfc1328
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5bfef87baa2dffa4605f9a7afa3833024f514430
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409236"
---
# <a name="imapipropdeleteprops"></a><span data-ttu-id="4e10f-103">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="4e10f-103">IMAPIProp::DeleteProps</span></span>

  
  
<span data-ttu-id="4e10f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e10f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e10f-105">Supprime une ou plusieurs propriétés d’un objet.</span><span class="sxs-lookup"><span data-stu-id="4e10f-105">Deletes one or more properties from an object.</span></span> 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="4e10f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4e10f-106">Parameters</span></span>

 <span data-ttu-id="4e10f-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="4e10f-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="4e10f-108">[in] Pointeur vers un tableau de balises de propriétés qui indiquent les propriétés à supprimer.</span><span class="sxs-lookup"><span data-stu-id="4e10f-108">[in] A pointer to an array of property tags that indicate the properties to delete.</span></span> <span data-ttu-id="4e10f-109">Le membre **cValues** de la structure [SPropTagArray](sproptagarray.md) pointée par  _lpPropTagArray_ ne doit pas être zéro et le paramètre  _lpPropTagArray_ lui-même ne doit pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="4e10f-109">The **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpPropTagArray_ must not be zero, and the  _lpPropTagArray_ parameter itself must not be NULL.</span></span> 
    
 <span data-ttu-id="4e10f-110">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="4e10f-110">_lppProblems_</span></span>
  
> <span data-ttu-id="4e10f-111">[in, out] Lors de l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; sinon, NULL, qui indique qu’il n’est pas nécessaire d’obtenir des informations d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4e10f-111">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates that there is no need for error information.</span></span> <span data-ttu-id="4e10f-112">Si  _lppProblems est_ un pointeur valide sur l’entrée, **DeleteProps** renvoie des informations détaillées sur les erreurs de suppression d’une ou de plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="4e10f-112">If  _lppProblems_ is a valid pointer on input, **DeleteProps** returns detailed information about errors in deleting one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4e10f-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4e10f-113">Return value</span></span>

<span data-ttu-id="4e10f-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e10f-114">S_OK</span></span> 
  
> <span data-ttu-id="4e10f-115">Les propriétés ont été supprimées avec succès.</span><span class="sxs-lookup"><span data-stu-id="4e10f-115">Properties were successfully deleted.</span></span>
    
<span data-ttu-id="4e10f-116">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4e10f-116">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="4e10f-117">L’appelant ne dispose pas des autorisations suffisantes pour supprimer des propriétés.</span><span class="sxs-lookup"><span data-stu-id="4e10f-117">The caller has insufficient permissions to delete properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e10f-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e10f-118">Remarks</span></span>

<span data-ttu-id="4e10f-119">La **méthode IMAPIProp::D eleteProps** supprime une ou plusieurs propriétés de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="4e10f-119">The **IMAPIProp::DeleteProps** method removes one or more properties from the current object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4e10f-120">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="4e10f-120">Notes to implementers</span></span>

<span data-ttu-id="4e10f-121">Vous n’avez pas besoin d’autoriser la suppression des propriétés de tous les objets.</span><span class="sxs-lookup"><span data-stu-id="4e10f-121">You do not have to allow properties to be deleted from all objects.</span></span> <span data-ttu-id="4e10f-122">Si l’objet n’est pas modifiable, renvoyez MAPI_E_NO_ACCESS la **méthode DeleteProps.**</span><span class="sxs-lookup"><span data-stu-id="4e10f-122">If the object is not modifiable, return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4e10f-123">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="4e10f-123">Notes to callers</span></span>

<span data-ttu-id="4e10f-124">Il n’est pas nécessaire de définir le type de propriété pour chaque balise de propriété dans le tableau de balises de propriétés pointant vers le _paramètre lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="4e10f-124">You do not have to set the property type for each property tag in the property tag array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="4e10f-125">Les types de propriétés sont ignorés ; seuls les identificateurs de propriété sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="4e10f-125">Property types are ignored; only the property identifiers are used.</span></span> 
  
<span data-ttu-id="4e10f-126">Notez que certains objets n’autorisent pas la modification et que ces objets MAPI_E_NO_ACCESS à partir de **la méthode DeleteProps.**</span><span class="sxs-lookup"><span data-stu-id="4e10f-126">Be aware that some objects do not allow modification and that these objects return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> <span data-ttu-id="4e10f-127">D’autres objets permettent la suppression de certaines propriétés, mais pas d’autres.</span><span class="sxs-lookup"><span data-stu-id="4e10f-127">Other objects allow some properties to be deleted, but not others.</span></span> <span data-ttu-id="4e10f-128">En cas de problème de suppression de certaines propriétés uniquement, **DeleteProps** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="4e10f-128">When there is a problem deleting only some of the properties, **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="4e10f-129">Si vous avez passé un pointeur valide dans le paramètre  _lppProblems,_ **DeleteProps** le définira sur une structure **SPropProblemArray** qui contient des informations détaillées sur les problèmes liés à chaque propriété.</span><span class="sxs-lookup"><span data-stu-id="4e10f-129">If you have passed a valid pointer in the  _lppProblems_ parameter, **DeleteProps** will set the pointer to an **SPropProblemArray** structure that contains detailed information about the problems with each property.</span></span> <span data-ttu-id="4e10f-130">Par exemple, si vous êtes en cours de suppression de toutes les propriétés d’un message et qu’il existe un problème avec une ou plusieurs de ses pièces jointes, la structure **SPropProblemArray** contient une entrée pour la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4e10f-130">For example, if you are deleting all of the properties of a message and there is a problem with one or more of its attachments, the **SPropProblemArray** structure will contain an entry for the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="4e10f-131">La structure pointée par  _lppProblems n’est_ valide que **si DeleteProps** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="4e10f-131">The structure pointed to by  _lppProblems_ is only valid if **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="4e10f-132">Si **DeleteProps renvoie** une erreur, n’essayez pas d’utiliser la structure **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="4e10f-132">If **DeleteProps** returns an error, do not attempt to use the **SPropProblemArray** structure.</span></span> <span data-ttu-id="4e10f-133">Appelez plutôt la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) de l’objet pour obtenir plus d’informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4e10f-133">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to obtain more information about the error.</span></span> 
  
<span data-ttu-id="4e10f-134">Libérez la structure **SPropProblemArray** renvoyée en appelant la [fonction MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="4e10f-134">Free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4e10f-135">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4e10f-135">MFCMAPI reference</span></span>

<span data-ttu-id="4e10f-136">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4e10f-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4e10f-137">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="4e10f-137">**File**</span></span>|<span data-ttu-id="4e10f-138">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="4e10f-138">**Function**</span></span>|<span data-ttu-id="4e10f-139">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="4e10f-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4e10f-140">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="4e10f-140">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="4e10f-141">DeleteProperty</span><span class="sxs-lookup"><span data-stu-id="4e10f-141">DeleteProperty</span></span>  <br/> |<span data-ttu-id="4e10f-142">MFCMAPI utilise **la méthode IMAPIProp::D eleteProps** pour supprimer une propriété d’un objet.</span><span class="sxs-lookup"><span data-stu-id="4e10f-142">MFCMAPI uses the **IMAPIProp::DeleteProps** method to delete a property from an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e10f-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e10f-143">See also</span></span>



[<span data-ttu-id="4e10f-144">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="4e10f-144">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="4e10f-145">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="4e10f-145">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="4e10f-146">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="4e10f-146">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="4e10f-147">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4e10f-147">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4e10f-148">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="4e10f-148">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="4e10f-149">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="4e10f-149">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="4e10f-150">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e10f-150">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="4e10f-151">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="4e10f-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

