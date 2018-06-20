---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Obtient une chaîne qui représente les détails de la personne, telles que le prénom, nom et une URL vers une image de profil.
ms.openlocfilehash: 158ce9b5c6a97ffff0325427ed07c74f518941d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787585"
---
# <a name="isocialpersongetdetails"></a><span data-ttu-id="5e4bf-103">ISocialPerson::GetDetails</span><span class="sxs-lookup"><span data-stu-id="5e4bf-103">ISocialPerson::GetDetails</span></span>

<span data-ttu-id="5e4bf-104">Obtient une chaîne qui représente les détails de la personne, telles que le prénom, nom et une URL vers une image de profil.</span><span class="sxs-lookup"><span data-stu-id="5e4bf-104">Gets a string that represents details for the person, such as the first name, last name, and a URL to a profile picture.</span></span> 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a><span data-ttu-id="5e4bf-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e4bf-105">Parameters</span></span>

<span data-ttu-id="5e4bf-106">_plus d’informations_</span><span class="sxs-lookup"><span data-stu-id="5e4bf-106">_details_</span></span>
  
> <span data-ttu-id="5e4bf-107">[out] Une valeur de chaîne XML qui représente les détails d’une personne.</span><span class="sxs-lookup"><span data-stu-id="5e4bf-107">[out] An XML string value that represents the details for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5e4bf-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="5e4bf-108">Remarks</span></span>

<span data-ttu-id="5e4bf-109">La chaîne XML renvoyée _Détails_ doit être conformes à la définition de schéma pour la **personne**, telle que définie dans le schéma pour l’extensibilité de fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="5e4bf-109">The returned  _details_ XML string must comply with the schema definition for **person**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span>
  
<span data-ttu-id="5e4bf-110">L’OSC appelle **GetDetails** si la mise en cache de la prise en charge du fournisseur OSC ou synchronisation hybride d’amis sur le réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="5e4bf-110">The OSC calls **GetDetails** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="5e4bf-111">Lorsque l’OSC obtient initialement activités amis pour l’utilisateur connecté, il appelle [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)et stocke les informations de vos amis dans un dossier contacts spécifique au réseau social, dans le magasin d’Outlook par défaut de l’utilisateur ayant ouvert une session sur .</span><span class="sxs-lookup"><span data-stu-id="5e4bf-111">When the OSC initially gets friends' activities for the logged on user, it calls [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), and stores friends' information in a contacts folder specific to the social network, in the logged on user's default Outlook store.</span></span> <span data-ttu-id="5e4bf-112">Par la suite l’OSC n’appelle **GetFriendsAndColleagues** ou **GetDetails** , sauf si l’intervalle d’actualisation du cache a expiré.</span><span class="sxs-lookup"><span data-stu-id="5e4bf-112">Subsequently the OSC does not call **GetFriendsAndColleagues** or **GetDetails** unless the refresh interval for the cache has expired.</span></span> <span data-ttu-id="5e4bf-113">Pour plus d’informations sur la façon dont l’OSC met en cache les informations de vos amis dans un dossier contacts, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="5e4bf-113">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5e4bf-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e4bf-114">See also</span></span>

- [<span data-ttu-id="5e4bf-115">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e4bf-115">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

