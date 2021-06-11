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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309603"
---
# <a name="ipersistmessage--iunknown"></a><span data-ttu-id="10f74-103">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="10f74-103">IPersistMessage : IUnknown</span></span>

  
  
<span data-ttu-id="10f74-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10f74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10f74-105">Permet aux visionneuses de formulaire de gérer le stockage d’un formulaire et de passer des différents états.</span><span class="sxs-lookup"><span data-stu-id="10f74-105">Enables form viewers to handle the storage of a form and to transition between the various states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10f74-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="10f74-106">Header file:</span></span>  <br/> |<span data-ttu-id="10f74-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="10f74-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="10f74-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="10f74-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="10f74-109">Persister les objets de message</span><span class="sxs-lookup"><span data-stu-id="10f74-109">Persist message objects</span></span>  <br/> |
|<span data-ttu-id="10f74-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="10f74-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="10f74-111">Objets de formulaires</span><span class="sxs-lookup"><span data-stu-id="10f74-111">Form objects</span></span>  <br/> |
|<span data-ttu-id="10f74-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="10f74-112">Called by:</span></span>  <br/> |<span data-ttu-id="10f74-113">Visionneuses de formulaires</span><span class="sxs-lookup"><span data-stu-id="10f74-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="10f74-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="10f74-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="10f74-115">IID_IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="10f74-115">IID_IPersistMessage</span></span>  <br/> |
|<span data-ttu-id="10f74-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="10f74-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="10f74-117">LPPERSISTMESSAGE</span><span class="sxs-lookup"><span data-stu-id="10f74-117">LPPERSISTMESSAGE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="10f74-118">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="10f74-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="10f74-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="10f74-119">GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="10f74-120">Renvoie une [structure MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente dans l’objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="10f74-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span>  <br/> |
|[<span data-ttu-id="10f74-121">GetClassID</span><span class="sxs-lookup"><span data-stu-id="10f74-121">GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="10f74-122">Renvoie un identificateur qui représente le serveur de formulaires qui peut gérer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="10f74-122">Returns an identifier that represents the form server that can manage the form.</span></span>  <br/> |
|[<span data-ttu-id="10f74-123">IsDirty</span><span class="sxs-lookup"><span data-stu-id="10f74-123">IsDirty</span></span>](ipersistmessage-isdirty.md) <br/> |<span data-ttu-id="10f74-124">Recherche dans le formulaire les modifications apportées depuis le dernier sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="10f74-124">Checks the form for changes that were made since the last save.</span></span>  <br/> |
|[<span data-ttu-id="10f74-125">InitNew</span><span class="sxs-lookup"><span data-stu-id="10f74-125">InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="10f74-126">Initialise un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="10f74-126">Initializes a new message.</span></span>  <br/> |
|[<span data-ttu-id="10f74-127">Load</span><span class="sxs-lookup"><span data-stu-id="10f74-127">Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="10f74-128">Charge le formulaire pour un message spécifié.</span><span class="sxs-lookup"><span data-stu-id="10f74-128">Loads the form for a specified message.</span></span>  <br/> |
|[<span data-ttu-id="10f74-129">Save</span><span class="sxs-lookup"><span data-stu-id="10f74-129">Save</span></span>](ipersistmessage-save.md) <br/> |<span data-ttu-id="10f74-130">Enregistre un formulaire révisé dans le message à partir duquel il a été chargé ou créé.</span><span class="sxs-lookup"><span data-stu-id="10f74-130">Saves a revised form back to the message from which it was loaded or created.</span></span>  <br/> |
|[<span data-ttu-id="10f74-131">SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="10f74-131">SaveCompleted</span></span>](ipersistmessage-savecompleted.md) <br/> |<span data-ttu-id="10f74-132">Avertit le formulaire qu’une opération d’enregistrer a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="10f74-132">Notifies the form that a save operation has been completed.</span></span>  <br/> |
|[<span data-ttu-id="10f74-133">HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="10f74-133">HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="10f74-134">Fait en sorte que le formulaire libère son message actuel.</span><span class="sxs-lookup"><span data-stu-id="10f74-134">Causes the form to release its current message.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10f74-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="10f74-135">Remarks</span></span>

<span data-ttu-id="10f74-136">Tous les formulaires sont requis pour **implémenter l’interface IPersistMessage.**</span><span class="sxs-lookup"><span data-stu-id="10f74-136">All forms are required to implement the **IPersistMessage** interface.</span></span> 
  
 <span data-ttu-id="10f74-137">**IPersistMessage** fonctionne de la même manière que l’interface OLE [IPersistStorage.](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10f74-137">**IPersistMessage** works similarly to the OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="10f74-138">Pour plus d’informations, voir les **méthodes IPersistStorage.**</span><span class="sxs-lookup"><span data-stu-id="10f74-138">For more information, see the **IPersistStorage** methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="10f74-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10f74-139">See also</span></span>



[<span data-ttu-id="10f74-140">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="10f74-140">MAPI Interfaces</span></span>](mapi-interfaces.md)

