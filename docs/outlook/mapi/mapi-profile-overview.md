---
title: Vue d’ensemble du profil MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e196800b717ce2528da4b9871bad7425f3a2c326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328162"
---
# <a name="mapi-profile-overview"></a><span data-ttu-id="9fd4f-103">Vue d’ensemble du profil MAPI</span><span class="sxs-lookup"><span data-stu-id="9fd4f-103">MAPI Profile Overview</span></span>

  
  
<span data-ttu-id="9fd4f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fd4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fd4f-105">Un profil est une collection d’informations sur les services de messagerie et les fournisseurs de services qu’un utilisateur d’une application cliente souhaite rendre disponibles pendant une session MAPI particulière.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-105">A profile is a collection of information about the message services and service providers that a user of a client application wants to be available during a particular MAPI session.</span></span> <span data-ttu-id="9fd4f-106">Chaque utilisateur possède au moins un profil . de nombreux utilisateurs en conservent plusieurs.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-106">Every user has at least one profile; many users keep several.</span></span> <span data-ttu-id="9fd4f-107">Par exemple, un utilisateur peut avoir un profil pour travailler avec un service de magasin de messages basé sur le serveur et un autre profil pour travailler avec un service de magasin de messages sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-107">For example, a user might have one profile to work with a server-based message store service and another profile to work with a message store service on the local computer.</span></span> <span data-ttu-id="9fd4f-108">Un utilisateur peut vouloir accéder à un ensemble de systèmes de messagerie en utilisant les services de transport appropriés pour une partie de la journée et un autre ensemble pour le reste de la journée.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-108">A user might want to access one set of messaging systems by using the appropriate transport services for part of the day and another set for the rest of the day.</span></span> <span data-ttu-id="9fd4f-109">Les profils offrent un moyen flexible de sélectionner des combinaisons de services système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-109">Profiles provide a flexible way to select combinations of messaging system services.</span></span> 
  
<span data-ttu-id="9fd4f-110">Les profils peuvent avoir jusqu’à 64 caractères alphanumériques.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-110">Profiles can have names up to 64 alphanumeric characters in length.</span></span> <span data-ttu-id="9fd4f-111">Les noms peuvent inclure des caractères d’accentuation, le trait de soulignement et des espaces incorporés, et ne peuvent pas inclure d’espaces de début ou de fin.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-111">The names can include accent characters, the underscore, and embedded spaces, and cannot include leading or trailing spaces.</span></span> 
  
<span data-ttu-id="9fd4f-112">Les profils sont organisés hiérarchiquement et divisés en sections, avec une section pour chaque service de messagerie et une section pour chaque fournisseur de services dans un service.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-112">Profiles are organized hierarchically and divided into sections, with one section for each message service and one section for each service provider in a service.</span></span> <span data-ttu-id="9fd4f-113">Les sections associées sont liées, ce qui facilite la navigation dans les informations.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-113">The related sections are linked, making it easier to navigate through the information.</span></span> <span data-ttu-id="9fd4f-114">Chaque section contient une série d’entrées que MAPI ou une application cliente utilise pour la configuration.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-114">Each section contains a series of entries that MAPI or a client application uses for configuration.</span></span>
  
<span data-ttu-id="9fd4f-115">Les entrées incluses dans un profil varient d’un service de message à l’autre.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-115">The entries included in a profile vary from message service to message service.</span></span> <span data-ttu-id="9fd4f-116">Voici quelques-unes des entrées courantes :</span><span class="sxs-lookup"><span data-stu-id="9fd4f-116">Some of the common entries include the following:</span></span>
  
- <span data-ttu-id="9fd4f-117">Nom de chaque service de messagerie ou fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-117">The name of each message service or service provider.</span></span>
    
- <span data-ttu-id="9fd4f-118">Nom des DLLs qui contiennent des fournisseurs de services et des services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-118">The name of the DLLs that contain service providers and message services.</span></span>
    
- <span data-ttu-id="9fd4f-119">Nom de la fonction de point d’entrée de chaque service de message.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-119">The name of each message service's entry point function.</span></span>
    
- <span data-ttu-id="9fd4f-120">Liste des fournisseurs de services qui font chaque service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-120">A list of the service providers that make up each message service.</span></span>
    
<span data-ttu-id="9fd4f-121">Les profils peuvent être créés au moment de l’installation, lorsque MAPI ou un service de message est chargé sur un ordinateur, ou à tout moment ultérieur.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-121">Profiles can be created at installation time, when MAPI or a message service is loaded onto a computer, or at any later time.</span></span> <span data-ttu-id="9fd4f-122">MAPI fournit l’Assistant Profil pour l’administration des profils.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-122">MAPI provides the Profile Wizard for profile administration.</span></span> 
  
<span data-ttu-id="9fd4f-123">L’Assistant Profil est une application qui crée de nouveaux profils avec un minimum de travail.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-123">The Profile Wizard is an application that creates new profiles with a minimum amount of work.</span></span> <span data-ttu-id="9fd4f-124">L’Assistant utilise les valeurs par défaut pour les paramètres dans la mesure du possible, ce qui permet aux utilisateurs de gagner du temps et des efforts.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-124">The wizard uses default values for settings wherever possible, saving users time and effort.</span></span> <span data-ttu-id="9fd4f-125">Les utilisateurs entrent des valeurs uniquement lorsque cela est absolument nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-125">Users enter values only when absolutely necessary.</span></span> <span data-ttu-id="9fd4f-126">Pour plus d’informations, [voir Création d’un profil à l’aide de l’Assistant Profil.](creating-a-profile-by-using-the-profile-wizard.md)</span><span class="sxs-lookup"><span data-stu-id="9fd4f-126">For more information, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span> <span data-ttu-id="9fd4f-127">Vous pouvez également utiliser l’outil Office Personnalisation pour créer un profil.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-127">You can also use the Office Customization Tool to create a new profile.</span></span> <span data-ttu-id="9fd4f-128">Pour plus d’informations, voir [Outil de personnalisation Office](https://go.microsoft.com/fwlink/?LinkId=123000).</span><span class="sxs-lookup"><span data-stu-id="9fd4f-128">For more information, see [Office Customization Tool](https://go.microsoft.com/fwlink/?LinkId=123000).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9fd4f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fd4f-129">See also</span></span>



[<span data-ttu-id="9fd4f-130">Fonctionnalités et architecture MAPI</span><span class="sxs-lookup"><span data-stu-id="9fd4f-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

