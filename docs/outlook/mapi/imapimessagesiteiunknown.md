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
ms.openlocfilehash: bf21ed1d41a61f600cfded777b699cf620c2e00f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321349"
---
# <a name="imapimessagesite--iunknown"></a><span data-ttu-id="23dfc-103">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="23dfc-103">IMAPIMessageSite : IUnknown</span></span>

  
  
<span data-ttu-id="23dfc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23dfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23dfc-105">Manipule les messages et est implémenté par le code de la visionneuse de formulaires (généralement une application cliente) qui répond à cette manipulation.</span><span class="sxs-lookup"><span data-stu-id="23dfc-105">Manipulates messages and is implemented by the form viewer code (typically a client application) that responds to such manipulation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23dfc-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="23dfc-106">Header file:</span></span>  <br/> |<span data-ttu-id="23dfc-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="23dfc-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="23dfc-108">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="23dfc-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="23dfc-109">Objets de site de messagerie</span><span class="sxs-lookup"><span data-stu-id="23dfc-109">Message site objects</span></span>  <br/> |
|<span data-ttu-id="23dfc-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="23dfc-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="23dfc-111">Visionneuses de formulaires</span><span class="sxs-lookup"><span data-stu-id="23dfc-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="23dfc-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="23dfc-112">Called by:</span></span>  <br/> |<span data-ttu-id="23dfc-113">Objets de formulaires</span><span class="sxs-lookup"><span data-stu-id="23dfc-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="23dfc-114">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="23dfc-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="23dfc-115">IID_IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="23dfc-115">IID_IMAPIMessageSite</span></span>  <br/> |
|<span data-ttu-id="23dfc-116">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="23dfc-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="23dfc-117">LPMAPIMESSAGESITE</span><span class="sxs-lookup"><span data-stu-id="23dfc-117">LPMAPIMESSAGESITE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="23dfc-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="23dfc-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="23dfc-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="23dfc-119">GetSession</span></span>](imapimessagesite-getsession.md) <br/> |<span data-ttu-id="23dfc-120">Renvoie la session MAPI dans laquelle le message actif a été créé ou ouvert.</span><span class="sxs-lookup"><span data-stu-id="23dfc-120">Returns the MAPI session in which the current message was created or opened.</span></span>  <br/> |
|[<span data-ttu-id="23dfc-121">GetStore</span><span class="sxs-lookup"><span data-stu-id="23dfc-121">GetStore</span></span>](imapimessagesite-getstore.md) <br/> |<span data-ttu-id="23dfc-122">Renvoie la Banque de messages qui contient le message actif, si ce type de magasin existe.</span><span class="sxs-lookup"><span data-stu-id="23dfc-122">Returns the message store that contains the current message, if such a store exists.</span></span>  <br/> |
|[<span data-ttu-id="23dfc-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="23dfc-123">GetFolder</span></span>](imapimessagesite-getfolder.md) <br/> |<span data-ttu-id="23dfc-124">Renvoie le dossier dans lequel le message actif a été créé ou ouvert, si ce dossier existe.</span><span class="sxs-lookup"><span data-stu-id="23dfc-124">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span>  <br/> |
|[<span data-ttu-id="23dfc-125">GetMessage</span><span class="sxs-lookup"><span data-stu-id="23dfc-125">GetMessage</span></span>](imapimessagesite-getmessage.md) <br/> |<span data-ttu-id="23dfc-126">Renvoie le message actif.</span><span class="sxs-lookup"><span data-stu-id="23dfc-126">Returns the current message.</span></span>  <br/> |
|[<span data-ttu-id="23dfc-127">GetFormManager</span><span class="sxs-lookup"><span data-stu-id="23dfc-127">GetFormManager</span></span>](imapimessagesite-getformmanager.md) <br/> |<span data-ttu-id="23dfc-128">Renvoie une interface du gestionnaire de formulaires, qu'un serveur de formulaires peut utiliser pour ouvrir un autre serveur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="23dfc-128">Returns a form manager interface, which a form server can use to open another form server.</span></span>  <br/> |
|[<span data-ttu-id="23dfc-129">NewMessage</span><span class="sxs-lookup"><span data-stu-id="23dfc-129">NewMessage</span></span>](imapimessagesite-newmessage.md) <br/> |<span data-ttu-id="23dfc-130">Crée un message.</span><span class="sxs-lookup"><span data-stu-id="23dfc-130">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="23dfc-131">CopyMessage</span><span class="sxs-lookup"><span data-stu-id="23dfc-131">CopyMessage</span></span>](imapimessagesite-copymessage.md) <br/> |<span data-ttu-id="23dfc-132">Copie le message actif dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="23dfc-132">Copies the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="23dfc-133">MoveMessage</span><span class="sxs-lookup"><span data-stu-id="23dfc-133">MoveMessage</span></span>](imapimessagesite-movemessage.md) <br/> |<span data-ttu-id="23dfc-134">Déplace le message actif vers un dossier.</span><span class="sxs-lookup"><span data-stu-id="23dfc-134">Moves the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="23dfc-135">DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="23dfc-135">DeleteMessage</span></span>](imapimessagesite-deletemessage.md) <br/> |<span data-ttu-id="23dfc-136">Supprime le message actif.</span><span class="sxs-lookup"><span data-stu-id="23dfc-136">Deletes the current message.</span></span>  <br/> |
|[<span data-ttu-id="23dfc-137">SaveMessage</span><span class="sxs-lookup"><span data-stu-id="23dfc-137">SaveMessage</span></span>](imapimessagesite-savemessage.md) <br/> |<span data-ttu-id="23dfc-138">Demande l'enregistrement du message actif.</span><span class="sxs-lookup"><span data-stu-id="23dfc-138">Requests that the current message be saved.</span></span>  <br/> |
|[<span data-ttu-id="23dfc-139">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="23dfc-139">SubmitMessage</span></span>](imapimessagesite-submitmessage.md) <br/> |<span data-ttu-id="23dfc-140">Demande que le message en cours soit mis en file d'attente pour remise.</span><span class="sxs-lookup"><span data-stu-id="23dfc-140">Requests that the current message be queued for delivery.</span></span>  <br/> |
|[<span data-ttu-id="23dfc-141">GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="23dfc-141">GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md) <br/> |<span data-ttu-id="23dfc-142">Renvoie les informations d'un objet de site de messagerie concernant les fonctionnalités du site de messagerie pour le message actif.</span><span class="sxs-lookup"><span data-stu-id="23dfc-142">Returns information from a message site object about the message site's capabilities for the current message.</span></span>  <br/> |
|[<span data-ttu-id="23dfc-143">Généré</span><span class="sxs-lookup"><span data-stu-id="23dfc-143">GetLastError</span></span>](imapimessagesite-getlasterror.md) <br/> |<span data-ttu-id="23dfc-144">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente qui s'est produite dans l'objet de site de message.</span><span class="sxs-lookup"><span data-stu-id="23dfc-144">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23dfc-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23dfc-145">See also</span></span>



[<span data-ttu-id="23dfc-146">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="23dfc-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

