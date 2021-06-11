---
title: Obtention des informations sur les amis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: Le Outlook Social Connector (OSC) appelle la méthode ISocialProvider::GetCapabilities pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.
ms.openlocfilehash: 697902631b010afab015e9cfb73fac81ac427d6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428794"
---
# <a name="getting-friends-information"></a><span data-ttu-id="3b0da-103">Obtention des informations sur les amis</span><span class="sxs-lookup"><span data-stu-id="3b0da-103">Getting friends information</span></span>

<span data-ttu-id="3b0da-104">Le Outlook Social Connector (OSC) appelle la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.</span><span class="sxs-lookup"><span data-stu-id="3b0da-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="3b0da-105">Si les éléments **getFriends** et **cacheFriends** dans les fonctionnalités **renvoyées** XML indiquent que le fournisseur OSC prend en charge l’obtention d’amis et la mise en cache d’amis en tant qu’éléments de contact Outlook dans un dossier de contacts correspondant, l’OSC peut effectuer la séquence d’appels suivante.</span><span class="sxs-lookup"><span data-stu-id="3b0da-105">If the **getFriends** and **cacheFriends** elements in the returned **capabilities** XML indicate that the OSC provider supports getting friends and caching friends as Outlook contact items in a corresponding contacts folder, the OSC can make the following calling sequence.</span></span> <span data-ttu-id="3b0da-106">L’OSC appelle les méthodes de cette séquence pour obtenir des informations et des images (telles que prises en charge par l’interface [ISocialPerson)](isocialpersoniunknown.md) pour les amis sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="3b0da-106">The OSC calls methods in this sequence to get information and pictures (as supported by the [ISocialPerson](isocialpersoniunknown.md) interface) for friends on the social network.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3b0da-107">OsC actualise le cache à un intervalle par défaut.</span><span class="sxs-lookup"><span data-stu-id="3b0da-107">The OSC refreshes the cache at a default interval.</span></span> <span data-ttu-id="3b0da-108">Si une erreur se produit lors de l’actualisation du cache, l’OSC réessaie à un autre intervalle prédéfinis, qui peut également être contrôlé en spécifiant l’élément **contactSyncRestartInterval** dans le **XML** des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="3b0da-108">If an error occurs during cache refresh, the OSC retries at another preset interval, which can also be controlled by specifying the **contactSyncRestartInterval** element in the **capabilities** XML.</span></span> <span data-ttu-id="3b0da-109">Pour plus d’informations sur l’actualisation du cache de contacts, voir [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="3b0da-109">For more information about refreshing the contacts cache, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
1. <span data-ttu-id="3b0da-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) : OSC obtient l’ID de l’utilisateur Office connecté au réseau social.</span><span class="sxs-lookup"><span data-stu-id="3b0da-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) —The OSC gets the user ID of the Office user who is logged onto the social network.</span></span> 
    
2. <span data-ttu-id="3b0da-111">[ISocialSession::GetPerson](isocialsession-getperson.md) : à l’aide de l’ID d’utilisateur de l’utilisateur Office, OSC obtient un **objet ISocialPerson** pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3b0da-111">[ISocialSession::GetPerson](isocialsession-getperson.md) —Using the user ID of the Office user, the OSC gets an **ISocialPerson** object for that user.</span></span> 
    
3. <span data-ttu-id="3b0da-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) : OSC obtient la liste des amis de l’utilisateur sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="3b0da-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) —The OSC gets the user's friend list on the social network.</span></span> 
    
4. <span data-ttu-id="3b0da-113">[ISocialSession::GetPerson](isocialsession-getperson.md) — Pour chaque personne dans le XML renvoyé par **GetFriendsAndColleagues**, l’OSC obtient une interface **ISocialPerson.**</span><span class="sxs-lookup"><span data-stu-id="3b0da-113">[ISocialSession::GetPerson](isocialsession-getperson.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets an **ISocialPerson** interface.</span></span> 
    
5. <span data-ttu-id="3b0da-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) — Pour chaque personne dans le XML renvoyé par **GetFriendsAndColleagues**, l’OSC obtient une ressource d’image.</span><span class="sxs-lookup"><span data-stu-id="3b0da-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets a picture resource.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b0da-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b0da-115">See also</span></span>

- [<span data-ttu-id="3b0da-116">XML pour les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="3b0da-116">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="3b0da-117">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="3b0da-117">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

