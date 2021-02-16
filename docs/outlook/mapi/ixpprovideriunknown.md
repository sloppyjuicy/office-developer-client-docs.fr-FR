---
title: IXPProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider
api_type:
- COM
ms.assetid: d5507785-c924-4981-ae80-19709ceb054d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0aa77ced9d0c242dcafb84ca1e1a60d02db9504a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404693"
---
# <a name="ixpprovider--iunknown"></a><span data-ttu-id="b543c-103">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b543c-103">IXPProvider : IUnknown</span></span>

  
  
<span data-ttu-id="b543c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b543c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b543c-105">Initialise un objet fournisseur de transport et arrête l’objet lorsqu’il n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b543c-105">Initializes a transport provider object and shuts down the object when it is no longer needed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b543c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b543c-106">Header file:</span></span>  <br/> |<span data-ttu-id="b543c-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="b543c-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="b543c-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="b543c-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b543c-109">Objets du fournisseur de transport</span><span class="sxs-lookup"><span data-stu-id="b543c-109">Transport provider objects</span></span>  <br/> |
|<span data-ttu-id="b543c-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="b543c-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b543c-111">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="b543c-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="b543c-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="b543c-112">Called by:</span></span>  <br/> |<span data-ttu-id="b543c-113">Lepooler MAPI</span><span class="sxs-lookup"><span data-stu-id="b543c-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="b543c-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="b543c-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b543c-115">IID_IXPProvider</span><span class="sxs-lookup"><span data-stu-id="b543c-115">IID_IXPProvider</span></span>  <br/> |
|<span data-ttu-id="b543c-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="b543c-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b543c-117">LPXPROVIDER</span><span class="sxs-lookup"><span data-stu-id="b543c-117">LPXPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b543c-118">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="b543c-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b543c-119">Arrêt</span><span class="sxs-lookup"><span data-stu-id="b543c-119">Shutdown</span></span>](ixpprovider-shutdown.md) <br/> |<span data-ttu-id="b543c-120">Ferme un fournisseur de transport de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="b543c-120">Closes down a transport provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="b543c-121">TransportLogon</span><span class="sxs-lookup"><span data-stu-id="b543c-121">TransportLogon</span></span>](ixpprovider-transportlogon.md) <br/> |<span data-ttu-id="b543c-122">Établit une session dans laquelle une application cliente se connecte à un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="b543c-122">Establishes a session in which a client application logs on to a transport provider.</span></span>  <br/> |
   

