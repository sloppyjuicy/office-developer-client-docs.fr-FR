---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Obtient une chaîne qui représente une collection d’activités de chacun des utilisateurs spécifiés par le paramètre hashedAddresses.
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404336"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="cabee-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="cabee-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="cabee-104">Obtient une chaîne qui représente une collection d’activités de chacun des utilisateurs spécifiés par le paramètre _hashedAddresses._</span><span class="sxs-lookup"><span data-stu-id="cabee-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="cabee-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="cabee-105">Parameters</span></span>

<span data-ttu-id="cabee-106">_hashedAddresses_</span><span class="sxs-lookup"><span data-stu-id="cabee-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="cabee-107">[in] Structure qui spécifie un tableau d’adresses SMTP hachées pour un ensemble d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="cabee-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="cabee-108">_startTime_</span><span class="sxs-lookup"><span data-stu-id="cabee-108">_startTime_</span></span>
  
> <span data-ttu-id="cabee-109">[in] Heure à laquelle les activités créées sont renvoyées.</span><span class="sxs-lookup"><span data-stu-id="cabee-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="cabee-110">_activities_</span><span class="sxs-lookup"><span data-stu-id="cabee-110">_activities_</span></span>
  
> <span data-ttu-id="cabee-111">[out] Chaîne XML qui représente l’ensemble des activités des utilisateurs spécifiés par _hashedAddresses_ sur le réseau social depuis _l’heure de début._</span><span class="sxs-lookup"><span data-stu-id="cabee-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cabee-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="cabee-112">Remarks</span></span>

<span data-ttu-id="cabee-113">L’OSC appelle **GetActivitiesEx** si le fournisseur OSC prend en charge la synchronisation à la demande des activités.</span><span class="sxs-lookup"><span data-stu-id="cabee-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="cabee-114">L’OSC stocke les informations renvoyées dans  _les activités_ en mémoire.</span><span class="sxs-lookup"><span data-stu-id="cabee-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="cabee-115">Pour plus d’informations sur la façon dont OSC utilise et met à jour ces informations en mémoire, voir [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="cabee-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="cabee-116">À compter Outlook Social Connector 2013, OSC prend en charge uniquement la synchronisation à la demande des activités et appelle **uniquement GetActivitiesEx** pour obtenir des activités.</span><span class="sxs-lookup"><span data-stu-id="cabee-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="cabee-117">Pour prendre en charge la recherche d’activités à la demande, définissez **cacheActivities** sur **false** et **getActivities** et **dynamicActivitiesLookupEx** comme **true**, et l’OSC appelle **GetActivitiesEx**.</span><span class="sxs-lookup"><span data-stu-id="cabee-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="cabee-118">La chaîne XML renvoyée doit être conforme à la définition de schéma pour **activityFeed**, telle que définie dans le schéma pour l’extensibilité du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="cabee-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="cabee-119">Le  _hachage hashedAddresses_ représente un ensemble d’adresses hachées pour chaque utilisateur affiché dans le volet Personnes.</span><span class="sxs-lookup"><span data-stu-id="cabee-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="cabee-120">Les adresses SMTP hachées sont chiffrées à l’aide de la fonction de hachage spécifiée par l’élément **hashFunction** dans le code XML des fonctionnalités **du** fournisseur.</span><span class="sxs-lookup"><span data-stu-id="cabee-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="cabee-121">L’utilisateur n’a pas besoin d’être un ami de l’utilisateur connecté représenté par la propriété [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md)</span><span class="sxs-lookup"><span data-stu-id="cabee-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="cabee-122">Le  _paramètre startTime_ est une **valeur Date** en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="cabee-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="cabee-123">Les valeurs d’heure locale doivent être converties en valeurs UTC **Date.**</span><span class="sxs-lookup"><span data-stu-id="cabee-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="cabee-124">Les activités que la **méthode GetActivitiesEx renvoie** doivent avoir une valeur d’heure de création supérieure à  _l’heure_ de début et inférieure ou égale à **Now**.</span><span class="sxs-lookup"><span data-stu-id="cabee-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="cabee-125">Si aucune modification n’a été apportée entre **startTime** et **Now,** le fournisseur doit renvoyer OSC_E_NO_CHANGES erreur.</span><span class="sxs-lookup"><span data-stu-id="cabee-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cabee-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cabee-126">See also</span></span>

- [<span data-ttu-id="cabee-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cabee-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="cabee-128">Synchronisation des amis et des activités</span><span class="sxs-lookup"><span data-stu-id="cabee-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

