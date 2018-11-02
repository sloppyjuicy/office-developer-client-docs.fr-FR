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
ms.openlocfilehash: a0d86b9b0342beea6b33db0219cb5889d2e63f03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592072"
---
# <a name="imapipropdeleteprops"></a><span data-ttu-id="151e3-103">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="151e3-103">IMAPIProp::DeleteProps</span></span>

  
  
<span data-ttu-id="151e3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="151e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="151e3-105">Supprime une ou plusieurs propriétés d’un objet.</span><span class="sxs-lookup"><span data-stu-id="151e3-105">Deletes one or more properties from an object.</span></span> 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="151e3-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="151e3-106">Parameters</span></span>

 <span data-ttu-id="151e3-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="151e3-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="151e3-108">[in] Pointeur vers un tableau de balises de propriété qui indiquent les propriétés à supprimer.</span><span class="sxs-lookup"><span data-stu-id="151e3-108">[in] A pointer to an array of property tags that indicate the properties to delete.</span></span> <span data-ttu-id="151e3-109">Le membre **cValues** de la structure [SPropTagArray](sproptagarray.md) désigné par _lpPropTagArray_ ne doit pas être zéro, et le paramètre _lpPropTagArray_ lui-même ne doit pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="151e3-109">The **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpPropTagArray_ must not be zero, and the  _lpPropTagArray_ parameter itself must not be NULL.</span></span> 
    
 <span data-ttu-id="151e3-110">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="151e3-110">_lppProblems_</span></span>
  
> <span data-ttu-id="151e3-111">[entrée, sortie] À l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; dans le cas contraire, la valeur NULL, ce qui indique qu’il n’est pas nécessaire pour les informations d’erreur.</span><span class="sxs-lookup"><span data-stu-id="151e3-111">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates that there is no need for error information.</span></span> <span data-ttu-id="151e3-112">Si _lppProblems_ est un pointeur valid en entrée, **DeleteProps** renvoie des informations détaillées sur les erreurs lors de la suppression d’une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="151e3-112">If  _lppProblems_ is a valid pointer on input, **DeleteProps** returns detailed information about errors in deleting one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="151e3-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="151e3-113">Return value</span></span>

<span data-ttu-id="151e3-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="151e3-114">S_OK</span></span> 
  
> <span data-ttu-id="151e3-115">Les propriétés ont été supprimées.</span><span class="sxs-lookup"><span data-stu-id="151e3-115">Properties were successfully deleted.</span></span>
    
<span data-ttu-id="151e3-116">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="151e3-116">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="151e3-117">L’appelant a des autorisations suffisantes pour supprimer des propriétés.</span><span class="sxs-lookup"><span data-stu-id="151e3-117">The caller has insufficient permissions to delete properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="151e3-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="151e3-118">Remarks</span></span>

<span data-ttu-id="151e3-119">La méthode **IMAPIProp::DeleteProps** supprime une ou plusieurs propriétés de l’objet actif.</span><span class="sxs-lookup"><span data-stu-id="151e3-119">The **IMAPIProp::DeleteProps** method removes one or more properties from the current object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="151e3-120">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="151e3-120">Notes to implementers</span></span>

<span data-ttu-id="151e3-121">Il est inutile que les propriétés doivent être supprimés de tous les objets.</span><span class="sxs-lookup"><span data-stu-id="151e3-121">You do not have to allow properties to be deleted from all objects.</span></span> <span data-ttu-id="151e3-122">Si l’objet n’est pas modifiable, renvoyer MAPI_E_NO_ACCESS à partir de la méthode **DeleteProps** .</span><span class="sxs-lookup"><span data-stu-id="151e3-122">If the object is not modifiable, return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="151e3-123">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="151e3-123">Notes to callers</span></span>

<span data-ttu-id="151e3-124">Vous n’êtes pas obligé de définir le type de propriété de chaque balise de propriété dans le tableau de balise de propriété indiqué par le paramètre _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="151e3-124">You do not have to set the property type for each property tag in the property tag array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="151e3-125">Types de propriété sont ignorées ; uniquement les identificateurs de propriété sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="151e3-125">Property types are ignored; only the property identifiers are used.</span></span> 
  
<span data-ttu-id="151e3-126">Sachez que certains objets ne permettent pas de modification et que ces objets retournent MAPI_E_NO_ACCESS à partir de la méthode **DeleteProps** .</span><span class="sxs-lookup"><span data-stu-id="151e3-126">Be aware that some objects do not allow modification and that these objects return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> <span data-ttu-id="151e3-127">Autres objets permettent de certaines propriétés d’être supprimé, mais pas à d’autres.</span><span class="sxs-lookup"><span data-stu-id="151e3-127">Other objects allow some properties to be deleted, but not others.</span></span> <span data-ttu-id="151e3-128">Lorsqu’il existe un problème de suppression de certaines propriétés, **DeleteProps** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="151e3-128">When there is a problem deleting only some of the properties, **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="151e3-129">Si vous avez passé un pointeur valide dans le paramètre _lppProblems_ , **DeleteProps** définira le pointeur vers une structure **SPropProblemArray** qui contient des informations détaillées sur les problèmes liés à chaque propriété.</span><span class="sxs-lookup"><span data-stu-id="151e3-129">If you have passed a valid pointer in the  _lppProblems_ parameter, **DeleteProps** will set the pointer to an **SPropProblemArray** structure that contains detailed information about the problems with each property.</span></span> <span data-ttu-id="151e3-130">Par exemple, si vous supprimez toutes les propriétés d’un message et il existe un problème avec un ou plusieurs de ses pièces jointes, la structure **SPropProblemArray** contient une entrée pour le **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments ](pidtagmessageattachments-canonical-property.md)) propriété.</span><span class="sxs-lookup"><span data-stu-id="151e3-130">For example, if you are deleting all of the properties of a message and there is a problem with one or more of its attachments, the **SPropProblemArray** structure will contain an entry for the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="151e3-131">La structure vers laquelle pointée _lppProblems_ est valide uniquement si **DeleteProps** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="151e3-131">The structure pointed to by  _lppProblems_ is only valid if **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="151e3-132">Si **DeleteProps** renvoie une erreur, n’essayez pas d’utiliser la structure **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="151e3-132">If **DeleteProps** returns an error, do not attempt to use the **SPropProblemArray** structure.</span></span> <span data-ttu-id="151e3-133">Au lieu de cela, appelez la méthode l’objet [IMAPIProp::GetLastError](imapiprop-getlasterror.md) pour obtenir plus d’informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="151e3-133">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to obtain more information about the error.</span></span> 
  
<span data-ttu-id="151e3-134">Libérez de la structure **SPropProblemArray** retournée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="151e3-134">Free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="151e3-135">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="151e3-135">MFCMAPI reference</span></span>

<span data-ttu-id="151e3-136">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="151e3-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="151e3-137">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="151e3-137">**File**</span></span>|<span data-ttu-id="151e3-138">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="151e3-138">**Function**</span></span>|<span data-ttu-id="151e3-139">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="151e3-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="151e3-140">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="151e3-140">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="151e3-141">DeleteProperty</span><span class="sxs-lookup"><span data-stu-id="151e3-141">DeleteProperty</span></span>  <br/> |<span data-ttu-id="151e3-142">MFCMAPI utilise la méthode **IMAPIProp::DeleteProps** pour supprimer une propriété d’un objet.</span><span class="sxs-lookup"><span data-stu-id="151e3-142">MFCMAPI uses the **IMAPIProp::DeleteProps** method to delete a property from an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="151e3-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="151e3-143">See also</span></span>



[<span data-ttu-id="151e3-144">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="151e3-144">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="151e3-145">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="151e3-145">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="151e3-146">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="151e3-146">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="151e3-147">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="151e3-147">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="151e3-148">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="151e3-148">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="151e3-149">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="151e3-149">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="151e3-150">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="151e3-150">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="151e3-151">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="151e3-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

