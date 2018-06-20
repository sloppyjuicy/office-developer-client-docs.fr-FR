---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Obtient une chaîne qui représente une collection de personnes.
ms.openlocfilehash: 36482a6068c592eb0ff07603b6458e8415c3586f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787594"
---
# <a name="isocialpersongetfriendsandcolleagues"></a><span data-ttu-id="597db-103">ISocialPerson::GetFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="597db-103">ISocialPerson::GetFriendsAndColleagues</span></span>

<span data-ttu-id="597db-104">Obtient une chaîne qui représente une collection de personnes.</span><span class="sxs-lookup"><span data-stu-id="597db-104">Gets a string that represents a collection of people.</span></span>
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="597db-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="597db-105">Parameters</span></span>

<span data-ttu-id="597db-106">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="597db-106">_personsCollection_</span></span>
  
> <span data-ttu-id="597db-107">[out] Chaîne XML qui représente un ensemble d’amis ou de la personne, et qui est conforme à la définition de **vos amis** définis dans le schéma XML pour l’extensibilité de fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="597db-107">[out] An XML string that represents a set of friends of the person, and that complies with the definition of **friends** as defined in the XML schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="597db-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="597db-108">Remarks</span></span>

<span data-ttu-id="597db-109">L’OSC appelle **GetFriendsAndColleagues** si la mise en cache de la prise en charge du fournisseur OSC ou synchronisation hybride d’amis sur le réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="597db-109">The OSC calls **GetFriendsAndColleagues** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="597db-110">Lorsque l’OSC appelle initialement la méthode **GetFriendsAndColleagues** pour l’utilisateur Outlook qui est connecté au réseau social, **GetFriendsAndColleagues** renvoie une chaîne XML qui représente des amis de l’utilisateur connecté sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="597db-110">When the OSC initially calls the **GetFriendsAndColleagues** method for the Outlook user who is logged on to the social network, **GetFriendsAndColleagues** returns an XML string that represents friends of the logged-on user on the social network.</span></span> <span data-ttu-id="597db-111">La chaîne XML conforme à la définition de schéma XML **amis** et spécifie un élément de la **personne** (qui également conforme à la définition de schéma de fournisseur OSC) pour chacun d'entre eux.</span><span class="sxs-lookup"><span data-stu-id="597db-111">The XML string complies with the **friends** XML schema definition and specifies a **person** element (which also complies with the OSC provider schema definition) for each friend.</span></span> 
  
<span data-ttu-id="597db-112">Lorsque **GetFriendsAndColleagues** renvoie des informations pour l’utilisateur connecté amis, l’OSC stocke ces informations dans un dossier contacts.</span><span class="sxs-lookup"><span data-stu-id="597db-112">When **GetFriendsAndColleagues** returns the friends information for the logged-on user, the OSC stores that information in a contacts folder.</span></span> <span data-ttu-id="597db-113">Ce dossier est spécifique au réseau social et réside dans le magasin d’Outlook ouvert une session sur l’utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="597db-113">This folder is specific to the social network and resides in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="597db-114">Pour plus d’informations sur la façon dont l’OSC met en cache les informations de vos amis dans un dossier contacts, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="597db-114">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="597db-115">Informations pour chaque ami retournée dans le paramètre _personsCollection_ est conforme à la définition de schéma XML pour la **personne**.</span><span class="sxs-lookup"><span data-stu-id="597db-115">Information for each friend returned in the  _personsCollection_ parameter complies with the XML schema definition for **person**.</span></span> <span data-ttu-id="597db-116">L’élément **personne** prend en charge plusieurs éléments d’information pour chaque ami, y compris les adresses de messagerie SMTP (qui correspondent aux éléments **emailAddress**, **emailAddress2**et **emailAddress3** ) que votre ami a spécifié sur la réseau social et l’ID utilisateur (qui correspond à l’élément **userID** ) qui identifie ce friend sur le réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="597db-116">The **person** element supports many pieces of information for each friend, including the SMTP email addresses (which map to the **emailAddress**, **emailAddress2**, and **emailAddress3** elements) that the friend has specified on the social network, and the user ID (which maps to the **userID** element) that identifies that friend on the social network.</span></span> 
  
<span data-ttu-id="597db-117">Pour afficher les activités pour un utilisateur Outlook sélectionné dans le volet personnes, l’OSC tente de faire correspondre l’utilisateur avec chaque ami renvoyé à partir de **GetFriendsAndColleagues**.</span><span class="sxs-lookup"><span data-stu-id="597db-117">To show activities for an Outlook user selected in the People Pane, the OSC tries to match the user with each friend returned from **GetFriendsAndColleagues**.</span></span> <span data-ttu-id="597db-118">Pour cela, la OSC correspondant à l’adresse SMTP de l’utilisateur Outlook sélectionné avec les adresses de messagerie chaque ami a spécifié sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="597db-118">The OSC does this by matching the SMTP address of the selected Outlook user with the email addresses that each friend has specified on the social network.</span></span> <span data-ttu-id="597db-119">Si l’OSC détecte une adresse de messagerie SMTP correspondante, l’OSC utilise correspondant **userID** de votre ami pour appeler la méthode [ISocialSession::GetPerson](isocialsession-getperson.md) .</span><span class="sxs-lookup"><span data-stu-id="597db-119">If the OSC finds a matching SMTP email address, the OSC uses the corresponding **userID** of the friend to call the [ISocialSession::GetPerson](isocialsession-getperson.md) method.</span></span> <span data-ttu-id="597db-120">Pour cela, pour obtenir un objet [ISocialPerson](isocialpersoniunknown.md) pour que friend, qui permet l’OSC obtenir les activités et les images de cet expéditeur à partir du réseau social.</span><span class="sxs-lookup"><span data-stu-id="597db-120">It does this to obtain an [ISocialPerson](isocialpersoniunknown.md) object for that friend, which then enables the OSC to get activities and pictures of that friend from the social network.</span></span> 
  
<span data-ttu-id="597db-121">Toutefois, si l’utilisateur Outlook sélectionné ne spécifie pas cette même adresse SMTP sur un compte sur le réseaux sociaux, ou si l’utilisateur Outlook n’a pas de compte sur ce réseau social, l’OSC ne sera pas en mesure de trouver une correspondance pour cet utilisateur et n’affiche pas les activiti es pour cet utilisateur sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="597db-121">However, if the selected Outlook user does not specify that same SMTP address on an account on the social network, or if the Outlook user does not have an account on that social network, the OSC will not be able to find a match for that user and will not display any activities for that user on the social network.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="597db-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="597db-122">See also</span></span>

- [<span data-ttu-id="597db-123">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="597db-123">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)
- [<span data-ttu-id="597db-124">Obtention d’informations sur des amis</span><span class="sxs-lookup"><span data-stu-id="597db-124">Getting Friends Information</span></span>](getting-friends-information.md)

