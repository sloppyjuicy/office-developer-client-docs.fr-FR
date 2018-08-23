---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 013903f36bf648c4aed194c88104e7dd981b199f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563939"
---
# <a name="imslogon--iunknown"></a><span data-ttu-id="6832b-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6832b-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="6832b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6832b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6832b-105">Ressources d’accès dans un message stockent objet d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="6832b-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6832b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6832b-106">Header file:</span></span>  <br/> |<span data-ttu-id="6832b-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="6832b-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="6832b-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="6832b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="6832b-109">Objets de message store d’ouverture de session</span><span class="sxs-lookup"><span data-stu-id="6832b-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="6832b-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="6832b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="6832b-111">Fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="6832b-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="6832b-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="6832b-112">Called by:</span></span>  <br/> |<span data-ttu-id="6832b-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="6832b-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="6832b-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="6832b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6832b-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="6832b-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="6832b-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="6832b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="6832b-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="6832b-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6832b-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="6832b-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6832b-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="6832b-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="6832b-120">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur qui s’est produite lors de l’objet de la banque de message.</span><span class="sxs-lookup"><span data-stu-id="6832b-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="6832b-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="6832b-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="6832b-122">Fournisseur de magasins de journaux d’un message.</span><span class="sxs-lookup"><span data-stu-id="6832b-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="6832b-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="6832b-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="6832b-124">Ouvre un dossier ou un objet de message et retourne un pointeur vers l’objet pour fournir un accès plus.</span><span class="sxs-lookup"><span data-stu-id="6832b-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="6832b-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="6832b-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="6832b-126">Compare deux identificateurs d’entrée pour déterminer si elles font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="6832b-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="6832b-127">Conseiller</span><span class="sxs-lookup"><span data-stu-id="6832b-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="6832b-128">Inscrit un objet avec un fournisseur de magasin de message pour les notifications sur les modifications dans la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="6832b-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="6832b-129">L’avertissement</span><span class="sxs-lookup"><span data-stu-id="6832b-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="6832b-130">Supprime l’inscription d’un objet pour la notification des modifications de banque de messages précédemment établie à l’aide d’un appel à la méthode **IMSLogon::Advise** .</span><span class="sxs-lookup"><span data-stu-id="6832b-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="6832b-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="6832b-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="6832b-132">Ouvre un objet d’état.</span><span class="sxs-lookup"><span data-stu-id="6832b-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6832b-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="6832b-133">Remarks</span></span>

<span data-ttu-id="6832b-134">L’objet d’ouverture de session du magasin de message est la partie d’un fournisseur de magasins d’ouvrir le message MAPI appelle directement.</span><span class="sxs-lookup"><span data-stu-id="6832b-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="6832b-135">Il existe une correspondance entre l’objet d’ouverture de session de magasin de message qui stockent des appels MAPI et le message d’objet applications clientes appellent ; Vous pouvez considérer les paramètres de connexion et stocker des objets sous forme d’un objet qui expose les deux interfaces.</span><span class="sxs-lookup"><span data-stu-id="6832b-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="6832b-136">Les deux objets sont créés, ensemble et libérés ensemble.</span><span class="sxs-lookup"><span data-stu-id="6832b-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6832b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6832b-137">See also</span></span>



[<span data-ttu-id="6832b-138">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="6832b-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

