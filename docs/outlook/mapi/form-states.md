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
ms.openlocfilehash: 61d20ff7010151a82c53cafc69270e6925796a5c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429165"
---
# <a name="form-states"></a><span data-ttu-id="eca74-103">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="eca74-103">Form states</span></span>

<span data-ttu-id="eca74-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eca74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eca74-105">Les objets de formulaire peuvent être dans l’un des cinq états distincts, selon les méthodes qui y ont été appelées et selon si des erreurs se sont produites lors de l’utilisation de ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="eca74-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="eca74-106">Les états sont décrits dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="eca74-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="eca74-107">État nonnitialisé</span><span class="sxs-lookup"><span data-stu-id="eca74-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="eca74-108">État normal</span><span class="sxs-lookup"><span data-stu-id="eca74-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="eca74-109">NoScribble State</span><span class="sxs-lookup"><span data-stu-id="eca74-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="eca74-110">HandsOffAfterSave, état</span><span class="sxs-lookup"><span data-stu-id="eca74-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="eca74-111">HandsOffFromNormal State</span><span class="sxs-lookup"><span data-stu-id="eca74-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="eca74-112">Les états concernent principalement l’état des données dans l’objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="eca74-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="eca74-113">Les différents états indiquent si les données doivent être enregistrées, si l’objet de formulaire doit autoriser les modifications apportées aux données et à quel point dans le processus d’enregistrement des données se trouve le formulaire.</span><span class="sxs-lookup"><span data-stu-id="eca74-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="eca74-114">En tant que tel, les états de formulaire et les transitions entre eux ont plus à faire avec l’implémentation de votre serveur de formulaires des méthodes d’interface [IPersistMessage : IUnknown](ipersistmessageiunknown.md) que les autres.</span><span class="sxs-lookup"><span data-stu-id="eca74-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="eca74-115">La connaissance de ces états est très utile pour une implémentation correcte des interfaces de formulaire MAPI que votre serveur de formulaires doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="eca74-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="eca74-116">Les rubriques de cette section décrivent les différents états, ainsi que les actions autorisées qui provoquent des transitions vers d’autres états.</span><span class="sxs-lookup"><span data-stu-id="eca74-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="eca74-117">Les transitions non répertoriées dans les rubriques ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="eca74-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="eca74-118">Si vos objets de formulaire font des transitions non possibles entre les états, ils ne se comporteront pas de la même façon que les clients de messagerie et pourraient entraîner un comportement imprévisible du client ou de l’objet formulaire.</span><span class="sxs-lookup"><span data-stu-id="eca74-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="eca74-119">Certaines transitions d’état dépendent des informations des états précédents.</span><span class="sxs-lookup"><span data-stu-id="eca74-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="eca74-120">Votre serveur de formulaire devra probablement implémenter un indicateur dans ses objets de formulaire pour indiquer si les valeurs des propriétés du message ont été modifiées pour faciliter les changements d’état ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="eca74-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eca74-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eca74-121">See also</span></span>

- [<span data-ttu-id="eca74-122">Développement de serveurs de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="eca74-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

