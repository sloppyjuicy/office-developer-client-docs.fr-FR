---
title: Prise en charge de la configuration du service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: aa1a433e90eda24f1199783bc604e047deb03ecd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418994"
---
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="4b7a3-103">Prise en charge de la configuration du service de messagerie</span><span class="sxs-lookup"><span data-stu-id="4b7a3-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="4b7a3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b7a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b7a3-105">Pour prendre en charge la configuration du service de message, utilisez la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="4b7a3-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="4b7a3-106">Implémenter une fonction de point d’entrée conforme au prototype [MSGSERVICEENTRY.](msgserviceentry.md)</span><span class="sxs-lookup"><span data-stu-id="4b7a3-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="4b7a3-107">Les fonctions de point d’entrée de service de message gèrent l’accès aux données de configuration et sont appelées dans les circonstances suivantes :</span><span class="sxs-lookup"><span data-stu-id="4b7a3-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="4b7a3-108">Lorsqu’un client se connecte pour récupérer des informations afin de configurer votre service de message.</span><span class="sxs-lookup"><span data-stu-id="4b7a3-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="4b7a3-109">Lorsqu’un client souhaite afficher ou modifier une propriété de configuration.</span><span class="sxs-lookup"><span data-stu-id="4b7a3-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="4b7a3-110">Bien que la plupart des services de message fournissent des fonctions de point d’entrée, comme ils le devraient, ces fonctions ne sont pas strictement requises.</span><span class="sxs-lookup"><span data-stu-id="4b7a3-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="4b7a3-111">Les services de message peuvent fournir l’accès aux données de configuration d’autres manières.</span><span class="sxs-lookup"><span data-stu-id="4b7a3-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="4b7a3-112">Toutefois, l’utilisation d’une fonction de point d’entrée standardise et simplifie le processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="4b7a3-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="4b7a3-113">MAPI s’attend à ce que toutes les fonctions de point d’entrée du service de message puissent stocker et récupérer des propriétés à partir des sections de profil associées à leur service de message.</span><span class="sxs-lookup"><span data-stu-id="4b7a3-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="4b7a3-114">Vous pouvez prendre en charge cette fonctionnalité de manière interactive, par programme ou de manière interactive et par programme.</span><span class="sxs-lookup"><span data-stu-id="4b7a3-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="4b7a3-115">Pour prendre en charge la configuration interactive, fournissez une feuille de propriétés qui affiche les propriétés impliquées dans la configuration de votre service de message.</span><span class="sxs-lookup"><span data-stu-id="4b7a3-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="4b7a3-116">En tant qu’option, vous pouvez également fournir des feuilles de propriétés pour chaque fournisseur configurable.</span><span class="sxs-lookup"><span data-stu-id="4b7a3-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="4b7a3-117">Certains services de message limitent les utilisateurs à une vue en lecture seule des propriétés de configuration . d’autres services de message permettent aux utilisateurs d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="4b7a3-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="4b7a3-118">Pour prendre en charge la configuration par programme, votre fonction de point d’entrée de service de message doit pouvoir fonctionner sans intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4b7a3-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="4b7a3-119">Si votre service de message peut être appelé par l’Assistant Profil, vous devez prendre en charge la configuration par programme.</span><span class="sxs-lookup"><span data-stu-id="4b7a3-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="4b7a3-120">Si votre service de message ne s’autorise pas à être configuré à l’aide de l’Assistant Profil, vous pouvez choisir de prendre en charge ou non la configuration par programme.</span><span class="sxs-lookup"><span data-stu-id="4b7a3-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="4b7a3-121">Pour plus d’informations sur la prise en charge de la configuration dans une fonction de point d’entrée de service de message, voir [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="4b7a3-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="4b7a3-122">Publiez le nom de votre fonction de point d’entrée de service de message dans le fichier de configuration Mapisvc.inf en incluant l’entrée suivante dans la section service de message :</span><span class="sxs-lookup"><span data-stu-id="4b7a3-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="4b7a3-123">Créez une ou plusieurs boîtes de dialogue de feuille de propriétés pour afficher les données de configuration.</span><span class="sxs-lookup"><span data-stu-id="4b7a3-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="4b7a3-124">Effectuez les tâches suivantes si vous souhaitez autoriser l’Assistant Profil à configurer votre service de message :</span><span class="sxs-lookup"><span data-stu-id="4b7a3-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="4b7a3-125">Implémenter une fonction de point d’entrée conforme au prototype [WIZARDENTRY.](wizardentry.md)</span><span class="sxs-lookup"><span data-stu-id="4b7a3-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="4b7a3-126">Implémentez une Windows de dialogue standard conforme au prototype [SERVICEWIZARDDLGPROC.](servicewizarddlgproc.md)</span><span class="sxs-lookup"><span data-stu-id="4b7a3-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="4b7a3-127">Améliorez votre fonction de point d’entrée de service de message pour répondre à des événements supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4b7a3-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b7a3-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b7a3-128">See also</span></span>

- [<span data-ttu-id="4b7a3-129">Implémentation du service de message</span><span class="sxs-lookup"><span data-stu-id="4b7a3-129">Message Service Implementation</span></span>](message-service-implementation.md)

