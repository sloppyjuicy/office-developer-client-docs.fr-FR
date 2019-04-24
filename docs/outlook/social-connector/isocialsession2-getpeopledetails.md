---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Renvoie une chaîne qui contient une collection de détails de personne et d'image pour les utilisateurs spécifiés par le paramètre personsAddresses.
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344869"
---
# <a name="isocialsession2getpeopledetails"></a><span data-ttu-id="8aedd-103">ISocialSession2::GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="8aedd-103">ISocialSession2::GetPeopleDetails</span></span>

<span data-ttu-id="8aedd-104">Renvoie une chaîne qui contient une collection de détails de personne et d'image pour les utilisateurs spécifiés par le paramètre _personsAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="8aedd-104">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="8aedd-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8aedd-105">Parameters</span></span>

<span data-ttu-id="8aedd-106">_personsAddresses_</span><span class="sxs-lookup"><span data-stu-id="8aedd-106">_personsAddresses_</span></span>
  
> <span data-ttu-id="8aedd-107">dans Chaîne XML qui spécifie les adresses SMTP hachées d'un ensemble d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8aedd-107">[in] An XML string that specifies the hashed SMTP addresses of a set of users.</span></span>
    
<span data-ttu-id="8aedd-108">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="8aedd-108">_personsCollection_</span></span>
  
> <span data-ttu-id="8aedd-109">remarquer Chaîne XML qui contient une collection de détails de personne et d'image.</span><span class="sxs-lookup"><span data-stu-id="8aedd-109">[out] An XML string that contains a collection of person and picture details.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8aedd-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="8aedd-110">Remarks</span></span>

<span data-ttu-id="8aedd-111">Outlook Social Connector (OSC) appelle **GetPeopleDetails** si le fournisseur OSC prend en charge la synchronisation à la demande ou hybride des amis et des non-amis.</span><span class="sxs-lookup"><span data-stu-id="8aedd-111">The Outlook Social Connector (OSC) calls **GetPeopleDetails** if the OSC provider supports on-demand or hybrid synchronization of friends and non-friends.</span></span> 
  
<span data-ttu-id="8aedd-112">Le paramètre _personsAddresses_ doit être conforme à la définition de schéma pour **hashedAddresses**, comme défini dans le schéma de l'extensibilité du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="8aedd-112">The  _personsAddresses_ parameter must conform to the schema definition for **hashedAddresses**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="8aedd-113">La chaîne _personsAddresses_ représente un ensemble d'adresses SMTP hachées pour chaque utilisateur affiché dans le volet de personnes.</span><span class="sxs-lookup"><span data-stu-id="8aedd-113">The  _personsAddresses_ string represents a set of hashed SMTP addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="8aedd-114">L'utilisateur ne doit pas nécessairement être un ami de l'utilisateur connecté représenté par la propriété [ISocialSession:: LoggedOnUserName](isocialsession-loggedonusername.md) .</span><span class="sxs-lookup"><span data-stu-id="8aedd-114">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> <span data-ttu-id="8aedd-115">Les adresses SMTP hachées sont chiffrées à l'aide de la fonction de hachage spécifiée par l'élément **hashFunction** dans le code XML des **fonctionnalités** du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8aedd-115">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="8aedd-116">L'élément OSC identifie chaque **hashedAddress** dans la collection _personAddresses_ à l'aide d'un élément **index** .</span><span class="sxs-lookup"><span data-stu-id="8aedd-116">The OSC identifies each **hashedAddress** in the  _personAddresses_ collection with an **index** element.</span></span> <span data-ttu-id="8aedd-117">Le fournisseur doit utiliser l'élément **index** pour identifier le code XML de la **personne** du destinataire lorsqu'il renvoie des **amis** XML pour **GetPeopleDetails**.</span><span class="sxs-lookup"><span data-stu-id="8aedd-117">The provider must use the **index** element to identify the recipient's **person** XML when it returns **friends** XML for **GetPeopleDetails**.</span></span> <span data-ttu-id="8aedd-118">Si le destinataire n'est pas un utilisateur inscrit sur le réseau social, le fournisseur ne doit pas \*\*\*\* renvoyer de code XML pour ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="8aedd-118">If the recipient is not a registered user on the social network, the provider must not return any **person** XML for that recipient.</span></span> <span data-ttu-id="8aedd-119">L'élément **index** de chaque utilisateur réseau représenté par la **personne** XML correspond à l'élément **index** du destinataire dans _personsAddresses_.</span><span class="sxs-lookup"><span data-stu-id="8aedd-119">The **index** element for each network user represented by **person** XML corresponds to the **index** element for the recipient in  _personsAddresses_.</span></span>
  
<span data-ttu-id="8aedd-120">L'OSC stocke les informations renvoyées par le paramètre _personsCollection_ en mémoire.</span><span class="sxs-lookup"><span data-stu-id="8aedd-120">The OSC stores the information returned by the  _personsCollection_ parameter in memory.</span></span> <span data-ttu-id="8aedd-121">La chaîne XML _personsCollection_ doit être conforme à la définition de schéma pour les **amis**, comme défini dans le schéma pour l'extensibilité du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="8aedd-121">The  _personsCollection_ XML string must conform to the schema definition for **friends**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="8aedd-122">Pour plus d'informations sur l'utilisation et la mise à jour de ces informations en mémoire par le OSC, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="8aedd-122">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8aedd-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8aedd-123">See also</span></span>

- [<span data-ttu-id="8aedd-124">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8aedd-124">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="8aedd-125">Synchronisation des amis et des activités</span><span class="sxs-lookup"><span data-stu-id="8aedd-125">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

