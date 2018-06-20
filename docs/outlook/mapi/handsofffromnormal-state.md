---
title: État HandsOffFromNormal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d0b7baf4ab17d12145170961a43ca4be252146a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783454"
---
# <a name="handsofffromnormal-state"></a><span data-ttu-id="3b276-103">État HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="3b276-103">HandsOffFromNormal State</span></span>

  
  
<span data-ttu-id="3b276-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3b276-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3b276-105">L’état HandsOffFromNormal est très similaire à l’état [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="3b276-105">The HandsOffFromNormal state is very similar to the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> <span data-ttu-id="3b276-106">Il fait partie du processus de l’enregistrement du contenu d’un formulaire dans un stockage permanent.</span><span class="sxs-lookup"><span data-stu-id="3b276-106">It is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="3b276-107">Dans cet état, l’objet de formulaire doit ne pas apporter des modifications à la copie en mémoire des valeurs des propriétés du message, car il peut ne pas être une autre possibilité d’enregistrer ces modifications.</span><span class="sxs-lookup"><span data-stu-id="3b276-107">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="3b276-108">Le tableau suivant décrit les transitions autorisées à partir de l’état HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="3b276-108">The following table describes allowed transitions from the HandsOffFromNormal state.</span></span> 
  
|<span data-ttu-id="3b276-109">Méthode IPersistMessage ** **</span><span class="sxs-lookup"><span data-stu-id="3b276-109">****IPersistMessage** method**</span></span>|<span data-ttu-id="3b276-110">**Action**</span><span class="sxs-lookup"><span data-stu-id="3b276-110">**Action**</span></span>|<span data-ttu-id="3b276-111">**Nouvel état**</span><span class="sxs-lookup"><span data-stu-id="3b276-111">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b276-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage ! =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="3b276-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="3b276-113">Remplacer message de l’objet message par _pMessage_, qui est le remplacement du message révoqué par l’appel précédent à [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span><span class="sxs-lookup"><span data-stu-id="3b276-113">Replace the message object's message with  _pMessage_, which is the replacement for the message revoked by the previous call to [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span></span> <span data-ttu-id="3b276-114">Les données dans le nouveau message sont garanties être le même que dans le message révoqué.</span><span class="sxs-lookup"><span data-stu-id="3b276-114">The data in the new message is guaranteed to be the same as in the revoked message.</span></span> <span data-ttu-id="3b276-115">Le message ne doit pas être marqué comme nettoyé ni [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) doit être appelée après cet appel.</span><span class="sxs-lookup"><span data-stu-id="3b276-115">The message should not be marked as clean, nor should [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) be called after this call.</span></span> <span data-ttu-id="3b276-116">Si l’appel de **méthode SaveCompleted** réussit, entrez l’état [Normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="3b276-116">If the **SaveCompleted** call succeeds, enter the [Normal](normal-state.md) state.</span></span> <span data-ttu-id="3b276-117">Dans le cas contraire, rester à l’état HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="3b276-117">Otherwise, stay in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="3b276-118">Normal ou HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="3b276-118">Normal or HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="3b276-119">**IPersistMessage::SaveCompleted** (_pMessage ==_ NULL)</span><span class="sxs-lookup"><span data-stu-id="3b276-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="3b276-120">La valeur la dernière erreur E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="3b276-120">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="3b276-121">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="3b276-121">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="3b276-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)ou [IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="3b276-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="3b276-123">La valeur la dernière erreur E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="3b276-123">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="3b276-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="3b276-124">HandsOffFromNormal</span></span>  <br/> |
|[<span data-ttu-id="3b276-125">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="3b276-125">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="3b276-126">Renvoie la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="3b276-126">Return the last error.</span></span>  <br/> |<span data-ttu-id="3b276-127">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="3b276-127">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="3b276-128">Autres [IPersistMessage : IUnknown](ipersistmessageiunknown.md) méthodes ou autres interfaces</span><span class="sxs-lookup"><span data-stu-id="3b276-128">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="3b276-129">La valeur la dernière erreur E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="3b276-129">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="3b276-130">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="3b276-130">HandsOffFromNormal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b276-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b276-131">See also</span></span>



[<span data-ttu-id="3b276-132">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="3b276-132">Form States</span></span>](form-states.md)

