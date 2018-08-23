---
title: États de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 195a82bfcc163ee01d2d42c71e79a8f5c9c620e5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564632"
---
# <a name="form-states"></a><span data-ttu-id="07aa0-103">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="07aa0-103">Form states</span></span>

<span data-ttu-id="07aa0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07aa0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07aa0-105">Objets de formulaire peuvent être l’un des cinq états distincts, en fonction de quelles méthodes ont été appelées y et si des erreurs se sont produites dans l’exécution de ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="07aa0-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="07aa0-106">Les États sont décrits dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="07aa0-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="07aa0-107">État non initialisé</span><span class="sxs-lookup"><span data-stu-id="07aa0-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="07aa0-108">État normal</span><span class="sxs-lookup"><span data-stu-id="07aa0-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="07aa0-109">État NoScribble</span><span class="sxs-lookup"><span data-stu-id="07aa0-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="07aa0-110">État HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="07aa0-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="07aa0-111">État HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="07aa0-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="07aa0-112">Les États concernent principalement l’état des données de l’objet form.</span><span class="sxs-lookup"><span data-stu-id="07aa0-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="07aa0-113">Si les données doivent être enregistrés, si l’objet form doit autoriser les modifications apportées aux données et quel point en cours de l’enregistrement des données en que du formulaire est de refléter les différents états.</span><span class="sxs-lookup"><span data-stu-id="07aa0-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="07aa0-114">De ce fait, les transitions entre les États de formulaire ont plus faire de l’implémentation du serveur de votre formulaire de [IPersistMessage : IUnknown](ipersistmessageiunknown.md) que d’autres méthodes de l’interface.</span><span class="sxs-lookup"><span data-stu-id="07aa0-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="07aa0-115">La base de connaissances de ces États est très utile pour la bonne mise en oeuvre des interfaces de formulaire MAPI que votre serveur de formulaire doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="07aa0-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="07aa0-116">Les rubriques de cette section décrivent les différents états possibles, ainsi que les actions autorisées qui provoquent des transitions vers d’autres États.</span><span class="sxs-lookup"><span data-stu-id="07aa0-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="07aa0-117">Toute transition ne pas répertoriée dans les rubriques n’est pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="07aa0-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="07aa0-118">Si vos objets formulaire apportez non autorisées transitions entre les États, ils seront comporte pas comme que les clients de messagerie prévoient et peuvent entraîner des comportement imprévisible de l’objet client ou un formulaire.</span><span class="sxs-lookup"><span data-stu-id="07aa0-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="07aa0-119">Transitions d’état dépendent des informations issues des États précédents.</span><span class="sxs-lookup"><span data-stu-id="07aa0-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="07aa0-120">Serveur de votre formulaire aura probablement implémenter un indicateur dans ses objets formulaire pour indiquer si les valeurs des propriétés du message ont été modifiés pour faciliter les modifications ultérieures de l’état.</span><span class="sxs-lookup"><span data-stu-id="07aa0-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="07aa0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07aa0-121">See also</span></span>

- [<span data-ttu-id="07aa0-122">Développement de serveurs de formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="07aa0-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

