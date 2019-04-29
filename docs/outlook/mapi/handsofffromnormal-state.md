---
title: État HandsOffFromNormal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 17fa0f3d4e74ce7d717a94378880f2cc46150fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426470"
---
# <a name="handsofffromnormal-state"></a><span data-ttu-id="e00cc-103">État HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="e00cc-103">HandsOffFromNormal State</span></span>

  
  
<span data-ttu-id="e00cc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e00cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e00cc-105">L'État HandsOffFromNormal est très semblable à l'état [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="e00cc-105">The HandsOffFromNormal state is very similar to the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> <span data-ttu-id="e00cc-106">Il fait partie du processus d'enregistrement du contenu d'un formulaire dans un emplacement de stockage permanent.</span><span class="sxs-lookup"><span data-stu-id="e00cc-106">It is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="e00cc-107">Dans cet État, l'objet Form ne doit pas apporter de modifications aux copies en mémoire des propriétés du message, car il se peut qu'il n'y ait pas une autre opportunité d'enregistrer ces modifications.</span><span class="sxs-lookup"><span data-stu-id="e00cc-107">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="e00cc-108">Le tableau suivant décrit les transitions autorisées à partir de l'État HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="e00cc-108">The following table describes allowed transitions from the HandsOffFromNormal state.</span></span> 
  
|<span data-ttu-id="e00cc-109">IPersistMessage \* \* méthode \* \*</span><span class="sxs-lookup"><span data-stu-id="e00cc-109">\*\*\*\*IPersistMessage\*\* method\*\*</span></span>|<span data-ttu-id="e00cc-110">**Action**</span><span class="sxs-lookup"><span data-stu-id="e00cc-110">**Action**</span></span>|<span data-ttu-id="e00cc-111">**Nouvel État**</span><span class="sxs-lookup"><span data-stu-id="e00cc-111">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e00cc-112">[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ null)</span><span class="sxs-lookup"><span data-stu-id="e00cc-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="e00cc-113">Remplacez le message de l'objet message par _pMessage_, qui remplace le message révoqué par l'appel précédent à [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md).</span><span class="sxs-lookup"><span data-stu-id="e00cc-113">Replace the message object's message with  _pMessage_, which is the replacement for the message revoked by the previous call to [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span></span> <span data-ttu-id="e00cc-114">Il est garanti que les données du nouveau message sont les mêmes que dans le message révoqué.</span><span class="sxs-lookup"><span data-stu-id="e00cc-114">The data in the new message is guaranteed to be the same as in the revoked message.</span></span> <span data-ttu-id="e00cc-115">Le message ne doit pas être marqué comme Clean et [IMAPIViewAdviseSink:: OnSaved](imapiviewadvisesink-onsaved.md) être appelé après cet appel.</span><span class="sxs-lookup"><span data-stu-id="e00cc-115">The message should not be marked as clean, nor should [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) be called after this call.</span></span> <span data-ttu-id="e00cc-116">Si l'appel **SaveCompleted** réussit, entrez l'état [normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="e00cc-116">If the **SaveCompleted** call succeeds, enter the [Normal](normal-state.md) state.</span></span> <span data-ttu-id="e00cc-117">Sinon, restez dans l'État HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="e00cc-117">Otherwise, stay in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="e00cc-118">Normal ou HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="e00cc-118">Normal or HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="e00cc-119">**IPersistMessage:: SaveCompleted** (_pMessage = =_ null)</span><span class="sxs-lookup"><span data-stu-id="e00cc-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="e00cc-120">Définissez la dernière erreur sur E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="e00cc-120">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="e00cc-121">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="e00cc-121">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="e00cc-122">**HandsOffMessage**, [IPersistMessage:: Save](ipersistmessage-save.md), [IPersistMessage:: InitNew](ipersistmessage-initnew.md)ou [IPersistMessage:: Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="e00cc-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="e00cc-123">Définissez la dernière erreur sur E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="e00cc-123">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="e00cc-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="e00cc-124">HandsOffFromNormal</span></span>  <br/> |
|[<span data-ttu-id="e00cc-125">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e00cc-125">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="e00cc-126">Renvoyer la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="e00cc-126">Return the last error.</span></span>  <br/> |<span data-ttu-id="e00cc-127">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="e00cc-127">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="e00cc-128">Autres [IPersistMessage:](ipersistmessageiunknown.md) méthodes ou méthodes IUnknown à partir d'autres interfaces</span><span class="sxs-lookup"><span data-stu-id="e00cc-128">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="e00cc-129">Définissez la dernière erreur sur E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="e00cc-129">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="e00cc-130">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="e00cc-130">HandsOffFromNormal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e00cc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e00cc-131">See also</span></span>



[<span data-ttu-id="e00cc-132">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="e00cc-132">Form States</span></span>](form-states.md)

