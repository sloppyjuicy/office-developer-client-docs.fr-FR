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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7eb65bbae2fca6648c3a701dfa5c83c5bf297ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309603"
---
# <a name="ipersistmessage--iunknown"></a><span data-ttu-id="8f44a-103">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8f44a-103">IPersistMessage : IUnknown</span></span>

  
  
<span data-ttu-id="8f44a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f44a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f44a-105">Permet aux visionneuses de formulaires de gérer le stockage d'un formulaire et de passer d'un État à l'autre.</span><span class="sxs-lookup"><span data-stu-id="8f44a-105">Enables form viewers to handle the storage of a form and to transition between the various states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8f44a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8f44a-106">Header file:</span></span>  <br/> |<span data-ttu-id="8f44a-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="8f44a-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="8f44a-108">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="8f44a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8f44a-109">Conserver les objets message</span><span class="sxs-lookup"><span data-stu-id="8f44a-109">Persist message objects</span></span>  <br/> |
|<span data-ttu-id="8f44a-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="8f44a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8f44a-111">Objets de formulaires</span><span class="sxs-lookup"><span data-stu-id="8f44a-111">Form objects</span></span>  <br/> |
|<span data-ttu-id="8f44a-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="8f44a-112">Called by:</span></span>  <br/> |<span data-ttu-id="8f44a-113">Visionneuses de formulaires</span><span class="sxs-lookup"><span data-stu-id="8f44a-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="8f44a-114">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="8f44a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8f44a-115">IID_IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="8f44a-115">IID_IPersistMessage</span></span>  <br/> |
|<span data-ttu-id="8f44a-116">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="8f44a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="8f44a-117">LPPERSISTMESSAGE</span><span class="sxs-lookup"><span data-stu-id="8f44a-117">LPPERSISTMESSAGE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8f44a-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="8f44a-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8f44a-119">Généré</span><span class="sxs-lookup"><span data-stu-id="8f44a-119">GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="8f44a-120">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente dans l'objet Form.</span><span class="sxs-lookup"><span data-stu-id="8f44a-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span>  <br/> |
|[<span data-ttu-id="8f44a-121">GetClassID</span><span class="sxs-lookup"><span data-stu-id="8f44a-121">GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="8f44a-122">Renvoie un identificateur qui représente le serveur de formulaires qui peut gérer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="8f44a-122">Returns an identifier that represents the form server that can manage the form.</span></span>  <br/> |
|[<span data-ttu-id="8f44a-123">IsDirty</span><span class="sxs-lookup"><span data-stu-id="8f44a-123">IsDirty</span></span>](ipersistmessage-isdirty.md) <br/> |<span data-ttu-id="8f44a-124">Vérifie si le formulaire a été modifié depuis le dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8f44a-124">Checks the form for changes that were made since the last save.</span></span>  <br/> |
|[<span data-ttu-id="8f44a-125">InitNew</span><span class="sxs-lookup"><span data-stu-id="8f44a-125">InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="8f44a-126">Initialise un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="8f44a-126">Initializes a new message.</span></span>  <br/> |
|[<span data-ttu-id="8f44a-127">Load</span><span class="sxs-lookup"><span data-stu-id="8f44a-127">Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="8f44a-128">Charge le formulaire pour un message spécifié.</span><span class="sxs-lookup"><span data-stu-id="8f44a-128">Loads the form for a specified message.</span></span>  <br/> |
|[<span data-ttu-id="8f44a-129">Save</span><span class="sxs-lookup"><span data-stu-id="8f44a-129">Save</span></span>](ipersistmessage-save.md) <br/> |<span data-ttu-id="8f44a-130">RéEnregistre un formulaire révisé dans le message à partir duquel il a été chargé ou créé.</span><span class="sxs-lookup"><span data-stu-id="8f44a-130">Saves a revised form back to the message from which it was loaded or created.</span></span>  <br/> |
|[<span data-ttu-id="8f44a-131">SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="8f44a-131">SaveCompleted</span></span>](ipersistmessage-savecompleted.md) <br/> |<span data-ttu-id="8f44a-132">Avertit le formulaire qu'une opération d'enregistrement a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="8f44a-132">Notifies the form that a save operation has been completed.</span></span>  <br/> |
|[<span data-ttu-id="8f44a-133">HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="8f44a-133">HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="8f44a-134">Entraîne la libération du message actuel par le formulaire.</span><span class="sxs-lookup"><span data-stu-id="8f44a-134">Causes the form to release its current message.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f44a-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="8f44a-135">Remarks</span></span>

<span data-ttu-id="8f44a-136">Tous les formulaires sont requis pour implémenter l'interface **IPersistMessage** .</span><span class="sxs-lookup"><span data-stu-id="8f44a-136">All forms are required to implement the **IPersistMessage** interface.</span></span> 
  
 <span data-ttu-id="8f44a-137">**IPersistMessage** fonctionne de la même manière que l'interface OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8f44a-137">**IPersistMessage** works similarly to the OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="8f44a-138">Pour plus d'informations, consultez les méthodes **IPersistStorage** .</span><span class="sxs-lookup"><span data-stu-id="8f44a-138">For more information, see the **IPersistStorage** methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8f44a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f44a-139">See also</span></span>



[<span data-ttu-id="8f44a-140">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="8f44a-140">MAPI Interfaces</span></span>](mapi-interfaces.md)

