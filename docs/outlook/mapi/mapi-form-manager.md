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
ms.openlocfilehash: 3059183103ca2552505486b5ec54366729ae4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430195"
---
# <a name="mapi-form-manager"></a><span data-ttu-id="b9d2d-103">Gestionnaire de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="b9d2d-103">MAPI Form Manager</span></span>

  
  
<span data-ttu-id="b9d2d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9d2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9d2d-105">Un gestionnaire de formulaires est un objet qui implémente l’interface [IMAPIFormMgr.](imapiformmgriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="b9d2d-105">A form manager is an object that implements the [IMAPIFormMgr](imapiformmgriunknown.md) interface.</span></span> <span data-ttu-id="b9d2d-106">La plupart des organisations utilisent le gestionnaire de formulaires fourni avec MAPI, appelé gestionnaire de formulaires par défaut.</span><span class="sxs-lookup"><span data-stu-id="b9d2d-106">Most organizations will use the form manager supplied with MAPI, referred to as the default form manager.</span></span> <span data-ttu-id="b9d2d-107">Toutefois, une organisation peut remplacer le gestionnaire de formulaires par défaut par un gestionnaire de formulaires personnalisé si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="b9d2d-107">However, an organization can replace the default form manager with a custom form manager if desired.</span></span> <span data-ttu-id="b9d2d-108">Le gestionnaire de formulaires s’occupe de la localisation des formulaires dans les bibliothèques de formulaires, du chargement des formulaires en réponse aux demandes des utilisateurs et de l’installation des formulaires dans la bibliothèque de formulaires locale, la bibliothèque de formulaires de dossiers ou la bibliothèque de formulaires personnels d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b9d2d-108">The form manager takes care of locating forms within form libraries, loading forms in response to user requests, and installing forms into a user's local form library, folder form library, or personal form library.</span></span> 
  
<span data-ttu-id="b9d2d-109">Pour qu’un utilisateur interagisse avec un message, une instance du serveur de formulaires pour la classe de message du message doit être créée et activée pour afficher le message et effectuer l’opération demandée sur le message.</span><span class="sxs-lookup"><span data-stu-id="b9d2d-109">For a user to interact with a message, an instance of the form server for the message's message class must be created and activated to display the message and carry out the requested operation on the message.</span></span> <span data-ttu-id="b9d2d-110">Comme décrit dans la rubrique Bibliothèques de [formulaires MAPI,](mapi-form-libraries.md)l’implémentation d’un formulaire peut exister à différents emplacements (bibliothèques de formulaires) et il n’est pas garanti qu’un formulaire ou son serveur sera disponible localement ou dans un état d’exécution lorsqu’un utilisateur souhaite interagir avec celui-ci.</span><span class="sxs-lookup"><span data-stu-id="b9d2d-110">As described in the topic [MAPI Form Libraries](mapi-form-libraries.md), a form's implementation can exist in several different locations (form libraries) and there is no guarantee that a form or its server will be locally available or in a running state when a user wants to interact with it.</span></span> <span data-ttu-id="b9d2d-111">Le gestionnaire de formulaires s’occupe des détails de la localisation et de l’activation du formulaire.</span><span class="sxs-lookup"><span data-stu-id="b9d2d-111">The form manager takes care of the details of locating and activating the form.</span></span>
  
<span data-ttu-id="b9d2d-112">Les clients utilisent les services fournis par le gestionnaire de formulaires pour rechercher et activer des formulaires.</span><span class="sxs-lookup"><span data-stu-id="b9d2d-112">Clients use services provided by the form manager to find and activate forms.</span></span> <span data-ttu-id="b9d2d-113">**L’interface IMAPIFormMgr** est implémentée par le gestionnaire de formulaires et est appelée par les clients pour accéder à ses services.</span><span class="sxs-lookup"><span data-stu-id="b9d2d-113">The **IMAPIFormMgr** interface is implemented by the form manager and is called by clients to access its services.</span></span> <span data-ttu-id="b9d2d-114">Le gestionnaire de formulaires est un composant essentiel, car il masque presque tous les détails de recherche et d’activation des formulaires des clients de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b9d2d-114">The form manager is an essential component because it hides almost all the details of finding and activating forms from messaging clients.</span></span> 
  
<span data-ttu-id="b9d2d-115">Lors du chargement des serveurs de formulaires, le gestionnaire de formulaires par défaut charge le formulaire à partir de la première bibliothèque de formulaires dans laquelle une implémentation de la classe de message du formulaire est trouvée.</span><span class="sxs-lookup"><span data-stu-id="b9d2d-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span></span> <span data-ttu-id="b9d2d-116">Le gestionnaire de formulaires par défaut recherche les bibliothèques de formulaires dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="b9d2d-116">The default form manager searches the form libraries in the following order:</span></span>
  
1. <span data-ttu-id="b9d2d-117">Bibliothèque de formulaires locale de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b9d2d-117">The user's local form library.</span></span> <span data-ttu-id="b9d2d-118">Cette bibliothèque de formulaires est d’abord recherché, car elle fournit l’accès le plus rapide à l’implémentation d’un formulaire si l’implémentation est installée dans la bibliothèque de formulaires locale.</span><span class="sxs-lookup"><span data-stu-id="b9d2d-118">This form library is searched first because it provides the fastest access to a form's implementation if the implementation is installed in the local form library.</span></span>
    
2. <span data-ttu-id="b9d2d-119">Bibliothèque de formulaires de dossiers du conteneur du message : le dossier dans lequel le message en cours de chargement est stocké.</span><span class="sxs-lookup"><span data-stu-id="b9d2d-119">The folder form library of the message's container — the folder in which the message being loaded is stored.</span></span>
    
3. <span data-ttu-id="b9d2d-120">Bibliothèque de formulaires personnels de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b9d2d-120">The user's personal form library.</span></span>
    
<span data-ttu-id="b9d2d-121">Un gestionnaire de formulaires personnalisé peut effectuer des recherches dans les bibliothèques de formulaires disponibles dans n’importe quel ordre ou implémenter d’autres bibliothèques de formulaires telles qu’une bibliothèque de formulaires à l’échelle de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="b9d2d-121">A custom form manager can search the available form libraries in any order, or can implement other form libraries such as an organization-wide form library.</span></span> <span data-ttu-id="b9d2d-122">Pour plus d’informations sur les bibliothèques de formulaires, voir [MAPI Form Libraries](mapi-form-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="b9d2d-122">For more details on form libraries, see [MAPI Form Libraries](mapi-form-libraries.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b9d2d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9d2d-123">See also</span></span>



[<span data-ttu-id="b9d2d-124">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="b9d2d-124">MAPI Forms</span></span>](mapi-forms.md)

