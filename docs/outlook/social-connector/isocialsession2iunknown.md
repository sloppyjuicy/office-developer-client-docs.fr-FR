---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Prend en charge l’ajout d’amis, la synchronisation à la demande ou hybride d’amis, la synchronisation à la demande des activités ou la connexion au réseau social à l’aide d’informations d’identification mises en cache.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408830"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="db1de-103">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="db1de-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="db1de-104">Prend en charge l’ajout d’amis, la synchronisation à la demande ou hybride d’amis, la synchronisation à la demande des activités ou la connexion au réseau social à l’aide d’informations d’identification mises en cache.</span><span class="sxs-lookup"><span data-stu-id="db1de-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="db1de-105">Members</span><span class="sxs-lookup"><span data-stu-id="db1de-105">Members</span></span>

<span data-ttu-id="db1de-106">Le tableau suivant indique les membres disponibles sur l’interface **ISocialSession2.**</span><span class="sxs-lookup"><span data-stu-id="db1de-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="db1de-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="db1de-107">**Name**</span></span>|<span data-ttu-id="db1de-108">**Type de membre**</span><span class="sxs-lookup"><span data-stu-id="db1de-108">**Member type**</span></span>|<span data-ttu-id="db1de-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="db1de-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="db1de-110">FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="db1de-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="db1de-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="db1de-111">Method</span></span>  <br/> |<span data-ttu-id="db1de-112">Ajoute la personne identifiée par les paramètres  _emailAddresses_ et  _displayName_ en tant qu’ami de l’utilisateur connecté sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="db1de-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="db1de-113">GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="db1de-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="db1de-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="db1de-114">Method</span></span>  <br/> |<span data-ttu-id="db1de-115">Obtient une chaîne qui représente une collection d’activités des utilisateurs spécifiés par le paramètre _hashedAddresses._</span><span class="sxs-lookup"><span data-stu-id="db1de-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="db1de-116">GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="db1de-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="db1de-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="db1de-117">Method</span></span>  <br/> |<span data-ttu-id="db1de-118">Renvoie une chaîne qui contient une collection de détails de personne et d’image pour les utilisateurs spécifiés par le paramètre _personsAddresses._</span><span class="sxs-lookup"><span data-stu-id="db1de-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="db1de-119">LogonCached</span><span class="sxs-lookup"><span data-stu-id="db1de-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="db1de-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="db1de-120">Method</span></span>  <br/> |<span data-ttu-id="db1de-121">Se connecte au site de réseau social à l’aide des informations d’identification mises en cache.</span><span class="sxs-lookup"><span data-stu-id="db1de-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db1de-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="db1de-122">Remarks</span></span>

<span data-ttu-id="db1de-123">Un fournisseur Outlook Social Connector (OSC) peut choisir d’implémenter cette interface si le fournisseur prend en charge la synchronisation à la demande ou hybride des amis, la synchronisation à la demande des activités ou la connexion au réseau social à l’aide d’informations d’identification mises en cache.</span><span class="sxs-lookup"><span data-stu-id="db1de-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="db1de-124">Si le fournisseur OSC implémente **ISocialSession2** et prend en charge les personnes suivantes sur le réseau social, l’OSC appelle [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) au lieu de [ISocialSession::FollowPerson](isocialsession-followperson.md), et le fournisseur doit également implémenter **ISocialSession2::FollowPersonEx.**</span><span class="sxs-lookup"><span data-stu-id="db1de-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="db1de-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db1de-125">See also</span></span>

- [<span data-ttu-id="db1de-126">Interfaces de fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="db1de-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

