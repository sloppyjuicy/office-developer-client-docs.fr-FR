---
title: Vue d’ensemble des formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4e7d48f6f6a47ce28aa0e1291ccef209b998c18e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432519"
---
# <a name="mapi-forms-overview"></a><span data-ttu-id="cbd10-103">Vue d’ensemble des formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="cbd10-103">MAPI forms overview</span></span>
  
<span data-ttu-id="cbd10-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbd10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbd10-105">Un formulaire MAPI est une visionneuse pour un message.</span><span class="sxs-lookup"><span data-stu-id="cbd10-105">A MAPI form is a viewer for a message.</span></span> <span data-ttu-id="cbd10-106">Chaque message possède une classe de message qui détermine le formulaire particulier qui est utilisé comme visionneuse.</span><span class="sxs-lookup"><span data-stu-id="cbd10-106">Every message has a message class that dictates the particular form that is used as its viewer.</span></span> <span data-ttu-id="cbd10-107">MAPI définit plusieurs classes de messages et a implémenté les formulaires d’affichage des messages de ces classes.</span><span class="sxs-lookup"><span data-stu-id="cbd10-107">MAPI defines several message classes and has implemented the forms for viewing messages of these classes.</span></span> <span data-ttu-id="cbd10-108">Les développeurs de logiciels clients peuvent créer des classes de messages et des formulaires personnalisés pour afficher les messages créés à l’aide des nouvelles classes.</span><span class="sxs-lookup"><span data-stu-id="cbd10-108">Client software developers can create new message classes and custom forms for viewing messages created by using the new classes.</span></span>
  
<span data-ttu-id="cbd10-109">Chaque formulaire personnalisé implémente un ensemble de commandes de menu standard, telles que **Ouvrir,** **Créer,** Supprimer et **Répondre,** et un ensemble de commandes spécifiques au formulaire particulier.</span><span class="sxs-lookup"><span data-stu-id="cbd10-109">Every custom form implements a set of standard menu commands, such as **Open**, **Create**, **Delete**, and **Reply**, and a set of commands that are specific to the particular form.</span></span> <span data-ttu-id="cbd10-110">Certaines commandes de formulaire sont intégrées à l’interface utilisateur de l’application cliente lorsque le formulaire est actif ; les autres commandes de formulaire remplacent complètement les commandes clientes.</span><span class="sxs-lookup"><span data-stu-id="cbd10-110">Some of the form commands are integrated with the user interface of the client application when the form is active; other form commands completely replace the client commands.</span></span> 
  
<span data-ttu-id="cbd10-111">L’illustration suivante montre la relation entre les composants MAPI impliqués dans l’utilisation de formulaires.</span><span class="sxs-lookup"><span data-stu-id="cbd10-111">The following illustration shows the relationship between the MAPI components involved in using forms.</span></span> 
  
<span data-ttu-id="cbd10-112">**Architecture de formulaire MAPI**</span><span class="sxs-lookup"><span data-stu-id="cbd10-112">**MAPI form architecture**</span></span>
  
<span data-ttu-id="cbd10-113">![Architecture de formulaire MAPI - Architecture](media/forms01.gif "de formulaire MAPI")</span><span class="sxs-lookup"><span data-stu-id="cbd10-113">![MAPI form architecture](media/forms01.gif "MAPI form architecture")</span></span>
  
<span data-ttu-id="cbd10-114">Dans le diagramme, notez que le gestionnaire de formulaires joue un rôle semblable à d’autres fournisseurs de services MAPI, bien qu’il ne s’agit pas d’un fournisseur de services lui-même.</span><span class="sxs-lookup"><span data-stu-id="cbd10-114">In the diagram, notice that the form manager plays a role that is similar to other MAPI service providers, although it is not a service provider itself.</span></span> <span data-ttu-id="cbd10-115">Le gestionnaire de formulaires est une DLL remplaçable qui implémente certaines interfaces MAPI.</span><span class="sxs-lookup"><span data-stu-id="cbd10-115">The form manager is a replaceable DLL that implements some of the MAPI interfaces.</span></span> <span data-ttu-id="cbd10-116">Bien que les développeurs peuvent implémenter leur propre gestionnaire de formulaires, la plupart des environnements utiliseront le gestionnaire de formulaires fourni par Microsoft en raison de la complexité du gestionnaire de formulaires.</span><span class="sxs-lookup"><span data-stu-id="cbd10-116">Although developers can implement their own form manager, most environments will use the form manager provided by Microsoft due to the form manager's complexity.</span></span>
  
<span data-ttu-id="cbd10-117">La liste suivante décrit les composants du diagramme et leur relation avec d’autres composants :</span><span class="sxs-lookup"><span data-stu-id="cbd10-117">The following list describes the components in the diagram and their relationship to other components:</span></span>
  
- <span data-ttu-id="cbd10-118">Client de messagerie : application qui peut utiliser des objets de formulaire.</span><span class="sxs-lookup"><span data-stu-id="cbd10-118">Messaging client: An application that can use form objects.</span></span> <span data-ttu-id="cbd10-119">Le client de messagerie utilise les interfaces de formulaire MAPI pour communiquer avec le gestionnaire de formulaires afin de charger des messages dans des objets de formulaire.</span><span class="sxs-lookup"><span data-stu-id="cbd10-119">The messaging client uses the MAPI form interfaces to communicate with the form manager to load messages into form objects.</span></span>
    
- <span data-ttu-id="cbd10-120">Interfaces de formulaire MAPI : norme définie pour la communication entre les composants MAPI liés aux formulaires.</span><span class="sxs-lookup"><span data-stu-id="cbd10-120">MAPI form interfaces: A defined standard for communication between MAPI components that are related to forms.</span></span>
    
- <span data-ttu-id="cbd10-121">Gestionnaire de formulaires : DLL que les clients de messagerie utilisent pour gérer l’installation des formulaires dans les bibliothèques de formulaires, le chargement des serveurs de formulaires et la communication initiale entre les clients de messagerie et les serveurs de formulaires.</span><span class="sxs-lookup"><span data-stu-id="cbd10-121">Form manager: The DLL that messaging clients use to handle installation of forms in form libraries, loading of form servers, and initial communication between messaging clients and form servers.</span></span>
    
- <span data-ttu-id="cbd10-122">Bibliothèques de formulaires : stockage permanent des fichiers exécutables associés à des serveurs de formulaires.</span><span class="sxs-lookup"><span data-stu-id="cbd10-122">Form libraries: Permanent storage for the executable files associated with form servers.</span></span>
    
- <span data-ttu-id="cbd10-123">Serveurs de formulaires : fichiers exécutables qui implémentent un formulaire.</span><span class="sxs-lookup"><span data-stu-id="cbd10-123">Form servers: Executable files that implement a form.</span></span> <span data-ttu-id="cbd10-124">Les serveurs de formulaires créent des objets de formulaire et des interfaces utilisateur pour traiter des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="cbd10-124">Form servers create form objects and user interfaces to deal with specific messages.</span></span> <span data-ttu-id="cbd10-125">Ce exécutable est également un serveur OLE et respecte les conventions OLE habituelles.</span><span class="sxs-lookup"><span data-stu-id="cbd10-125">This executable is also an OLE server and adheres to the usual OLE conventions.</span></span>
    
- <span data-ttu-id="cbd10-126">Objets de formulaire : objets d’exécuter créés par des serveurs de formulaires qui correspondent à des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="cbd10-126">Form objects: Run-time objects created by form servers that correspond to specific messages.</span></span> <span data-ttu-id="cbd10-127">Les objets de formulaire s’exécutent dans le même contexte de processus que leur serveur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="cbd10-127">Form objects run in the same process context as their form server.</span></span>
    
<span data-ttu-id="cbd10-128">Pour plus d’informations sur les composants de formulaire MAPI, voir [MAPI Forms](mapi-forms.md).</span><span class="sxs-lookup"><span data-stu-id="cbd10-128">For more information about MAPI form components, see [MAPI Forms](mapi-forms.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cbd10-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbd10-129">See also</span></span>

- [<span data-ttu-id="cbd10-130">Fonctionnalités et architecture MAPI</span><span class="sxs-lookup"><span data-stu-id="cbd10-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

