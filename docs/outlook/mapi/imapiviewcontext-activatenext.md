---
title: IMAPIViewContextActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.ActivateNext
api_type:
- COM
ms.assetid: 25ce90ac-526e-48a0-9edb-bd266375d4f4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6613e4168fea6536b1df873da12f2c215be515bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588502"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="ff3de-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="ff3de-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="ff3de-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff3de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff3de-105">Active le message suivant ou précédent dans l’ordre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ff3de-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="ff3de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff3de-106">Parameters</span></span>

<span data-ttu-id="ff3de-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="ff3de-107">_ulDir_</span></span>
  
> <span data-ttu-id="ff3de-108">[in] Indicateurs d’état en donnant des informations sur le message à activer.</span><span class="sxs-lookup"><span data-stu-id="ff3de-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="ff3de-109">Paramètres de l’indicateur valides sont :</span><span class="sxs-lookup"><span data-stu-id="ff3de-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="ff3de-110">VCDIR_CATEGORY : La visionneuse doit activer un message dans une autre catégorie de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="ff3de-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="ff3de-111">Le message doit être activé est la suivante :</span><span class="sxs-lookup"><span data-stu-id="ff3de-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="ff3de-112">Le premier message dans la catégorie de vue suivante si cet indicateur est ed **ou**avec VCDIR_NEXT.</span><span class="sxs-lookup"><span data-stu-id="ff3de-112">The first message in the next view category if this flag is **OR**ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="ff3de-113">Le dernier message de la catégorie de vue précédente si cet indicateur est **liées avec VCDIR_PREV**et à la catégorie précédente est développé.</span><span class="sxs-lookup"><span data-stu-id="ff3de-113">The last message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="ff3de-114">Le premier message dans la catégorie de vue précédente si cet indicateur est **liées avec VCDIR_PREV**et de la catégorie précédente n’est pas développé.</span><span class="sxs-lookup"><span data-stu-id="ff3de-114">The first message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="ff3de-115">Dans ce cas, la catégorie précédente subit extension automatique.</span><span class="sxs-lookup"><span data-stu-id="ff3de-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="ff3de-116">VCDIR_DELETE : La visionneuse doit activer le message suivant ou précédent, car le message en cours a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="ff3de-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="ff3de-117">VCDIR_MOVE : La visionneuse doit activer le message suivant ou précédent, car le message en cours a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="ff3de-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="ff3de-118">VCDIR_NEXT : La visionneuse doit activer le message suivant dans l’ordre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ff3de-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="ff3de-119">VCDIR_PREV : La visionneuse doit activer le message précédent dans l’ordre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ff3de-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="ff3de-120">VCDIR_UNREAD : La visionneuse doit activer le message non lu suivant ou précédent dans l’ordre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ff3de-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="ff3de-121">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="ff3de-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="ff3de-122">[in] Pointeur vers un **RECT** Windows structure contenant la taille et la position de la fenêtre à utiliser pour afficher le message activé.</span><span class="sxs-lookup"><span data-stu-id="ff3de-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ff3de-123">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="ff3de-123">Return value</span></span>

<span data-ttu-id="ff3de-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="ff3de-124">S_OK</span></span> 
  
> <span data-ttu-id="ff3de-125">Le message a été activé avec succès.</span><span class="sxs-lookup"><span data-stu-id="ff3de-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="ff3de-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="ff3de-126">S_FALSE</span></span> 
  
> <span data-ttu-id="ff3de-127">Le message a été activé avec succès, mais un autre type de formulaire a été ouvert dans le processus.</span><span class="sxs-lookup"><span data-stu-id="ff3de-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff3de-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="ff3de-128">Remarks</span></span>

<span data-ttu-id="ff3de-129">Objets de formulaire appeler la méthode **IMAPIViewContext::ActivateNext** pour modifier le message affiché à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ff3de-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="ff3de-130">La valeur passée dans le paramètre _ulDir_ indique que le message doit être activé et, dans certains cas, pourquoi.</span><span class="sxs-lookup"><span data-stu-id="ff3de-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="ff3de-131">Les indicateurs VCDIR_NEXT et VCDIR_PREVIOUS correspondent aux utilisateurs de choisir la commande **suivant** ou **précédent** dans un affichage, respectivement.</span><span class="sxs-lookup"><span data-stu-id="ff3de-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="ff3de-132">Ces opérations correspondent généralement à un déplacement haut ou vers le bas d’un message dans la liste de l’utilisateur du formulaire des messages.</span><span class="sxs-lookup"><span data-stu-id="ff3de-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="ff3de-133">Les indicateurs VCDIR_DELETE et VCDIR_MOVE sont définis par les [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) et les méthodes de [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="ff3de-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="ff3de-134">Implémentations des méthodes suivantes appelez **ActivateNext** avec le sens approprié, puis effectuez l’opération demandée dans le message si l’appel **ActivateNext** sans erreur.</span><span class="sxs-lookup"><span data-stu-id="ff3de-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="ff3de-135">Formulaire permettent généralement aux utilisateurs de spécifier le sens de déplacement dans la liste des messages.</span><span class="sxs-lookup"><span data-stu-id="ff3de-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ff3de-136">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="ff3de-136">Notes to implementers</span></span>

<span data-ttu-id="ff3de-137">Votre implémentation de [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) rend le message suivant ou précédent dans le dossier, selon la valeur _ulDir_, le message en cours.</span><span class="sxs-lookup"><span data-stu-id="ff3de-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="ff3de-138">Une fois **ActivateNext** renvoie, appelez [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) pour obtenir un pointeur vers le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="ff3de-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ff3de-139">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="ff3de-139">Notes to callers</span></span>

<span data-ttu-id="ff3de-140">Si **ActivateNext** renvoie S_FALSE, ou si un message en cours n’est pas présent, effectuez la procédure d’arrêt normal qui doit inclure l’appel de méthode de [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) de votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="ff3de-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="ff3de-141">Si un message précédent ou suivant est affiché, utilisez le rectangle de fenêtre passé dans le paramètre _prcPosRect_ pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="ff3de-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ff3de-142">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ff3de-142">MFCMAPI reference</span></span>

<span data-ttu-id="ff3de-143">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ff3de-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ff3de-144">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="ff3de-144">**File**</span></span>|<span data-ttu-id="ff3de-145">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="ff3de-145">**Function**</span></span>|<span data-ttu-id="ff3de-146">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="ff3de-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff3de-147">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="ff3de-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="ff3de-148">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="ff3de-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="ff3de-149">MFCMAPI implémente la méthode **IMAPIViewContext::ActivateNext** dans cette fonction.</span><span class="sxs-lookup"><span data-stu-id="ff3de-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff3de-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff3de-150">See also</span></span>

- [<span data-ttu-id="ff3de-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="ff3de-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="ff3de-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff3de-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- [<span data-ttu-id="ff3de-153">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="ff3de-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

