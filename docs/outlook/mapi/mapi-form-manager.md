---
title: Gestionnaire de formulaire MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f78c25285c7ac3f8736006e4a45079a7d9a6d867
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592296"
---
# <a name="mapi-form-manager"></a><span data-ttu-id="b4d2e-103">Gestionnaire de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="b4d2e-103">MAPI Form Manager</span></span>

  
  
<span data-ttu-id="b4d2e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4d2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4d2e-105">Un gestionnaire de formulaire est un objet qui implémente l’interface [IMAPIFormMgr](imapiformmgriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="b4d2e-105">A form manager is an object that implements the [IMAPIFormMgr](imapiformmgriunknown.md) interface.</span></span> <span data-ttu-id="b4d2e-106">La plupart des organisations utiliseront le Gestionnaire de formulaire fourni avec MAPI, appelé le Gestionnaire de formulaire par défaut.</span><span class="sxs-lookup"><span data-stu-id="b4d2e-106">Most organizations will use the form manager supplied with MAPI, referred to as the default form manager.</span></span> <span data-ttu-id="b4d2e-107">Toutefois, une organisation peut remplacer le Gestionnaire de formulaire par défaut avec un gestionnaire de formulaire personnalisé si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="b4d2e-107">However, an organization can replace the default form manager with a custom form manager if desired.</span></span> <span data-ttu-id="b4d2e-108">Le Gestionnaire de formulaire se charge de localisation des formulaires dans les bibliothèques de formulaires, le chargement des formulaires en réponse aux requêtes des utilisateurs et l’installation de formulaires dans la bibliothèque de formulaires local, bibliothèque de formulaires de dossier ou bibliothèque de formulaires personnels d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b4d2e-108">The form manager takes care of locating forms within form libraries, loading forms in response to user requests, and installing forms into a user's local form library, folder form library, or personal form library.</span></span> 
  
<span data-ttu-id="b4d2e-109">Pour un utilisateur d’interagir avec un message, une instance du serveur de formulaire pour la classe de message du message doit être créée et activée pour afficher le message et d’effectuer l’opération demandée dans le message.</span><span class="sxs-lookup"><span data-stu-id="b4d2e-109">For a user to interact with a message, an instance of the form server for the message's message class must be created and activated to display the message and carry out the requested operation on the message.</span></span> <span data-ttu-id="b4d2e-110">Comme décrit dans la rubrique [Bibliothèques de formulaires MAPI](mapi-form-libraries.md), mise en œuvre d’un formulaire peut exister dans plusieurs emplacements (bibliothèques de formulaires) et il n’existe aucune garantie qu’un formulaire ou à son serveur sera disponible localement ou en cours d’exécution d’état lorsqu’un utilisateur souhaite interagir avec lui.</span><span class="sxs-lookup"><span data-stu-id="b4d2e-110">As described in the topic [MAPI Form Libraries](mapi-form-libraries.md), a form's implementation can exist in several different locations (form libraries) and there is no guarantee that a form or its server will be locally available or in a running state when a user wants to interact with it.</span></span> <span data-ttu-id="b4d2e-111">Le Gestionnaire de formulaire prend en charge les détails de localisation et d’activation du formulaire.</span><span class="sxs-lookup"><span data-stu-id="b4d2e-111">The form manager takes care of the details of locating and activating the form.</span></span>
  
<span data-ttu-id="b4d2e-112">Clients utilisent les services fournis par le Gestionnaire de formulaire pour rechercher et d’activer les formulaires.</span><span class="sxs-lookup"><span data-stu-id="b4d2e-112">Clients use services provided by the form manager to find and activate forms.</span></span> <span data-ttu-id="b4d2e-113">L’interface **IMAPIFormMgr** est implémentée par le Gestionnaire de formulaire et est appelé par les clients pour accéder à ses services.</span><span class="sxs-lookup"><span data-stu-id="b4d2e-113">The **IMAPIFormMgr** interface is implemented by the form manager and is called by clients to access its services.</span></span> <span data-ttu-id="b4d2e-114">Le Gestionnaire de formulaire est un composant essentiel, car il masque presque tous les détails de la recherche et activer des formulaires à partir de clients de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b4d2e-114">The form manager is an essential component because it hides almost all the details of finding and activating forms from messaging clients.</span></span> 
  
<span data-ttu-id="b4d2e-115">Lors du chargement des serveurs de formulaire, le Gestionnaire de formulaire par défaut charge le formulaire à partir de la première bibliothèque de formulaires dans laquelle se trouve une implémentation de la classe de message du formulaire.</span><span class="sxs-lookup"><span data-stu-id="b4d2e-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span></span> <span data-ttu-id="b4d2e-116">Le Gestionnaire de formulaire par défaut recherche les bibliothèques de formulaires dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="b4d2e-116">The default form manager searches the form libraries in the following order:</span></span>
  
1. <span data-ttu-id="b4d2e-117">Bibliothèque de formulaires local de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b4d2e-117">The user's local form library.</span></span> <span data-ttu-id="b4d2e-118">Cette bibliothèque de formulaires est recherchée en premier, car elle fournit un accès rapide à l’implémentation d’un formulaire si l’implémentation est installée dans la bibliothèque de formulaires local.</span><span class="sxs-lookup"><span data-stu-id="b4d2e-118">This form library is searched first because it provides the fastest access to a form's implementation if the implementation is installed in the local form library.</span></span>
    
2. <span data-ttu-id="b4d2e-119">La bibliothèque de formulaires dossier du conteneur du message : le dossier dans lequel est stocké le message en cours de chargement.</span><span class="sxs-lookup"><span data-stu-id="b4d2e-119">The folder form library of the message's container — the folder in which the message being loaded is stored.</span></span>
    
3. <span data-ttu-id="b4d2e-120">Bibliothèque de formulaires personnels de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b4d2e-120">The user's personal form library.</span></span>
    
<span data-ttu-id="b4d2e-121">Un gestionnaire de formulaire personnalisé peut rechercher les bibliothèques de formulaires disponibles dans n’importe quel ordre, ou peut implémenter des autres bibliothèques de formulaires, par exemple une bibliothèque de formulaires de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="b4d2e-121">A custom form manager can search the available form libraries in any order, or can implement other form libraries such as an organization-wide form library.</span></span> <span data-ttu-id="b4d2e-122">Pour plus d’informations sur les bibliothèques de formulaires, voir [Bibliothèques de formulaires MAPI](mapi-form-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="b4d2e-122">For more details on form libraries, see [MAPI Form Libraries](mapi-form-libraries.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b4d2e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4d2e-123">See also</span></span>



[<span data-ttu-id="b4d2e-124">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="b4d2e-124">MAPI Forms</span></span>](mapi-forms.md)

