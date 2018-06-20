---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 44a31e46c43a065c720564f2aa193913dbfd9a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783573"
---
# <a name="iabcontainercopyentries"></a><span data-ttu-id="9364d-103">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="9364d-103">IABContainer::CopyEntries</span></span>

  
  
<span data-ttu-id="9364d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9364d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9364d-105">Copie une ou plusieurs entrées, les utilisateurs de messagerie en général ou des listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="9364d-105">Copies one or more entries, typically messaging users or distribution lists.</span></span>
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9364d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9364d-106">Parameters</span></span>

 <span data-ttu-id="9364d-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="9364d-107">_lpEntries_</span></span>
  
> <span data-ttu-id="9364d-108">[in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui contient les identificateurs d’entrée des entrées à copier.</span><span class="sxs-lookup"><span data-stu-id="9364d-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contains the entry identifiers of the entries to copy.</span></span> 
    
 <span data-ttu-id="9364d-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9364d-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="9364d-110">[in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows qui affiche cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9364d-110">[in] The handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="9364d-111">Le paramètre _ulUIParam_ doit être égal à zéro si l’indicateur AB_NO_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="9364d-111">The  _ulUIParam_ parameter must be zero if the AB_NO_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="9364d-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="9364d-112">_lpProgress_</span></span>
  
> <span data-ttu-id="9364d-113">[in] Pointeur vers un objet de progression qui affiche un indicateur de progression, ou valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="9364d-113">[in] A pointer to a progress object that displays a progress indicator, or NULL.</span></span> <span data-ttu-id="9364d-114">Si _lpProgress_ est NULL, un indicateur de progression doit être affiché à l’aide de l’objet de l’avancement fourni par MAPI par le biais de la méthode [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="9364d-114">If  _lpProgress_ is NULL, a progress indicator should be displayed by using the progress object supplied by MAPI through the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> <span data-ttu-id="9364d-115">Le paramètre _lpProgress_ est ignoré si l’indicateur AB_NO_DIALOG est défini dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="9364d-115">The  _lpProgress_ parameter is ignored if the AB_NO_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="9364d-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9364d-116">_ulFlags_</span></span>
  
> <span data-ttu-id="9364d-117">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’opération de copie est effectuée.</span><span class="sxs-lookup"><span data-stu-id="9364d-117">[in] A bitmask of flags that controls how the copy operation is performed.</span></span> <span data-ttu-id="9364d-118">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="9364d-118">The following flags can be set:</span></span>
    
<span data-ttu-id="9364d-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="9364d-119">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="9364d-120">Supprime l’affichage d’un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="9364d-120">Suppresses display of a progress indicator.</span></span> <span data-ttu-id="9364d-121">Si cet indicateur n’est pas défini, un indicateur de progression est affiché.</span><span class="sxs-lookup"><span data-stu-id="9364d-121">If this flag is not set, a progress indicator is displayed.</span></span>
    
<span data-ttu-id="9364d-122">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="9364d-122">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="9364d-123">Indique qu’un niveau de vérification de l’entrée en double libre doit être effectué.</span><span class="sxs-lookup"><span data-stu-id="9364d-123">Indicates that a loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="9364d-124">L’implémentation de vérification de l’entrée en double en vrac est spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9364d-124">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="9364d-125">Par exemple, un fournisseur peut définir une correspondance partielle, comme les deux entrées qui ont le même nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9364d-125">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="9364d-126">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="9364d-126">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="9364d-127">Indique qu’un niveau strict de vérification de l’entrée en double doit être effectué.</span><span class="sxs-lookup"><span data-stu-id="9364d-127">Indicates that a strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="9364d-128">L’implémentation de vérification stricte entrée en double est spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9364d-128">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="9364d-129">Par exemple, un fournisseur peut définir une correspondance exacte comme les deux entrées qui ont à la fois le même nom et l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="9364d-129">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="9364d-130">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="9364d-130">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="9364d-131">Indique qu’une nouvelle entrée doit remplacer un s’il est déterminé que les deux sont des doublons.</span><span class="sxs-lookup"><span data-stu-id="9364d-131">Indicates that a new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9364d-132">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="9364d-132">Return value</span></span>

<span data-ttu-id="9364d-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="9364d-133">S_OK</span></span> 
  
> <span data-ttu-id="9364d-134">L’opération de copie a réussi.</span><span class="sxs-lookup"><span data-stu-id="9364d-134">The copy operation succeeded.</span></span>
    
<span data-ttu-id="9364d-135">MAPI_W_PARTIAL_COMPLETION SE PRODUIT</span><span class="sxs-lookup"><span data-stu-id="9364d-135">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="9364d-136">L’opération de copie a réussi, mais un ou plusieurs des entrées pas peuvent être copié.</span><span class="sxs-lookup"><span data-stu-id="9364d-136">The copy operation succeeded overall, but one or more of the entries could not be copied.</span></span> <span data-ttu-id="9364d-137">Lorsque cette valeur est renvoyée, l’appel doit être traité comme étant réussi.</span><span class="sxs-lookup"><span data-stu-id="9364d-137">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="9364d-138">Pour tester cette valeur, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="9364d-138">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="9364d-139">Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="9364d-139">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9364d-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="9364d-140">Remarks</span></span>

<span data-ttu-id="9364d-141">La méthode **IABContainer::CopyEntries** copie les entrées à partir du conteneur même ou un autre conteneur.</span><span class="sxs-lookup"><span data-stu-id="9364d-141">The **IABContainer::CopyEntries** method copies entries from the same container or a different container.</span></span> <span data-ttu-id="9364d-142">Un appel à **CopyEntries** est fonctionnellement équivalent à l’appel suivant pour chaque entrée à copier :</span><span class="sxs-lookup"><span data-stu-id="9364d-142">A call to **CopyEntries** is functionally equivalent to making the following calls for each entry to be copied:</span></span> 
  
1. <span data-ttu-id="9364d-143">La méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) pour créer la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="9364d-143">The [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the new entry.</span></span> 
    
2. <span data-ttu-id="9364d-144">La méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour lire les propriétés à partir de l’entrée à copier.</span><span class="sxs-lookup"><span data-stu-id="9364d-144">The [IMAPIProp::GetProps](imapiprop-getprops.md) method to read properties from the entry to be copied.</span></span> 
    
3. <span data-ttu-id="9364d-145">La méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour écrire des propriétés dans la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="9364d-145">The [IMAPIProp::SetProps](imapiprop-setprops.md) method to write properties to the new entry.</span></span> 
    
4. <span data-ttu-id="9364d-146">Méthode de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la nouvelle entrée pour effectuer une sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="9364d-146">The new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to perform a save.</span></span> 
    
5. <span data-ttu-id="9364d-147">Méthode [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) de la nouvelle entrée fourniture de référence du conteneur.</span><span class="sxs-lookup"><span data-stu-id="9364d-147">The new entry's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) method to release the container's reference.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="9364d-148">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="9364d-148">Notes to implementers</span></span>

<span data-ttu-id="9364d-149">Tous les conteneurs qui prennent en charge la méthode **IABContainer::CopyEntries** doivent être modifiables.</span><span class="sxs-lookup"><span data-stu-id="9364d-149">All containers that support the **IABContainer::CopyEntries** method must be modifiable.</span></span> <span data-ttu-id="9364d-150">Définir l’indicateur AB_MODIFIABLE de votre conteneur dans sa propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) pour indiquer qu’il est modifiable.</span><span class="sxs-lookup"><span data-stu-id="9364d-150">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="9364d-151">À prendre en charge tous les indicateurs ; Toutefois, l’interprétation et l’utilisation de ces indicateurs est spécifique à l’implémentation — autrement dit, vous pouvez déterminer la signification de la sémantique des indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT dans le cadre de votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="9364d-151">You must support all of the flags; however, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags mean in the context of your implementation.</span></span> <span data-ttu-id="9364d-152">Si vous ne pouvez pas ou ne déterminez pas si une entrée est un doublon, toujours autoriser l’entrée doit être copié.</span><span class="sxs-lookup"><span data-stu-id="9364d-152">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be copied.</span></span> 
  
<span data-ttu-id="9364d-153">Si l’indicateur CREATE_REPLACE est défini, copiez toujours l’entrée indépendamment si CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT est défini et si l’entrée est un doublon.</span><span class="sxs-lookup"><span data-stu-id="9364d-153">If the CREATE_REPLACE flag is set, always copy the entry regardless of whether CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT is set and whether the entry is a duplicate.</span></span> 
  
<span data-ttu-id="9364d-154">Si CREATE_REPLACE n’est pas définie et CREATE_CHECK_DUP_STRICT est défini, vérifiez les doublons.</span><span class="sxs-lookup"><span data-stu-id="9364d-154">If CREATE_REPLACE is not set and CREATE_CHECK_DUP_STRICT is set, check for duplicates.</span></span> <span data-ttu-id="9364d-155">Si une entrée s’avère être un double, ne pas copier l’entrée.</span><span class="sxs-lookup"><span data-stu-id="9364d-155">If an entry is determined to be a duplicate, do not copy the entry.</span></span> 
  
<span data-ttu-id="9364d-156">Vous n’avez pas besoin prendre en charge CREATE_REPLACE ; ne pas de prise en charge CREATE_REPLACE signifie que vous pouvez l’ignorer et toujours effectuer une copie.</span><span class="sxs-lookup"><span data-stu-id="9364d-156">You do not need to support CREATE_REPLACE; not supporting CREATE_REPLACE means that you can safely ignore it and always perform a copy.</span></span> 
  
<span data-ttu-id="9364d-157">Renvoie l’avertissement MAPI_W_PARTIAL_COMPLETION se produit uniquement si une entrée non dupliquée ne peut pas être copiée.</span><span class="sxs-lookup"><span data-stu-id="9364d-157">Return the warning MAPI_W_PARTIAL_COMPLETION only if a nonduplicate entry cannot be copied.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9364d-158">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="9364d-158">Notes to callers</span></span>

<span data-ttu-id="9364d-159">Utilisez les indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT pour indiquer au fournisseur comment vous souhaitez le conteneur d’effectuer la vérification de l’entrée en double.</span><span class="sxs-lookup"><span data-stu-id="9364d-159">Use the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags to indicate to the provider how you want the container to perform duplicate-entry checking.</span></span> <span data-ttu-id="9364d-160">Si vous avez besoin d’avoir une entrée ajoutée qu’il s’agisse d’un doublon, ne pas définir une de ces indicateurs ou définir l’indicateur CREATE_REPLACE.</span><span class="sxs-lookup"><span data-stu-id="9364d-160">If you need to have an entry added regardless of whether it is a duplicate, either do not set either of these flags or set the CREATE_REPLACE flag.</span></span> <span data-ttu-id="9364d-161">CREATE_REPLACE indique que vous n’êtes pas si une entrée est un doublon ; vous souhaitez toujours remplacer l’entrée d’origine.</span><span class="sxs-lookup"><span data-stu-id="9364d-161">CREATE_REPLACE indicates that you do not care if an entry is a duplicate; you always want it to replace the original entry.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9364d-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9364d-162">See also</span></span>



[<span data-ttu-id="9364d-163">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="9364d-163">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="9364d-164">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="9364d-164">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="9364d-165">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9364d-165">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="9364d-166">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="9364d-166">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="9364d-167">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="9364d-167">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

