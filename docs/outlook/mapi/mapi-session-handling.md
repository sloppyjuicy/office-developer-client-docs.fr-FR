---
title: Gestion de Session MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 98c4bd0dba630db32fdb2309be3d29ebc13b1131
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328223"
---
# <a name="mapi-session-handling"></a><span data-ttu-id="0e7e0-103">Gestion de Session MAPI</span><span class="sxs-lookup"><span data-stu-id="0e7e0-103">MAPI Session Handling</span></span>

  
  
<span data-ttu-id="0e7e0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e7e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e7e0-105">Avant de pouvoir communiquer avec des fournisseurs de services et un système de messagerie sous-jacent, vous devez établir une session.</span><span class="sxs-lookup"><span data-stu-id="0e7e0-105">Before you can communicate with service providers and an underlying messaging system, you must establish a session.</span></span> <span data-ttu-id="0e7e0-106">Une session MAPI est un lien entre un client et d'autres composants MAPI.</span><span class="sxs-lookup"><span data-stu-id="0e7e0-106">A MAPI session is a link from a client to other MAPI components.</span></span> <span data-ttu-id="0e7e0-107">Suite à la réussite du démarrage d'une session, MAPI renvoie aux clients un pointeur vers un objet session, un objet qui implémente l'interface **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="0e7e0-107">As the result of successfully starting a session, MAPI returns to clients a pointer to a session object — an object that implements the **IMAPISession** interface.</span></span> <span data-ttu-id="0e7e0-108">Pour plus d'informations, consultez la rubrique [IMAPISession: IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="0e7e0-108">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="0e7e0-109">Vous pouvez utiliser les méthodes de l'interface **IMAPISession** pour accéder aux objets des fournisseurs de carnet d'adresses et de banque de messages, accéder à plusieurs tables, afficher des formulaires, définir des propriétés de fournisseur de transport et effectuer des tâches de profil et de service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="0e7e0-109">You can use the methods of the **IMAPISession** interface to access the objects of address book and message store providers, access several tables, display forms, set transport provider properties, and perform profile and message service administration.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="0e7e0-110">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="0e7e0-110">In this section</span></span>

[<span data-ttu-id="0e7e0-111">Démarrage d'une session MAPI</span><span class="sxs-lookup"><span data-stu-id="0e7e0-111">Starting a MAPI Session</span></span>](starting-a-mapi-session.md)
  
> <span data-ttu-id="0e7e0-112">Décrit comment démarrer une session MAPI et inclut des liens vers des rubriques contenant des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="0e7e0-112">Describes how to start a MAPI session and includes links to topics with more detailed information.</span></span>
    
[<span data-ttu-id="0e7e0-113">Fermeture d'une session MAPI</span><span class="sxs-lookup"><span data-stu-id="0e7e0-113">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)
  
> <span data-ttu-id="0e7e0-114">Décrit comment mettre fin à une session MAPI.</span><span class="sxs-lookup"><span data-stu-id="0e7e0-114">Describes how to end a MAPI session.</span></span>
    
[<span data-ttu-id="0e7e0-115">Accès aux objets à l'aide de la session</span><span class="sxs-lookup"><span data-stu-id="0e7e0-115">Accessing Objects by Using the Session</span></span>](accessing-objects-by-using-the-session.md)
  
> <span data-ttu-id="0e7e0-116">Indique comment utiliser un pointeur de session pour accéder aux objets session.</span><span class="sxs-lookup"><span data-stu-id="0e7e0-116">Describes how to use a session pointer to access session objects.</span></span>
    
[<span data-ttu-id="0e7e0-117">Récupération de l'identité principale et de l'identité du fournisseur</span><span class="sxs-lookup"><span data-stu-id="0e7e0-117">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
> <span data-ttu-id="0e7e0-118">Décrit les propriétés utilisées pour extraire l'identité principale et l'identité du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0e7e0-118">Describes the properties used to retrieve primary and provider identity.</span></span>
    
[<span data-ttu-id="0e7e0-119">Table d'État et objets d'État</span><span class="sxs-lookup"><span data-stu-id="0e7e0-119">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)
  
> <span data-ttu-id="0e7e0-120">Indique comment accéder aux informations à partir de la table d'État.</span><span class="sxs-lookup"><span data-stu-id="0e7e0-120">Describes how to access information from the status table.</span></span>
    

