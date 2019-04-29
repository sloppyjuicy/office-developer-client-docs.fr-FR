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
ms.openlocfilehash: 7ee641214e1eaae667af356fd8dbe51ff7dc7982
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419393"
---
# <a name="imapiviewcontextsetadvisesink"></a><span data-ttu-id="2be67-103">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="2be67-103">IMAPIViewContext::SetAdviseSink</span></span>

  
  
<span data-ttu-id="2be67-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2be67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2be67-105">Gère l'inscription d'un formulaire pour recevoir des notifications sur les modifications apportées à la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="2be67-105">Manages a form's registration to receive notifications about changes in the viewer.</span></span> 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a><span data-ttu-id="2be67-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2be67-106">Parameters</span></span>

 <span data-ttu-id="2be67-107">_pmvns_</span><span class="sxs-lookup"><span data-stu-id="2be67-107">_pmvns_</span></span>
  
> <span data-ttu-id="2be67-108">dans Pointeur vers un objet récepteur Form Advise ou NULL.</span><span class="sxs-lookup"><span data-stu-id="2be67-108">[in] Pointer to a form advise sink object or NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2be67-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2be67-109">Return value</span></span>

<span data-ttu-id="2be67-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="2be67-110">S_OK</span></span> 
  
> <span data-ttu-id="2be67-111">L'enregistrement ou l'annulation de la notification de formulaire a réussi.</span><span class="sxs-lookup"><span data-stu-id="2be67-111">The registration or cancellation for form notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2be67-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="2be67-112">Remarks</span></span>

<span data-ttu-id="2be67-113">Objets de formulaire appelez la méthode **IMAPIViewContext:: SetAdviseSink** pour vous inscrire afin d'en savoir plus sur les modifications apportées à la visionneuse de formulaires ou annuler une inscription précédente.</span><span class="sxs-lookup"><span data-stu-id="2be67-113">Form objects call the **IMAPIViewContext::SetAdviseSink** method to either register to learn about changes in the form viewer or cancel a prior registration.</span></span> <span data-ttu-id="2be67-114">Lorsque _pmvns_ est défini sur null, le formulaire veut annuler une inscription.</span><span class="sxs-lookup"><span data-stu-id="2be67-114">When  _pmvns_ is set to NULL, the form wants to cancel a registration.</span></span> <span data-ttu-id="2be67-115">Lorsque _pmvns_ pointe vers un récepteur de formulaire Advise valide, le formulaire veut s'inscrire aux notifications futures.</span><span class="sxs-lookup"><span data-stu-id="2be67-115">When  _pmvns_ points to a valid form advise sink, the form wants to register for future notifications.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2be67-116">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="2be67-116">Notes to implementers</span></span>

<span data-ttu-id="2be67-117">Lorsque **SetAdviseSink** inclut un pointeur de récepteur de formulaire, conservez une référence à celui-ci jusqu'à ce qu'un autre appel **SetAdviseSink** soit effectué pour annuler la notification.</span><span class="sxs-lookup"><span data-stu-id="2be67-117">When **SetAdviseSink** includes a form advise sink pointer, keep a reference to it until another **SetAdviseSink** call is made to cancel notification.</span></span> <span data-ttu-id="2be67-118">Envoyer une notification lorsqu'une modification survient dans votre visionneuse et lorsque vous chargez un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="2be67-118">Send a notification when a change occurs in your viewer and when you are loading a new message.</span></span> 
  
<span data-ttu-id="2be67-119">Pour plus d'informations, consultez la rubrique [envoi et réception](sending-and-receiving-form-notifications.md)de notifications de formulaire.</span><span class="sxs-lookup"><span data-stu-id="2be67-119">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2be67-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2be67-120">MFCMAPI reference</span></span>

<span data-ttu-id="2be67-121">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2be67-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2be67-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="2be67-122">**File**</span></span>|<span data-ttu-id="2be67-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="2be67-123">**Function**</span></span>|<span data-ttu-id="2be67-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="2be67-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2be67-125">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="2be67-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="2be67-126">CMyMAPIFormViewer:: SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="2be67-126">CMyMAPIFormViewer::SetAdviseSink</span></span>  <br/> |<span data-ttu-id="2be67-127">MFCMAPI implémente la méthode **IMAPIViewContext:: SetAdviseSink** dans cette fonction.</span><span class="sxs-lookup"><span data-stu-id="2be67-127">MFCMAPI implements the **IMAPIViewContext::SetAdviseSink** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2be67-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2be67-128">See also</span></span>



[<span data-ttu-id="2be67-129">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="2be67-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

