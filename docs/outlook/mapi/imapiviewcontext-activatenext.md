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
ms.openlocfilehash: 5b10f744e3033aab63820e4cd5e414f4c01c27cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410615"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="512fb-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="512fb-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="512fb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="512fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="512fb-105">Active le message suivant ou précédent dans l'ordre d'affichage.</span><span class="sxs-lookup"><span data-stu-id="512fb-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="512fb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="512fb-106">Parameters</span></span>

<span data-ttu-id="512fb-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="512fb-107">_ulDir_</span></span>
  
> <span data-ttu-id="512fb-108">dans Indicateurs d'État donnant des informations sur le message à activer.</span><span class="sxs-lookup"><span data-stu-id="512fb-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="512fb-109">Les paramètres d'indicateur valides sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="512fb-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="512fb-110">VCDIR_CATEGORY: la visionneuse doit activer un message dans une autre catégorie de l'affichage.</span><span class="sxs-lookup"><span data-stu-id="512fb-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="512fb-111">Le message à activer est le suivant:</span><span class="sxs-lookup"><span data-stu-id="512fb-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="512fb-112">Premier message de la catégorie d'affichage suivante si cet indicateur est **ou**Ed avec VCDIR_NEXT.</span><span class="sxs-lookup"><span data-stu-id="512fb-112">The first message in the next view category if this flag is **OR**ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="512fb-113">Dernier message de la catégorie vue précédente si cet indicateur est **ou**Ed avec VCDIR_PREV et si la catégorie précédente est développée.</span><span class="sxs-lookup"><span data-stu-id="512fb-113">The last message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="512fb-114">Premier message de la catégorie vue précédente si cet indicateur est **ou**Ed avec VCDIR_PREV et que la catégorie précédente n'est pas développée.</span><span class="sxs-lookup"><span data-stu-id="512fb-114">The first message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="512fb-115">Dans ce cas, la catégorie précédente passe automatiquement en expansion.</span><span class="sxs-lookup"><span data-stu-id="512fb-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="512fb-116">VCDIR_DELETE: la visionneuse doit activer le message suivant ou précédent, car le message actif a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="512fb-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="512fb-117">VCDIR_MOVE: la visionneuse doit activer le message suivant ou précédent, car le message actif a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="512fb-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="512fb-118">VCDIR_NEXT: la visionneuse doit activer le prochain message dans l'ordre d'affichage.</span><span class="sxs-lookup"><span data-stu-id="512fb-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="512fb-119">VCDIR_PREV: la visionneuse doit activer le message précédent dans l'ordre d'affichage.</span><span class="sxs-lookup"><span data-stu-id="512fb-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="512fb-120">VCDIR_UNREAD: la visionneuse doit activer le message non lu suivant ou précédent dans l'ordre d'affichage.</span><span class="sxs-lookup"><span data-stu-id="512fb-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="512fb-121">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="512fb-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="512fb-122">dans Pointeur vers une structure **Rect** Windows contenant la taille et la position de la fenêtre à utiliser pour afficher le message activé.</span><span class="sxs-lookup"><span data-stu-id="512fb-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="512fb-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="512fb-123">Return value</span></span>

<span data-ttu-id="512fb-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="512fb-124">S_OK</span></span> 
  
> <span data-ttu-id="512fb-125">Le message a été correctement activé.</span><span class="sxs-lookup"><span data-stu-id="512fb-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="512fb-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="512fb-126">S_FALSE</span></span> 
  
> <span data-ttu-id="512fb-127">Le message a été activé avec succès, mais un autre type de formulaire a été ouvert dans le processus.</span><span class="sxs-lookup"><span data-stu-id="512fb-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="512fb-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="512fb-128">Remarks</span></span>

<span data-ttu-id="512fb-129">Les objets de formulaire appellent la méthode **IMAPIViewContext:: ActivateNext,** pour modifier le message qui est affiché à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="512fb-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="512fb-130">La valeur transmise dans le paramètre _ulDir_ indique quel message doit être activé et, dans certains cas, pourquoi.</span><span class="sxs-lookup"><span data-stu-id="512fb-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="512fb-131">Les indicateurs VCDIR_NEXT et VCDIR_PREVIOUS correspondent respectivement aux utilisateurs de la commande **suivante** ou **précédente** dans une vue.</span><span class="sxs-lookup"><span data-stu-id="512fb-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="512fb-132">Ces opérations correspondent généralement au passage d'un message vers le haut ou vers le bas dans la liste des messages de la visionneuse de formulaires.</span><span class="sxs-lookup"><span data-stu-id="512fb-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="512fb-133">Les indicateurs VCDIR_DELETE et VCDIR_MOVE sont définis par les méthodes [IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md) et [IMAPIMessageSite:: MoveMessage](imapimessagesite-movemessage.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="512fb-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="512fb-134">Les implémentations de ces méthodes appellent **ActivateNext,** avec la direction appropriée, puis effectuent l'opération demandée sur le message si l'appel de **ActivateNext,** n'a pas échoué.</span><span class="sxs-lookup"><span data-stu-id="512fb-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="512fb-135">Les visionneuses de formulaires permettent généralement aux utilisateurs de spécifier le sens de déplacement dans la liste des messages.</span><span class="sxs-lookup"><span data-stu-id="512fb-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="512fb-136">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="512fb-136">Notes to implementers</span></span>

<span data-ttu-id="512fb-137">Votre implémentation de [IMAPIViewContext:: ActivateNext,](imapiviewcontext-activatenext.md) crée le message suivant ou précédent dans le dossier, en fonction de la valeur de _ulDir_, le message actif.</span><span class="sxs-lookup"><span data-stu-id="512fb-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="512fb-138">Une fois **ActivateNext,** renvoyé, appelez [IMAPIMessageSite:: GetMessage](imapimessagesite-getmessage.md) pour obtenir un pointeur vers le message nouvellement activé.</span><span class="sxs-lookup"><span data-stu-id="512fb-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="512fb-139">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="512fb-139">Notes to callers</span></span>

<span data-ttu-id="512fb-140">Si **ActivateNext,** renvoie S_FALSE ou s'il n'existe pas de message en cours, effectuez votre procédure d'arrêt normale, qui doit inclure l'appel de la méthode [IMAPIForm:: ShutdownForm](imapiform-shutdownform.md) de votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="512fb-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="512fb-141">Si un message suivant ou précédent est affiché, utilisez le rectangle de fenêtre passé dans le paramètre _prcPosRect_ pour l'afficher.</span><span class="sxs-lookup"><span data-stu-id="512fb-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="512fb-142">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="512fb-142">MFCMAPI reference</span></span>

<span data-ttu-id="512fb-143">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="512fb-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="512fb-144">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="512fb-144">**File**</span></span>|<span data-ttu-id="512fb-145">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="512fb-145">**Function**</span></span>|<span data-ttu-id="512fb-146">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="512fb-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="512fb-147">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="512fb-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="512fb-148">CMyMAPIFormViewer:: ActivateNext,</span><span class="sxs-lookup"><span data-stu-id="512fb-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="512fb-149">MFCMAPI implémente la méthode **IMAPIViewContext:: ActivateNext,** dans cette fonction.</span><span class="sxs-lookup"><span data-stu-id="512fb-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="512fb-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="512fb-150">See also</span></span>

- [<span data-ttu-id="512fb-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="512fb-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="512fb-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="512fb-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- [<span data-ttu-id="512fb-153">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="512fb-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

