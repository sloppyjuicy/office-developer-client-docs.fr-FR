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
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="ea61c-103">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ea61c-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="ea61c-104">Représente une instance d’un fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="ea61c-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="ea61c-105">Members</span><span class="sxs-lookup"><span data-stu-id="ea61c-105">Members</span></span>

<span data-ttu-id="ea61c-106">Le tableau suivant indique les membres qui sont disponibles sur l’interface **ISocialProvider.**</span><span class="sxs-lookup"><span data-stu-id="ea61c-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="ea61c-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="ea61c-107">**Name**</span></span>|<span data-ttu-id="ea61c-108">**Type de membre**</span><span class="sxs-lookup"><span data-stu-id="ea61c-108">**Member type**</span></span>|<span data-ttu-id="ea61c-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="ea61c-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ea61c-110">DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="ea61c-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="ea61c-111">Propriété</span><span class="sxs-lookup"><span data-stu-id="ea61c-111">Property</span></span>  <br/> |<span data-ttu-id="ea61c-112">Renvoie un tableau de chaînes qui spécifient les URL de site pour le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="ea61c-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="ea61c-113">GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="ea61c-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="ea61c-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="ea61c-114">Method</span></span>  <br/> |<span data-ttu-id="ea61c-115">Récupère une interface [ISocialSession](isocialsessioniunknown.md) configurée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ea61c-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="ea61c-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="ea61c-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="ea61c-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="ea61c-117">Method</span></span>  <br/> |<span data-ttu-id="ea61c-118">Obtient une chaîne qui décrit les fonctionnalités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ea61c-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="ea61c-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="ea61c-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="ea61c-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="ea61c-120">Method</span></span>  <br/> |<span data-ttu-id="ea61c-121">Obtient une interface [ISocialSession.](isocialsessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="ea61c-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="ea61c-122">GetStatusSettings</span><span class="sxs-lookup"><span data-stu-id="ea61c-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="ea61c-123">Méthode</span><span class="sxs-lookup"><span data-stu-id="ea61c-123">Method</span></span>  <br/> |<span data-ttu-id="ea61c-124">Cette méthode n’est actuellement pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ea61c-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="ea61c-125">Load</span><span class="sxs-lookup"><span data-stu-id="ea61c-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="ea61c-126">Méthode</span><span class="sxs-lookup"><span data-stu-id="ea61c-126">Method</span></span>  <br/> |<span data-ttu-id="ea61c-127">Initialise le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="ea61c-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="ea61c-128">SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="ea61c-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="ea61c-129">Propriété</span><span class="sxs-lookup"><span data-stu-id="ea61c-129">Property</span></span>  <br/> |<span data-ttu-id="ea61c-130">Renvoie un GUID qui représente un identificateur unique pour le réseau social.</span><span class="sxs-lookup"><span data-stu-id="ea61c-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|[<span data-ttu-id="ea61c-131">SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="ea61c-131">SocialNetworkIcon</span></span>](isocialprovider-socialnetworkicon.md) <br/> |<span data-ttu-id="ea61c-132">Propriété</span><span class="sxs-lookup"><span data-stu-id="ea61c-132">Property</span></span>  <br/> |<span data-ttu-id="ea61c-133">Renvoie un tableau d’octets qui représente l’icône du réseau social.</span><span class="sxs-lookup"><span data-stu-id="ea61c-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="ea61c-134">SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="ea61c-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="ea61c-135">Propriété</span><span class="sxs-lookup"><span data-stu-id="ea61c-135">Property</span></span>  <br/> |<span data-ttu-id="ea61c-136">Renvoie une chaîne qui représente le nom du réseau social.</span><span class="sxs-lookup"><span data-stu-id="ea61c-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="ea61c-137">Version</span><span class="sxs-lookup"><span data-stu-id="ea61c-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="ea61c-138">Propriété</span><span class="sxs-lookup"><span data-stu-id="ea61c-138">Property</span></span>  <br/> |<span data-ttu-id="ea61c-139">Renvoie une chaîne qui représente le numéro de version du fournisseur pour ce réseau social.</span><span class="sxs-lookup"><span data-stu-id="ea61c-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea61c-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="ea61c-140">Remarks</span></span>

<span data-ttu-id="ea61c-141">Un fournisseur OSC doit implémenter cette interface pour communiquer avec l’OSC.</span><span class="sxs-lookup"><span data-stu-id="ea61c-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ea61c-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea61c-142">See also</span></span>

- [<span data-ttu-id="ea61c-143">Outlook Interfaces de fournisseur de connecteurs sociaux</span><span class="sxs-lookup"><span data-stu-id="ea61c-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

