---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Prend en charge l'ajout de amis, la synchronisation à la demande ou hybride des amis, la synchronisation à la demande des activités ou la connexion au réseau social à l'aide des informations d'identification mises en cache.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345296"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="05781-103">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="05781-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="05781-104">Prend en charge l'ajout de amis, la synchronisation à la demande ou hybride des amis, la synchronisation à la demande des activités ou la connexion au réseau social à l'aide des informations d'identification mises en cache.</span><span class="sxs-lookup"><span data-stu-id="05781-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="05781-105">Members</span><span class="sxs-lookup"><span data-stu-id="05781-105">Members</span></span>

<span data-ttu-id="05781-106">Le tableau suivant indique les membres qui sont disponibles sur l'interface **ISocialSession2** .</span><span class="sxs-lookup"><span data-stu-id="05781-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="05781-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="05781-107">**Name**</span></span>|<span data-ttu-id="05781-108">**Type de membre**</span><span class="sxs-lookup"><span data-stu-id="05781-108">**Member type**</span></span>|<span data-ttu-id="05781-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="05781-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="05781-110">FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="05781-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="05781-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="05781-111">Method</span></span>  <br/> |<span data-ttu-id="05781-112">Ajoute la personne identifiée par les paramètres _EmailAddresses_ et _DisplayName_ comme un ami pour l'utilisateur connecté sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="05781-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="05781-113">GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="05781-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="05781-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="05781-114">Method</span></span>  <br/> |<span data-ttu-id="05781-115">Obtient une valeur de type String qui représente une collection d'activités des utilisateurs spécifiés par le paramètre _hashedAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="05781-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="05781-116">GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="05781-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="05781-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="05781-117">Method</span></span>  <br/> |<span data-ttu-id="05781-118">Renvoie une chaîne qui contient une collection de détails de personne et d'image pour les utilisateurs spécifiés par le paramètre _personsAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="05781-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="05781-119">LogonCached</span><span class="sxs-lookup"><span data-stu-id="05781-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="05781-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="05781-120">Method</span></span>  <br/> |<span data-ttu-id="05781-121">Ouvre une session sur le site réseau social en utilisant les informations d'identification mises en cache.</span><span class="sxs-lookup"><span data-stu-id="05781-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05781-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="05781-122">Remarks</span></span>

<span data-ttu-id="05781-123">Un fournisseur Outlook Social Connector (OSC) peut choisir d'implémenter cette interface si le fournisseur prend en charge la synchronisation à la demande ou hybride des amis, la synchronisation à la demande des activités ou la connexion au réseau social à l'aide des informations d'identification mises en cache.</span><span class="sxs-lookup"><span data-stu-id="05781-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="05781-124">Si le fournisseur OSC implémente **ISocialSession2** et prend en charge les personnes suivantes sur le réseau social, le OSC appelle [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md) au lieu de [ISocialSession:: followPerson](isocialsession-followperson.md), et le fournisseur doit implémenter **ISocialSession2:: FollowPersonEx**.</span><span class="sxs-lookup"><span data-stu-id="05781-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="05781-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05781-125">See also</span></span>

- [<span data-ttu-id="05781-126">Interfaces de fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="05781-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

