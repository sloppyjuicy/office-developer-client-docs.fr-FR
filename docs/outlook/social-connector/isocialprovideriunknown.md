---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Représente une instance d'un fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285483"
---
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="d7a72-103">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d7a72-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="d7a72-104">Représente une instance d'un fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="d7a72-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="d7a72-105">Members</span><span class="sxs-lookup"><span data-stu-id="d7a72-105">Members</span></span>

<span data-ttu-id="d7a72-106">Le tableau suivant indique les membres qui sont disponibles sur l'interface **ISocialProvider** .</span><span class="sxs-lookup"><span data-stu-id="d7a72-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="d7a72-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="d7a72-107">**Name**</span></span>|<span data-ttu-id="d7a72-108">**Type de membre**</span><span class="sxs-lookup"><span data-stu-id="d7a72-108">**Member type**</span></span>|<span data-ttu-id="d7a72-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="d7a72-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d7a72-110">DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="d7a72-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="d7a72-111">Propriété</span><span class="sxs-lookup"><span data-stu-id="d7a72-111">Property</span></span>  <br/> |<span data-ttu-id="d7a72-112">Renvoie un tableau de chaînes qui spécifient les URL de site pour le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="d7a72-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="d7a72-113">GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="d7a72-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="d7a72-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="d7a72-114">Method</span></span>  <br/> |<span data-ttu-id="d7a72-115">Récupère une interface [ISocialSession](isocialsessioniunknown.md) configurée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d7a72-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="d7a72-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="d7a72-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="d7a72-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="d7a72-117">Method</span></span>  <br/> |<span data-ttu-id="d7a72-118">Obtient une valeur de type String qui décrit les fonctionnalités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d7a72-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="d7a72-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="d7a72-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="d7a72-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="d7a72-120">Method</span></span>  <br/> |<span data-ttu-id="d7a72-121">Obtient une interface [ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="d7a72-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="d7a72-122">GetStatusSettings</span><span class="sxs-lookup"><span data-stu-id="d7a72-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="d7a72-123">Méthode</span><span class="sxs-lookup"><span data-stu-id="d7a72-123">Method</span></span>  <br/> |<span data-ttu-id="d7a72-124">Cette méthode n'est pas prise en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="d7a72-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="d7a72-125">Load</span><span class="sxs-lookup"><span data-stu-id="d7a72-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="d7a72-126">Méthode</span><span class="sxs-lookup"><span data-stu-id="d7a72-126">Method</span></span>  <br/> |<span data-ttu-id="d7a72-127">Initialise le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="d7a72-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="d7a72-128">SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="d7a72-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="d7a72-129">Propriété</span><span class="sxs-lookup"><span data-stu-id="d7a72-129">Property</span></span>  <br/> |<span data-ttu-id="d7a72-130">Renvoie un GUID qui représente un identificateur unique pour le réseau social.</span><span class="sxs-lookup"><span data-stu-id="d7a72-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|[<span data-ttu-id="d7a72-131">SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="d7a72-131">SocialNetworkIcon</span></span>](isocialprovider-socialnetworkicon.md) <br/> |<span data-ttu-id="d7a72-132">Propriété</span><span class="sxs-lookup"><span data-stu-id="d7a72-132">Property</span></span>  <br/> |<span data-ttu-id="d7a72-133">Renvoie un tableau d'octets qui représente l'icône du réseau social.</span><span class="sxs-lookup"><span data-stu-id="d7a72-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="d7a72-134">SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="d7a72-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="d7a72-135">Propriété</span><span class="sxs-lookup"><span data-stu-id="d7a72-135">Property</span></span>  <br/> |<span data-ttu-id="d7a72-136">Renvoie une valeur de type String qui représente le nom du réseau social.</span><span class="sxs-lookup"><span data-stu-id="d7a72-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="d7a72-137">Version</span><span class="sxs-lookup"><span data-stu-id="d7a72-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="d7a72-138">Propriété</span><span class="sxs-lookup"><span data-stu-id="d7a72-138">Property</span></span>  <br/> |<span data-ttu-id="d7a72-139">Renvoie une valeur de type String qui représente le numéro de version du fournisseur de ce réseau social.</span><span class="sxs-lookup"><span data-stu-id="d7a72-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7a72-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7a72-140">Remarks</span></span>

<span data-ttu-id="d7a72-141">Un fournisseur OSC doit implémenter cette interface pour communiquer avec OSC.</span><span class="sxs-lookup"><span data-stu-id="d7a72-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d7a72-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7a72-142">See also</span></span>

- [<span data-ttu-id="d7a72-143">Interfaces de fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="d7a72-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

