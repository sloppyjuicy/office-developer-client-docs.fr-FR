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
ms.openlocfilehash: 7c24494d924b63f5e137f8e9928257967469f19c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787621"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="5bfd2-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="5bfd2-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="5bfd2-104">Obtient une chaîne qui représente une collection d’activités de chacun des utilisateurs spécifiés par le paramètre _hashedAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="5bfd2-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="5bfd2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5bfd2-105">Parameters</span></span>

<span data-ttu-id="5bfd2-106">_hashedAddresses_</span><span class="sxs-lookup"><span data-stu-id="5bfd2-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="5bfd2-107">[in] Une structure qui spécifie un tableau de hachage SMTP adresses pour un ensemble d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="5bfd2-108">_heure de début_</span><span class="sxs-lookup"><span data-stu-id="5bfd2-108">_startTime_</span></span>
  
> <span data-ttu-id="5bfd2-109">[in] Heure après laquelle les activités créées seront retournées.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="5bfd2-110">_activités_</span><span class="sxs-lookup"><span data-stu-id="5bfd2-110">_activities_</span></span>
  
> <span data-ttu-id="5bfd2-111">[out] Chaîne XML qui représente l’ensemble des activités des utilisateurs spécifiés par _hashedAddresses_ sur le réseau social depuis _l’heure de début_.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5bfd2-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="5bfd2-112">Remarks</span></span>

<span data-ttu-id="5bfd2-113">L’OSC appelle **GetActivitiesEx** si le fournisseur OSC prend en charge la synchronisation de la demande d’activités.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="5bfd2-114">L’OSC stocke les informations retournées dans les _activités_ en mémoire.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="5bfd2-115">Pour plus d’informations sur la façon dont l’OSC utilise et met à jour ces informations en mémoire, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="5bfd2-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="5bfd2-116">Démarrage dans Outlook Social Connector 2013, l’OSC prend en charge la synchronisation des activités uniquement sur demande et appelle uniquement pour obtenir des activités **GetActivitiesEx** .</span><span class="sxs-lookup"><span data-stu-id="5bfd2-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="5bfd2-117">Pour prendre en charge de la recherche des activités à la demande, définissez **cacheActivities** comme **false**et **getActivities** et **dynamicActivitiesLookupEx** **a la valeur True**et la OSC appellera **GetActivitiesEx**.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="5bfd2-118">La chaîne XML renvoyée doit être conformes à la définition de schéma pour **activityFeed**, telle que définie dans le schéma pour l’extensibilité de fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="5bfd2-119">Le String _hashedAddresses_ représente un ensemble d’adresses de hachage pour chaque utilisateur affiché dans le volet personnes.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="5bfd2-120">Les adresses SMTP hachage sont chiffrés à l’aide de la fonction de hachage spécifiée par l’élément **hashFunction** dans du fournisseur **fonctionnalités** XML.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="5bfd2-121">L’utilisateur ne dispose pas à un ami de l’utilisateur connecté, représenté par la propriété [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) .</span><span class="sxs-lookup"><span data-stu-id="5bfd2-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="5bfd2-122">Le paramètre _startTime_ est une valeur de **Date** en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="5bfd2-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="5bfd2-123">Valeurs d’heure locale doivent être convertis en valeurs de **Date** UTC.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="5bfd2-124">Activités retournée par la méthode **GetActivitiesEx** doivent avoir une valeur d’heure de création qui est supérieure à _l’heure de début_ et inférieure ou égale à **maintenant**.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="5bfd2-125">Si aucune modification n’ont eu lieu entre les **heures de début** et **maintenant**, le fournisseur doit renvoyer une erreur OSC_E_NO_CHANGES.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5bfd2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bfd2-126">See also</span></span>

- [<span data-ttu-id="5bfd2-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5bfd2-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="5bfd2-128">Synchronisation de vos amis et activités</span><span class="sxs-lookup"><span data-stu-id="5bfd2-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

