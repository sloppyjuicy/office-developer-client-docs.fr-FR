---
title: IPersistMessage IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage
api_type:
- COM
ms.assetid: 40ec6dd4-2206-4e59-aafe-53aaf693f973
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7eb65bbae2fca6648c3a701dfa5c83c5bf297ec5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396182"
---
# <a name="ipersistmessage--iunknown"></a><span data-ttu-id="a46b3-103">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a46b3-103">IPersistMessage : IUnknown</span></span>

  
  
<span data-ttu-id="a46b3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a46b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a46b3-105">Permet les visionneuses de formulaire gérer le stockage d’un formulaire et à la transition entre les différents états possibles.</span><span class="sxs-lookup"><span data-stu-id="a46b3-105">Enables form viewers to handle the storage of a form and to transition between the various states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a46b3-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a46b3-106">Header file:</span></span>  <br/> |<span data-ttu-id="a46b3-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="a46b3-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="a46b3-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="a46b3-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="a46b3-109">Persistance des objets de message</span><span class="sxs-lookup"><span data-stu-id="a46b3-109">Persist message objects</span></span>  <br/> |
|<span data-ttu-id="a46b3-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="a46b3-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="a46b3-111">Objets de formulaire</span><span class="sxs-lookup"><span data-stu-id="a46b3-111">Form objects</span></span>  <br/> |
|<span data-ttu-id="a46b3-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="a46b3-112">Called by:</span></span>  <br/> |<span data-ttu-id="a46b3-113">Visionneuses de formulaire</span><span class="sxs-lookup"><span data-stu-id="a46b3-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="a46b3-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="a46b3-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a46b3-115">IID_IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="a46b3-115">IID_IPersistMessage</span></span>  <br/> |
|<span data-ttu-id="a46b3-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="a46b3-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="a46b3-117">LPPERSISTMESSAGE</span><span class="sxs-lookup"><span data-stu-id="a46b3-117">LPPERSISTMESSAGE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a46b3-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="a46b3-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a46b3-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="a46b3-119">GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="a46b3-120">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente dans l’objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="a46b3-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span>  <br/> |
|[<span data-ttu-id="a46b3-121">GetClassID</span><span class="sxs-lookup"><span data-stu-id="a46b3-121">GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="a46b3-122">Renvoie un identificateur qui représente le serveur de formulaire qui peut gérer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="a46b3-122">Returns an identifier that represents the form server that can manage the form.</span></span>  <br/> |
|[<span data-ttu-id="a46b3-123">IsDirty</span><span class="sxs-lookup"><span data-stu-id="a46b3-123">IsDirty</span></span>](ipersistmessage-isdirty.md) <br/> |<span data-ttu-id="a46b3-124">Vérifie le formulaire pour que les modifications qui ont été apportées depuis le dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a46b3-124">Checks the form for changes that were made since the last save.</span></span>  <br/> |
|[<span data-ttu-id="a46b3-125">InitNew</span><span class="sxs-lookup"><span data-stu-id="a46b3-125">InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="a46b3-126">Initialise un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="a46b3-126">Initializes a new message.</span></span>  <br/> |
|[<span data-ttu-id="a46b3-127">Load</span><span class="sxs-lookup"><span data-stu-id="a46b3-127">Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="a46b3-128">Charge le formulaire de message spécifié.</span><span class="sxs-lookup"><span data-stu-id="a46b3-128">Loads the form for a specified message.</span></span>  <br/> |
|[<span data-ttu-id="a46b3-129">Save</span><span class="sxs-lookup"><span data-stu-id="a46b3-129">Save</span></span>](ipersistmessage-save.md) <br/> |<span data-ttu-id="a46b3-130">Enregistre un formulaire révisé dans le message à partir de laquelle il a été chargé ou créé.</span><span class="sxs-lookup"><span data-stu-id="a46b3-130">Saves a revised form back to the message from which it was loaded or created.</span></span>  <br/> |
|[<span data-ttu-id="a46b3-131">Méthode SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="a46b3-131">SaveCompleted</span></span>](ipersistmessage-savecompleted.md) <br/> |<span data-ttu-id="a46b3-132">Avertit le formulaire qui un enregistrement opération a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="a46b3-132">Notifies the form that a save operation has been completed.</span></span>  <br/> |
|[<span data-ttu-id="a46b3-133">HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="a46b3-133">HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="a46b3-134">Le formulaire libérer le message en cours.</span><span class="sxs-lookup"><span data-stu-id="a46b3-134">Causes the form to release its current message.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a46b3-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="a46b3-135">Remarks</span></span>

<span data-ttu-id="a46b3-136">Tous les formulaires sont requis pour implémenter l’interface **IPersistMessage** .</span><span class="sxs-lookup"><span data-stu-id="a46b3-136">All forms are required to implement the **IPersistMessage** interface.</span></span> 
  
 <span data-ttu-id="a46b3-137">**IPersistMessage** fonctionne de façon similaire à l’interface OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a46b3-137">**IPersistMessage** works similarly to the OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="a46b3-138">Pour plus d’informations, voir les méthodes **IPersistStorage** .</span><span class="sxs-lookup"><span data-stu-id="a46b3-138">For more information, see the **IPersistStorage** methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a46b3-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a46b3-139">See also</span></span>



[<span data-ttu-id="a46b3-140">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a46b3-140">MAPI Interfaces</span></span>](mapi-interfaces.md)

