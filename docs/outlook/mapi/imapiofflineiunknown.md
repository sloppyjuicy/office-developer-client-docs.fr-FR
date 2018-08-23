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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 616bb4774e2ca5385e7da867477cb8849d94336b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568384"
---
# <a name="imapioffline--iunknown"></a><span data-ttu-id="50c2c-103">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50c2c-103">IMAPIOffline : IUnknown</span></span>

  
  
<span data-ttu-id="50c2c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50c2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50c2c-105">Fournit des informations pour un objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="50c2c-105">Provides information for an offline object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50c2c-106">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="50c2c-106">Provided by:</span></span>  <br/> |<span data-ttu-id="50c2c-107">Requête sur [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span><span class="sxs-lookup"><span data-stu-id="50c2c-107">Query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span></span> <br/> |
|<span data-ttu-id="50c2c-108">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="50c2c-108">Called by:</span></span>  <br/> |<span data-ttu-id="50c2c-109">Client</span><span class="sxs-lookup"><span data-stu-id="50c2c-109">Client</span></span>  <br/> |
|<span data-ttu-id="50c2c-110">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="50c2c-110">Interface identifier:</span></span>  <br/> |<span data-ttu-id="50c2c-111">IID_IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="50c2c-111">IID_IMAPIOffline</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="50c2c-112">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="50c2c-112">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50c2c-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="50c2c-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="50c2c-114">Définit l’état actuel d’un objet en mode hors connexion en ligne ou hors connexion.</span><span class="sxs-lookup"><span data-stu-id="50c2c-114">Sets the current state of an offline object to online or offline.</span></span>  <br/> |
|<span data-ttu-id="50c2c-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="50c2c-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span></span> <br/> |<span data-ttu-id="50c2c-116">Obtient les conditions pour lequel les rappels sont pris en charge par un objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="50c2c-116">Gets the conditions for which callbacks are supported by an offline object.</span></span>  <br/> |
|<span data-ttu-id="50c2c-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="50c2c-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="50c2c-118">Obtient l’état en ligne ou hors connexion en cours d’un objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="50c2c-118">Gets the current online or offline state of an offline object.</span></span>  <br/> |
| <span data-ttu-id="50c2c-119">*Membres de l’espace réservé*</span><span class="sxs-lookup"><span data-stu-id="50c2c-119">*Placeholder member*</span></span>  <br/> |<span data-ttu-id="50c2c-120">Ce membre est un espace réservé et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="50c2c-120">This member is a placeholder and is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50c2c-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="50c2c-121">Remarks</span></span>

<span data-ttu-id="50c2c-122">Un client utilise **[HrOpenOfflineObj](hropenofflineobj.md)** pour ouvrir et obtenir un objet en mode hors connexion qui prend en charge **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="50c2c-122">A client uses **[HrOpenOfflineObj](hropenofflineobj.md)** to open and obtain an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="50c2c-123">Étant donné que **IMAPIOfflineMgr** hérite de [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx), le client de requête cette interface (à l’aide de [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)) pour obtenir un pointeur vers le pointeur d’interface de **IMAPIOffline** pour l’objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="50c2c-123">Because **IMAPIOfflineMgr** inherits from [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx), the client can query this interface (by using [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)) to obtain a pointer to the interface pointer for **IMAPIOffline** for the offline object.</span></span> <span data-ttu-id="50c2c-124">Le client peut ensuite obtenir ou définir l’état actuel de l’objet, ou Découvrez les fonctionnalités de rappel de l’objet (en appelant **IMAPIOffline::GetCapabilities** ) et choisissez configurer des rappels à l’aide de **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span><span class="sxs-lookup"><span data-stu-id="50c2c-124">The client can then get or set the current state of the object, or find out about the callback capabilities of the object (by calling **IMAPIOffline::GetCapabilities** ) and choose to set up callbacks by using **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> 
  
<span data-ttu-id="50c2c-125">Un membre de cette interface est un espace réservé réservé à un usage interne de Microsoft Outlook 2013 et sujette à modification.</span><span class="sxs-lookup"><span data-stu-id="50c2c-125">A member in this interface is a placeholder reserved for the internal use of Microsoft Outlook 2013 and is subject to change.</span></span> <span data-ttu-id="50c2c-126">Les autres membres de cette interface doivent être utilisés uniquement comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="50c2c-126">Other members in this interface must be used only as documented.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50c2c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50c2c-127">See also</span></span>



[<span data-ttu-id="50c2c-128">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="50c2c-128">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="50c2c-129">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="50c2c-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="50c2c-130">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="50c2c-130">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="50c2c-131">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="50c2c-131">MAPI Interfaces</span></span>](mapi-interfaces.md)

