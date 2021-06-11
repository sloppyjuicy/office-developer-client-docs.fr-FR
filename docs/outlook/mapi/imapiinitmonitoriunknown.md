---
title: 'IMAPIInitMonitor : IUnknown'
manager: lindalu
26ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIInitMonitor
api_type:
- COM
ms.assetid: ad71ea65-394d-4be2-a9da-cd23099bc2cc
description: IMAPIInitMonitor
Last modified: April 26, 2021
ms.openlocfilehash: dd17d50b04755d9d9c2a10a9b02cd821faf1f7ec
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062045"
---
# <a name="imapiinitmonitor--iunknown"></a><span data-ttu-id="d48c6-103">IMAPIInitMonitor : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d48c6-103">IMAPIInitMonitor : IUnknown</span></span>

<span data-ttu-id="d48c6-104">**S’applique** à : Outlook 2013 | Outlook 2016 | Outlook 2019</span><span class="sxs-lookup"><span data-stu-id="d48c6-104">**Applies to**: Outlook 2013 | Outlook 2016 | Outlook 2019</span></span>

<span data-ttu-id="d48c6-105">Parfois, une application qui utilise MAPI peut vouloir savoir quand l’initialisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="d48c6-105">There are times when an application which consumes MAPI might want to know when the initialization is completed.</span></span> <span data-ttu-id="d48c6-106">Par exemple, il possède plusieurs threads qui peuvent initialiser MAPI, ou en réponse à l’initialisation de MAPI, l’application souhaite effectuer un travail, mais ne souhaite pas toujours faire tourner la pile MAPI.</span><span class="sxs-lookup"><span data-stu-id="d48c6-106">For example, it has multiple threads which could initialize MAPI, or in response to MAPI being initialized the application would like perform some work, but does not want to always spin up the MAPI stack.</span></span> <span data-ttu-id="d48c6-107">Le moniteur d’initialisation fournit cette fonctionnalité via un [objet CreateMAPIInitializationMonitor.](createmapiinitializationmonitor.md)</span><span class="sxs-lookup"><span data-stu-id="d48c6-107">The initialization monitor provides this functionality through a [CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md) object.</span></span>

| <span data-ttu-id="d48c6-108">informations rapides</span><span class="sxs-lookup"><span data-stu-id="d48c6-108">quick info</span></span> | <span data-ttu-id="d48c6-109">result</span><span class="sxs-lookup"><span data-stu-id="d48c6-109">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="d48c6-110">Hérite de :</span><span class="sxs-lookup"><span data-stu-id="d48c6-110">Inherits from:</span></span>  <br/> |<span data-ttu-id="d48c6-111">IUnknown</span><span class="sxs-lookup"><span data-stu-id="d48c6-111">IUnknown</span></span>  <br/> |
|<span data-ttu-id="d48c6-112">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="d48c6-112">Implemented by:</span></span>  <br/> | <span data-ttu-id="d48c6-113">OLMAPI32.DLL</span><span class="sxs-lookup"><span data-stu-id="d48c6-113">OLMAPI32.DLL</span></span> <br/> |
|<span data-ttu-id="d48c6-114">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="d48c6-114">Called by:</span></span>  <br/> |<span data-ttu-id="d48c6-115">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="d48c6-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="d48c6-116">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="d48c6-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d48c6-117">IID_IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="d48c6-117">IID_IMAPIInitMonitor</span></span>  <br/> |

## <a name="vtable-order"></a><span data-ttu-id="d48c6-118">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="d48c6-118">Vtable order</span></span>

| <span data-ttu-id="d48c6-119">fonction</span><span class="sxs-lookup"><span data-stu-id="d48c6-119">function</span></span> | <span data-ttu-id="d48c6-120">description</span><span class="sxs-lookup"><span data-stu-id="d48c6-120">description</span></span> |
|:-----|:-----|
|[<span data-ttu-id="d48c6-121">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="d48c6-121">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md) <br/> |<span data-ttu-id="d48c6-122">Renvoie l’état actuel de l’initialisation MAPI.</span><span class="sxs-lookup"><span data-stu-id="d48c6-122">Returns the current state of MAPI initialization.</span></span>  <br/> |
|[<span data-ttu-id="d48c6-123">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="d48c6-123">IMAPIInitMonitor::Wait</span></span>](imapiinitmonitor-wait.md) <br/> |<span data-ttu-id="d48c6-124">Lance un appel BLOCKING sur ce thread, qui retourne soit lorsque le nombre de millisecondes spécifié est écoulé, soit que MAPI a été initialisé.</span><span class="sxs-lookup"><span data-stu-id="d48c6-124">Initiates a BLOCKING call on this thread, which will return either when the specified number of milliseconds have elapsed or MAPI has been initialized.</span></span>  <span data-ttu-id="d48c6-125">INFINITE peut être utilisé pour une attente infinie.</span><span class="sxs-lookup"><span data-stu-id="d48c6-125">INFINITE can be used to for an infinite wait.</span></span>  <br/> |
|[<span data-ttu-id="d48c6-126">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="d48c6-126">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md) <br/> |<span data-ttu-id="d48c6-127">Démarrez une attente pour l’initialisation de MAPI ou le nombre spécifié de millisecondes qui s’écoulént.</span><span class="sxs-lookup"><span data-stu-id="d48c6-127">Start a wait for MAPI initialization or the specified number of milliseconds to elapse.</span></span> <span data-ttu-id="d48c6-128">Cette commande retourne une interface IMAPIWaitResult qui doit avoir appelé « End » afin de commencer l’attente.</span><span class="sxs-lookup"><span data-stu-id="d48c6-128">This return an IMAPIWaitResult interface which should have “End” called in order begin the wait.</span></span>  <span data-ttu-id="d48c6-129">Cela permet à l’appelant de contrôler quel thread est bloqué pendant que nous sommes en attente.</span><span class="sxs-lookup"><span data-stu-id="d48c6-129">This allows the caller to control which thread is blocked while we are waiting.</span></span> <br/> |
