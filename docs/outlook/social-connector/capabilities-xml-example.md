---
title: Exemple de fonctionnalités XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: 'L’exemple XML de cette rubrique est une chaîne XML renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode ISocialProvider:: GetCapabilities pour un réseau social. Le XML montre comment un fournisseur OSC spécifie ses capacités et ses conditions requises pour le OSC.'
ms.openlocfilehash: 3340f5b1e0718edd1a062ab817c6621c338bee42
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542260"
---
# <a name="capabilities-xml-example"></a><span data-ttu-id="0c908-104">Exemple de fonctionnalités XML</span><span class="sxs-lookup"><span data-stu-id="0c908-104">Capabilities XML example</span></span>

<span data-ttu-id="0c908-105">L’exemple XML de cette rubrique est une chaîne XML renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) pour un réseau social.</span><span class="sxs-lookup"><span data-stu-id="0c908-105">The XML example in this topic is an XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method for a social network.</span></span> <span data-ttu-id="0c908-106">Le XML montre comment un fournisseur OSC spécifie ses capacités et ses conditions requises pour le OSC.</span><span class="sxs-lookup"><span data-stu-id="0c908-106">The XML shows how an OSC provider specifies its capabilities and requirements for the OSC.</span></span> 
  
## <a name="capabilities-for-friends"></a><span data-ttu-id="0c908-107">Fonctionnalités pour les amis</span><span class="sxs-lookup"><span data-stu-id="0c908-107">Capabilities for friends</span></span>

<span data-ttu-id="0c908-108">Dans cet exemple, le fournisseur OSC spécifie les éléments suivants pour afficher ses fonctionnalités dans la prise en charge de la fonctionnalité Friends:</span><span class="sxs-lookup"><span data-stu-id="0c908-108">In this example, the OSC provider specifies the following elements to show its capabilities in supporting the friends feature:</span></span>
  
- <span data-ttu-id="0c908-109">**getFriends** comme **true** pour indiquer que le fournisseur OSC prend en charge la méthode [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) pour obtenir les informations des amis par programme.</span><span class="sxs-lookup"><span data-stu-id="0c908-109">**getFriends** as **true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method to get friends' information programmatically.</span></span> 
    
- <span data-ttu-id="0c908-110">**cacheFriends** comme **true** pour prendre en charge la mise en cache des informations des amis dans un dossier de contacts Outlook.</span><span class="sxs-lookup"><span data-stu-id="0c908-110">**cacheFriends** as **true** to support caching friends' information in an Outlook contacts folder.</span></span> 
    
- <span data-ttu-id="0c908-111">**contactSyncRestartInterval** en tant que 60 pour indiquer qu’en cas d’erreur, l’OSC doit réessayer d’actualiser le cache toutes les 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="0c908-111">**contactSyncRestartInterval** as 60 to indicate that on error, the OSC should retry refreshing the cache every 60 minutes.</span></span> 
    
- <span data-ttu-id="0c908-112">**followPerson** comme **true** pour indiquer la possibilité d’ajouter des amis sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="0c908-112">**followPerson** as **true** to indicate the ability to add friends on the social network.</span></span> 
    
- <span data-ttu-id="0c908-113">**doNotFollowPerson** **false** pour indiquer que le fournisseur OSC ne prend pas en charge la suppression d’une personne en tant qu’ami sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="0c908-113">**doNotFollowPerson** as **false** to indicate the OSC provider does not support removing a person as a friend on the social network.</span></span> 
    
- <span data-ttu-id="0c908-114">**dynamicContactsLookup** **false** pour indiquer que OSC ne doit pas stocker les informations des amis dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="0c908-114">**dynamicContactsLookup** as **false** to indicate that the OSC should not store friends' information in memory.</span></span> 
    
## <a name="capabilities-for-activities"></a><span data-ttu-id="0c908-115">Fonctionnalités pour les activités</span><span class="sxs-lookup"><span data-stu-id="0c908-115">Capabilities for activities</span></span>

<span data-ttu-id="0c908-116">Le fournisseur OSC spécifie les éléments suivants pour montrer sa capacité à prendre en charge les activités:</span><span class="sxs-lookup"><span data-stu-id="0c908-116">The OSC provider specifies the following elements to show its capability to support activities:</span></span>
  
- <span data-ttu-id="0c908-117">**GetActivities** comme **true** pour indiquer que le fournisseur OSC prend en charge la méthode [ISocialProfile:: GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) pour obtenir les activités de Friends par programme.</span><span class="sxs-lookup"><span data-stu-id="0c908-117">**getActivities** as **true** to indicate that the OSC provider supports the [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) method to get friends' activities programmatically.</span></span> 
    
- <span data-ttu-id="0c908-118">**cacheActivities** **false** pour prendre en charge la mise en cache des activités d’amis dans le dossier de flux d’actualités Outlook masqué.</span><span class="sxs-lookup"><span data-stu-id="0c908-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span></span> 
    
- <span data-ttu-id="0c908-119">**dynamicActivitiesLookupEx** comme **true** pour indiquer que le OSC doit stocker les activités de Friend dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="0c908-119">**dynamicActivitiesLookupEx** as **true** to indicate that the OSC should store friends' activities in memory.</span></span> 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a><span data-ttu-id="0c908-120">Fonctionnalités d’authentification et de configuration de compte</span><span class="sxs-lookup"><span data-stu-id="0c908-120">Capabilities for authentication and account configuration</span></span>

<span data-ttu-id="0c908-121">Le fournisseur OSC spécifie les éléments suivants pour montrer sa prise en charge de la configuration de l’authentification et des comptes:</span><span class="sxs-lookup"><span data-stu-id="0c908-121">The OSC provider specifies the following elements to show its support for authentication and account configuration:</span></span>
  
- <span data-ttu-id="0c908-122">**useLogonWebAuth** **false** pour indiquer que le fournisseur OSC prend en charge l’authentification de base.</span><span class="sxs-lookup"><span data-stu-id="0c908-122">**useLogonWebAuth** as **false** to indicate that the OSC provider supports basic authentication.</span></span> 
    
- <span data-ttu-id="0c908-123">**supportsAutoConfigure** **false** pour indiquer que OSC ne doit pas tenter de configurer et d’ouvrir automatiquement une session sur le réseau social de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0c908-123">**supportsAutoConfigure** as **false** to indicate that the OSC should not attempt to automatically configure and log on to the social network for the user.</span></span> 
    
- <span data-ttu-id="0c908-124">**useLogonCached** et **hideRememberMyPassword** **false** pour indiquer que OSC doit demander un mot de passe à chaque fois et ne doit pas utiliser les informations d’identification d’ouverture de session mises en cache pour se connecter.</span><span class="sxs-lookup"><span data-stu-id="0c908-124">**useLogonCached** and **hideRememberMyPassword** as **false** to indicate that the OSC should prompt for password every time and should not use cached logon credentials to log on.</span></span> 
    
- <span data-ttu-id="0c908-125">**DisplayUrl** **false** pour indiquer que OSC ne doit pas afficher l’URL du réseau social dans la boîte de dialogue Configuration du compte.</span><span class="sxs-lookup"><span data-stu-id="0c908-125">**displayUrl** as **false** to indicate that the OSC should not display the URL for the social network in the account configuration dialog box.</span></span> 
    
- <span data-ttu-id="0c908-126">**hideHyperlinks** comme **false** pour indiquer que le fournisseur OSC prend en charge uniquement les comptes existants avec des mots de passe connus et que OSC ne doit pas afficher les liens de **Cliquer ici pour créer un compte** et avoir **oublié votre mot de passe?** liens hypertexte dans le boîte de dialogue Configuration du compte.</span><span class="sxs-lookup"><span data-stu-id="0c908-126">**hideHyperlinks** as **false** to indicate that the OSC provider supports only existing accounts with known passwords, and the OSC should not display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box.</span></span> 
    
## <a name="xml-example"></a><span data-ttu-id="0c908-127">Exemple XML</span><span class="sxs-lookup"><span data-stu-id="0c908-127">XML example</span></span>

<span data-ttu-id="0c908-128">L’exemple suivant montre les **fonctionnalités** XML d’un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="0c908-128">The following example shows the **capabilities** XML of an OSC provider.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<capabilities xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <getFriends>true</getFriends>
  <cacheFriends>true</cacheFriends>
  <followPerson>true</followPerson>
  <doNotFollowPerson>false</doNotFollowPerson>
  <getActivities>true</getActivities>
  <cacheActivities>false</cacheActivities>
  <displayUrl>false</displayUrl>
  <useLogonWebAuth>false</useLogonWebAuth>
  <hideHyperlinks>false</hideHyperlinks>
  <supportsAutoConfigure>false</supportsAutoConfigure>
  <contactSyncRestartInterval>60</contactSyncRestartInterval>
  <dynamicActivitiesLookupEx>true</dynamicActivitiesLookupEx>
  <dynamicContactsLookup>false</dynamicContactsLookup>
  <useLogonCached>false</useLogonCached>
  <hideRememberMyPassword>false</hideRememberMyPassword>
  <createAccountUrl>https://contoso.com/createAccount</createAccountUrl>
  <forgotPasswordUrl>https://contoso.com/forgotPassword</forgotPasswordUrl>
</capabilities>

```

## <a name="see-also"></a><span data-ttu-id="0c908-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c908-129">See also</span></span>

- [<span data-ttu-id="0c908-130">Exemples de fournisseurs XML OSC</span><span class="sxs-lookup"><span data-stu-id="0c908-130">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="0c908-131">XML pour les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="0c908-131">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="0c908-132">Exemple de code XML pour les amis</span><span class="sxs-lookup"><span data-stu-id="0c908-132">Friends XML Example</span></span>](friends-xml-example.md)  
- [<span data-ttu-id="0c908-133">Exemple de XML d’informations sur les activités</span><span class="sxs-lookup"><span data-stu-id="0c908-133">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="0c908-134">Schéma XML du fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="0c908-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

