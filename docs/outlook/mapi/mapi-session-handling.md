---
title: Gestion de Session MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 98c4bd0dba630db32fdb2309be3d29ebc13b1131
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422060"
---
# <a name="mapi-session-handling"></a><span data-ttu-id="ba71d-103">Gestion de Session MAPI</span><span class="sxs-lookup"><span data-stu-id="ba71d-103">MAPI Session Handling</span></span>

  
  
<span data-ttu-id="ba71d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba71d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba71d-105">Avant de pouvoir communiquer avec des fournisseurs de services et un système de messagerie sous-jacent, vous devez établir une session.</span><span class="sxs-lookup"><span data-stu-id="ba71d-105">Before you can communicate with service providers and an underlying messaging system, you must establish a session.</span></span> <span data-ttu-id="ba71d-106">Une session MAPI est un lien entre un client et d’autres composants MAPI.</span><span class="sxs-lookup"><span data-stu-id="ba71d-106">A MAPI session is a link from a client to other MAPI components.</span></span> <span data-ttu-id="ba71d-107">Suite au démarrage réussi d’une session, MAPI renvoie aux clients un pointeur vers un objet de session , un objet qui implémente l’interface **IMAPISession.**</span><span class="sxs-lookup"><span data-stu-id="ba71d-107">As the result of successfully starting a session, MAPI returns to clients a pointer to a session object — an object that implements the **IMAPISession** interface.</span></span> <span data-ttu-id="ba71d-108">Pour plus d’informations, [voir IMAPISession : IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="ba71d-108">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="ba71d-109">Vous pouvez utiliser les méthodes de l’interface **IMAPISession** pour accéder aux objets des fournisseurs de carnet d’adresses et de magasins de messages, accéder à plusieurs tables, afficher des formulaires, définir des propriétés de fournisseur de transport et effectuer l’administration de service de profil et de message.</span><span class="sxs-lookup"><span data-stu-id="ba71d-109">You can use the methods of the **IMAPISession** interface to access the objects of address book and message store providers, access several tables, display forms, set transport provider properties, and perform profile and message service administration.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="ba71d-110">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="ba71d-110">In this section</span></span>

[<span data-ttu-id="ba71d-111">Démarrage d’une session MAPI</span><span class="sxs-lookup"><span data-stu-id="ba71d-111">Starting a MAPI Session</span></span>](starting-a-mapi-session.md)
  
> <span data-ttu-id="ba71d-112">Décrit comment démarrer une session MAPI et inclut des liens vers des rubriques avec des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="ba71d-112">Describes how to start a MAPI session and includes links to topics with more detailed information.</span></span>
    
[<span data-ttu-id="ba71d-113">Fin d’une session MAPI</span><span class="sxs-lookup"><span data-stu-id="ba71d-113">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)
  
> <span data-ttu-id="ba71d-114">Décrit comment mettre fin à une session MAPI.</span><span class="sxs-lookup"><span data-stu-id="ba71d-114">Describes how to end a MAPI session.</span></span>
    
[<span data-ttu-id="ba71d-115">Accès aux objets à l’aide de la session</span><span class="sxs-lookup"><span data-stu-id="ba71d-115">Accessing Objects by Using the Session</span></span>](accessing-objects-by-using-the-session.md)
  
> <span data-ttu-id="ba71d-116">Décrit comment utiliser un pointeur de session pour accéder aux objets de session.</span><span class="sxs-lookup"><span data-stu-id="ba71d-116">Describes how to use a session pointer to access session objects.</span></span>
    
[<span data-ttu-id="ba71d-117">Récupération de l’identité principale et du fournisseur</span><span class="sxs-lookup"><span data-stu-id="ba71d-117">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
> <span data-ttu-id="ba71d-118">Décrit les propriétés utilisées pour récupérer l’identité principale et l’identité du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ba71d-118">Describes the properties used to retrieve primary and provider identity.</span></span>
    
[<span data-ttu-id="ba71d-119">Table d’état et objets d’état</span><span class="sxs-lookup"><span data-stu-id="ba71d-119">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)
  
> <span data-ttu-id="ba71d-120">Décrit comment accéder aux informations à partir du tableau d’état.</span><span class="sxs-lookup"><span data-stu-id="ba71d-120">Describes how to access information from the status table.</span></span>
    

