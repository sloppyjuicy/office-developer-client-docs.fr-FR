---
title: Installation du Service de Message prise en charge
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: bf3e79ad32801a659df2c68016167d3b547ddc6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787291"
---
# <a name="supporting-message-service-installation"></a><span data-ttu-id="1d805-103">Installation du Service de Message prise en charge</span><span class="sxs-lookup"><span data-stu-id="1d805-103">Supporting Message Service Installation</span></span>

  
  
<span data-ttu-id="1d805-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1d805-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1d805-105">Le programme d’installation pour l’installation de votre service de message doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1d805-105">The setup program for installing your message service should do the following:</span></span>
  
1. <span data-ttu-id="1d805-106">Copiez les fichiers de service de message, telles que le service de message et le fournisseur de services de DLL, à partir d’un CD-ROM ou un disque, sur un lecteur local sur la station de travail.</span><span class="sxs-lookup"><span data-stu-id="1d805-106">Copy message service files, such as the message service and service provider DLLs, from a CD or disk, to a local drive on the workstation.</span></span> <span data-ttu-id="1d805-107">Les fichiers qui doivent être copiés dépendent de votre service de message.</span><span class="sxs-lookup"><span data-stu-id="1d805-107">The files that need to be copied depend on your message service.</span></span> <span data-ttu-id="1d805-108">En règle générale, vous allez copier au moins une DLL.</span><span class="sxs-lookup"><span data-stu-id="1d805-108">Typically you will copy at least one DLL.</span></span>
    
2. <span data-ttu-id="1d805-109">Ajouter des entrées dans le fichier de configuration Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="1d805-109">Add entries to the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="1d805-110">Pour plus d’informations sur la modification de ce fichier pour prendre en charge les fournisseurs de services dans votre service de message, voir le [Fichier de Format de fichier MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="1d805-110">For more information about how to modify this file to support the service providers in your message service, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
3. <span data-ttu-id="1d805-111">Ajouter des entrées, selon le cas, dans le Registre système pour les services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1d805-111">Add entries, as appropriate, to the system registry for message services.</span></span> <span data-ttu-id="1d805-112">Pour plus d’informations sur la façon dont les entrées doivent apparaître dans le Registre système, consultez [installation du sous-système MAPI](installing-the-mapi-subsystem.md).</span><span class="sxs-lookup"><span data-stu-id="1d805-112">For more information about how the entries should appear in the system registry, see [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span></span>
    
4. <span data-ttu-id="1d805-113">Créer un profil par défaut s’il n’existe pas encore à l’aide d’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="1d805-113">Create a default profile if one does not yet exist by using one of the following items:</span></span>
    
  - <span data-ttu-id="1d805-114">L’Assistant profil pour créer un profil à l’aide d’intervention de l’utilisateur à travers une série de boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1d805-114">The Profile Wizard to create a profile by using user interaction through a series of dialog boxes.</span></span> <span data-ttu-id="1d805-115">Pour plus d’informations sur l’utilisation de l’Assistant profil, voir [Création d’un profil à l’aide de l’Assistant profil](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="1d805-115">For more information about using the Profile Wizard, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span>
    
  - <span data-ttu-id="1d805-116">Le panneau pour créer un profil à l’aide d’intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1d805-116">The Control Panel to create a profile by using user interaction.</span></span> <span data-ttu-id="1d805-117">Le panneau de configuration offre davantage de flexibilité que l’Assistant profil pour configurer les services de message et la définition des propriétés de profil à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1d805-117">The Control Panel offers the user more flexibility than the Profile Wizard for configuring the message services and setting profile properties.</span></span> 
    
<span data-ttu-id="1d805-118">Placez le programme d’installation dans un répertoire public désigné.</span><span class="sxs-lookup"><span data-stu-id="1d805-118">Place the setup program in a designated public directory.</span></span> <span data-ttu-id="1d805-119">Ceci est important parce que la plupart des clients de configuration, comme le panneau de configuration, exigent que les utilisateurs entrent le nom du répertoire.</span><span class="sxs-lookup"><span data-stu-id="1d805-119">This is important because most configuration clients, such as the Control Panel, require that users enter the name of the directory.</span></span> <span data-ttu-id="1d805-120">Le panneau de configuration appelle un programme d’installation lorsqu’un utilisateur clique sur le bouton **Ajouter** , appelle la boîte de dialogue **Disque** et spécifie le chemin d’accès au programme.</span><span class="sxs-lookup"><span data-stu-id="1d805-120">The Control Panel invokes a setup program when a user clicks the **Add** button, invokes the **Have Disk** dialog box, and specifies the path to the program.</span></span> <span data-ttu-id="1d805-121">Le panneau de configuration s’exécute le programme et appelle la fonction de point d’entrée de votre service de message avec le paramètre _ulContext_ défini sur MSG_SERVICE_INSTALL.</span><span class="sxs-lookup"><span data-stu-id="1d805-121">The Control Panel runs the program and calls your message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_INSTALL.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="1d805-122">Étant donné que les profils sont un composant de l’architecture MAPI consommables, n’oubliez pas que votre programme d’installation ne stocke pas rien dans le profil par défaut qui serait difficile à recréer.</span><span class="sxs-lookup"><span data-stu-id="1d805-122">Because profiles are an expendable part of the MAPI architecture, be sure that your installation program does not store anything in the default profile that would be difficult to recreate.</span></span> <span data-ttu-id="1d805-123">Il n’existe aucun utilitaire pour la récupération du profil, sur le déplacement des profils à partir d’un ordinateur à un autre, de sauvegarde hors connexion ou pour effectuer la restauration individuelle ou globale à partir des copies de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="1d805-123">There are no utilities for profile recovery, for moving profiles from one computer to another, for off-line backup, or for individual or global restoration from backup copies.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1d805-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d805-124">See also</span></span>



[<span data-ttu-id="1d805-125">Mise en œuvre de message</span><span class="sxs-lookup"><span data-stu-id="1d805-125">Message Service Implementation</span></span>](message-service-implementation.md)

