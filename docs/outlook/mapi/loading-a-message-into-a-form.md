---
title: Chargement d’un Message dans un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d677958b1a429201c05b5195c58bd7462d0f3d37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784523"
---
# <a name="loading-a-message-into-a-form"></a><span data-ttu-id="bb957-103">Chargement d’un Message dans un formulaire</span><span class="sxs-lookup"><span data-stu-id="bb957-103">Loading a Message Into a Form</span></span>

  
  
<span data-ttu-id="bb957-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb957-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bb957-105">Pour charger un message existant dans un formulaire à l’aide d’un serveur de formulaire, utilisez une des stratégies suivantes.</span><span class="sxs-lookup"><span data-stu-id="bb957-105">To load an existing message into a form using a form server, use one of the following strategies.</span></span>
  
- <span data-ttu-id="bb957-106">Appelez [IMAPISession::PrepareForm](imapisession-prepareform.md) pour créer un jeton et puis [IMAPISession::ShowForm](imapisession-showform.md) pour afficher le formulaire.</span><span class="sxs-lookup"><span data-stu-id="bb957-106">Call [IMAPISession::PrepareForm](imapisession-prepareform.md) to create a token and then [IMAPISession::ShowForm](imapisession-showform.md) to display the form.</span></span> 
    
- <span data-ttu-id="bb957-107">Appelez [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span><span class="sxs-lookup"><span data-stu-id="bb957-107">Call [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span></span> 
    
<span data-ttu-id="bb957-108">À l’aide de la stratégie **PrepareForm** et **ShowForm** est relativement simple, mais il les résultats dans les formulaires sont modales par rapport à votre client.</span><span class="sxs-lookup"><span data-stu-id="bb957-108">Using the **PrepareForm** and **ShowForm** strategy is comparatively easy, but it results in forms that are modal with respect to your client.</span></span> <span data-ttu-id="bb957-109">Il s’agit, car l’appel vers **ShowForm** ne retourne pas jusqu'à ce que le formulaire s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="bb957-109">This is because the call to **ShowForm** does not return until the form has exited.</span></span> <span data-ttu-id="bb957-110">Si vous avez besoin gérer les formulaires en mode asynchrone, n’utilisez pas cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="bb957-110">If you need to handle forms asynchronously, do not use this strategy.</span></span> 
  
<span data-ttu-id="bb957-111">À l’aide de la stratégie **LoadForm** est plus difficile, car la méthode requiert plusieurs paramètres.</span><span class="sxs-lookup"><span data-stu-id="bb957-111">Using the **LoadForm** strategy is more difficult because the method requires several parameters.</span></span> <span data-ttu-id="bb957-112">Ces paramètres indiquer au Gestionnaire de formulaire pour lancer le formulaire correct de serveur dans le contexte approprié et afficher le message approprié.</span><span class="sxs-lookup"><span data-stu-id="bb957-112">These parameters instruct the form manager to launch the proper form server in the proper context and display the proper message.</span></span> <span data-ttu-id="bb957-113">Si le serveur de formulaire est en cours d’exécution, le Gestionnaire de formulaire charge le message sur le serveur de formulaire sans lancer une nouvelle instance du serveur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="bb957-113">If the form server is already running, the form manager loads the message into the form server without launching a new instance of the form server.</span></span> 
  
<span data-ttu-id="bb957-114">Pour spécifier le serveur de formulaire à la barre de lancement, passez à la classe de message gérée par le serveur cible dans le contenu du paramètre _lpszMessageClass_ .</span><span class="sxs-lookup"><span data-stu-id="bb957-114">To specify which form server to launch, pass the message class handled by the target server in the contents of the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="bb957-115">La classe de message approprié peut être déterminée en récupérant la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) du message à charger.</span><span class="sxs-lookup"><span data-stu-id="bb957-115">The appropriate message class can be determined by retrieving the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message to be loaded.</span></span> <span data-ttu-id="bb957-116">Il n’est parfois aucun serveur de formulaire pour la classe de message spécifiée uniquement un serveur de formulaire qui gère les messages de la superclasse du message.</span><span class="sxs-lookup"><span data-stu-id="bb957-116">Sometimes there is no form server for the specified message class, only a form server that handles messages belonging to the message's superclass.</span></span> <span data-ttu-id="bb957-117">Si vous préférez que le message d’être chargé uniquement par un serveur de formulaire spécifiquement conçu pour gérer les messages de cette classe, définir l’indicateur MAPIFORM_EXACTMATCH dans l’appel **LoadForm** .</span><span class="sxs-lookup"><span data-stu-id="bb957-117">If you prefer that the message be loaded only by a form server specifically meant to handle messages of that class, set the MAPIFORM_EXACTMATCH flag in the **LoadForm** call.</span></span> <span data-ttu-id="bb957-118">Pour plus d’informations, consultez [Classes de Message MAPI](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="bb957-118">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
 <span data-ttu-id="bb957-119">**LoadForm** requiert également un pointeur vers le site de messagerie de l’afficheur et contexte d’affichage et la valeur du message cible **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) et **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) Propriétés.</span><span class="sxs-lookup"><span data-stu-id="bb957-119">**LoadForm** also requires a pointer to your viewer's message site and view context and the value for the target message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) and **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) properties.</span></span>
  

