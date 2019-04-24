---
title: Vue d'ensemble du profil MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: e196800b717ce2528da4b9871bad7425f3a2c326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328162"
---
# <a name="mapi-profile-overview"></a><span data-ttu-id="cefbc-103">Vue d'ensemble du profil MAPI</span><span class="sxs-lookup"><span data-stu-id="cefbc-103">MAPI Profile Overview</span></span>

  
  
<span data-ttu-id="cefbc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cefbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cefbc-105">Un profil est une collection d'informations sur les services de messagerie et les fournisseurs de services qu'un utilisateur d'une application cliente souhaite être disponible au cours d'une session MAPI particulière.</span><span class="sxs-lookup"><span data-stu-id="cefbc-105">A profile is a collection of information about the message services and service providers that a user of a client application wants to be available during a particular MAPI session.</span></span> <span data-ttu-id="cefbc-106">Chaque utilisateur possède au moins un profil; de nombreux utilisateurs en ont toujours plusieurs.</span><span class="sxs-lookup"><span data-stu-id="cefbc-106">Every user has at least one profile; many users keep several.</span></span> <span data-ttu-id="cefbc-107">Par exemple, un utilisateur peut avoir un profil à utiliser avec un service de banque de messages basé sur un serveur et un autre pour travailler avec un service de banque de messages sur l'ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="cefbc-107">For example, a user might have one profile to work with a server-based message store service and another profile to work with a message store service on the local computer.</span></span> <span data-ttu-id="cefbc-108">Un utilisateur peut accéder à un ensemble de systèmes de messagerie en utilisant les services de transport appropriés pour une partie de la journée et un autre pour le reste de la journée.</span><span class="sxs-lookup"><span data-stu-id="cefbc-108">A user might want to access one set of messaging systems by using the appropriate transport services for part of the day and another set for the rest of the day.</span></span> <span data-ttu-id="cefbc-109">Les profils permettent de sélectionner des combinaisons de services de système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="cefbc-109">Profiles provide a flexible way to select combinations of messaging system services.</span></span> 
  
<span data-ttu-id="cefbc-110">Le nom des profils peut contenir jusqu'à 64 caractères alphanumériques.</span><span class="sxs-lookup"><span data-stu-id="cefbc-110">Profiles can have names up to 64 alphanumeric characters in length.</span></span> <span data-ttu-id="cefbc-111">Les noms peuvent inclure des caractères d'accentuation, le trait de soulignement et les espaces incorporés, et ne peuvent pas contenir d'espaces de début ou de fin.</span><span class="sxs-lookup"><span data-stu-id="cefbc-111">The names can include accent characters, the underscore, and embedded spaces, and cannot include leading or trailing spaces.</span></span> 
  
<span data-ttu-id="cefbc-112">Les profils sont organisés de façon hiérarchique et sont divisés en sections, avec une section pour chaque service de messagerie et une section pour chaque fournisseur de services dans un service.</span><span class="sxs-lookup"><span data-stu-id="cefbc-112">Profiles are organized hierarchically and divided into sections, with one section for each message service and one section for each service provider in a service.</span></span> <span data-ttu-id="cefbc-113">Les sections associées sont liées, ce qui facilite la navigation dans les informations.</span><span class="sxs-lookup"><span data-stu-id="cefbc-113">The related sections are linked, making it easier to navigate through the information.</span></span> <span data-ttu-id="cefbc-114">Chaque section contient une série d'entrées que MAPI ou une application cliente utilise pour la configuration.</span><span class="sxs-lookup"><span data-stu-id="cefbc-114">Each section contains a series of entries that MAPI or a client application uses for configuration.</span></span>
  
<span data-ttu-id="cefbc-115">Les entrées incluses dans un profil varient en fonction du service de messagerie vers le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="cefbc-115">The entries included in a profile vary from message service to message service.</span></span> <span data-ttu-id="cefbc-116">Voici quelques entrées communes:</span><span class="sxs-lookup"><span data-stu-id="cefbc-116">Some of the common entries include the following:</span></span>
  
- <span data-ttu-id="cefbc-117">Nom de chaque service de messagerie ou fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="cefbc-117">The name of each message service or service provider.</span></span>
    
- <span data-ttu-id="cefbc-118">Le nom des dll qui contiennent les fournisseurs de services et les services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="cefbc-118">The name of the DLLs that contain service providers and message services.</span></span>
    
- <span data-ttu-id="cefbc-119">Nom de la fonction de point d'entrée de chaque service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="cefbc-119">The name of each message service's entry point function.</span></span>
    
- <span data-ttu-id="cefbc-120">Une liste des fournisseurs de services qui composent chaque service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="cefbc-120">A list of the service providers that make up each message service.</span></span>
    
<span data-ttu-id="cefbc-121">Des profils peuvent être créés lors de l'installation, lorsque MAPI ou un service de messagerie est chargé sur un ordinateur, ou ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="cefbc-121">Profiles can be created at installation time, when MAPI or a message service is loaded onto a computer, or at any later time.</span></span> <span data-ttu-id="cefbc-122">MAPI fournit l'Assistant Profil pour l'administration des profils.</span><span class="sxs-lookup"><span data-stu-id="cefbc-122">MAPI provides the Profile Wizard for profile administration.</span></span> 
  
<span data-ttu-id="cefbc-123">L'Assistant Profil est une application qui crée des profils avec un volume de travail minimal.</span><span class="sxs-lookup"><span data-stu-id="cefbc-123">The Profile Wizard is an application that creates new profiles with a minimum amount of work.</span></span> <span data-ttu-id="cefbc-124">L'Assistant utilise les valeurs par défaut des paramètres dans la mesure du possible, ce qui permet aux utilisateurs d'économiser du temps et de l'énergie.</span><span class="sxs-lookup"><span data-stu-id="cefbc-124">The wizard uses default values for settings wherever possible, saving users time and effort.</span></span> <span data-ttu-id="cefbc-125">Les utilisateurs ne peuvent entrer des valeurs qu'en cas d'absolue nécessité.</span><span class="sxs-lookup"><span data-stu-id="cefbc-125">Users enter values only when absolutely necessary.</span></span> <span data-ttu-id="cefbc-126">Pour plus d'informations, consultez [la rubrique Création d'un profil à l'aide de l'Assistant Profil](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="cefbc-126">For more information, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span> <span data-ttu-id="cefbc-127">Vous pouvez également utiliser l'outil de personnalisation Office pour créer un nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="cefbc-127">You can also use the Office Customization Tool to create a new profile.</span></span> <span data-ttu-id="cefbc-128">Pour plus d’informations, voir [Outil de personnalisation Office](https://go.microsoft.com/fwlink/?LinkId=123000).</span><span class="sxs-lookup"><span data-stu-id="cefbc-128">For more information, see [Office Customization Tool](https://go.microsoft.com/fwlink/?LinkId=123000).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cefbc-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cefbc-129">See also</span></span>



[<span data-ttu-id="cefbc-130">Architecture et fonctionnalités MAPI</span><span class="sxs-lookup"><span data-stu-id="cefbc-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

