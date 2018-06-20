---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Effectue la catégorisation d’envoi après sur un élément de courrier en fonction de son PidTagConversationId.
ms.openlocfilehash: efecfc2d0d865428cb958fc15a858bbc7807c5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782577"
---
# <a name="hrprocessconvactionforsentitem"></a><span data-ttu-id="bed16-103">HrProcessConvActionForSentItem</span><span class="sxs-lookup"><span data-stu-id="bed16-103">HrProcessConvActionForSentItem</span></span>

<span data-ttu-id="bed16-104">Effectue la catégorisation d’envoi après sur un élément de courrier en fonction de son [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="bed16-104">Performs post-send categorization on a mail item based on its [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bed16-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="bed16-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bed16-106">Exportés par :</span><span class="sxs-lookup"><span data-stu-id="bed16-106">Exported by:</span></span>  <br/> |<span data-ttu-id="bed16-107">Outlook.exe</span><span class="sxs-lookup"><span data-stu-id="bed16-107">Outlook.exe</span></span>  <br/> |
|<span data-ttu-id="bed16-108">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="bed16-108">Called by:</span></span>  <br/> |<span data-ttu-id="bed16-109">Client</span><span class="sxs-lookup"><span data-stu-id="bed16-109">Client</span></span>  <br/> |
|<span data-ttu-id="bed16-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="bed16-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="bed16-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="bed16-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a><span data-ttu-id="bed16-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bed16-112">Parameters</span></span>

<span data-ttu-id="bed16-113">_pmbinStoreEid_</span><span class="sxs-lookup"><span data-stu-id="bed16-113">_pmbinStoreEid_</span></span>
  
> <span data-ttu-id="bed16-114">[in] [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) de la banque ou le [PidTagStoreEntryId](http://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) de l’élément de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bed16-114">[in] The [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the store, or the [PidTagStoreEntryId](http://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="bed16-115">Ne peut pas être NULL ou non valide.</span><span class="sxs-lookup"><span data-stu-id="bed16-115">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="bed16-116">_pmbinMsgEid_</span><span class="sxs-lookup"><span data-stu-id="bed16-116">_pmbinMsgEid_</span></span>
  
> <span data-ttu-id="bed16-117">[in] [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) de l’élément de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bed16-117">[in] The [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="bed16-118">Ne peut pas être NULL ou non valide.</span><span class="sxs-lookup"><span data-stu-id="bed16-118">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="bed16-119">_pmbinConvID_</span><span class="sxs-lookup"><span data-stu-id="bed16-119">_pmbinConvID_</span></span>
  
> <span data-ttu-id="bed16-120">[in] [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) de l’élément de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bed16-120">[in] The [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="bed16-121">Ne peut pas être NULL ou non valide.</span><span class="sxs-lookup"><span data-stu-id="bed16-121">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="bed16-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="bed16-122">_dwFlags_</span></span>
  
> <span data-ttu-id="bed16-123">[in] Masque de bits qui spécifie des informations supplémentaires sur l’appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="bed16-123">[in] A bitmask that specifies additional information about the method call.</span></span>
    
   - <span data-ttu-id="bed16-124">0 — aucune des options supplémentaires ne sont utilisées dans cet appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="bed16-124">0—No additional options are used in this method call.</span></span> <span data-ttu-id="bed16-125">Il s’agit de la valeur recommandée.</span><span class="sxs-lookup"><span data-stu-id="bed16-125">This is the recommended value.</span></span> 
    
   - <span data-ttu-id="bed16-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ est en fait la [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) du message.</span><span class="sxs-lookup"><span data-stu-id="bed16-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ is actually the [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) of the message.</span></span> <span data-ttu-id="bed16-127">À l’aide d’un **PidTagSearchKey** consomme beaucoup de ressources et doit être évitée si une [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) est disponible.</span><span class="sxs-lookup"><span data-stu-id="bed16-127">Using a **PidTagSearchKey** is resource intensive, and should be avoided if a [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) is available.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="bed16-128">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="bed16-128">Return values</span></span>

|<span data-ttu-id="bed16-129">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="bed16-129">**HRESULT**</span></span>|<span data-ttu-id="bed16-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="bed16-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bed16-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="bed16-131">S_OK</span></span>  <br/> |<span data-ttu-id="bed16-132">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="bed16-132">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="bed16-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="bed16-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="bed16-134">_dwFlags_ contient un indicateur inconnu.</span><span class="sxs-lookup"><span data-stu-id="bed16-134">_dwFlags_ contains an unknown flag.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bed16-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="bed16-135">Remarks</span></span>

<span data-ttu-id="bed16-136">Catégories sont considérés comme des informations personnelles et ne doivent pas être transmises à l’extérieur de la boîte aux lettres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bed16-136">Categories are considered personal information and should not be transmitted outside the mailbox of the user.</span></span> <span data-ttu-id="bed16-137">Par conséquent, n’appelez pas **HrProcessConvActionForSentItem** sur un élément de courrier en attente.</span><span class="sxs-lookup"><span data-stu-id="bed16-137">Therefore, do not call **HrProcessConvActionForSentItem** on an unsent mail item.</span></span> <span data-ttu-id="bed16-138">Au lieu de cela, envoyer l’élément, puis d’appeler **HrProcessConvActionForSentItem** sur la copie archivée.</span><span class="sxs-lookup"><span data-stu-id="bed16-138">Instead, send the item, and then call **HrProcessConvActionForSentItem** on the archived copy.</span></span> <span data-ttu-id="bed16-139">La copie archivée peut-être être stockée dans le dossier éléments envoyés, ou un emplacement équivalent.</span><span class="sxs-lookup"><span data-stu-id="bed16-139">The archived copy may be stored in the Sent Items folder, or an equivalent location.</span></span> 
  
<span data-ttu-id="bed16-140">Votre application doit être en cours avec Outlook.exe, par exemple à partir d’un complément COM, pour appeler **HrProcessConvActionForSentItem**.</span><span class="sxs-lookup"><span data-stu-id="bed16-140">Your application must be in-process with Outlook.exe, such as from a COM add-in, to call **HrProcessConvActionForSentItem**.</span></span> <span data-ttu-id="bed16-141">Si vous essayez d’appeler **HrProcessConvActionForSentItem** out-of-process, **HrProcessConvActionForSentItem** lève une exception de violation d’accès.</span><span class="sxs-lookup"><span data-stu-id="bed16-141">If you attempt to call **HrProcessConvActionForSentItem** out-of-process, **HrProcessConvActionForSentItem** will throw an access-violation exception.</span></span> 
  

