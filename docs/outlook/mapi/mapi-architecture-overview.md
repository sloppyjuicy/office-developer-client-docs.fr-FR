---
title: Vue d'ensemble de l'architecture MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 98a723528a714918ad7e0f10534efb0d38ef139a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410076"
---
# <a name="mapi-architecture-overview"></a><span data-ttu-id="5089d-103">Vue d'ensemble de l'architecture MAPI</span><span class="sxs-lookup"><span data-stu-id="5089d-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="5089d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5089d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5089d-105">MAPI définit une architecture modulaire, comme illustré dans l'illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="5089d-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="5089d-106">![Architecture d'Outlook 2010] (media/amapi_43.gif "Architecture d'Outlook 2010")</span><span class="sxs-lookup"><span data-stu-id="5089d-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="5089d-107">L'application MAPI est appelée application cliente, car il s'agit d'un client du sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="5089d-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="5089d-108">Les applications de messagerie utilisent la messagerie en tant que partie centrale de leur traitement et offrent des fonctionnalités de messagerie étendues, telles que l'échange d'informations de différents types dans différents formats et la possibilité d'enregistrer et d'organiser les informations localement.</span><span class="sxs-lookup"><span data-stu-id="5089d-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="5089d-109">Les applications de messagerie, de planification et de flux de travail sont des exemples d'applications basées sur la messagerie.</span><span class="sxs-lookup"><span data-stu-id="5089d-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="5089d-110">Le sous-système MAPI est constitué d'une interface utilisateur commune et des interfaces de programmation.</span><span class="sxs-lookup"><span data-stu-id="5089d-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="5089d-111">L'interface utilisateur commune est un ensemble de boîtes de dialogue qui donne aux applications client une apparence cohérente et des utilisateurs de manière cohérente.</span><span class="sxs-lookup"><span data-stu-id="5089d-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="5089d-112">MAPI dispose d'interfaces de programmation qui sont utilisées par le sous-système MAPI, par les développeurs de logiciels clients et par les développeurs de fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="5089d-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="5089d-113">L'interface de programmation MAPI est l'interface de programmation principale basée sur les objets.</span><span class="sxs-lookup"><span data-stu-id="5089d-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="5089d-114">L'interface de programmation MAPI est similaire au modèle objet de composant OLE et est utilisée par le sous-système MAPI et les applications clientes basées sur la messagerie écrites en C ou C++.</span><span class="sxs-lookup"><span data-stu-id="5089d-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="5089d-115">En tant que développeur de logiciels client, vous effectuez des appels MAPI directement via l'interface de programmation MAPI.</span><span class="sxs-lookup"><span data-stu-id="5089d-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="5089d-116">Vous pouvez implémenter la messagerie avec une seule interface client MAPI ou une combinaison d'interfaces.</span><span class="sxs-lookup"><span data-stu-id="5089d-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="5089d-117">Une seule application peut effectuer des appels à des méthodes ou des fonctions appartenant à l'une des interfaces.</span><span class="sxs-lookup"><span data-stu-id="5089d-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5089d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5089d-118">See also</span></span>

<span data-ttu-id="5089d-119">-[Architecture et fonctionnalités MAPI](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="5089d-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

