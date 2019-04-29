---
title: Envoi et réception de notifications de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4ee47b51a98cf732f4e9af2a87fa1734a7250208
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431854"
---
# <a name="sending-and-receiving-form-notifications"></a><span data-ttu-id="3af36-103">Envoi et réception de notifications de formulaire</span><span class="sxs-lookup"><span data-stu-id="3af36-103">Sending and Receiving Form Notifications</span></span>

  
  
<span data-ttu-id="3af36-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3af36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3af36-105">Les notifications de formulaire sont utilisées dans MAPI pour faciliter la communication à partir du formulaire vers votre afficheur, ainsi que de votre visionneuse vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="3af36-105">Form notifications are used in MAPI to facilitate communication both from the form to your viewer as well as from your viewer to the form.</span></span>
  
<span data-ttu-id="3af36-106">Les formulaires envoient des notifications à votre visionneuse lorsque l'un des événements suivants se produit:</span><span class="sxs-lookup"><span data-stu-id="3af36-106">Forms send notifications to your viewer when one of the following events occur:</span></span>
  
- <span data-ttu-id="3af36-107">Le formulaire est fermé.</span><span class="sxs-lookup"><span data-stu-id="3af36-107">The form is closed.</span></span>
    
- <span data-ttu-id="3af36-108">Un nouveau message est chargé dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="3af36-108">A new message is loaded in the form.</span></span>
    
- <span data-ttu-id="3af36-109">Une opération d'enregistrement est terminée.</span><span class="sxs-lookup"><span data-stu-id="3af36-109">A save operation is completed.</span></span>
    
- <span data-ttu-id="3af36-110">Un message est envoyé.</span><span class="sxs-lookup"><span data-stu-id="3af36-110">A message is sent.</span></span>
    
<span data-ttu-id="3af36-111">Chacun de ces types d'événements correspond à une méthode particulière dans [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md), l'une des interfaces que votre visionneuse de formulaire doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="3af36-111">Each of these event types correspond to a particular method in [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), one of the interfaces that your form viewer must implement.</span></span> <span data-ttu-id="3af36-112">Lorsqu'un événement se produit, le formulaire appelle la méthode **IMAPIViewAdviseSink** correspondante dans le récepteur d'avertissement de votre visionneuse.</span><span class="sxs-lookup"><span data-stu-id="3af36-112">When an event occurs, the form calls the corresponding **IMAPIViewAdviseSink** method in your viewer's advise sink.</span></span> <span data-ttu-id="3af36-113">Par exemple, lorsqu'un nouveau message arrive que votre visionneuse doit inclure dans son affichage, le formulaire appelle votre méthode [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="3af36-113">For example, when a new message arrives that your viewer should include in its display, the form calls your [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) method.</span></span> 
  
<span data-ttu-id="3af36-114">Implémentez votre récepteur d'avis d'affichage d'une manière adaptée à votre visionneuse; Il n'existe pas d'implémentation standard.</span><span class="sxs-lookup"><span data-stu-id="3af36-114">Implement your view advise sink in a way that makes sense for your viewer; there is no standard implementation.</span></span> <span data-ttu-id="3af36-115">Par exemple, dans **OnNewMessage** , vous pouvez mettre à jour l'affichage de la table des matières du dossier actif pour inclure le message nouvellement arrivé.</span><span class="sxs-lookup"><span data-stu-id="3af36-115">For example, in **OnNewMessage** you can update the view of the current folder's contents table to include the newly arrived message.</span></span> <span data-ttu-id="3af36-116">Dans [IMAPIViewAdviseSink:: OnSubmitted](imapiviewadvisesink-onsubmitted.md), la méthode qui est appelée lorsque vous recevez un événement de message envoyé, vous pouvez copier le message envoyé dans un dossier éléments envoyés.</span><span class="sxs-lookup"><span data-stu-id="3af36-116">In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), the method that is called when you receive a submitted message event, you can copy the submitted message to a Sent Items folder.</span></span>
  
<span data-ttu-id="3af36-117">Les formulaires reçoivent une notification à partir de votre visionneuse lorsqu'une modification se produit et que vous chargez un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="3af36-117">Forms receive notification from your viewer when a change occurs that affects the form and when you are loading a new message.</span></span> <span data-ttu-id="3af36-118">Pour avertir un formulaire, appelez l'une des méthodes de **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink:: OnChange](imapiformadvisesink-onchange.md) ou [IMAPIFormAdviseSink:: OnActivateNext](imapiformadvisesink-onactivatenext.md).</span><span class="sxs-lookup"><span data-stu-id="3af36-118">To notify a form, call one of the methods of **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) or [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span></span> <span data-ttu-id="3af36-119">Appelez **OnChange** pour communiquer le statut.</span><span class="sxs-lookup"><span data-stu-id="3af36-119">Call **OnChange** to communicate status.</span></span> <span data-ttu-id="3af36-120">Par exemple, si le formulaire affiche le dernier élément dans un dossier lors de l'arrivée d'un nouveau message, appelez la fonction **OnChange** avec l'indicateur VCSTATUS_NEXT défini pour indiquer au formulaire qu'il existe maintenant un élément suivant.</span><span class="sxs-lookup"><span data-stu-id="3af36-120">For example, if the form is displaying the last item in a folder when a new message arrives, call **OnChange** with the VCSTATUS_NEXT flag set to tell the form that there is now a next item.</span></span> 
  
<span data-ttu-id="3af36-121">Appelez **OnActivateNext** pour alerter le formulaire à l'arrivée d'un nouveau message qu'il peut ou ne peut pas afficher.</span><span class="sxs-lookup"><span data-stu-id="3af36-121">Call **OnActivateNext** to alert the form to the arrival of a new message that it may or may not be able to display.</span></span> <span data-ttu-id="3af36-122">TransMettez la classe de message du message à **OnActivateNext**.</span><span class="sxs-lookup"><span data-stu-id="3af36-122">Pass the message class of the message to **OnActivateNext**.</span></span> 
  
<span data-ttu-id="3af36-123">Les notifications d'un objet Form à l'application client sont gérées par l'interface **IMAPIViewAdviseSink** de l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="3af36-123">Notifications by a form object to the client application are handled by the client application's **IMAPIViewAdviseSink** interface.</span></span> <span data-ttu-id="3af36-124">Pour plus d'informations, consultez la rubrique [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="3af36-124">For more information, see [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).</span></span>
  

