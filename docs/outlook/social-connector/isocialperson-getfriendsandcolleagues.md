---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Obtient une valeur de type String qui représente une collection de personnes.
ms.openlocfilehash: f755476f66ab2f91471b88c74baff899f31b83e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407654"
---
# <a name="isocialpersongetfriendsandcolleagues"></a><span data-ttu-id="4e7d8-103">ISocialPerson::GetFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="4e7d8-103">ISocialPerson::GetFriendsAndColleagues</span></span>

<span data-ttu-id="4e7d8-104">Obtient une valeur de type String qui représente une collection de personnes.</span><span class="sxs-lookup"><span data-stu-id="4e7d8-104">Gets a string that represents a collection of people.</span></span>
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="4e7d8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e7d8-105">Parameters</span></span>

<span data-ttu-id="4e7d8-106">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="4e7d8-106">_personsCollection_</span></span>
  
> <span data-ttu-id="4e7d8-107">remarquer Une chaîne XML qui représente un ensemble d'amis de la personne et qui est conforme à la définition des **amis** définie dans le schéma XML pour l'extensibilité du fournisseur OSC (Outlook Social Connector).</span><span class="sxs-lookup"><span data-stu-id="4e7d8-107">[out] An XML string that represents a set of friends of the person, and that complies with the definition of **friends** as defined in the XML schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4e7d8-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e7d8-108">Remarks</span></span>

<span data-ttu-id="4e7d8-109">L'OSC appelle **GetFriendsAndColleagues** si le fournisseur OSC prend en charge la synchronisation mise en cache ou hybride des amis sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="4e7d8-109">The OSC calls **GetFriendsAndColleagues** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="4e7d8-110">Lorsque la méthode OSC appelle initialement la méthode **GetFriendsAndColleagues** pour l'utilisateur Outlook qui est connecté au réseau social, **GetFriendsAndColleagues** renvoie une chaîne XML qui représente les amis de l'utilisateur connecté sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="4e7d8-110">When the OSC initially calls the **GetFriendsAndColleagues** method for the Outlook user who is logged on to the social network, **GetFriendsAndColleagues** returns an XML string that represents friends of the logged-on user on the social network.</span></span> <span data-ttu-id="4e7d8-111">La chaîne XML est conforme à la \*\*\*\* définition de schéma XML friends et spécifie un élément **Person** (qui est également conforme à la définition de schéma du fournisseur OSC) pour chaque Friend.</span><span class="sxs-lookup"><span data-stu-id="4e7d8-111">The XML string complies with the **friends** XML schema definition and specifies a **person** element (which also complies with the OSC provider schema definition) for each friend.</span></span> 
  
<span data-ttu-id="4e7d8-112">Lorsque **GetFriendsAndColleagues** renvoie les informations sur les amis de l'utilisateur connecté, OSC stocke ces informations dans un dossier de contacts.</span><span class="sxs-lookup"><span data-stu-id="4e7d8-112">When **GetFriendsAndColleagues** returns the friends information for the logged-on user, the OSC stores that information in a contacts folder.</span></span> <span data-ttu-id="4e7d8-113">Ce dossier est propre au réseau social et réside dans la Banque Outlook par défaut de l'utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="4e7d8-113">This folder is specific to the social network and resides in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="4e7d8-114">Pour plus d'informations sur la façon dont OSC met en cache les informations des amis dans un dossier contacts, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="4e7d8-114">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="4e7d8-115">Les informations de chaque ami renvoyé dans le paramètre _personsCollection_ sont conformes à la définition de schéma XML pour **Person**.</span><span class="sxs-lookup"><span data-stu-id="4e7d8-115">Information for each friend returned in the  _personsCollection_ parameter complies with the XML schema definition for **person**.</span></span> <span data-ttu-id="4e7d8-116">L'élément **Person** prend en charge de nombreux éléments d'information pour chaque ami, y compris les adresses de messagerie SMTP (qui correspondent aux éléments **EmailAddress**, **EmailAddress2**et **EmailAddress3** ) spécifiés par l'ami sur le réseau social et ID d'utilisateur (qui correspond à l'élément **userid** ) qui identifie cet ami sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="4e7d8-116">The **person** element supports many pieces of information for each friend, including the SMTP email addresses (which map to the **emailAddress**, **emailAddress2**, and **emailAddress3** elements) that the friend has specified on the social network, and the user ID (which maps to the **userID** element) that identifies that friend on the social network.</span></span> 
  
<span data-ttu-id="4e7d8-117">Pour afficher les activités d'un utilisateur Outlook sélectionné dans le volet de personnes, le OSC tente de faire correspondre l'utilisateur avec chaque ami renvoyé depuis **GetFriendsAndColleagues**.</span><span class="sxs-lookup"><span data-stu-id="4e7d8-117">To show activities for an Outlook user selected in the People Pane, the OSC tries to match the user with each friend returned from **GetFriendsAndColleagues**.</span></span> <span data-ttu-id="4e7d8-118">Le OSC effectue cette opération en comparant l'adresse SMTP de l'utilisateur Outlook sélectionné aux adresses de messagerie spécifiées par chaque ami sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="4e7d8-118">The OSC does this by matching the SMTP address of the selected Outlook user with the email addresses that each friend has specified on the social network.</span></span> <span data-ttu-id="4e7d8-119">Si OSC trouve une adresse de messagerie SMTP correspondante, le OSC utilise l'ID de l' **utilisateur** correspondant pour appeler la méthode [ISocialSession:: GetPerson](isocialsession-getperson.md) .</span><span class="sxs-lookup"><span data-stu-id="4e7d8-119">If the OSC finds a matching SMTP email address, the OSC uses the corresponding **userID** of the friend to call the [ISocialSession::GetPerson](isocialsession-getperson.md) method.</span></span> <span data-ttu-id="4e7d8-120">Il effectue cette opération pour obtenir un objet [ISocialPerson](isocialpersoniunknown.md) pour cet ami, qui lui permet d'obtenir des activités et des images de cet ami à partir du réseau social.</span><span class="sxs-lookup"><span data-stu-id="4e7d8-120">It does this to obtain an [ISocialPerson](isocialpersoniunknown.md) object for that friend, which then enables the OSC to get activities and pictures of that friend from the social network.</span></span> 
  
<span data-ttu-id="4e7d8-121">Toutefois, si l'utilisateur Outlook sélectionné ne spécifie pas la même adresse SMTP sur un compte sur le réseau social ou si l'utilisateur Outlook ne dispose pas d'un compte sur ce réseau social, le OSC ne peut pas trouver de correspondance pour cet utilisateur et n'affiche aucune opération. es pour cet utilisateur sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="4e7d8-121">However, if the selected Outlook user does not specify that same SMTP address on an account on the social network, or if the Outlook user does not have an account on that social network, the OSC will not be able to find a match for that user and will not display any activities for that user on the social network.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e7d8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e7d8-122">See also</span></span>

- [<span data-ttu-id="4e7d8-123">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e7d8-123">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)
- [<span data-ttu-id="4e7d8-124">Obtention d'informations sur les amis</span><span class="sxs-lookup"><span data-stu-id="4e7d8-124">Getting Friends Information</span></span>](getting-friends-information.md)

