---
title: IMAPIOffline IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline
api_type:
- COM
ms.assetid: 211281ff-3c22-1b51-4b72-ca1e313c7202
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 20d8c39765b0dbbfdde530361894d0a27876010a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321265"
---
# <a name="imapioffline--iunknown"></a><span data-ttu-id="84901-103">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="84901-103">IMAPIOffline : IUnknown</span></span>

  
  
<span data-ttu-id="84901-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84901-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84901-105">Fournit des informations pour un objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="84901-105">Provides information for an offline object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84901-106">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="84901-106">Provided by:</span></span>  <br/> |<span data-ttu-id="84901-107">Requête sur [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span><span class="sxs-lookup"><span data-stu-id="84901-107">Query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span></span> <br/> |
|<span data-ttu-id="84901-108">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="84901-108">Called by:</span></span>  <br/> |<span data-ttu-id="84901-109">Client</span><span class="sxs-lookup"><span data-stu-id="84901-109">Client</span></span>  <br/> |
|<span data-ttu-id="84901-110">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="84901-110">Interface identifier:</span></span>  <br/> |<span data-ttu-id="84901-111">IID_IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="84901-111">IID_IMAPIOffline</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="84901-112">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="84901-112">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84901-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="84901-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="84901-114">Définit l’état actuel d’un objet hors connexion sur en ligne ou hors connexion.</span><span class="sxs-lookup"><span data-stu-id="84901-114">Sets the current state of an offline object to online or offline.</span></span>  <br/> |
|<span data-ttu-id="84901-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="84901-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span></span> <br/> |<span data-ttu-id="84901-116">Obtient les conditions pour lesquelles les rappels sont pris en charge par un objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="84901-116">Gets the conditions for which callbacks are supported by an offline object.</span></span>  <br/> |
|<span data-ttu-id="84901-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="84901-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="84901-118">Obtient l’état actuel en ligne ou hors connexion d’un objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="84901-118">Gets the current online or offline state of an offline object.</span></span>  <br/> |
| <span data-ttu-id="84901-119">*Membre d’espace réservé*</span><span class="sxs-lookup"><span data-stu-id="84901-119">*Placeholder member*</span></span>  <br/> |<span data-ttu-id="84901-120">Ce membre est un espace réservé et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="84901-120">This member is a placeholder and is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84901-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="84901-121">Remarks</span></span>

<span data-ttu-id="84901-122">Un client utilise **[HrOpenOfflineObj](hropenofflineobj.md)** pour ouvrir et obtenir un objet hors connexion qui prend en charge **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="84901-122">A client uses **[HrOpenOfflineObj](hropenofflineobj.md)** to open and obtain an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="84901-123">Étant donné que **IMAPIOfflineMgr** hérite [d’IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)le client peut interroger cette interface (à l’aide de [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) pour obtenir un pointeur vers le pointeur d’interface pour **IMAPIOffline** pour l’objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="84901-123">Because **IMAPIOfflineMgr** inherits from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), the client can query this interface (by using [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) to obtain a pointer to the interface pointer for **IMAPIOffline** for the offline object.</span></span> <span data-ttu-id="84901-124">Le client peut ensuite obtenir ou définir l’état actuel de l’objet, ou connaître les fonctionnalités de rappel de l’objet (en appelant **IMAPIOffline::GetCapabilities)** et choisir de configurer des rappels à l’aide d’IMAPIOfflineMgr . **[](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="84901-124">The client can then get or set the current state of the object, or find out about the callback capabilities of the object (by calling **IMAPIOffline::GetCapabilities** ) and choose to set up callbacks by using **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> 
  
<span data-ttu-id="84901-125">Un membre de cette interface est un espace réservé à l’utilisation interne de Microsoft Outlook 2013 et peut faire l’objet de changements.</span><span class="sxs-lookup"><span data-stu-id="84901-125">A member in this interface is a placeholder reserved for the internal use of Microsoft Outlook 2013 and is subject to change.</span></span> <span data-ttu-id="84901-126">Les autres membres de cette interface doivent être utilisés uniquement comme documentés.</span><span class="sxs-lookup"><span data-stu-id="84901-126">Other members in this interface must be used only as documented.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="84901-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84901-127">See also</span></span>



[<span data-ttu-id="84901-128">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="84901-128">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="84901-129">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="84901-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="84901-130">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="84901-130">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="84901-131">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="84901-131">MAPI Interfaces</span></span>](mapi-interfaces.md)

