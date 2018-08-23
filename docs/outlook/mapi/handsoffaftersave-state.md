---
title: État HandsOffAfterSave
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 274e7206171e1874e3625896952f861d25f3b382
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564534"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="38462-103">État HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="38462-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="38462-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38462-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38462-105">L’état HandsOffAfterSave fait partie du processus de l’enregistrement du contenu d’un formulaire dans un stockage permanent.</span><span class="sxs-lookup"><span data-stu-id="38462-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="38462-106">Dans cet état, l’objet de formulaire doit ne pas apporter des modifications à la copie en mémoire des valeurs des propriétés du message, car il peut ne pas être une autre possibilité d’enregistrer ces modifications.</span><span class="sxs-lookup"><span data-stu-id="38462-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="38462-107">Le tableau suivant décrit les transitions autorisées à partir de l’état HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="38462-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="38462-108">**Méthode IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="38462-108">**IPersistMessage method**</span></span>|<span data-ttu-id="38462-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="38462-109">**Action**</span></span>|<span data-ttu-id="38462-110">**Nouvel état**</span><span class="sxs-lookup"><span data-stu-id="38462-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="38462-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage ! =_ NULL)</span><span class="sxs-lookup"><span data-stu-id="38462-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="38462-112">Ouvrir des objets incorporés.</span><span class="sxs-lookup"><span data-stu-id="38462-112">Open any embedded objects.</span></span> <span data-ttu-id="38462-113">Les données dans le message stockée dans _pMessage_ sont garanties être la même que le message dans l’appel [IPersistMessage::Save](ipersistmessage-save.md) précédent.</span><span class="sxs-lookup"><span data-stu-id="38462-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="38462-114">Si l’appel de **méthode SaveCompleted** réussit, entrez son état Normal.</span><span class="sxs-lookup"><span data-stu-id="38462-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="38462-115">Dans le cas contraire, la valeur de la dernière erreur E_OUTOFMEMORY et rester à l’état HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="38462-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="38462-116">[Normal](normal-state.md) ou HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="38462-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="38462-117">**IPersistMessage::SaveCompleted** (_pMessage ==_ NULL)</span><span class="sxs-lookup"><span data-stu-id="38462-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="38462-118">La valeur la dernière erreur E_INVALIDARG ou E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="38462-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="38462-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="38462-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="38462-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Enregistrer**ou [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="38462-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="38462-121">Définissez la dernière erreur à et E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="38462-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="38462-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="38462-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="38462-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="38462-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="38462-124">Chargement de l’objet de formulaire avec des données à partir du message cible.</span><span class="sxs-lookup"><span data-stu-id="38462-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="38462-125">Cet appel peut se produire lorsque l’objet de formulaire va le message suivant ou précédent dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="38462-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="38462-126">Normal</span><span class="sxs-lookup"><span data-stu-id="38462-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="38462-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="38462-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="38462-128">Renvoie la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="38462-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="38462-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="38462-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="38462-130">Autres [IPersistMessage : IUnknown](ipersistmessageiunknown.md) méthodes ou autres interfaces</span><span class="sxs-lookup"><span data-stu-id="38462-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="38462-131">Définissez la dernière erreur à et E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="38462-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="38462-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="38462-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38462-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38462-133">See also</span></span>



[<span data-ttu-id="38462-134">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="38462-134">Form States</span></span>](form-states.md)

