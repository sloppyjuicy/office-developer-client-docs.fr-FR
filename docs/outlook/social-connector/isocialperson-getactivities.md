---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Cette méthode a été déconseillée dans Outlook Social Connector 2013.
ms.openlocfilehash: af952b6d57325e1b52093fcf655e6fdc271ca34f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787586"
---
# <a name="isocialpersongetactivities"></a><span data-ttu-id="f65aa-103">ISocialPerson::GetActivities</span><span class="sxs-lookup"><span data-stu-id="f65aa-103">ISocialPerson::GetActivities</span></span>

<span data-ttu-id="f65aa-104">Cette méthode a été déconseillée dans Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="f65aa-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a><span data-ttu-id="f65aa-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="f65aa-105">Remarks</span></span>

<span data-ttu-id="f65aa-106">Démarrage dans Outlook Social Connector 2013, l’OSC prend en charge la synchronisation des activités uniquement sur demande et non mis en cache ou synchronisation hybride des activités.</span><span class="sxs-lookup"><span data-stu-id="f65aa-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="f65aa-107">L’OSC ignore le paramètre **cacheActivities** dans le XML des fonctionnalités et n’appelle pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f65aa-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and does not call this method.</span></span> <span data-ttu-id="f65aa-108">Pour prendre en charge la recherche d’activités dynamique, implémentez la méthode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="f65aa-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="f65aa-109">Définir **cacheActivities** comme **faux**, **getActivities** et **dynamicActivitiesLookupEx** en tant que **la valeur true**, ce qui vous invite à l’OSC à appeler **ISocialSession2::GetActivitiesEx** à la place.</span><span class="sxs-lookup"><span data-stu-id="f65aa-109">Set **cacheActivities** as **false**, **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="f65aa-110">Pour plus d’informations sur comment l’OSC Obtient les activités de vos amis, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="f65aa-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f65aa-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f65aa-111">See also</span></span>

- [<span data-ttu-id="f65aa-112">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f65aa-112">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

