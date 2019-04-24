---
title: IMAPIClientShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown
api_type:
- COM
ms.assetid: b6a5096f-ad27-48b3-b569-f33efc20fa72
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350875"
---
# <a name="imapiclientshutdown--iunknown"></a><span data-ttu-id="8aaa3-103">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8aaa3-103">IMAPIClientShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="8aaa3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8aaa3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8aaa3-105">Permet à un client MAPI de procéder à l'arrêt rapide du processus client.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-105">Enables a MAPI client to carry out fast shutdown of the client process.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8aaa3-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8aaa3-106">Header file:</span></span>  <br/> |<span data-ttu-id="8aaa3-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8aaa3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8aaa3-108">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="8aaa3-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8aaa3-109">Objet [IMAPISession](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="8aaa3-109">[IMAPISession](imapisessioniunknown.md) object</span></span>  <br/> |
|<span data-ttu-id="8aaa3-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="8aaa3-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8aaa3-111">Sous-système MAPI</span><span class="sxs-lookup"><span data-stu-id="8aaa3-111">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="8aaa3-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="8aaa3-112">Called by:</span></span>  <br/> |<span data-ttu-id="8aaa3-113">Client MAPI</span><span class="sxs-lookup"><span data-stu-id="8aaa3-113">MAPI client</span></span>  <br/> |
|<span data-ttu-id="8aaa3-114">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="8aaa3-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8aaa3-115">IID_IMAPIClientShutdown</span><span class="sxs-lookup"><span data-stu-id="8aaa3-115">IID_IMAPIClientShutdown</span></span>  <br/> |
|<span data-ttu-id="8aaa3-116">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="8aaa3-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="8aaa3-117">LPMAPICLIENTSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="8aaa3-117">LPMAPICLIENTSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8aaa3-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="8aaa3-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8aaa3-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="8aaa3-119">QueryFastShutdown</span></span>](imapiclientshutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="8aaa3-120">Interroge le sous-système MAPI pour la prise en charge de l'arrêt rapide fourni par les fournisseurs MAPI chargés.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-120">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>  <br/> |
|[<span data-ttu-id="8aaa3-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="8aaa3-121">NotifyProcessShutdown</span></span>](imapiclientshutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="8aaa3-122">Indique l'intention du client MAPI de continuer à arrêter.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-122">Indicates the intention of the MAPI client to proceed with shut down.</span></span>  <br/> |
|[<span data-ttu-id="8aaa3-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="8aaa3-123">DoFastShutdown</span></span>](imapiclientshutdown-dofastshutdown.md) <br/> |<span data-ttu-id="8aaa3-124">Indique l'intention du client MAPI de quitter immédiatement le processus client.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-124">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8aaa3-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="8aaa3-125">Remarks</span></span>

<span data-ttu-id="8aaa3-126">L'objectif de l'arrêt rapide est de permettre à un client MAPI et à tout fournisseur MAPI chargé avec lequel le client MAPI dispose d'une session MAPI active pour enregistrer les paramètres et les données MAPI.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-126">The purpose of fast shutdown is to allow a MAPI client and any loaded MAPI provider with which the MAPI client has an active MAPI session to save MAPI settings and data.</span></span> <span data-ttu-id="8aaa3-127">Cela permet au client MAPI de déconnecter toutes les références externes et de quitter sans provoquer de perte de données.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-127">This enables the MAPI client to disconnect all external references and exit without causing any data loss.</span></span> <span data-ttu-id="8aaa3-128">Un client MAPI qui doit effectuer un arrêt rapide doit utiliser l'interface **IMAPIClientShutdown** .</span><span class="sxs-lookup"><span data-stu-id="8aaa3-128">A MAPI client that needs to perform fast shutdown must use the **IMAPIClientShutdown** interface.</span></span> <span data-ttu-id="8aaa3-129">Le client MAPI peut obtenir un pointeur vers cette interface en appelant la méthode IUnknown:: QueryInterface sur n'importe quel objet [IMAPISession](imapisessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="8aaa3-129">The MAPI client can obtain a pointer to this interface by calling the IUnknown::QueryInterface method on any [IMAPISession](imapisessioniunknown.md) object.</span></span> 
  
<span data-ttu-id="8aaa3-130">Un client MAPI lance toujours un arrêt rapide en appelant la méthode **IMAPIClientShutdown:: QueryFastShutdown** .</span><span class="sxs-lookup"><span data-stu-id="8aaa3-130">A MAPI client always initiates a fast shutdown by calling the **IMAPIClientShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="8aaa3-131">Le sous-système MAPI répond à la requête du client MAPI en vérifiant si les fournisseurs MAPI chargés prennent en charge l'arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-131">The MAPI subsystem responds to the MAPI client's query by verifying whether loaded MAPI providers support the client's fast shutdown.</span></span> <span data-ttu-id="8aaa3-132">L'administrateur peut utiliser les paramètres du Registre Windows pour déterminer le niveau de prise en charge des fournisseurs qui est nécessaire pour permettre aux clients MAPI de poursuivre l'arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-132">The administrator can use Windows registry settings to help determine the level of provider support that is necessary for MAPI clients to proceed with fast shutdown.</span></span> <span data-ttu-id="8aaa3-133">Pour plus d'informations, consultez la rubrique options de l' [utilisateur à arrêt rapide](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="8aaa3-133">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="8aaa3-134">Pour poursuivre l'arrêt rapide, le client appelle la méthode **IMAPIClientShutdown:: NotifyProcessShutdown** pour indiquer au sous-système MAPI l'intention de s'arrêter.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-134">To proceed with fast shutdown, the client calls the **IMAPIClientShutdown::NotifyProcessShutdown** method to indicate to the MAPI subsystem the intention to shut down.</span></span> <span data-ttu-id="8aaa3-135">Le client appelle ensuite la méthode **IMAPIClientShutdown::D ofastshutdown** pour indiquer que le processus client quitte immédiatement.</span><span class="sxs-lookup"><span data-stu-id="8aaa3-135">The client then calls the **IMAPIClientShutdown::DoFastShutdown** method to indicate that the client process is exiting immediately.</span></span> 
  
<span data-ttu-id="8aaa3-136">Pour plus d'informations sur l'arrêt rapide, consultez la rubrique [vue d'ensemble de l'arrêt rapide](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8aaa3-136">For more information about fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="8aaa3-137">Pour plus d'informations sur la façon d'effectuer l'arrêt rapide, consultez [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="8aaa3-137">For information about how to perform fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8aaa3-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8aaa3-138">See also</span></span>



[<span data-ttu-id="8aaa3-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="8aaa3-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="8aaa3-140">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="8aaa3-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

