---
title: IMAPIMessageSite IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite
api_type:
- COM
ms.assetid: 883448f5-0d3f-486d-80a3-7b961c209cd0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 75ef8d6f2134e0269745f92dab1f790228692853
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783861"
---
# <a name="imapimessagesite--iunknown"></a><span data-ttu-id="47140-103">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47140-103">IMAPIMessageSite : IUnknown</span></span>

  
  
<span data-ttu-id="47140-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="47140-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="47140-105">Gère les messages et est implémentée par le code de visionneuse de formulaire (généralement, une application cliente) qui répond à ce manipulation.</span><span class="sxs-lookup"><span data-stu-id="47140-105">Manipulates messages and is implemented by the form viewer code (typically a client application) that responds to such manipulation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47140-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="47140-106">Header file:</span></span>  <br/> |<span data-ttu-id="47140-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="47140-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="47140-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="47140-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="47140-109">Objets du site</span><span class="sxs-lookup"><span data-stu-id="47140-109">Message site objects</span></span>  <br/> |
|<span data-ttu-id="47140-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="47140-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="47140-111">Visionneuses de formulaire</span><span class="sxs-lookup"><span data-stu-id="47140-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="47140-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="47140-112">Called by:</span></span>  <br/> |<span data-ttu-id="47140-113">Objets de formulaire</span><span class="sxs-lookup"><span data-stu-id="47140-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="47140-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="47140-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="47140-115">IID_IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="47140-115">IID_IMAPIMessageSite</span></span>  <br/> |
|<span data-ttu-id="47140-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="47140-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="47140-117">LPMAPIMESSAGESITE</span><span class="sxs-lookup"><span data-stu-id="47140-117">LPMAPIMESSAGESITE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="47140-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="47140-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="47140-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="47140-119">GetSession</span></span>](imapimessagesite-getsession.md) <br/> |<span data-ttu-id="47140-120">Renvoie la session MAPI dans lequel le message en cours a été créé ou ouvert.</span><span class="sxs-lookup"><span data-stu-id="47140-120">Returns the MAPI session in which the current message was created or opened.</span></span>  <br/> |
|[<span data-ttu-id="47140-121">GetStore</span><span class="sxs-lookup"><span data-stu-id="47140-121">GetStore</span></span>](imapimessagesite-getstore.md) <br/> |<span data-ttu-id="47140-122">Renvoie la banque de messages qui contient le message en cours, si une banque de ce type existe.</span><span class="sxs-lookup"><span data-stu-id="47140-122">Returns the message store that contains the current message, if such a store exists.</span></span>  <br/> |
|[<span data-ttu-id="47140-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="47140-123">GetFolder</span></span>](imapimessagesite-getfolder.md) <br/> |<span data-ttu-id="47140-124">Renvoie le dossier dans lequel le message en cours a été créé ou ouvert, si un tel dossier existe.</span><span class="sxs-lookup"><span data-stu-id="47140-124">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span>  <br/> |
|[<span data-ttu-id="47140-125">GetMessage</span><span class="sxs-lookup"><span data-stu-id="47140-125">GetMessage</span></span>](imapimessagesite-getmessage.md) <br/> |<span data-ttu-id="47140-126">Renvoie le message en cours.</span><span class="sxs-lookup"><span data-stu-id="47140-126">Returns the current message.</span></span>  <br/> |
|[<span data-ttu-id="47140-127">GetFormManager</span><span class="sxs-lookup"><span data-stu-id="47140-127">GetFormManager</span></span>](imapimessagesite-getformmanager.md) <br/> |<span data-ttu-id="47140-128">Renvoie une interface du Gestionnaire de formulaire un serveur de formulaire peut utiliser pour ouvrir un autre serveur du formulaire.</span><span class="sxs-lookup"><span data-stu-id="47140-128">Returns a form manager interface, which a form server can use to open another form server.</span></span>  <br/> |
|[<span data-ttu-id="47140-129">NewMessage</span><span class="sxs-lookup"><span data-stu-id="47140-129">NewMessage</span></span>](imapimessagesite-newmessage.md) <br/> |<span data-ttu-id="47140-130">Crée un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="47140-130">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="47140-131">CopyMessage</span><span class="sxs-lookup"><span data-stu-id="47140-131">CopyMessage</span></span>](imapimessagesite-copymessage.md) <br/> |<span data-ttu-id="47140-132">Copie le message en cours dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="47140-132">Copies the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="47140-133">MoveMessage</span><span class="sxs-lookup"><span data-stu-id="47140-133">MoveMessage</span></span>](imapimessagesite-movemessage.md) <br/> |<span data-ttu-id="47140-134">Déplace le message en cours dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="47140-134">Moves the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="47140-135">DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="47140-135">DeleteMessage</span></span>](imapimessagesite-deletemessage.md) <br/> |<span data-ttu-id="47140-136">Supprime le message en cours.</span><span class="sxs-lookup"><span data-stu-id="47140-136">Deletes the current message.</span></span>  <br/> |
|[<span data-ttu-id="47140-137">SaveMessage</span><span class="sxs-lookup"><span data-stu-id="47140-137">SaveMessage</span></span>](imapimessagesite-savemessage.md) <br/> |<span data-ttu-id="47140-138">Demandes d’enregistrer le message en cours.</span><span class="sxs-lookup"><span data-stu-id="47140-138">Requests that the current message be saved.</span></span>  <br/> |
|[<span data-ttu-id="47140-139">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="47140-139">SubmitMessage</span></span>](imapimessagesite-submitmessage.md) <br/> |<span data-ttu-id="47140-140">Demande que le message en cours est en attente de remise.</span><span class="sxs-lookup"><span data-stu-id="47140-140">Requests that the current message be queued for delivery.</span></span>  <br/> |
|[<span data-ttu-id="47140-141">GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="47140-141">GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md) <br/> |<span data-ttu-id="47140-142">Retourne des informations à partir d’un objet de site message sur le message fonctionnalités du site pour le message en cours.</span><span class="sxs-lookup"><span data-stu-id="47140-142">Returns information from a message site object about the message site's capabilities for the current message.</span></span>  <br/> |
|[<span data-ttu-id="47140-143">GetLastError</span><span class="sxs-lookup"><span data-stu-id="47140-143">GetLastError</span></span>](imapimessagesite-getlasterror.md) <br/> |<span data-ttu-id="47140-144">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente à l’objet de site de message en cours.</span><span class="sxs-lookup"><span data-stu-id="47140-144">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47140-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47140-145">See also</span></span>



[<span data-ttu-id="47140-146">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="47140-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

