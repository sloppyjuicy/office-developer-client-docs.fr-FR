---
title: Chargement d’un message dans un formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: afecd3b334dd2cf7b2953916872982e6459a8434
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412414"
---
# <a name="loading-a-message-into-a-form"></a><span data-ttu-id="cb9de-103">Chargement d’un message dans un formulaire</span><span class="sxs-lookup"><span data-stu-id="cb9de-103">Loading a Message Into a Form</span></span>

  
  
<span data-ttu-id="cb9de-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb9de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb9de-105">Pour charger un message existant dans un formulaire à l’aide d’un serveur de formulaires, utilisez l’une des stratégies suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb9de-105">To load an existing message into a form using a form server, use one of the following strategies.</span></span>
  
- <span data-ttu-id="cb9de-106">Appelez [IMAPISession::P repareForm](imapisession-prepareform.md) pour créer un jeton, puis [IMAPISession::ShowForm](imapisession-showform.md) pour afficher le formulaire.</span><span class="sxs-lookup"><span data-stu-id="cb9de-106">Call [IMAPISession::PrepareForm](imapisession-prepareform.md) to create a token and then [IMAPISession::ShowForm](imapisession-showform.md) to display the form.</span></span> 
    
- <span data-ttu-id="cb9de-107">Appelez [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span><span class="sxs-lookup"><span data-stu-id="cb9de-107">Call [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span></span> 
    
<span data-ttu-id="cb9de-108">L’utilisation de la stratégie **PrepareForm** et **ShowForm** est relativement simple, mais elle se traduit par des formulaires modaux par rapport à votre client.</span><span class="sxs-lookup"><span data-stu-id="cb9de-108">Using the **PrepareForm** and **ShowForm** strategy is comparatively easy, but it results in forms that are modal with respect to your client.</span></span> <span data-ttu-id="cb9de-109">Cela est dû au fait que l’appel **à ShowForm** ne revient pas tant que le formulaire n’est pas sorti.</span><span class="sxs-lookup"><span data-stu-id="cb9de-109">This is because the call to **ShowForm** does not return until the form has exited.</span></span> <span data-ttu-id="cb9de-110">Si vous devez gérer les formulaires de manière asynchrone, n’utilisez pas cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="cb9de-110">If you need to handle forms asynchronously, do not use this strategy.</span></span> 
  
<span data-ttu-id="cb9de-111">L’utilisation de la stratégie **LoadForm** est plus difficile, car la méthode nécessite plusieurs paramètres.</span><span class="sxs-lookup"><span data-stu-id="cb9de-111">Using the **LoadForm** strategy is more difficult because the method requires several parameters.</span></span> <span data-ttu-id="cb9de-112">Ces paramètres indiquent au gestionnaire de formulaire de lancer le serveur de formulaires approprié dans le contexte approprié et d’afficher le message approprié.</span><span class="sxs-lookup"><span data-stu-id="cb9de-112">These parameters instruct the form manager to launch the proper form server in the proper context and display the proper message.</span></span> <span data-ttu-id="cb9de-113">Si le serveur de formulaires est déjà en cours d’exécution, le gestionnaire de formulaire charge le message dans le serveur de formulaires sans lancer une nouvelle instance du serveur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="cb9de-113">If the form server is already running, the form manager loads the message into the form server without launching a new instance of the form server.</span></span> 
  
<span data-ttu-id="cb9de-114">Pour spécifier le serveur de formulaire à lancer, passez la classe de message gérée par le serveur cible dans le contenu du _paramètre lpszMessageClass._</span><span class="sxs-lookup"><span data-stu-id="cb9de-114">To specify which form server to launch, pass the message class handled by the target server in the contents of the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="cb9de-115">La classe de message appropriée peut être déterminée en récupérant la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) du message à charger.</span><span class="sxs-lookup"><span data-stu-id="cb9de-115">The appropriate message class can be determined by retrieving the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message to be loaded.</span></span> <span data-ttu-id="cb9de-116">Parfois, il n’existe pas de serveur de formulaires pour la classe de message spécifiée, uniquement un serveur de formulaires qui gère les messages appartenant à la superclasse du message.</span><span class="sxs-lookup"><span data-stu-id="cb9de-116">Sometimes there is no form server for the specified message class, only a form server that handles messages belonging to the message's superclass.</span></span> <span data-ttu-id="cb9de-117">Si vous préférez que le message soit chargé uniquement par un serveur de formulaires spécifiquement destiné à gérer les messages de cette classe, définissez l’indicateur MAPIFORM_EXACTMATCH dans **l’appel LoadForm.**</span><span class="sxs-lookup"><span data-stu-id="cb9de-117">If you prefer that the message be loaded only by a form server specifically meant to handle messages of that class, set the MAPIFORM_EXACTMATCH flag in the **LoadForm** call.</span></span> <span data-ttu-id="cb9de-118">Pour plus d’informations, voir [CLASSES de message MAPI.](mapi-message-classes.md)</span><span class="sxs-lookup"><span data-stu-id="cb9de-118">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
 <span data-ttu-id="cb9de-119">**LoadForm** nécessite également un pointeur vers le site de message de votre visionneuse et le contexte d’affichage, ainsi que la valeur des propriétés **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) et **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message cible.</span><span class="sxs-lookup"><span data-stu-id="cb9de-119">**LoadForm** also requires a pointer to your viewer's message site and view context and the value for the target message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) and **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) properties.</span></span>
  

