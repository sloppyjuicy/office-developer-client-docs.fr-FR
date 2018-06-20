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
ms.openlocfilehash: e68211049bc0f958ae24975f4ab4063953eef567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783710"
---
# <a name="imapiclientshutdown--iunknown"></a><span data-ttu-id="08916-103">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="08916-103">IMAPIClientShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="08916-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="08916-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="08916-105">Permet à un client MAPI effectuer un arrêt rapide du processus de client.</span><span class="sxs-lookup"><span data-stu-id="08916-105">Enables a MAPI client to carry out fast shutdown of the client process.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08916-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="08916-106">Header file:</span></span>  <br/> |<span data-ttu-id="08916-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08916-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="08916-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="08916-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="08916-109">Objet [IMAPISession](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="08916-109">[IMAPISession](imapisessioniunknown.md) object</span></span>  <br/> |
|<span data-ttu-id="08916-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="08916-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="08916-111">Sous-système MAPI</span><span class="sxs-lookup"><span data-stu-id="08916-111">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="08916-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="08916-112">Called by:</span></span>  <br/> |<span data-ttu-id="08916-113">Client MAPI</span><span class="sxs-lookup"><span data-stu-id="08916-113">MAPI client</span></span>  <br/> |
|<span data-ttu-id="08916-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="08916-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="08916-115">IID_IMAPIClientShutdown</span><span class="sxs-lookup"><span data-stu-id="08916-115">IID_IMAPIClientShutdown</span></span>  <br/> |
|<span data-ttu-id="08916-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="08916-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="08916-117">LPMAPICLIENTSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="08916-117">LPMAPICLIENTSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="08916-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="08916-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="08916-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="08916-119">QueryFastShutdown</span></span>](imapiclientshutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="08916-120">Requêtes du sous-système MAPI pour arrêt rapide prennent en charge fournie par les fournisseurs MAPI chargés.</span><span class="sxs-lookup"><span data-stu-id="08916-120">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>  <br/> |
|[<span data-ttu-id="08916-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="08916-121">NotifyProcessShutdown</span></span>](imapiclientshutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="08916-122">Indique l’intention de poursuivre du client MAPI arrêté.</span><span class="sxs-lookup"><span data-stu-id="08916-122">Indicates the intention of the MAPI client to proceed with shut down.</span></span>  <br/> |
|[<span data-ttu-id="08916-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="08916-123">DoFastShutdown</span></span>](imapiclientshutdown-dofastshutdown.md) <br/> |<span data-ttu-id="08916-124">Indique l’intention du client MAPI pour quitter le processus de client immédiatement.</span><span class="sxs-lookup"><span data-stu-id="08916-124">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08916-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="08916-125">Remarks</span></span>

<span data-ttu-id="08916-126">L’objectif de l’arrêt rapide consiste à autoriser un client MAPI et tout fournisseur MAPI chargé avec lequel le client MAPI a une session MAPI active pour enregistrer les données et les paramètres MAPI.</span><span class="sxs-lookup"><span data-stu-id="08916-126">The purpose of fast shutdown is to allow a MAPI client and any loaded MAPI provider with which the MAPI client has an active MAPI session to save MAPI settings and data.</span></span> <span data-ttu-id="08916-127">Cela permet au client MAPI déconnecter toutes les références externes et quitter sans entraînant la perte de données.</span><span class="sxs-lookup"><span data-stu-id="08916-127">This enables the MAPI client to disconnect all external references and exit without causing any data loss.</span></span> <span data-ttu-id="08916-128">Un client MAPI qui doit effectuer l’arrêt rapide doit utiliser l’interface **IMAPIClientShutdown** .</span><span class="sxs-lookup"><span data-stu-id="08916-128">A MAPI client that needs to perform fast shutdown must use the **IMAPIClientShutdown** interface.</span></span> <span data-ttu-id="08916-129">Le client MAPI permettre obtenir un pointeur vers cette interface en appelant la méthode IUnknown::QueryInterface sur n’importe quel objet [IMAPISession](imapisessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="08916-129">The MAPI client can obtain a pointer to this interface by calling the IUnknown::QueryInterface method on any [IMAPISession](imapisessioniunknown.md) object.</span></span> 
  
<span data-ttu-id="08916-130">Un client MAPI initie toujours un arrêt rapide en appelant la méthode **IMAPIClientShutdown::QueryFastShutdown** .</span><span class="sxs-lookup"><span data-stu-id="08916-130">A MAPI client always initiates a fast shutdown by calling the **IMAPIClientShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="08916-131">Le sous-système MAPI répond aux requêtes du client MAPI en vérifiant si chargés fournisseurs MAPI prennent en charge l’arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="08916-131">The MAPI subsystem responds to the MAPI client's query by verifying whether loaded MAPI providers support the client's fast shutdown.</span></span> <span data-ttu-id="08916-132">L’administrateur peut utiliser les paramètres du Registre Windows pour aider à déterminer le niveau de prise en charge de fournisseur qui est nécessaire pour les clients MAPI poursuivre l’arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="08916-132">The administrator can use Windows registry settings to help determine the level of provider support that is necessary for MAPI clients to proceed with fast shutdown.</span></span> <span data-ttu-id="08916-133">Pour plus d’informations, voir [Options d’utilisateur de l’arrêt rapide](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="08916-133">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="08916-134">Pour procéder à l’arrêt rapide, le client appelle la méthode de **IMAPIClientShutdown::NotifyProcessShutdown** pour indiquer le sous-système MAPI l’intention d’arrêter.</span><span class="sxs-lookup"><span data-stu-id="08916-134">To proceed with fast shutdown, the client calls the **IMAPIClientShutdown::NotifyProcessShutdown** method to indicate to the MAPI subsystem the intention to shut down.</span></span> <span data-ttu-id="08916-135">Le client appelle ensuite la méthode **IMAPIClientShutdown::DoFastShutdown** pour indiquer que le processus client va s’arrêter immédiatement.</span><span class="sxs-lookup"><span data-stu-id="08916-135">The client then calls the **IMAPIClientShutdown::DoFastShutdown** method to indicate that the client process is exiting immediately.</span></span> 
  
<span data-ttu-id="08916-136">Pour plus d’informations sur l’arrêt rapide, voir [Vue d’ensemble rapide de l’arrêt](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="08916-136">For more information about fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="08916-137">Pour plus d’informations sur l’exécution de l’arrêt rapide avec succès, voir [Meilleures pratiques pour l’arrêt rapide](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="08916-137">For information about how to perform fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08916-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08916-138">See also</span></span>



[<span data-ttu-id="08916-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="08916-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="08916-140">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="08916-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

