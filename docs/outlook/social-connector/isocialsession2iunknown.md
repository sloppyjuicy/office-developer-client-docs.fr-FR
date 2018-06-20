---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Prend en charge l’ajout de contacts, de synchronisation à la demande ou hybride de vos amis, à la demande la synchronisation des activités ou ouvrant une session sur le réseau social à l’aide de mises en cache les informations d’identification.
ms.openlocfilehash: b14804d35e54ebe9fe2a529fb2664f0a661653bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787622"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="3fb0d-103">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3fb0d-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="3fb0d-104">Prend en charge l’ajout de contacts, de synchronisation à la demande ou hybride de vos amis, à la demande la synchronisation des activités ou ouvrant une session sur le réseau social à l’aide de mises en cache les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="3fb0d-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="3fb0d-105">Membres</span><span class="sxs-lookup"><span data-stu-id="3fb0d-105">Members</span></span>

<span data-ttu-id="3fb0d-106">Le tableau suivant indique les membres qui sont disponibles sur l’interface **ISocialSession2** .</span><span class="sxs-lookup"><span data-stu-id="3fb0d-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="3fb0d-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="3fb0d-107">**Name**</span></span>|<span data-ttu-id="3fb0d-108">**Type de membre**</span><span class="sxs-lookup"><span data-stu-id="3fb0d-108">**Member type**</span></span>|<span data-ttu-id="3fb0d-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="3fb0d-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3fb0d-110">FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="3fb0d-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="3fb0d-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="3fb0d-111">Method</span></span>  <br/> |<span data-ttu-id="3fb0d-112">Ajoute la personne identifiée par les paramètres _emailAddresses_ et _displayName_ comme un ami pour l’utilisateur connecté sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="3fb0d-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="3fb0d-113">GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="3fb0d-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="3fb0d-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="3fb0d-114">Method</span></span>  <br/> |<span data-ttu-id="3fb0d-115">Obtient une chaîne qui représente une collection d’activités des utilisateurs spécifiés par le paramètre _hashedAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="3fb0d-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="3fb0d-116">GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="3fb0d-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="3fb0d-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="3fb0d-117">Method</span></span>  <br/> |<span data-ttu-id="3fb0d-118">Renvoie une chaîne qui constituée une collection d’une personne et l’image plus d’informations pour les utilisateurs spécifiés par le paramètre _personsAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="3fb0d-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="3fb0d-119">LogonCached</span><span class="sxs-lookup"><span data-stu-id="3fb0d-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="3fb0d-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="3fb0d-120">Method</span></span>  <br/> |<span data-ttu-id="3fb0d-121">Ouvre une session sur le site de réseau social à l’aide des informations d’identification mises en cache.</span><span class="sxs-lookup"><span data-stu-id="3fb0d-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fb0d-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="3fb0d-122">Remarks</span></span>

<span data-ttu-id="3fb0d-123">Un fournisseur Outlook Social Connector (OSC) peut choisir d’implémenter cette interface si le fournisseur prend en charge la synchronisation de la demande ou hybride de vos amis, à la demande la synchronisation des activités ou ouvrant une session sur le réseau social à l’aide des informations d’identification mises en cache.</span><span class="sxs-lookup"><span data-stu-id="3fb0d-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="3fb0d-124">Si le fournisseur OSC implémente **ISocialSession2** et prend en charge de suivi de personnes sur le réseaux sociaux, le OSC appellent [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) au lieu de [ISocialSession::FollowPerson](isocialsession-followperson.md), et le fournisseur doit implémenter **ISocialSession2::FollowPersonEx**, également.</span><span class="sxs-lookup"><span data-stu-id="3fb0d-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3fb0d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fb0d-125">See also</span></span>

- [<span data-ttu-id="3fb0d-126">Interfaces de fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="3fb0d-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

