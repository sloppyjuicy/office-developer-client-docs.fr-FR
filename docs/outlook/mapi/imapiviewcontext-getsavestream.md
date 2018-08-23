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
ms.openlocfilehash: 47ea122fce7969b326dbd48f875696b91de464f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568573"
---
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="2d034-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="2d034-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="2d034-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d034-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d034-105">Récupère un flux de données à utiliser pour l’enregistrement du message en cours.</span><span class="sxs-lookup"><span data-stu-id="2d034-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="2d034-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d034-106">Parameters</span></span>

 <span data-ttu-id="2d034-107">_pulFlags_</span><span class="sxs-lookup"><span data-stu-id="2d034-107">_pulFlags_</span></span>
  
> <span data-ttu-id="2d034-108">[out] Pointeur vers un masque de bits d’indicateurs qui contrôle la façon dont le texte du message doit être enregistré.</span><span class="sxs-lookup"><span data-stu-id="2d034-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="2d034-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="2d034-109">The following flag can be set:</span></span>
    
<span data-ttu-id="2d034-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2d034-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2d034-111">Le texte du message est enregistré au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="2d034-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="2d034-112">Si l’indicateur MAPI_UNICODE n’est pas définie, le texte est enregistré au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="2d034-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="2d034-113">_pulFormat_</span><span class="sxs-lookup"><span data-stu-id="2d034-113">_pulFormat_</span></span>
  
> <span data-ttu-id="2d034-114">[out] Pointeur vers un masque de bits d’indicateurs qui contrôle le format du texte enregistré.</span><span class="sxs-lookup"><span data-stu-id="2d034-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="2d034-115">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="2d034-115">The following flags can be set:</span></span>
    
<span data-ttu-id="2d034-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="2d034-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="2d034-117">Le texte du message doit être enregistré en tant que texte mis en forme dans le Format de texte enrichi (RTF).</span><span class="sxs-lookup"><span data-stu-id="2d034-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="2d034-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="2d034-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="2d034-119">Le texte du message doit être enregistré en tant que texte brut.</span><span class="sxs-lookup"><span data-stu-id="2d034-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="2d034-120">_ppstm_</span><span class="sxs-lookup"><span data-stu-id="2d034-120">_ppstm_</span></span>
  
> <span data-ttu-id="2d034-121">[out] Pointeur vers un pointeur vers le flux qui contiendra le message enregistré.</span><span class="sxs-lookup"><span data-stu-id="2d034-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2d034-122">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="2d034-122">Return value</span></span>

<span data-ttu-id="2d034-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="2d034-123">S_OK</span></span> 
  
> <span data-ttu-id="2d034-124">Le flux de données a été récupéré correctement.</span><span class="sxs-lookup"><span data-stu-id="2d034-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2d034-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="2d034-125">Remarks</span></span>

<span data-ttu-id="2d034-126">Objets de formulaire appeler la méthode **IMAPIViewContext::GetSaveStream** pour récupérer un objet qui implémente l’interface **IStream** pour prendre en charge la gestion de l’action Enregistrer sous dans la visionneuse de formulaire de flux.</span><span class="sxs-lookup"><span data-stu-id="2d034-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="2d034-127">La méthode [IMAPIForm::DoVerb](imapiform-doverb.md) , qui est implémentée sous la forme et appelée par la visionneuse de formulaire pour appeler un verbe, ne doit pas renvoyer jusqu'à ce que le message est entièrement converti au format texte approprié et placé dans le flux approprié.</span><span class="sxs-lookup"><span data-stu-id="2d034-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2d034-128">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="2d034-128">Notes to callers</span></span>

<span data-ttu-id="2d034-129">Ne pas écrire dans le flux indiqué par _ppstm_ avant d’appeler **GetSaveStream**.</span><span class="sxs-lookup"><span data-stu-id="2d034-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="2d034-130">Lorsque **GetSaveStream** renvoie, ne pas réinitialiser la position du pointeur de la recherche.</span><span class="sxs-lookup"><span data-stu-id="2d034-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="2d034-131">Ce pointeur doit rester à la fin du texte du message enregistré.</span><span class="sxs-lookup"><span data-stu-id="2d034-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d034-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d034-132">See also</span></span>



[<span data-ttu-id="2d034-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d034-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

