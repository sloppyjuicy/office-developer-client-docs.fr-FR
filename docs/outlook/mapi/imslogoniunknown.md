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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 991e48aa458a58ad2d7d688e81dbb357ef9bda5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428878"
---
# <a name="imslogon--iunknown"></a><span data-ttu-id="98ed4-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="98ed4-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="98ed4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98ed4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98ed4-105">Accède aux ressources d’un objet d’ouverture de magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="98ed4-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98ed4-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="98ed4-106">Header file:</span></span>  <br/> |<span data-ttu-id="98ed4-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="98ed4-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="98ed4-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="98ed4-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="98ed4-109">Objets d’ouverture de la boutique de messages</span><span class="sxs-lookup"><span data-stu-id="98ed4-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="98ed4-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="98ed4-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="98ed4-111">Fournisseurs de magasins de messages</span><span class="sxs-lookup"><span data-stu-id="98ed4-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="98ed4-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="98ed4-112">Called by:</span></span>  <br/> |<span data-ttu-id="98ed4-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="98ed4-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="98ed4-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="98ed4-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="98ed4-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="98ed4-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="98ed4-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="98ed4-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="98ed4-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="98ed4-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="98ed4-118">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="98ed4-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="98ed4-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="98ed4-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="98ed4-120">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur qui s’est produite pour l’objet de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="98ed4-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="98ed4-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="98ed4-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="98ed4-122">Déconnecte un fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="98ed4-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="98ed4-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="98ed4-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="98ed4-124">Ouvre un dossier ou un objet message et renvoie un pointeur vers l’objet pour fournir un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="98ed4-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="98ed4-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="98ed4-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="98ed4-126">Compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="98ed4-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="98ed4-127">Conseiller</span><span class="sxs-lookup"><span data-stu-id="98ed4-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="98ed4-128">Enregistre un objet auprès d’un fournisseur de magasins de messages pour les notifications concernant les modifications apportées à la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="98ed4-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="98ed4-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="98ed4-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="98ed4-130">Supprime l’inscription d’un objet pour la notification des modifications de magasin de messages précédemment établies à l’aide d’un appel à la méthode **IMSLogon::Advise.**</span><span class="sxs-lookup"><span data-stu-id="98ed4-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="98ed4-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="98ed4-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="98ed4-132">Ouvre un objet status.</span><span class="sxs-lookup"><span data-stu-id="98ed4-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98ed4-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="98ed4-133">Remarks</span></span>

<span data-ttu-id="98ed4-134">L’objet d’ouverture de magasin de messages est la partie d’un fournisseur de magasin de messages ouvert que MAPI appelle directement.</span><span class="sxs-lookup"><span data-stu-id="98ed4-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="98ed4-135">Il existe une correspondance un-à-un entre l’objet d’ouverture de conférence de la boutique de messages que MAPI appelle et l’objet de magasin de messages appelé par les applications clientes ; vous pouvez penser à l’ouverture de site et stocker des objets comme un seul objet qui expose deux interfaces.</span><span class="sxs-lookup"><span data-stu-id="98ed4-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="98ed4-136">Les deux objets sont créés ensemble et libérés ensemble.</span><span class="sxs-lookup"><span data-stu-id="98ed4-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98ed4-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98ed4-137">See also</span></span>



[<span data-ttu-id="98ed4-138">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="98ed4-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

