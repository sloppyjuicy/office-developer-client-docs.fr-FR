---
title: IMAPIViewContextGetSaveStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetSaveStream
api_type:
- COM
ms.assetid: 8316bfa1-3077-401f-aa1e-e9492aca12a8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 68eb74f53d6cee4661c98604ec2ea37609e20ab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408424"
---
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="d9c76-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="d9c76-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="d9c76-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9c76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9c76-105">Extrait un flux à utiliser pour enregistrer le message actuel.</span><span class="sxs-lookup"><span data-stu-id="d9c76-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="d9c76-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d9c76-106">Parameters</span></span>

 <span data-ttu-id="d9c76-107">_nbFlags_</span><span class="sxs-lookup"><span data-stu-id="d9c76-107">_pulFlags_</span></span>
  
> <span data-ttu-id="d9c76-108">[out] Pointeur vers un masque de bits d’indicateurs qui contrôle la façon dont le texte du message doit être enregistré.</span><span class="sxs-lookup"><span data-stu-id="d9c76-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="d9c76-109">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="d9c76-109">The following flag can be set:</span></span>
    
<span data-ttu-id="d9c76-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d9c76-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d9c76-111">Le texte du message est enregistré au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="d9c76-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="d9c76-112">Si l’MAPI_UNICODE n’est pas définie, le texte est enregistré au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="d9c76-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="d9c76-113">_atomFormat_</span><span class="sxs-lookup"><span data-stu-id="d9c76-113">_pulFormat_</span></span>
  
> <span data-ttu-id="d9c76-114">[out] Pointeur vers un masque de bits d’indicateurs qui contrôle le format du texte enregistré.</span><span class="sxs-lookup"><span data-stu-id="d9c76-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="d9c76-115">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="d9c76-115">The following flags can be set:</span></span>
    
<span data-ttu-id="d9c76-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="d9c76-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="d9c76-117">Le texte du message doit être enregistré en tant que texte formaté au format RTF (Rich Text Format).</span><span class="sxs-lookup"><span data-stu-id="d9c76-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="d9c76-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="d9c76-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="d9c76-119">Le texte du message doit être enregistré en tant que texte simple.</span><span class="sxs-lookup"><span data-stu-id="d9c76-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="d9c76-120">_ppstm_</span><span class="sxs-lookup"><span data-stu-id="d9c76-120">_ppstm_</span></span>
  
> <span data-ttu-id="d9c76-121">[out] Pointeur vers un pointeur vers le flux qui contiendra le message enregistré.</span><span class="sxs-lookup"><span data-stu-id="d9c76-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d9c76-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d9c76-122">Return value</span></span>

<span data-ttu-id="d9c76-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9c76-123">S_OK</span></span> 
  
> <span data-ttu-id="d9c76-124">Le flux a été récupéré avec succès.</span><span class="sxs-lookup"><span data-stu-id="d9c76-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d9c76-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="d9c76-125">Remarks</span></span>

<span data-ttu-id="d9c76-126">Les objets form appellent la méthode **IMAPIViewContext::GetSaveStream** pour récupérer un flux d’un objet qui implémente l’interface **IStream** pour prendre en charge la gestion du verbe Enregistrer sous dans la visionneuse de formulaires.</span><span class="sxs-lookup"><span data-stu-id="d9c76-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="d9c76-127">La méthode [IMAPIForm::D oVerb,](imapiform-doverb.md) implémentée dans le serveur de formulaires et appelée par la visionneuse de formulaire pour appeler un verbe, ne doit pas renvoyer tant que le message n’a pas été entièrement converti au format de texte approprié et placé dans le flux approprié.</span><span class="sxs-lookup"><span data-stu-id="d9c76-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d9c76-128">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="d9c76-128">Notes to callers</span></span>

<span data-ttu-id="d9c76-129">N’écrivez pas dans le flux pointé par  _ppstm_ avant **d’appeler GetSaveStream**.</span><span class="sxs-lookup"><span data-stu-id="d9c76-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="d9c76-130">Lorsque **GetSaveStream est de** retour, ne réinitialisez pas la position du pointeur de recherche.</span><span class="sxs-lookup"><span data-stu-id="d9c76-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="d9c76-131">Ce pointeur doit rester à la fin du texte du message enregistré.</span><span class="sxs-lookup"><span data-stu-id="d9c76-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d9c76-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9c76-132">See also</span></span>



[<span data-ttu-id="d9c76-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9c76-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

