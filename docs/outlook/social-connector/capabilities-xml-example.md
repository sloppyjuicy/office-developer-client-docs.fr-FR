---
title: Exemple de code XML des fonctionnalités
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: L’exemple de code XML de cette rubrique est une chaîne XML renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode ISocialProvider::GetCapabilities pour un réseau social. Le code XML montre comment un fournisseur OSC spécifie ses fonctionnalités et la configuration requise pour l’OSC.
ms.openlocfilehash: 5cafd6d29de8b4357e9e0ce6dab30b125f53b8ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787581"
---
# <a name="capabilities-xml-example"></a><span data-ttu-id="1254f-104">Exemple de code XML des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="1254f-104">Capabilities XML example</span></span>

<span data-ttu-id="1254f-105">L’exemple de code XML de cette rubrique est une chaîne XML renvoyée à Outlook Social Connector (OSC) après avoir appelé la méthode [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) pour un réseau social.</span><span class="sxs-lookup"><span data-stu-id="1254f-105">The XML example in this topic is an XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method for a social network.</span></span> <span data-ttu-id="1254f-106">Le code XML montre comment un fournisseur OSC spécifie ses fonctionnalités et la configuration requise pour l’OSC.</span><span class="sxs-lookup"><span data-stu-id="1254f-106">The XML shows how an OSC provider specifies its capabilities and requirements for the OSC.</span></span> 
  
## <a name="capabilities-for-friends"></a><span data-ttu-id="1254f-107">Fonctionnalités d’amis</span><span class="sxs-lookup"><span data-stu-id="1254f-107">Capabilities for friends</span></span>

<span data-ttu-id="1254f-108">Dans cet exemple, le fournisseur OSC spécifie les éléments suivants pour afficher ses fonctionnalités de prise en charge de la fonctionnalité d’amis :</span><span class="sxs-lookup"><span data-stu-id="1254f-108">In this example, the OSC provider specifies the following elements to show its capabilities in supporting the friends feature:</span></span>
  
- <span data-ttu-id="1254f-109">**getFriends** en tant que **la valeur true** pour indiquer que le fournisseur OSC prend en charge la méthode [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) pour obtenir des informations de vos amis par programme.</span><span class="sxs-lookup"><span data-stu-id="1254f-109">**getFriends** as **true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method to get friends' information programmatically.</span></span> 
    
- <span data-ttu-id="1254f-110">**cacheFriends** en tant que **la valeur true** pour prendre en charge les informations de mise en cache amis dans un dossier de contacts Outlook.</span><span class="sxs-lookup"><span data-stu-id="1254f-110">**cacheFriends** as **true** to support caching friends' information in an Outlook contacts folder.</span></span> 
    
- <span data-ttu-id="1254f-111">**contactSyncRestartInterval** 60 pour indiquer que sur erreur, l’OSC doit recommencer l’actualisation du cache toutes les 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="1254f-111">**contactSyncRestartInterval** as 60 to indicate that on error, the OSC should retry refreshing the cache every 60 minutes.</span></span> 
    
- <span data-ttu-id="1254f-112">**followPerson** en tant que **la valeur true** pour indiquer la possibilité d’ajouter des amis sur le réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="1254f-112">**followPerson** as **true** to indicate the ability to add friends on the social network.</span></span> 
    
- <span data-ttu-id="1254f-113">**doNotFollowPerson** en tant que **valeur false** pour indiquer que le fournisseur OSC ne gère pas la suppression d’une personne comme un ami sur le réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="1254f-113">**doNotFollowPerson** as **false** to indicate the OSC provider does not support removing a person as a friend on the social network.</span></span> 
    
- <span data-ttu-id="1254f-114">**dynamicContactsLookup** en tant que **valeur false** pour indiquer que l’OSC ne devez pas stocker les informations de vos amis en mémoire.</span><span class="sxs-lookup"><span data-stu-id="1254f-114">**dynamicContactsLookup** as **false** to indicate that the OSC should not store friends' information in memory.</span></span> 
    
## <a name="capabilities-for-activities"></a><span data-ttu-id="1254f-115">Fonctionnalités pour les activités</span><span class="sxs-lookup"><span data-stu-id="1254f-115">Capabilities for activities</span></span>

<span data-ttu-id="1254f-116">Le fournisseur OSC spécifie les éléments pour afficher sa capacité à prendre en charge les activités suivantes :</span><span class="sxs-lookup"><span data-stu-id="1254f-116">The OSC provider specifies the following elements to show its capability to support activities:</span></span>
  
- <span data-ttu-id="1254f-117">**getActivities** en tant que **la valeur true** pour indiquer que le fournisseur OSC prend en charge la méthode [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) pour obtenir par programme des activités de vos amis.</span><span class="sxs-lookup"><span data-stu-id="1254f-117">**getActivities** as **true** to indicate that the OSC provider supports the [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) method to get friends' activities programmatically.</span></span> 
    
- <span data-ttu-id="1254f-118">**cacheActivities** en tant que **valeur false** pour prendre en charge les activités de mise en cache des amis dans le dossier Outlook de News masqué.</span><span class="sxs-lookup"><span data-stu-id="1254f-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span></span> 
    
- <span data-ttu-id="1254f-119">**dynamicActivitiesLookupEx** en tant que **la valeur true** pour indiquer que l’OSC doit stocker les activités amis en mémoire.</span><span class="sxs-lookup"><span data-stu-id="1254f-119">**dynamicActivitiesLookupEx** as **true** to indicate that the OSC should store friends' activities in memory.</span></span> 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a><span data-ttu-id="1254f-120">Fonctionnalités de configuration de compte et d’authentification</span><span class="sxs-lookup"><span data-stu-id="1254f-120">Capabilities for authentication and account configuration</span></span>

<span data-ttu-id="1254f-121">Le fournisseur OSC spécifie les éléments suivants pour afficher la prise en charge pour l’authentification et la configuration de compte :</span><span class="sxs-lookup"><span data-stu-id="1254f-121">The OSC provider specifies the following elements to show its support for authentication and account configuration:</span></span>
  
- <span data-ttu-id="1254f-122">**useLogonWebAuth** en tant que **valeur false** pour indiquer que le fournisseur OSC prend en charge l’authentification de base.</span><span class="sxs-lookup"><span data-stu-id="1254f-122">**useLogonWebAuth** as **false** to indicate that the OSC provider supports basic authentication.</span></span> 
    
- <span data-ttu-id="1254f-123">**supportsAutoConfigure** en tant que **valeur false** pour indiquer que l’OSC ne doit pas essayer configurer automatiquement et ouvrez une session sur le réseau social pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1254f-123">**supportsAutoConfigure** as **false** to indicate that the OSC should not attempt to automatically configure and log on to the social network for the user.</span></span> 
    
- <span data-ttu-id="1254f-124">**useLogonCached** et **hideRememberMyPassword** en tant que **valeur false** pour indiquer que l’OSC doit demander le mot de passe chaque fois et ne doit pas utiliser mis en cache les informations d’identification d’ouverture de session pour vous connecter.</span><span class="sxs-lookup"><span data-stu-id="1254f-124">**useLogonCached** and **hideRememberMyPassword** as **false** to indicate that the OSC should prompt for password every time and should not use cached logon credentials to log on.</span></span> 
    
- <span data-ttu-id="1254f-125">**displayUrl** en tant que **valeur false** pour indiquer que l’OSC ne doit pas afficher l’URL pour le réseau social dans la boîte de dialogue de configuration de compte.</span><span class="sxs-lookup"><span data-stu-id="1254f-125">**displayUrl** as **false** to indicate that the OSC should not display the URL for the social network in the account configuration dialog box.</span></span> 
    
- <span data-ttu-id="1254f-126">**hideHyperlinks** en tant que **valeur false** pour indiquer que le fournisseur OSC prend en charge uniquement des comptes existants par mot de passe connus et le OSC ne doit pas afficher la **Cliquez ici pour créer un compte** et **vous avez oublié votre mot de passe ?** des liens hypertexte dans le boîte de dialogue de configuration de compte.</span><span class="sxs-lookup"><span data-stu-id="1254f-126">**hideHyperlinks** as **false** to indicate that the OSC provider supports only existing accounts with known passwords, and the OSC should not display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box.</span></span> 
    
## <a name="xml-example"></a><span data-ttu-id="1254f-127">Exemple de code XML</span><span class="sxs-lookup"><span data-stu-id="1254f-127">XML example</span></span>

<span data-ttu-id="1254f-128">L’exemple suivant montre le XML des **fonctionnalités** d’un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="1254f-128">The following example shows the **capabilities** XML of an OSC provider.</span></span> 
  
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
  <createAccountUrl>http://contoso.com/createAccount</createAccountUrl>
  <forgotPasswordUrl>http://contoso.com/forgotPassword</forgotPasswordUrl>
</capabilities>

```

## <a name="see-also"></a><span data-ttu-id="1254f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1254f-129">See also</span></span>

- [<span data-ttu-id="1254f-130">Exemples de code XML de fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="1254f-130">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="1254f-131">Fichier XML pour les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="1254f-131">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="1254f-132">Exemple de code XML amis</span><span class="sxs-lookup"><span data-stu-id="1254f-132">Friends XML Example</span></span>](friends-xml-example.md)  
- [<span data-ttu-id="1254f-133">Exemple de flux XML d’activité</span><span class="sxs-lookup"><span data-stu-id="1254f-133">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="1254f-134">Fournisseur Outlook Social Connector schéma XML</span><span class="sxs-lookup"><span data-stu-id="1254f-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

