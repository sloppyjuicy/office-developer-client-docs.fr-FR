---
title: Vue d’ensemble de l’architecture MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a0f2efc17ca8790502f11d677498013cbe10205d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579353"
---
# <a name="mapi-architecture-overview"></a><span data-ttu-id="4cfec-103">Vue d’ensemble de l’architecture MAPI</span><span class="sxs-lookup"><span data-stu-id="4cfec-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="4cfec-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cfec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cfec-105">MAPI définit une architecture modulaire, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="4cfec-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="4cfec-106">![Architecture Outlook 2010] (media/amapi_43.gif "Architecture Outlook 2010")</span><span class="sxs-lookup"><span data-stu-id="4cfec-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="4cfec-107">L’application MAPI est appelée une application cliente car il s’agit d’un client du sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="4cfec-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="4cfec-108">Applications de messagerie utilisent la messagerie dans le cadre de leur traitement centrale et offrent des fonctionnalités de messagerie étendues, telles que l’échange d’informations de différents types dans différents formats et la possibilité d’enregistrer et organiser les informations localement.</span><span class="sxs-lookup"><span data-stu-id="4cfec-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="4cfec-109">Message électronique, la planification, et les applications de flux de travail sont des exemples d’applications de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4cfec-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="4cfec-110">Le sous-système MAPI est composé d’une interface utilisateur commune et les interfaces de programmation.</span><span class="sxs-lookup"><span data-stu-id="4cfec-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="4cfec-111">L’interface utilisateur courants est un ensemble de boîtes de dialogue qui offre aux applications clientes en uniformiser l’apparence et les utilisateurs fonctionnent de manière cohérente.</span><span class="sxs-lookup"><span data-stu-id="4cfec-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="4cfec-112">MAPI a des interfaces qui sont utilisés par le sous-système MAPI, les développeurs de logiciels clients et par les développeurs de fournisseur de service de programmation.</span><span class="sxs-lookup"><span data-stu-id="4cfec-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="4cfec-113">L’interface de programmation MAPI est l’interface de programmation orientée objet principal.</span><span class="sxs-lookup"><span data-stu-id="4cfec-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="4cfec-114">L’interface de programmation MAPI est similaire au modèle d’objet OLE composant et est utilisée par le sous-système MAPI et les applications clientes de messagerie écrites en C ou C++.</span><span class="sxs-lookup"><span data-stu-id="4cfec-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="4cfec-115">En tant que développeur de logiciels clients, effectuer des appels MAPI directement par le biais de l’interface de programmation MAPI.</span><span class="sxs-lookup"><span data-stu-id="4cfec-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="4cfec-116">Vous pouvez implémenter de messagerie avec une interface de client MAPI unique ou une combinaison des interfaces.</span><span class="sxs-lookup"><span data-stu-id="4cfec-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="4cfec-117">Une seule application pouvez émettre des appels aux méthodes ou aux fonctions appartenant à une des interfaces.</span><span class="sxs-lookup"><span data-stu-id="4cfec-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4cfec-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cfec-118">See also</span></span>

<span data-ttu-id="4cfec-119">-[Architecture et des fonctionnalités MAPI](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="4cfec-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

