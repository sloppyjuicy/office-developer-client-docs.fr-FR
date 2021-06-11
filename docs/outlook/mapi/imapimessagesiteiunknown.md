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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bf21ed1d41a61f600cfded777b699cf620c2e00f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433366"
---
# <a name="imapimessagesite--iunknown"></a><span data-ttu-id="b87f7-103">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b87f7-103">IMAPIMessageSite : IUnknown</span></span>

  
  
<span data-ttu-id="b87f7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b87f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b87f7-105">Manipule les messages et est implémenté par le code de la visionneuse de formulaires (généralement une application cliente) qui répond à cette manipulation.</span><span class="sxs-lookup"><span data-stu-id="b87f7-105">Manipulates messages and is implemented by the form viewer code (typically a client application) that responds to such manipulation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b87f7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b87f7-106">Header file:</span></span>  <br/> |<span data-ttu-id="b87f7-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="b87f7-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="b87f7-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="b87f7-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b87f7-109">Objets de site de message</span><span class="sxs-lookup"><span data-stu-id="b87f7-109">Message site objects</span></span>  <br/> |
|<span data-ttu-id="b87f7-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="b87f7-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b87f7-111">Visionneuses de formulaires</span><span class="sxs-lookup"><span data-stu-id="b87f7-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="b87f7-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="b87f7-112">Called by:</span></span>  <br/> |<span data-ttu-id="b87f7-113">Objets de formulaires</span><span class="sxs-lookup"><span data-stu-id="b87f7-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="b87f7-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="b87f7-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b87f7-115">IID_IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="b87f7-115">IID_IMAPIMessageSite</span></span>  <br/> |
|<span data-ttu-id="b87f7-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="b87f7-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b87f7-117">LPMAPIMESSAGESITE</span><span class="sxs-lookup"><span data-stu-id="b87f7-117">LPMAPIMESSAGESITE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b87f7-118">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="b87f7-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b87f7-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="b87f7-119">GetSession</span></span>](imapimessagesite-getsession.md) <br/> |<span data-ttu-id="b87f7-120">Renvoie la session MAPI dans laquelle le message actuel a été créé ou ouvert.</span><span class="sxs-lookup"><span data-stu-id="b87f7-120">Returns the MAPI session in which the current message was created or opened.</span></span>  <br/> |
|[<span data-ttu-id="b87f7-121">GetStore</span><span class="sxs-lookup"><span data-stu-id="b87f7-121">GetStore</span></span>](imapimessagesite-getstore.md) <br/> |<span data-ttu-id="b87f7-122">Renvoie la magasine de messages qui contient le message actuel, si tel est le cas.</span><span class="sxs-lookup"><span data-stu-id="b87f7-122">Returns the message store that contains the current message, if such a store exists.</span></span>  <br/> |
|[<span data-ttu-id="b87f7-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="b87f7-123">GetFolder</span></span>](imapimessagesite-getfolder.md) <br/> |<span data-ttu-id="b87f7-124">Renvoie le dossier dans lequel le message actuel a été créé ou ouvert, s’il existe un tel dossier.</span><span class="sxs-lookup"><span data-stu-id="b87f7-124">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span>  <br/> |
|[<span data-ttu-id="b87f7-125">GetMessage</span><span class="sxs-lookup"><span data-stu-id="b87f7-125">GetMessage</span></span>](imapimessagesite-getmessage.md) <br/> |<span data-ttu-id="b87f7-126">Renvoie le message actuel.</span><span class="sxs-lookup"><span data-stu-id="b87f7-126">Returns the current message.</span></span>  <br/> |
|[<span data-ttu-id="b87f7-127">GetFormManager</span><span class="sxs-lookup"><span data-stu-id="b87f7-127">GetFormManager</span></span>](imapimessagesite-getformmanager.md) <br/> |<span data-ttu-id="b87f7-128">Renvoie une interface de gestionnaire de formulaires, qu’un serveur de formulaires peut utiliser pour ouvrir un autre serveur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="b87f7-128">Returns a form manager interface, which a form server can use to open another form server.</span></span>  <br/> |
|[<span data-ttu-id="b87f7-129">NewMessage</span><span class="sxs-lookup"><span data-stu-id="b87f7-129">NewMessage</span></span>](imapimessagesite-newmessage.md) <br/> |<span data-ttu-id="b87f7-130">Crée un message.</span><span class="sxs-lookup"><span data-stu-id="b87f7-130">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="b87f7-131">CopyMessage</span><span class="sxs-lookup"><span data-stu-id="b87f7-131">CopyMessage</span></span>](imapimessagesite-copymessage.md) <br/> |<span data-ttu-id="b87f7-132">Copie le message actuel dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="b87f7-132">Copies the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="b87f7-133">MoveMessage</span><span class="sxs-lookup"><span data-stu-id="b87f7-133">MoveMessage</span></span>](imapimessagesite-movemessage.md) <br/> |<span data-ttu-id="b87f7-134">Déplace le message actuel vers un dossier.</span><span class="sxs-lookup"><span data-stu-id="b87f7-134">Moves the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="b87f7-135">DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="b87f7-135">DeleteMessage</span></span>](imapimessagesite-deletemessage.md) <br/> |<span data-ttu-id="b87f7-136">Supprime le message actuel.</span><span class="sxs-lookup"><span data-stu-id="b87f7-136">Deletes the current message.</span></span>  <br/> |
|[<span data-ttu-id="b87f7-137">SaveMessage</span><span class="sxs-lookup"><span data-stu-id="b87f7-137">SaveMessage</span></span>](imapimessagesite-savemessage.md) <br/> |<span data-ttu-id="b87f7-138">Demande que le message actuel soit enregistré.</span><span class="sxs-lookup"><span data-stu-id="b87f7-138">Requests that the current message be saved.</span></span>  <br/> |
|[<span data-ttu-id="b87f7-139">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="b87f7-139">SubmitMessage</span></span>](imapimessagesite-submitmessage.md) <br/> |<span data-ttu-id="b87f7-140">Demande que le message actuel soit mis en file d’attente pour remise.</span><span class="sxs-lookup"><span data-stu-id="b87f7-140">Requests that the current message be queued for delivery.</span></span>  <br/> |
|[<span data-ttu-id="b87f7-141">GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="b87f7-141">GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md) <br/> |<span data-ttu-id="b87f7-142">Renvoie des informations à partir d’un objet de site de message sur les fonctionnalités du site de message pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="b87f7-142">Returns information from a message site object about the message site's capabilities for the current message.</span></span>  <br/> |
|[<span data-ttu-id="b87f7-143">GetLastError</span><span class="sxs-lookup"><span data-stu-id="b87f7-143">GetLastError</span></span>](imapimessagesite-getlasterror.md) <br/> |<span data-ttu-id="b87f7-144">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet de site de message.</span><span class="sxs-lookup"><span data-stu-id="b87f7-144">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b87f7-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b87f7-145">See also</span></span>



[<span data-ttu-id="b87f7-146">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="b87f7-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

