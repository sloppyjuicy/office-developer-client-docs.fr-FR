---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Obtient une valeur de type String qui représente les détails de la personne, tels que le prénom, le nom et l'URL d'une image de profil.
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286142"
---
# <a name="isocialpersongetdetails"></a><span data-ttu-id="400cf-103">ISocialPerson::GetDetails</span><span class="sxs-lookup"><span data-stu-id="400cf-103">ISocialPerson::GetDetails</span></span>

<span data-ttu-id="400cf-104">Obtient une valeur de type String qui représente les détails de la personne, tels que le prénom, le nom et l'URL d'une image de profil.</span><span class="sxs-lookup"><span data-stu-id="400cf-104">Gets a string that represents details for the person, such as the first name, last name, and a URL to a profile picture.</span></span> 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a><span data-ttu-id="400cf-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="400cf-105">Parameters</span></span>

<span data-ttu-id="400cf-106">_détails_</span><span class="sxs-lookup"><span data-stu-id="400cf-106">_details_</span></span>
  
> <span data-ttu-id="400cf-107">remarquer Valeur de chaîne XML qui représente les détails d'une personne.</span><span class="sxs-lookup"><span data-stu-id="400cf-107">[out] An XML string value that represents the details for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="400cf-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="400cf-108">Remarks</span></span>

<span data-ttu-id="400cf-109">La chaîne XML de _Détails_ renvoyée doit être conforme à la définition de schéma pour **Person**, comme défini dans le schéma pour l'extensibilité du fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="400cf-109">The returned  _details_ XML string must comply with the schema definition for **person**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span>
  
<span data-ttu-id="400cf-110">L'OSC appelle **GetDetails** si le fournisseur OSC prend en charge la synchronisation mise en cache ou hybride des amis sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="400cf-110">The OSC calls **GetDetails** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="400cf-111">Lorsque l'objet OSC Obtient initialement des activités de Friends pour l'utilisateur connecté, il appelle [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)et stocke les informations des amis dans un dossier de contacts spécifique au réseau social, dans la Banque Outlook par défaut de l'utilisateur connecté. .</span><span class="sxs-lookup"><span data-stu-id="400cf-111">When the OSC initially gets friends' activities for the logged on user, it calls [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), and stores friends' information in a contacts folder specific to the social network, in the logged on user's default Outlook store.</span></span> <span data-ttu-id="400cf-112">Par la suite, OSC n'appelle pas **GetFriendsAndColleagues** ou **GetDetails** , sauf si l'intervalle d'actualisation du cache a expiré.</span><span class="sxs-lookup"><span data-stu-id="400cf-112">Subsequently the OSC does not call **GetFriendsAndColleagues** or **GetDetails** unless the refresh interval for the cache has expired.</span></span> <span data-ttu-id="400cf-113">Pour plus d'informations sur la façon dont OSC met en cache les informations des amis dans un dossier contacts, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="400cf-113">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="400cf-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="400cf-114">See also</span></span>

- [<span data-ttu-id="400cf-115">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="400cf-115">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

