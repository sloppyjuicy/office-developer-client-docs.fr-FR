---
title: Gestion de Session MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: cdf3052175870287ff1a66d3745e90f8b8fff256
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784702"
---
# <a name="mapi-session-handling"></a><span data-ttu-id="75c2c-103">Gestion de Session MAPI</span><span class="sxs-lookup"><span data-stu-id="75c2c-103">MAPI Session Handling</span></span>

  
  
<span data-ttu-id="75c2c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="75c2c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="75c2c-105">Pour pouvoir communiquer avec les fournisseurs de services et un système de messagerie sous-jacent, vous devez établir une session.</span><span class="sxs-lookup"><span data-stu-id="75c2c-105">Before you can communicate with service providers and an underlying messaging system, you must establish a session.</span></span> <span data-ttu-id="75c2c-106">Une session MAPI est un lien à partir d’un client à d’autres composants MAPI.</span><span class="sxs-lookup"><span data-stu-id="75c2c-106">A MAPI session is a link from a client to other MAPI components.</span></span> <span data-ttu-id="75c2c-107">Comme le résultat de démarrage d’une session MAPI renvoie aux clients un pointeur vers un objet de session, un objet qui implémente l’interface **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="75c2c-107">As the result of successfully starting a session, MAPI returns to clients a pointer to a session object — an object that implements the **IMAPISession** interface.</span></span> <span data-ttu-id="75c2c-108">Pour plus d’informations, voir [IMAPISession : IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="75c2c-108">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="75c2c-109">Vous pouvez utiliser les méthodes de l’interface **IMAPISession** pour accéder aux objets de fournisseurs de magasins de messages et du carnet d’adresses, accéder à plusieurs tables, afficher des formulaires, définir des propriétés du fournisseur de transport et effectuer l’administration du service de profil et le message.</span><span class="sxs-lookup"><span data-stu-id="75c2c-109">You can use the methods of the **IMAPISession** interface to access the objects of address book and message store providers, access several tables, display forms, set transport provider properties, and perform profile and message service administration.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="75c2c-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="75c2c-110">In this section</span></span>

[<span data-ttu-id="75c2c-111">Démarrage d’une Session MAPI</span><span class="sxs-lookup"><span data-stu-id="75c2c-111">Starting a MAPI Session</span></span>](starting-a-mapi-session.md)
  
> <span data-ttu-id="75c2c-112">Décrit comment démarrer une session MAPI et inclut des liens vers des rubriques contenant des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="75c2c-112">Describes how to start a MAPI session and includes links to topics with more detailed information.</span></span>
    
[<span data-ttu-id="75c2c-113">Mettre fin à une Session MAPI</span><span class="sxs-lookup"><span data-stu-id="75c2c-113">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)
  
> <span data-ttu-id="75c2c-114">Décrit comment mettre fin à une session MAPI.</span><span class="sxs-lookup"><span data-stu-id="75c2c-114">Describes how to end a MAPI session.</span></span>
    
[<span data-ttu-id="75c2c-115">Accès aux objets à l’aide de la Session</span><span class="sxs-lookup"><span data-stu-id="75c2c-115">Accessing Objects by Using the Session</span></span>](accessing-objects-by-using-the-session.md)
  
> <span data-ttu-id="75c2c-116">Décrit comment utiliser un pointeur de session pour accéder aux objets de la session.</span><span class="sxs-lookup"><span data-stu-id="75c2c-116">Describes how to use a session pointer to access session objects.</span></span>
    
[<span data-ttu-id="75c2c-117">Extraction de principal et identité du fournisseur</span><span class="sxs-lookup"><span data-stu-id="75c2c-117">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
> <span data-ttu-id="75c2c-118">Décrit les propriétés utilisées pour extraire le principal et l’identité du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="75c2c-118">Describes the properties used to retrieve primary and provider identity.</span></span>
    
[<span data-ttu-id="75c2c-119">Table d’état et les objets d’état</span><span class="sxs-lookup"><span data-stu-id="75c2c-119">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)
  
> <span data-ttu-id="75c2c-120">Décrit comment accéder aux informations à partir de la table d’état.</span><span class="sxs-lookup"><span data-stu-id="75c2c-120">Describes how to access information from the status table.</span></span>
    

