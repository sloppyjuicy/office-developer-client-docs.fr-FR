---
title: Obtention d’informations sur vos amis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: L’Outlook Social Connector (OSC) appelle la méthode ISocialProvider::GetCapabilities pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.
ms.openlocfilehash: 68443992351f4c83e8e560a753941e97bf91de67
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787575"
---
# <a name="getting-friends-information"></a><span data-ttu-id="7f61e-103">Obtention d’informations sur vos amis</span><span class="sxs-lookup"><span data-stu-id="7f61e-103">Getting friends information</span></span>

<span data-ttu-id="7f61e-104">L’Outlook Social Connector (OSC) appelle la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour déterminer les fonctionnalités du fournisseur OSC pour un réseau social.</span><span class="sxs-lookup"><span data-stu-id="7f61e-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="7f61e-105">Si les éléments **getFriends** et **cacheFriends** dans le renvoyée XML des **capacités** indiquent que le fournisseur OSC prend en charge la mise en route d’amis et éléments dans un dossier contacts correspondant de contact amis mise en cache comme Outlook, l’OSC peut-il la séquence d’appel suivante.</span><span class="sxs-lookup"><span data-stu-id="7f61e-105">If the **getFriends** and **cacheFriends** elements in the returned **capabilities** XML indicate that the OSC provider supports getting friends and caching friends as Outlook contact items in a corresponding contacts folder, the OSC can make the following calling sequence.</span></span> <span data-ttu-id="7f61e-106">L’OSC appelle des méthodes dans l’ordre ci-après pour obtenir des informations et des images (comme pris en charge par l’interface [ISocialPerson](isocialpersoniunknown.md) ) pour vos amis sur le réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="7f61e-106">The OSC calls methods in this sequence to get information and pictures (as supported by the [ISocialPerson](isocialpersoniunknown.md) interface) for friends on the social network.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7f61e-107">L’OSC actualise le cache selon un intervalle par défaut.</span><span class="sxs-lookup"><span data-stu-id="7f61e-107">The OSC refreshes the cache at a default interval.</span></span> <span data-ttu-id="7f61e-108">Si une erreur se produit au cours du cache Actualiser, les tentatives OSC à un autre intervalle prédéfini, qui peut également être contrôlé en spécifiant l’élément **contactSyncRestartInterval** dans le XML des **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="7f61e-108">If an error occurs during cache refresh, the OSC retries at another preset interval, which can also be controlled by specifying the **contactSyncRestartInterval** element in the **capabilities** XML.</span></span> <span data-ttu-id="7f61e-109">Pour plus d’informations sur l’actualisation du cache de contacts, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="7f61e-109">For more information about refreshing the contacts cache, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
1. <span data-ttu-id="7f61e-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) — le OSC Obtient l’ID d’utilisateur de l’utilisateur d’Office qui est connecté au réseau social.</span><span class="sxs-lookup"><span data-stu-id="7f61e-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) —The OSC gets the user ID of the Office user who is logged onto the social network.</span></span> 
    
2. <span data-ttu-id="7f61e-111">[ISocialSession::GetPerson](isocialsession-getperson.md) — avec l’ID d’utilisateur de l’utilisateur d’Office, l’OSC Obtient un objet **ISocialPerson** pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7f61e-111">[ISocialSession::GetPerson](isocialsession-getperson.md) —Using the user ID of the Office user, the OSC gets an **ISocialPerson** object for that user.</span></span> 
    
3. <span data-ttu-id="7f61e-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) — l’OSC Obtient la liste ami de l’utilisateur sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="7f61e-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) —The OSC gets the user's friend list on the social network.</span></span> 
    
4. <span data-ttu-id="7f61e-113">[ISocialSession::GetPerson](isocialsession-getperson.md) — pour chaque personne dans le code XML renvoyé par **GetFriendsAndColleagues**, l’OSC Obtient une interface **ISocialPerson** .</span><span class="sxs-lookup"><span data-stu-id="7f61e-113">[ISocialSession::GetPerson](isocialsession-getperson.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets an **ISocialPerson** interface.</span></span> 
    
5. <span data-ttu-id="7f61e-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) — pour chaque personne dans le code XML renvoyé par **GetFriendsAndColleagues**, l’OSC Obtient une ressource de l’image.</span><span class="sxs-lookup"><span data-stu-id="7f61e-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets a picture resource.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f61e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f61e-115">See also</span></span>

- [<span data-ttu-id="7f61e-116">Fichier XML pour les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="7f61e-116">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="7f61e-117">Séquences d'appels classiques OSC</span><span class="sxs-lookup"><span data-stu-id="7f61e-117">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

