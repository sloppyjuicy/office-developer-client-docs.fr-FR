---
title: Prise en charge de la configuration du service de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e1782f3c20c1741e0e4b1859f1b29d835444009c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787276"
---
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="4a997-103">Prise en charge de la configuration du service de message</span><span class="sxs-lookup"><span data-stu-id="4a997-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="4a997-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a997-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a997-105">Pour prendre en charge la configuration du service de message, utilisez la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="4a997-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="4a997-106">Implémenter une fonction de point d’entrée est conforme au prototype [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="4a997-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="4a997-107">Fonctions de point d’entrée message service gérer l’accès aux données de configuration et sont appelées dans les circonstances suivantes :</span><span class="sxs-lookup"><span data-stu-id="4a997-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="4a997-108">Lorsqu’un client se connecte pour récupérer des informations pour configurer votre service de message.</span><span class="sxs-lookup"><span data-stu-id="4a997-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="4a997-109">Lorsqu’un client souhaite afficher ou modifier une propriété de configuration.</span><span class="sxs-lookup"><span data-stu-id="4a997-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="4a997-110">Bien que la plupart des services de messagerie fournissent des fonctions de point d’entrée, comme il faut, ces fonctions ne sont pas obligatoires.</span><span class="sxs-lookup"><span data-stu-id="4a997-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="4a997-111">Services de messagerie peuvent fournir l’accès aux données de configuration par d’autres moyens.</span><span class="sxs-lookup"><span data-stu-id="4a997-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="4a997-112">Toutefois, à l’aide d’une fonction de point d’entrée normalise et simplifie le processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="4a997-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="4a997-113">MAPI attend tous les messages service entrée point les fonctions pour être en mesure de stocker et récupérer les propriétés des sections qui sont associées au service de message de leur profil.</span><span class="sxs-lookup"><span data-stu-id="4a997-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="4a997-114">Prendre en charge cette fonctionnalité interactive, par programmation, ou les deux interactive et par programme.</span><span class="sxs-lookup"><span data-stu-id="4a997-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="4a997-115">Pour prendre en charge la configuration interactive, fournir une feuille de propriétés qui affiche les propriétés nécessaires à la configuration de votre service de message.</span><span class="sxs-lookup"><span data-stu-id="4a997-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="4a997-116">En tant qu’option, vous pouvez également fournir des feuilles de propriétés pour chaque fournisseur configurable.</span><span class="sxs-lookup"><span data-stu-id="4a997-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="4a997-117">Certains services message restreindre les utilisateurs à un affichage en lecture seule des propriétés de configuration ; autres services de messagerie permettent aux utilisateurs d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="4a997-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="4a997-118">Pour prendre en charge la configuration par programme, votre fonction de point d’entrée message service doit être en mesure de fonctionner sans intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4a997-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="4a997-119">Si votre service de message peut être appelé par l’Assistant profil, à prendre en charge une configuration par programme.</span><span class="sxs-lookup"><span data-stu-id="4a997-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="4a997-120">Si votre service de message n’autorise pas elle-même être configurés à l’aide de l’Assistant profil, vous pouvez choisir s’il faut prendre en charge la configuration par programme.</span><span class="sxs-lookup"><span data-stu-id="4a997-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="4a997-121">Pour plus d’informations sur la prise en charge de configuration dans une entrée de service de message point fonction, voir [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="4a997-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="4a997-122">Publier le nom de la fonction de point de message service entrée dans le fichier de configuration Mapisvc.inf en incluant l’entrée suivante dans la section service de message :</span><span class="sxs-lookup"><span data-stu-id="4a997-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="4a997-123">Créer une ou plusieurs propriétés feuille boîtes de dialogue pour afficher les données de configuration.</span><span class="sxs-lookup"><span data-stu-id="4a997-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="4a997-124">Effectuer les tâches suivantes si vous souhaitez permettre à l’Assistant profil configurer votre service de message :</span><span class="sxs-lookup"><span data-stu-id="4a997-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="4a997-125">Implémenter une fonction de point d’entrée est conforme au prototype [WIZARDENTRY](wizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="4a997-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="4a997-126">Implémenter une procédure de boîte de dialogue Windows standard qui est conforme au prototype [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) .</span><span class="sxs-lookup"><span data-stu-id="4a997-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="4a997-127">Améliorez votre fonction point d’entrée message service pour répondre aux événements supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4a997-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a997-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a997-128">See also</span></span>

- [<span data-ttu-id="4a997-129">Mise en œuvre de message</span><span class="sxs-lookup"><span data-stu-id="4a997-129">Message Service Implementation</span></span>](message-service-implementation.md)

