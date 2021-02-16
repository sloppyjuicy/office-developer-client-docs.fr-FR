---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Représente une instance d’un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409957"
---
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="d06e5-103">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d06e5-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="d06e5-104">Représente une instance d’un fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="d06e5-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="d06e5-105">Members</span><span class="sxs-lookup"><span data-stu-id="d06e5-105">Members</span></span>

<span data-ttu-id="d06e5-106">Le tableau suivant indique les membres qui sont disponibles sur l’interface **ISocialProvider.**</span><span class="sxs-lookup"><span data-stu-id="d06e5-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="d06e5-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="d06e5-107">**Name**</span></span>|<span data-ttu-id="d06e5-108">**Type de membre**</span><span class="sxs-lookup"><span data-stu-id="d06e5-108">**Member type**</span></span>|<span data-ttu-id="d06e5-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="d06e5-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d06e5-110">DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="d06e5-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="d06e5-111">Propriété</span><span class="sxs-lookup"><span data-stu-id="d06e5-111">Property</span></span>  <br/> |<span data-ttu-id="d06e5-112">Renvoie un tableau de chaînes qui spécifient les URL de site pour le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="d06e5-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="d06e5-113">GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="d06e5-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="d06e5-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="d06e5-114">Method</span></span>  <br/> |<span data-ttu-id="d06e5-115">Récupère une interface [ISocialSession](isocialsessioniunknown.md) configurée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d06e5-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="d06e5-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="d06e5-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="d06e5-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="d06e5-117">Method</span></span>  <br/> |<span data-ttu-id="d06e5-118">Obtient une chaîne qui décrit les fonctionnalités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d06e5-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="d06e5-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="d06e5-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="d06e5-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="d06e5-120">Method</span></span>  <br/> |<span data-ttu-id="d06e5-121">Obtient une interface [ISocialSession.](isocialsessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="d06e5-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="d06e5-122">GetStatusSettings</span><span class="sxs-lookup"><span data-stu-id="d06e5-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="d06e5-123">Méthode</span><span class="sxs-lookup"><span data-stu-id="d06e5-123">Method</span></span>  <br/> |<span data-ttu-id="d06e5-124">Cette méthode n’est actuellement pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d06e5-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="d06e5-125">Load</span><span class="sxs-lookup"><span data-stu-id="d06e5-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="d06e5-126">Méthode</span><span class="sxs-lookup"><span data-stu-id="d06e5-126">Method</span></span>  <br/> |<span data-ttu-id="d06e5-127">Initialise le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="d06e5-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="d06e5-128">SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="d06e5-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="d06e5-129">Propriété</span><span class="sxs-lookup"><span data-stu-id="d06e5-129">Property</span></span>  <br/> |<span data-ttu-id="d06e5-130">Renvoie un GUID qui représente un identificateur unique pour le réseau social.</span><span class="sxs-lookup"><span data-stu-id="d06e5-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|[<span data-ttu-id="d06e5-131">SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="d06e5-131">SocialNetworkIcon</span></span>](isocialprovider-socialnetworkicon.md) <br/> |<span data-ttu-id="d06e5-132">Propriété</span><span class="sxs-lookup"><span data-stu-id="d06e5-132">Property</span></span>  <br/> |<span data-ttu-id="d06e5-133">Renvoie un tableau d’octets qui représente l’icône du réseau social.</span><span class="sxs-lookup"><span data-stu-id="d06e5-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="d06e5-134">SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="d06e5-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="d06e5-135">Propriété</span><span class="sxs-lookup"><span data-stu-id="d06e5-135">Property</span></span>  <br/> |<span data-ttu-id="d06e5-136">Renvoie une chaîne qui représente le nom du réseau social.</span><span class="sxs-lookup"><span data-stu-id="d06e5-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="d06e5-137">Version</span><span class="sxs-lookup"><span data-stu-id="d06e5-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="d06e5-138">Propriété</span><span class="sxs-lookup"><span data-stu-id="d06e5-138">Property</span></span>  <br/> |<span data-ttu-id="d06e5-139">Renvoie une chaîne qui représente le numéro de version du fournisseur pour ce réseau social.</span><span class="sxs-lookup"><span data-stu-id="d06e5-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d06e5-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="d06e5-140">Remarks</span></span>

<span data-ttu-id="d06e5-141">Un fournisseur OSC doit implémenter cette interface pour communiquer avec l’OSC.</span><span class="sxs-lookup"><span data-stu-id="d06e5-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d06e5-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d06e5-142">See also</span></span>

- [<span data-ttu-id="d06e5-143">Interfaces de fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="d06e5-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

