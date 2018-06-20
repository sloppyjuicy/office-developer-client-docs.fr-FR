---
title: Vue d’ensemble des formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 91bc0641723a92d8dc86bf3d1037d8e9936930ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784624"
---
# <a name="mapi-forms-overview"></a><span data-ttu-id="b0ec4-103">Vue d’ensemble des formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="b0ec4-103">MAPI forms overview</span></span>
  
<span data-ttu-id="b0ec4-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b0ec4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b0ec4-105">Un formulaire MAPI est une visionneuse pour un message.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-105">A MAPI form is a viewer for a message.</span></span> <span data-ttu-id="b0ec4-106">Chaque message possède une classe de message qui dicte le formulaire particulier qui est utilisé en tant que sa visionneuse.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-106">Every message has a message class that dictates the particular form that is used as its viewer.</span></span> <span data-ttu-id="b0ec4-107">MAPI définit plusieurs classes de message et a mis en œuvre les formulaires pour l’affichage des messages de ces classes.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-107">MAPI defines several message classes and has implemented the forms for viewing messages of these classes.</span></span> <span data-ttu-id="b0ec4-108">Les développeurs de logiciels clients peuvent créer des formulaires personnalisés pour l’affichage des messages créés à l’aide de nouvelles classes et nouvelles classes de message.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-108">Client software developers can create new message classes and custom forms for viewing messages created by using the new classes.</span></span>
  
<span data-ttu-id="b0ec4-109">Chaque formulaire personnalisé implémente un ensemble de commandes de menus standard, telles que **Ouvrir**, **créer**, **Supprimer**et **réponse**, et un ensemble de commandes qui sont spécifiques à la forme particulière.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-109">Every custom form implements a set of standard menu commands, such as **Open**, **Create**, **Delete**, and **Reply**, and a set of commands that are specific to the particular form.</span></span> <span data-ttu-id="b0ec4-110">Certaines des commandes de formulaire sont intégrés dans l’interface utilisateur de l’application cliente lorsque le formulaire est actif ; autres commandes remplacent complètement les commandes client.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-110">Some of the form commands are integrated with the user interface of the client application when the form is active; other form commands completely replace the client commands.</span></span> 
  
<span data-ttu-id="b0ec4-111">L’illustration suivante montre la relation entre les composants MAPI impliqués dans l’aide de formulaires.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-111">The following illustration shows the relationship between the MAPI components involved in using forms.</span></span> 
  
<span data-ttu-id="b0ec4-112">**Architecture de formulaire MAPI**</span><span class="sxs-lookup"><span data-stu-id="b0ec4-112">**MAPI form architecture**</span></span>
  
<span data-ttu-id="b0ec4-113">![Architecture de formulaire MAPI] (media/forms01.gif "Architecture de formulaire MAPI")</span><span class="sxs-lookup"><span data-stu-id="b0ec4-113">![MAPI form architecture](media/forms01.gif "MAPI form architecture")</span></span>
  
<span data-ttu-id="b0ec4-114">Dans le diagramme, notez que le Gestionnaire de formulaire joue un rôle qui est similaire aux autres fournisseurs de services MAPI, même s’il n’est pas un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-114">In the diagram, notice that the form manager plays a role that is similar to other MAPI service providers, although it is not a service provider itself.</span></span> <span data-ttu-id="b0ec4-115">Le Gestionnaire de formulaire est une DLL remplaçable qui implémente des interfaces MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-115">The form manager is a replaceable DLL that implements some of the MAPI interfaces.</span></span> <span data-ttu-id="b0ec4-116">Bien que les développeurs peuvent implémenter leur propre responsable de formulaire, la plupart des environnements utiliseront le Gestionnaire de formulaire fourni par Microsoft en raison de la complexité du responsable de l’écran.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-116">Although developers can implement their own form manager, most environments will use the form manager provided by Microsoft due to the form manager's complexity.</span></span>
  
<span data-ttu-id="b0ec4-117">La liste suivante décrit les composants dans le schéma et leurs relations à d’autres composants :</span><span class="sxs-lookup"><span data-stu-id="b0ec4-117">The following list describes the components in the diagram and their relationship to other components:</span></span>
  
- <span data-ttu-id="b0ec4-118">Client de messagerie : une application qui peut utiliser les objets de formulaire.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-118">Messaging client: An application that can use form objects.</span></span> <span data-ttu-id="b0ec4-119">Le client de messagerie utilise les interfaces de formulaire MAPI pour communiquer avec le Gestionnaire de formulaire pour charger des messages dans les objets de formulaire.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-119">The messaging client uses the MAPI form interfaces to communicate with the form manager to load messages into form objects.</span></span>
    
- <span data-ttu-id="b0ec4-120">Interfaces de formulaire MAPI : une norme pour la communication entre les composants MAPI qui sont associés aux formulaires.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-120">MAPI form interfaces: A defined standard for communication between MAPI components that are related to forms.</span></span>
    
- <span data-ttu-id="b0ec4-121">Gestionnaire de formulaire : la DLL qui utilisent des clients de messagerie pour gérer l’installation des formulaires dans les bibliothèques de formulaires, le chargement des serveurs de formulaire et la communication entre les clients de messagerie et les serveurs de formulaire initiale.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-121">Form manager: The DLL that messaging clients use to handle installation of forms in form libraries, loading of form servers, and initial communication between messaging clients and form servers.</span></span>
    
- <span data-ttu-id="b0ec4-122">Bibliothèques de formulaires : stockage Permanent pour les fichiers exécutables associés à des serveurs de formulaire.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-122">Form libraries: Permanent storage for the executable files associated with form servers.</span></span>
    
- <span data-ttu-id="b0ec4-123">Serveurs de formulaire : les fichiers exécutables qui implémentent un formulaire.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-123">Form servers: Executable files that implement a form.</span></span> <span data-ttu-id="b0ec4-124">Serveurs de formulaire créent des objets et des interfaces utilisateur pour traiter des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-124">Form servers create form objects and user interfaces to deal with specific messages.</span></span> <span data-ttu-id="b0ec4-125">Ce fichier exécutable est également un serveur OLE et respecte les conventions OLE habituelles.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-125">This executable is also an OLE server and adheres to the usual OLE conventions.</span></span>
    
- <span data-ttu-id="b0ec4-126">Objets de formulaire : objets exécution créés par les serveurs de formulaire qui correspondent à des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-126">Form objects: Run-time objects created by form servers that correspond to specific messages.</span></span> <span data-ttu-id="b0ec4-127">Objets de formulaire exécutent dans le même contexte de processus comme serveur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="b0ec4-127">Form objects run in the same process context as their form server.</span></span>
    
<span data-ttu-id="b0ec4-128">Pour plus d’informations sur les composants de formulaire MAPI, voir [Formulaires MAPI](mapi-forms.md).</span><span class="sxs-lookup"><span data-stu-id="b0ec4-128">For more information about MAPI form components, see [MAPI Forms](mapi-forms.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b0ec4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0ec4-129">See also</span></span>

- [<span data-ttu-id="b0ec4-130">Architecture et des fonctionnalités MAPI</span><span class="sxs-lookup"><span data-stu-id="b0ec4-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

