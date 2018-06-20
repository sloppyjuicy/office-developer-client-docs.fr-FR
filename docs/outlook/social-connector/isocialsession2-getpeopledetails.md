---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Renvoie une chaîne qui constituée une collection d’une personne et l’image plus d’informations pour les utilisateurs spécifiés par le paramètre personsAddresses.
ms.openlocfilehash: 756f8de3a0615420826fe725528c92351d521832
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787623"
---
# <a name="isocialsession2getpeopledetails"></a><span data-ttu-id="a72ee-103">ISocialSession2::GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="a72ee-103">ISocialSession2::GetPeopleDetails</span></span>

<span data-ttu-id="a72ee-104">Renvoie une chaîne qui constituée une collection d’une personne et l’image plus d’informations pour les utilisateurs spécifiés par le paramètre _personsAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="a72ee-104">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="a72ee-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a72ee-105">Parameters</span></span>

<span data-ttu-id="a72ee-106">_personsAddresses_</span><span class="sxs-lookup"><span data-stu-id="a72ee-106">_personsAddresses_</span></span>
  
> <span data-ttu-id="a72ee-107">[in] Chaîne XML qui spécifie les adresses SMTP de hachage d’un ensemble d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a72ee-107">[in] An XML string that specifies the hashed SMTP addresses of a set of users.</span></span>
    
<span data-ttu-id="a72ee-108">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="a72ee-108">_personsCollection_</span></span>
  
> <span data-ttu-id="a72ee-109">[out] Chaîne XML qui contient une collection de détails de la personne et de l’image.</span><span class="sxs-lookup"><span data-stu-id="a72ee-109">[out] An XML string that contains a collection of person and picture details.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a72ee-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="a72ee-110">Remarks</span></span>

<span data-ttu-id="a72ee-111">L’Outlook Social Connector (OSC) appelle **GetPeopleDetails** si le fournisseur OSC prend en charge la synchronisation à la demande ou hybride de vos amis et non amis.</span><span class="sxs-lookup"><span data-stu-id="a72ee-111">The Outlook Social Connector (OSC) calls **GetPeopleDetails** if the OSC provider supports on-demand or hybrid synchronization of friends and non-friends.</span></span> 
  
<span data-ttu-id="a72ee-112">Le paramètre _personsAddresses_ doit être conforme à la définition de schéma pour **hashedAddresses**, telle que définie dans le schéma pour l’extensibilité de fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="a72ee-112">The  _personsAddresses_ parameter must conform to the schema definition for **hashedAddresses**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="a72ee-113">La chaîne _personsAddresses_ représente un ensemble de hachage adresses SMTP pour chaque utilisateur affiché dans le volet personnes.</span><span class="sxs-lookup"><span data-stu-id="a72ee-113">The  _personsAddresses_ string represents a set of hashed SMTP addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="a72ee-114">L’utilisateur ne dispose pas à un ami de l’utilisateur connecté, représenté par la propriété [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) .</span><span class="sxs-lookup"><span data-stu-id="a72ee-114">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> <span data-ttu-id="a72ee-115">Les adresses SMTP hachage sont chiffrés à l’aide de la fonction de hachage spécifiée par l’élément **hashFunction** dans du fournisseur **fonctionnalités** XML.</span><span class="sxs-lookup"><span data-stu-id="a72ee-115">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="a72ee-116">L’OSC identifie chaque **hashedAddress** dans la collection _personAddresses_ avec un élément **d’index** .</span><span class="sxs-lookup"><span data-stu-id="a72ee-116">The OSC identifies each **hashedAddress** in the  _personAddresses_ collection with an **index** element.</span></span> <span data-ttu-id="a72ee-117">Le fournisseur doit utiliser l’élément **d’index** pour identifier le destinataire **personne** XML lorsqu’elle retourne **amis** XML pour **GetPeopleDetails**.</span><span class="sxs-lookup"><span data-stu-id="a72ee-117">The provider must use the **index** element to identify the recipient's **person** XML when it returns **friends** XML for **GetPeopleDetails**.</span></span> <span data-ttu-id="a72ee-118">Si le destinataire n’est pas un utilisateur inscrit sur le réseaux sociaux, le fournisseur ne doit pas retourner toute **personne** XML du destinataire.</span><span class="sxs-lookup"><span data-stu-id="a72ee-118">If the recipient is not a registered user on the social network, the provider must not return any **person** XML for that recipient.</span></span> <span data-ttu-id="a72ee-119">L’élément **d’index** pour chaque utilisateur réseau représenté par une **personne** XML correspond à l’élément **d’index** pour le destinataire dans _personsAddresses_.</span><span class="sxs-lookup"><span data-stu-id="a72ee-119">The **index** element for each network user represented by **person** XML corresponds to the **index** element for the recipient in  _personsAddresses_.</span></span>
  
<span data-ttu-id="a72ee-120">L’OSC stocke les informations renvoyées par le paramètre _personsCollection_ en mémoire.</span><span class="sxs-lookup"><span data-stu-id="a72ee-120">The OSC stores the information returned by the  _personsCollection_ parameter in memory.</span></span> <span data-ttu-id="a72ee-121">La chaîne XML _personsCollection_ doit être conforme à la définition de schéma pour des **amis**, telle que définie dans le schéma pour l’extensibilité de fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="a72ee-121">The  _personsCollection_ XML string must conform to the schema definition for **friends**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="a72ee-122">Pour plus d’informations sur la façon dont l’OSC utilise et met à jour ces informations en mémoire, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="a72ee-122">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a72ee-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a72ee-123">See also</span></span>

- [<span data-ttu-id="a72ee-124">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a72ee-124">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="a72ee-125">Synchronisation de vos amis et activités</span><span class="sxs-lookup"><span data-stu-id="a72ee-125">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

