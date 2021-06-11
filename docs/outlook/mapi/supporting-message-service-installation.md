---
title: Prise en charge de l’installation du service de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 328884e8758e679eb1c9d968547cba02c01d4d47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404700"
---
# <a name="supporting-message-service-installation"></a><span data-ttu-id="8d7c3-103">Prise en charge de l’installation du service de message</span><span class="sxs-lookup"><span data-stu-id="8d7c3-103">Supporting Message Service Installation</span></span>

  
  
<span data-ttu-id="8d7c3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d7c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d7c3-105">Le programme d’installation de votre service de message doit :</span><span class="sxs-lookup"><span data-stu-id="8d7c3-105">The setup program for installing your message service should do the following:</span></span>
  
1. <span data-ttu-id="8d7c3-106">Copiez les fichiers de service de message, tels que le service de messagerie et les DLLs de fournisseur de services, à partir d’un CD ou d’un disque, vers un lecteur local sur la station de travail.</span><span class="sxs-lookup"><span data-stu-id="8d7c3-106">Copy message service files, such as the message service and service provider DLLs, from a CD or disk, to a local drive on the workstation.</span></span> <span data-ttu-id="8d7c3-107">Les fichiers qui doivent être copiés dépendent de votre service de message.</span><span class="sxs-lookup"><span data-stu-id="8d7c3-107">The files that need to be copied depend on your message service.</span></span> <span data-ttu-id="8d7c3-108">En règle générale, vous copiez au moins une DLL.</span><span class="sxs-lookup"><span data-stu-id="8d7c3-108">Typically you will copy at least one DLL.</span></span>
    
2. <span data-ttu-id="8d7c3-109">Ajoutez des entrées au fichier de configuration Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="8d7c3-109">Add entries to the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="8d7c3-110">Pour plus d’informations sur la modification de ce fichier afin de prendre en charge les fournisseurs de services dans votre service de messagerie, voir Format de fichier [de MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="8d7c3-110">For more information about how to modify this file to support the service providers in your message service, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
3. <span data-ttu-id="8d7c3-111">Ajoutez, le cas échéant, des entrées au Registre système pour les services de messages.</span><span class="sxs-lookup"><span data-stu-id="8d7c3-111">Add entries, as appropriate, to the system registry for message services.</span></span> <span data-ttu-id="8d7c3-112">Pour plus d’informations sur la façon dont les entrées doivent apparaître dans le Registre système, voir [Installation du sous-système MAPI](installing-the-mapi-subsystem.md).</span><span class="sxs-lookup"><span data-stu-id="8d7c3-112">For more information about how the entries should appear in the system registry, see [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span></span>
    
4. <span data-ttu-id="8d7c3-113">Créez un profil par défaut s’il n’en existe pas encore à l’aide de l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8d7c3-113">Create a default profile if one does not yet exist by using one of the following items:</span></span>
    
  - <span data-ttu-id="8d7c3-114">Assistant Profil pour créer un profil à l’aide de l’interaction utilisateur par le biais d’une série de boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8d7c3-114">The Profile Wizard to create a profile by using user interaction through a series of dialog boxes.</span></span> <span data-ttu-id="8d7c3-115">Pour plus d’informations sur l’utilisation de l’Assistant Profil, voir [Création d’un profil à l’aide de l’Assistant Profil.](creating-a-profile-by-using-the-profile-wizard.md)</span><span class="sxs-lookup"><span data-stu-id="8d7c3-115">For more information about using the Profile Wizard, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span>
    
  - <span data-ttu-id="8d7c3-116">Panneau de contrôle pour créer un profil à l’aide de l’interaction utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8d7c3-116">The Control Panel to create a profile by using user interaction.</span></span> <span data-ttu-id="8d7c3-117">Le Panneau de configuration offre à l’utilisateur plus de flexibilité que l’Assistant Profil pour la configuration des services de message et la définition des propriétés de profil.</span><span class="sxs-lookup"><span data-stu-id="8d7c3-117">The Control Panel offers the user more flexibility than the Profile Wizard for configuring the message services and setting profile properties.</span></span> 
    
<span data-ttu-id="8d7c3-118">Placez le programme d’installation dans un répertoire public désigné.</span><span class="sxs-lookup"><span data-stu-id="8d7c3-118">Place the setup program in a designated public directory.</span></span> <span data-ttu-id="8d7c3-119">Ceci est important car la plupart des clients de configuration, tels que le Panneau de configuration, exigent que les utilisateurs entrent le nom de l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="8d7c3-119">This is important because most configuration clients, such as the Control Panel, require that users enter the name of the directory.</span></span> <span data-ttu-id="8d7c3-120">Le Panneau de configuration appelle un programme  d’installation lorsqu’un utilisateur clique sur le bouton Ajouter, appelle la boîte de dialogue Avoir un disque et spécifie le chemin d’accès au programme. </span><span class="sxs-lookup"><span data-stu-id="8d7c3-120">The Control Panel invokes a setup program when a user clicks the **Add** button, invokes the **Have Disk** dialog box, and specifies the path to the program.</span></span> <span data-ttu-id="8d7c3-121">Le Panneau de contrôle exécute le programme et appelle la fonction de point d’entrée de votre service de message avec le paramètre  _ulContext_ paramétré sur MSG_SERVICE_INSTALL.</span><span class="sxs-lookup"><span data-stu-id="8d7c3-121">The Control Panel runs the program and calls your message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_INSTALL.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="8d7c3-122">Étant donné que les profils font partie intégrante de l’architecture MAPI, assurez-vous que votre programme d’installation ne stocke rien dans le profil par défaut qui serait difficile à recréer.</span><span class="sxs-lookup"><span data-stu-id="8d7c3-122">Because profiles are an expendable part of the MAPI architecture, be sure that your installation program does not store anything in the default profile that would be difficult to recreate.</span></span> <span data-ttu-id="8d7c3-123">Il n’existe aucun utilitaire pour la récupération de profil, pour le déplacement de profils d’un ordinateur à un autre, pour la sauvegarde hors ligne ou pour une restauration individuelle ou globale à partir de copies de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="8d7c3-123">There are no utilities for profile recovery, for moving profiles from one computer to another, for off-line backup, or for individual or global restoration from backup copies.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8d7c3-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d7c3-124">See also</span></span>



[<span data-ttu-id="8d7c3-125">Implémentation du service de message</span><span class="sxs-lookup"><span data-stu-id="8d7c3-125">Message Service Implementation</span></span>](message-service-implementation.md)

