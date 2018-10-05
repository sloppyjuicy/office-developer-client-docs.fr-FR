---
title: Vue d’ensemble des profils MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e196800b717ce2528da4b9871bad7425f3a2c326
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385626"
---
# <a name="mapi-profile-overview"></a><span data-ttu-id="b32e0-103">Vue d’ensemble des profils MAPI</span><span class="sxs-lookup"><span data-stu-id="b32e0-103">MAPI Profile Overview</span></span>

  
  
<span data-ttu-id="b32e0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b32e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b32e0-105">Un profil est une collection d’informations sur les services de messagerie et les fournisseurs de services qu’un utilisateur d’une application cliente souhaite soit disponible pendant une session MAPI spécifique.</span><span class="sxs-lookup"><span data-stu-id="b32e0-105">A profile is a collection of information about the message services and service providers that a user of a client application wants to be available during a particular MAPI session.</span></span> <span data-ttu-id="b32e0-106">Chaque utilisateur dispose d’au moins un profil ; nombre d’utilisateurs conserver plusieurs.</span><span class="sxs-lookup"><span data-stu-id="b32e0-106">Every user has at least one profile; many users keep several.</span></span> <span data-ttu-id="b32e0-107">Par exemple, un utilisateur peut avoir un profil pour fonctionner avec un service de banque de messages sur le serveur et un autre profil pour fonctionner avec un service de banque de messages sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="b32e0-107">For example, a user might have one profile to work with a server-based message store service and another profile to work with a message store service on the local computer.</span></span> <span data-ttu-id="b32e0-108">Un utilisateur souhaite accéder à un ensemble de systèmes de messagerie à l’aide des services de transport approprié pour une partie de la journée et un autre pour le reste de la journée.</span><span class="sxs-lookup"><span data-stu-id="b32e0-108">A user might want to access one set of messaging systems by using the appropriate transport services for part of the day and another set for the rest of the day.</span></span> <span data-ttu-id="b32e0-109">Les profils fournissent une grande souplesse pour sélectionner des combinaisons de services de système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b32e0-109">Profiles provide a flexible way to select combinations of messaging system services.</span></span> 
  
<span data-ttu-id="b32e0-110">Profils peuvent contenir jusqu'à 64 caractères alphanumériques, les noms de longueur.</span><span class="sxs-lookup"><span data-stu-id="b32e0-110">Profiles can have names up to 64 alphanumeric characters in length.</span></span> <span data-ttu-id="b32e0-111">Les noms peuvent inclure des caractères d’accentuation, le trait de soulignement et des espaces et ne peut pas contenir d’espaces de début ou de fin.</span><span class="sxs-lookup"><span data-stu-id="b32e0-111">The names can include accent characters, the underscore, and embedded spaces, and cannot include leading or trailing spaces.</span></span> 
  
<span data-ttu-id="b32e0-112">Les profils sont organisées de façon hiérarchique et divisés en sections, avec une section pour chaque service de message et une section pour chaque fournisseur de services dans un service.</span><span class="sxs-lookup"><span data-stu-id="b32e0-112">Profiles are organized hierarchically and divided into sections, with one section for each message service and one section for each service provider in a service.</span></span> <span data-ttu-id="b32e0-113">Les sections connexes sont liées, ce qui facilite parcourir les informations.</span><span class="sxs-lookup"><span data-stu-id="b32e0-113">The related sections are linked, making it easier to navigate through the information.</span></span> <span data-ttu-id="b32e0-114">Chaque section contient une série d’entrées MAPI ou une application cliente utilise pour la configuration.</span><span class="sxs-lookup"><span data-stu-id="b32e0-114">Each section contains a series of entries that MAPI or a client application uses for configuration.</span></span>
  
<span data-ttu-id="b32e0-115">Les entrées incluses dans un profil varient à partir du service de message au service de message.</span><span class="sxs-lookup"><span data-stu-id="b32e0-115">The entries included in a profile vary from message service to message service.</span></span> <span data-ttu-id="b32e0-116">Certaines entrées courantes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b32e0-116">Some of the common entries include the following:</span></span>
  
- <span data-ttu-id="b32e0-117">Le nom de chaque service de message ou d’un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="b32e0-117">The name of each message service or service provider.</span></span>
    
- <span data-ttu-id="b32e0-118">Nom des DLL qui contiennent des fournisseurs de services et services de message.</span><span class="sxs-lookup"><span data-stu-id="b32e0-118">The name of the DLLs that contain service providers and message services.</span></span>
    
- <span data-ttu-id="b32e0-119">Nom de la fonction de point d’entrée du service de chaque message.</span><span class="sxs-lookup"><span data-stu-id="b32e0-119">The name of each message service's entry point function.</span></span>
    
- <span data-ttu-id="b32e0-120">Liste des fournisseurs de services qui constituent le service de chaque message.</span><span class="sxs-lookup"><span data-stu-id="b32e0-120">A list of the service providers that make up each message service.</span></span>
    
<span data-ttu-id="b32e0-121">Profils peuvent être créés au moment de l’installation, lorsque MAPI ou un service de message est chargé sur un ordinateur, ou ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="b32e0-121">Profiles can be created at installation time, when MAPI or a message service is loaded onto a computer, or at any later time.</span></span> <span data-ttu-id="b32e0-122">MAPI propose l’Assistant profil pour l’administration des profils.</span><span class="sxs-lookup"><span data-stu-id="b32e0-122">MAPI provides the Profile Wizard for profile administration.</span></span> 
  
<span data-ttu-id="b32e0-123">L’Assistant profil est une application qui crée des profils avec un minimum de travail.</span><span class="sxs-lookup"><span data-stu-id="b32e0-123">The Profile Wizard is an application that creates new profiles with a minimum amount of work.</span></span> <span data-ttu-id="b32e0-124">L’Assistant utilise le valeurs par défaut pour les paramètres dans la mesure du possible, l’enregistrement d’effort et l’heure d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b32e0-124">The wizard uses default values for settings wherever possible, saving users time and effort.</span></span> <span data-ttu-id="b32e0-125">Les utilisateurs entrent des valeurs uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b32e0-125">Users enter values only when absolutely necessary.</span></span> <span data-ttu-id="b32e0-126">Pour plus d’informations, consultez [Création d’un profil à l’aide de l’Assistant profil](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="b32e0-126">For more information, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span> <span data-ttu-id="b32e0-127">Vous pouvez également utiliser l’outil de personnalisation Office pour créer un nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="b32e0-127">You can also use the Office Customization Tool to create a new profile.</span></span> <span data-ttu-id="b32e0-128">Pour plus d’informations, voir [Outil de personnalisation Office](https://go.microsoft.com/fwlink/?LinkId=123000).</span><span class="sxs-lookup"><span data-stu-id="b32e0-128">For more information, see [Office Customization Tool](https://go.microsoft.com/fwlink/?LinkId=123000).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b32e0-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b32e0-129">See also</span></span>



[<span data-ttu-id="b32e0-130">Architecture et des fonctionnalités MAPI</span><span class="sxs-lookup"><span data-stu-id="b32e0-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

