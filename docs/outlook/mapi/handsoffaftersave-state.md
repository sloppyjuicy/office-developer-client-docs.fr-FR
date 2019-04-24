---
title: État HandsOffAfterSave
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299523"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="fe536-103">État HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="fe536-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="fe536-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe536-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe536-105">L'État HandsOffAfterSave fait partie du processus d'enregistrement du contenu d'un formulaire dans un emplacement de stockage permanent.</span><span class="sxs-lookup"><span data-stu-id="fe536-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="fe536-106">Dans cet État, l'objet Form ne doit pas apporter de modifications aux copies en mémoire des propriétés du message, car il se peut qu'il n'y ait pas une autre opportunité d'enregistrer ces modifications.</span><span class="sxs-lookup"><span data-stu-id="fe536-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="fe536-107">Le tableau suivant décrit les transitions autorisées à partir de l'État HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="fe536-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="fe536-108">**Méthode IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="fe536-108">**IPersistMessage method**</span></span>|<span data-ttu-id="fe536-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="fe536-109">**Action**</span></span>|<span data-ttu-id="fe536-110">**Nouvel État**</span><span class="sxs-lookup"><span data-stu-id="fe536-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fe536-111">[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ null)</span><span class="sxs-lookup"><span data-stu-id="fe536-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="fe536-112">Ouvrez les objets incorporés.</span><span class="sxs-lookup"><span data-stu-id="fe536-112">Open any embedded objects.</span></span> <span data-ttu-id="fe536-113">Les données contenues dans le message stocké dans _pMessage_ sont garanties de la même manière que le message de l'appel [IPersistMessage:: Save](ipersistmessage-save.md) précédent.</span><span class="sxs-lookup"><span data-stu-id="fe536-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="fe536-114">Si l'appel **SaveCompleted** réussit, entrez l'état normal.</span><span class="sxs-lookup"><span data-stu-id="fe536-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="fe536-115">Dans le cas contraire, définissez la dernière erreur sur E_OUTOFMEMORY et restez dans l'État HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="fe536-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="fe536-116">[Normal](normal-state.md) ou HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="fe536-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="fe536-117">**IPersistMessage:: SaveCompleted** (_pMessage = =_ null)</span><span class="sxs-lookup"><span data-stu-id="fe536-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="fe536-118">Définissez la dernière erreur sur E_INVALIDARG ou E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="fe536-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="fe536-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="fe536-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="fe536-120">[IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md), **Enregistrer**ou [IPersistMessage:: InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="fe536-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="fe536-121">Définissez la dernière erreur sur et renvoyez E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="fe536-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="fe536-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="fe536-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="fe536-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="fe536-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="fe536-124">Charge l'objet Form avec les données du message cible.</span><span class="sxs-lookup"><span data-stu-id="fe536-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="fe536-125">Cet appel peut se produire lorsque l'objet de formulaire passe au message suivant ou précédent dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="fe536-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="fe536-126">Normal</span><span class="sxs-lookup"><span data-stu-id="fe536-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="fe536-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="fe536-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="fe536-128">Renvoyer la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="fe536-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="fe536-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="fe536-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="fe536-130">Autres [IPersistMessage:](ipersistmessageiunknown.md) méthodes ou méthodes IUnknown à partir d'autres interfaces</span><span class="sxs-lookup"><span data-stu-id="fe536-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="fe536-131">Définissez la dernière erreur sur et renvoyez E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="fe536-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="fe536-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="fe536-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe536-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe536-133">See also</span></span>



[<span data-ttu-id="fe536-134">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="fe536-134">Form States</span></span>](form-states.md)

