---
title: IMAPIViewContextSetAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 555bb4820dc36934fb28197b7e222633a5248125
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583182"
---
# <a name="imapiviewcontextsetadvisesink"></a><span data-ttu-id="a0307-103">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="a0307-103">IMAPIViewContext::SetAdviseSink</span></span>

  
  
<span data-ttu-id="a0307-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0307-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0307-105">Gère l’inscription d’un formulaire pour recevoir des notifications sur les modifications dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="a0307-105">Manages a form's registration to receive notifications about changes in the viewer.</span></span> 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a><span data-ttu-id="a0307-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0307-106">Parameters</span></span>

 <span data-ttu-id="a0307-107">_pmvns_</span><span class="sxs-lookup"><span data-stu-id="a0307-107">_pmvns_</span></span>
  
> <span data-ttu-id="a0307-108">[in] Pointeur vers un formulaire de notification objet récepteur ou NULL.</span><span class="sxs-lookup"><span data-stu-id="a0307-108">[in] Pointer to a form advise sink object or NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a0307-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a0307-109">Return value</span></span>

<span data-ttu-id="a0307-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0307-110">S_OK</span></span> 
  
> <span data-ttu-id="a0307-111">L’inscription ou l’annulation de la notification de formulaire a réussi.</span><span class="sxs-lookup"><span data-stu-id="a0307-111">The registration or cancellation for form notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0307-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="a0307-112">Remarks</span></span>

<span data-ttu-id="a0307-113">Objets de formulaire appeler la méthode de **IMAPIViewContext::SetAdviseSink** pouvez en savoir plus sur les modifications dans la visionneuse de formulaire ou d’annuler une inscription préalable.</span><span class="sxs-lookup"><span data-stu-id="a0307-113">Form objects call the **IMAPIViewContext::SetAdviseSink** method to either register to learn about changes in the form viewer or cancel a prior registration.</span></span> <span data-ttu-id="a0307-114">Lorsque _pmvns_ est défini sur NULL, le formulaire souhaite annuler un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a0307-114">When  _pmvns_ is set to NULL, the form wants to cancel a registration.</span></span> <span data-ttu-id="a0307-115">Lorsque le récepteur de notification de points _pmvns_ à un formulaire valid, le formulaire souhaite enregistrer les notifications ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a0307-115">When  _pmvns_ points to a valid form advise sink, the form wants to register for future notifications.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a0307-116">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="a0307-116">Notes to implementers</span></span>

<span data-ttu-id="a0307-117">Lorsque **SetAdviseSink** comprend un formulaire pointeur du récepteur de notification, conserver une référence à celui-ci jusqu'à ce qu’un autre appel **SetAdviseSink** est effectué pour annuler la notification.</span><span class="sxs-lookup"><span data-stu-id="a0307-117">When **SetAdviseSink** includes a form advise sink pointer, keep a reference to it until another **SetAdviseSink** call is made to cancel notification.</span></span> <span data-ttu-id="a0307-118">Envoyer une notification lorsque cet événement se produit une modification dans votre visionneuse et lors du chargement d’un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="a0307-118">Send a notification when a change occurs in your viewer and when you are loading a new message.</span></span> 
  
<span data-ttu-id="a0307-119">Pour plus d’informations, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="a0307-119">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a0307-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a0307-120">MFCMAPI reference</span></span>

<span data-ttu-id="a0307-121">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a0307-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a0307-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="a0307-122">**File**</span></span>|<span data-ttu-id="a0307-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="a0307-123">**Function**</span></span>|<span data-ttu-id="a0307-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="a0307-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0307-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="a0307-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="a0307-126">CMyMAPIFormViewer::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="a0307-126">CMyMAPIFormViewer::SetAdviseSink</span></span>  <br/> |<span data-ttu-id="a0307-127">MFCMAPI implémente la méthode **IMAPIViewContext::SetAdviseSink** dans cette fonction.</span><span class="sxs-lookup"><span data-stu-id="a0307-127">MFCMAPI implements the **IMAPIViewContext::SetAdviseSink** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a0307-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0307-128">See also</span></span>



[<span data-ttu-id="a0307-129">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="a0307-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

