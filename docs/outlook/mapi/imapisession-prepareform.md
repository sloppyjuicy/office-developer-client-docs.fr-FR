---
title: IMAPISessionPrepareForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335762"
---
# <a name="imapisessionprepareform"></a><span data-ttu-id="6bf07-103">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="6bf07-103">IMAPISession::PrepareForm</span></span>

  
  
<span data-ttu-id="6bf07-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bf07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bf07-105">Crée un jeton numérique que la méthode [IMAPISession::ShowForm](imapisession-showform.md) utilise pour accéder à un message.</span><span class="sxs-lookup"><span data-stu-id="6bf07-105">Creates a numeric token that the [IMAPISession::ShowForm](imapisession-showform.md) method uses to access a message.</span></span> 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a><span data-ttu-id="6bf07-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6bf07-106">Parameters</span></span>

 <span data-ttu-id="6bf07-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6bf07-107">_lpInterface_</span></span>
  
> <span data-ttu-id="6bf07-108">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au message.</span><span class="sxs-lookup"><span data-stu-id="6bf07-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message.</span></span> <span data-ttu-id="6bf07-109">La **transmission de** null entraîne l’utilisation de l’interface standard, ou [IMessage.](imessageimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="6bf07-109">Passing **null** results in the standard interface, or [IMessage](imessageimapiprop.md), being used.</span></span> <span data-ttu-id="6bf07-110">Le  _paramètre lpInterface_ doit être **null** ou IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="6bf07-110">The  _lpInterface_ parameter must be **null** or IID_IMessage.</span></span> 
    
 <span data-ttu-id="6bf07-111">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="6bf07-111">_lpMessage_</span></span>
  
> <span data-ttu-id="6bf07-112">[in] Pointeur vers le message à afficher dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="6bf07-112">[in] A pointer to the message to be displayed in the form.</span></span>
    
 <span data-ttu-id="6bf07-113">_lpulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="6bf07-113">_lpulMessageToken_</span></span>
  
> <span data-ttu-id="6bf07-114">[out] Pointeur vers un jeton de message, qui est utilisé par la méthode **IMAPISession::ShowForm** pour accéder au message pointé par  _lpMessage_.</span><span class="sxs-lookup"><span data-stu-id="6bf07-114">[out] A pointer to a message token, which is used by the **IMAPISession::ShowForm** method to access the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6bf07-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6bf07-115">Return value</span></span>

<span data-ttu-id="6bf07-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6bf07-116">S_OK</span></span> 
  
> <span data-ttu-id="6bf07-117">La préparation du formulaire a réussi.</span><span class="sxs-lookup"><span data-stu-id="6bf07-117">The form preparation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6bf07-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="6bf07-118">Remarks</span></span>

<span data-ttu-id="6bf07-119">La méthode **IMAPISession::P repareForm** crée un jeton de message pour le message pointé par le paramètre  _lpMessage_ et appelle la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) du message.</span><span class="sxs-lookup"><span data-stu-id="6bf07-119">The **IMAPISession::PrepareForm** method creates a message token for the message pointed to by the  _lpMessage_ parameter and calls the message's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="6bf07-120">Ce jeton est transmis dans le  _paramètre ulMessageToken_ à **IMAPISession::ShowForm**.</span><span class="sxs-lookup"><span data-stu-id="6bf07-120">This token is passed in the  _ulMessageToken_ parameter to **IMAPISession::ShowForm**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6bf07-121">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="6bf07-121">Notes to callers</span></span>

<span data-ttu-id="6bf07-122">Si l’appel à **PrepareForm** réussit, relâchez le message pointé par  _lpMessage_ en appelant sa méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) avant d’appeler **ShowForm**.</span><span class="sxs-lookup"><span data-stu-id="6bf07-122">If the call to **PrepareForm** succeeds, release the message pointed to by  _lpMessage_ by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method before you call **ShowForm**.</span></span> <span data-ttu-id="6bf07-123">L’échec de la libération du message avant l’appel **de ShowForm** peut provoquer des fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="6bf07-123">Failure to release the message before you call **ShowForm** can cause memory leaks.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6bf07-124">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6bf07-124">MFCMAPI reference</span></span>

<span data-ttu-id="6bf07-125">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6bf07-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6bf07-126">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="6bf07-126">**File**</span></span>|<span data-ttu-id="6bf07-127">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="6bf07-127">**Function**</span></span>|<span data-ttu-id="6bf07-128">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="6bf07-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6bf07-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="6bf07-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="6bf07-130">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="6bf07-130">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="6bf07-131">MFCMAPI utilise la méthode **IMAPISession::P repareForm,** avec **IMAPISession::ShowForm**, pour afficher un message sous forme modale.</span><span class="sxs-lookup"><span data-stu-id="6bf07-131">MFCMAPI uses the **IMAPISession::PrepareForm** method, along with **IMAPISession::ShowForm**, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6bf07-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bf07-132">See also</span></span>



[<span data-ttu-id="6bf07-133">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="6bf07-133">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="6bf07-134">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6bf07-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="6bf07-135">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="6bf07-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

