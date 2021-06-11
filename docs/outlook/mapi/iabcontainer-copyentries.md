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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ddb730ed92db4c8d281e7c8d5d9b18bc44505598
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346395"
---
# <a name="iabcontainercopyentries"></a><span data-ttu-id="b92c1-103">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="b92c1-103">IABContainer::CopyEntries</span></span>

  
  
<span data-ttu-id="b92c1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b92c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b92c1-105">Copie une ou plusieurs entrées, généralement des utilisateurs de messagerie ou des listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="b92c1-105">Copies one or more entries, typically messaging users or distribution lists.</span></span>
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b92c1-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b92c1-106">Parameters</span></span>

 <span data-ttu-id="b92c1-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="b92c1-107">_lpEntries_</span></span>
  
> <span data-ttu-id="b92c1-108">[in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui contient les identificateurs d’entrée des entrées à copier.</span><span class="sxs-lookup"><span data-stu-id="b92c1-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contains the entry identifiers of the entries to copy.</span></span> 
    
 <span data-ttu-id="b92c1-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b92c1-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="b92c1-110">[in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b92c1-110">[in] The handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="b92c1-111">Le _paramètre ulUIParam_ doit être zéro si l’AB_NO_DIALOG est définie dans _le paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="b92c1-111">The  _ulUIParam_ parameter must be zero if the AB_NO_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b92c1-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="b92c1-112">_lpProgress_</span></span>
  
> <span data-ttu-id="b92c1-113">[in] Pointeur vers un objet de progression qui affiche un indicateur de progression, ou NULL.</span><span class="sxs-lookup"><span data-stu-id="b92c1-113">[in] A pointer to a progress object that displays a progress indicator, or NULL.</span></span> <span data-ttu-id="b92c1-114">Si _lpProgress_ est NULL, un indicateur de progression doit être affiché à l’aide de l’objet de progression fourni par MAPI via la méthode [IMAPISupport::D oProgressDialog.](imapisupport-doprogressdialog.md)</span><span class="sxs-lookup"><span data-stu-id="b92c1-114">If  _lpProgress_ is NULL, a progress indicator should be displayed by using the progress object supplied by MAPI through the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> <span data-ttu-id="b92c1-115">Le  _paramètre lpProgress est_ ignoré si l’AB_NO_DIALOG est définie dans  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="b92c1-115">The  _lpProgress_ parameter is ignored if the AB_NO_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="b92c1-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b92c1-116">_ulFlags_</span></span>
  
> <span data-ttu-id="b92c1-117">[in] Masque de bits d’indicateurs qui contrôle le fonctionnement de l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="b92c1-117">[in] A bitmask of flags that controls how the copy operation is performed.</span></span> <span data-ttu-id="b92c1-118">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="b92c1-118">The following flags can be set:</span></span>
    
<span data-ttu-id="b92c1-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b92c1-119">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="b92c1-120">Supprime l’affichage d’un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="b92c1-120">Suppresses display of a progress indicator.</span></span> <span data-ttu-id="b92c1-121">Si cet indicateur n’est pas définie, un indicateur de progression s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b92c1-121">If this flag is not set, a progress indicator is displayed.</span></span>
    
<span data-ttu-id="b92c1-122">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="b92c1-122">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="b92c1-123">Indique qu’un niveau souple de vérification des entrées en double doit être effectué.</span><span class="sxs-lookup"><span data-stu-id="b92c1-123">Indicates that a loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="b92c1-124">L’implémentation de la vérification des entrées libres en double est spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b92c1-124">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="b92c1-125">Par exemple, un fournisseur peut définir une correspondance souple comme deux entrées qui ont le même nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b92c1-125">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="b92c1-126">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="b92c1-126">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="b92c1-127">Indique qu’un niveau strict de vérification des entrées en double doit être effectué.</span><span class="sxs-lookup"><span data-stu-id="b92c1-127">Indicates that a strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="b92c1-128">L’implémentation d’une vérification stricte des entrées en double est propre au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b92c1-128">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="b92c1-129">Par exemple, un fournisseur peut définir une correspondance stricte comme deux entrées qui ont à la fois le même nom d’affichage et la même adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b92c1-129">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="b92c1-130">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="b92c1-130">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="b92c1-131">Indique qu’une nouvelle entrée doit remplacer une entrée existante s’il est déterminé que les deux sont des doublons.</span><span class="sxs-lookup"><span data-stu-id="b92c1-131">Indicates that a new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b92c1-132">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b92c1-132">Return value</span></span>

<span data-ttu-id="b92c1-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="b92c1-133">S_OK</span></span> 
  
> <span data-ttu-id="b92c1-134">L’opération de copie a réussi.</span><span class="sxs-lookup"><span data-stu-id="b92c1-134">The copy operation succeeded.</span></span>
    
<span data-ttu-id="b92c1-135">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="b92c1-135">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="b92c1-136">L’opération de copie a réussi globalement, mais une ou plusieurs des entrées n’ont pas pu être copiées.</span><span class="sxs-lookup"><span data-stu-id="b92c1-136">The copy operation succeeded overall, but one or more of the entries could not be copied.</span></span> <span data-ttu-id="b92c1-137">Lorsque cette valeur est renvoyée, l’appel doit être géré comme réussi.</span><span class="sxs-lookup"><span data-stu-id="b92c1-137">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="b92c1-138">Pour tester cette valeur, utilisez la macro **HR_FAILED** macro.</span><span class="sxs-lookup"><span data-stu-id="b92c1-138">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="b92c1-139">Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="b92c1-139">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b92c1-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="b92c1-140">Remarks</span></span>

<span data-ttu-id="b92c1-141">La **méthode IABContainer::CopyEntries** copie les entrées du même conteneur ou d’un autre conteneur.</span><span class="sxs-lookup"><span data-stu-id="b92c1-141">The **IABContainer::CopyEntries** method copies entries from the same container or a different container.</span></span> <span data-ttu-id="b92c1-142">Un appel à **CopyEntries équivaut** à effectuer les appels suivants pour chaque entrée à copier :</span><span class="sxs-lookup"><span data-stu-id="b92c1-142">A call to **CopyEntries** is functionally equivalent to making the following calls for each entry to be copied:</span></span> 
  
1. <span data-ttu-id="b92c1-143">Méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) pour créer la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="b92c1-143">The [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the new entry.</span></span> 
    
2. <span data-ttu-id="b92c1-144">La [méthode IMAPIProp::GetProps](imapiprop-getprops.md) pour lire les propriétés de l’entrée à copier.</span><span class="sxs-lookup"><span data-stu-id="b92c1-144">The [IMAPIProp::GetProps](imapiprop-getprops.md) method to read properties from the entry to be copied.</span></span> 
    
3. <span data-ttu-id="b92c1-145">La [méthode IMAPIProp::SetProps](imapiprop-setprops.md) pour écrire des propriétés dans la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="b92c1-145">The [IMAPIProp::SetProps](imapiprop-setprops.md) method to write properties to the new entry.</span></span> 
    
4. <span data-ttu-id="b92c1-146">Méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la nouvelle entrée pour effectuer un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b92c1-146">The new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to perform a save.</span></span> 
    
5. <span data-ttu-id="b92c1-147">Méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) de la nouvelle entrée pour libérer la référence du conteneur.</span><span class="sxs-lookup"><span data-stu-id="b92c1-147">The new entry's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the container's reference.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="b92c1-148">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="b92c1-148">Notes to implementers</span></span>

<span data-ttu-id="b92c1-149">Tous les conteneurs qui la prise en charge de la méthode **IABContainer::CopyEntries** doivent être modifiables.</span><span class="sxs-lookup"><span data-stu-id="b92c1-149">All containers that support the **IABContainer::CopyEntries** method must be modifiable.</span></span> <span data-ttu-id="b92c1-150">Définissez l’indicateur AB_MODIFIABLE conteneur dans sa propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) pour indiquer qu’il est modifiable.</span><span class="sxs-lookup"><span data-stu-id="b92c1-150">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="b92c1-151">Vous devez prendre en charge tous les indicateurs ; toutefois, l’interprétation et l’utilisation de ces indicateurs sont spécifiques à l’implémentation, c’est-à-dire que vous pouvez déterminer ce que signifient la sémantique des indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT dans le contexte de votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="b92c1-151">You must support all of the flags; however, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags mean in the context of your implementation.</span></span> <span data-ttu-id="b92c1-152">Si vous ne pouvez pas ou ne déterminez pas si une entrée est en double, autorisez toujours la copie de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="b92c1-152">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be copied.</span></span> 
  
<span data-ttu-id="b92c1-153">Si l CREATE_REPLACE est définie, copiez toujours l’entrée, qu’elle soit CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT et qu’elle soit en double.</span><span class="sxs-lookup"><span data-stu-id="b92c1-153">If the CREATE_REPLACE flag is set, always copy the entry regardless of whether CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT is set and whether the entry is a duplicate.</span></span> 
  
<span data-ttu-id="b92c1-154">Si CREATE_REPLACE n’est pas définie et CREATE_CHECK_DUP_STRICT est définie, recherchez les doublons.</span><span class="sxs-lookup"><span data-stu-id="b92c1-154">If CREATE_REPLACE is not set and CREATE_CHECK_DUP_STRICT is set, check for duplicates.</span></span> <span data-ttu-id="b92c1-155">Si une entrée est déterminée comme dupliquée, ne copiez pas l’entrée.</span><span class="sxs-lookup"><span data-stu-id="b92c1-155">If an entry is determined to be a duplicate, do not copy the entry.</span></span> 
  
<span data-ttu-id="b92c1-156">Vous n’avez pas besoin de prendre en charge CREATE_REPLACE; Ne pas prendre CREATE_REPLACE signifie que vous pouvez l’ignorer en toute sécurité et toujours effectuer une copie.</span><span class="sxs-lookup"><span data-stu-id="b92c1-156">You do not need to support CREATE_REPLACE; not supporting CREATE_REPLACE means that you can safely ignore it and always perform a copy.</span></span> 
  
<span data-ttu-id="b92c1-157">Renvoyer l’avertissement MAPI_W_PARTIAL_COMPLETION uniquement si une entrée non mise en place ne peut pas être copiée.</span><span class="sxs-lookup"><span data-stu-id="b92c1-157">Return the warning MAPI_W_PARTIAL_COMPLETION only if a nonduplicate entry cannot be copied.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b92c1-158">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="b92c1-158">Notes to callers</span></span>

<span data-ttu-id="b92c1-159">Utilisez les indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT pour indiquer au fournisseur comment vous souhaitez que le conteneur effectue la vérification des entrées en double.</span><span class="sxs-lookup"><span data-stu-id="b92c1-159">Use the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags to indicate to the provider how you want the container to perform duplicate-entry checking.</span></span> <span data-ttu-id="b92c1-160">Si une entrée doit être ajoutée, qu’il s’agit d’un doublon ou non, ne définissez pas l’un de ces indicateurs ou définissez l’CREATE_REPLACE’indicateur.</span><span class="sxs-lookup"><span data-stu-id="b92c1-160">If you need to have an entry added regardless of whether it is a duplicate, either do not set either of these flags or set the CREATE_REPLACE flag.</span></span> <span data-ttu-id="b92c1-161">CREATE_REPLACE indique que vous ne vous souciez pas si une entrée est en double ; vous souhaitez toujours qu’elle remplace l’entrée d’origine.</span><span class="sxs-lookup"><span data-stu-id="b92c1-161">CREATE_REPLACE indicates that you do not care if an entry is a duplicate; you always want it to replace the original entry.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b92c1-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b92c1-162">See also</span></span>



[<span data-ttu-id="b92c1-163">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="b92c1-163">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="b92c1-164">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="b92c1-164">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="b92c1-165">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b92c1-165">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="b92c1-166">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="b92c1-166">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="b92c1-167">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b92c1-167">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

