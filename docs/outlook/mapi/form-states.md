---
title: États de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 61d20ff7010151a82c53cafc69270e6925796a5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327516"
---
# <a name="form-states"></a><span data-ttu-id="c34f2-103">États de formulaire</span><span class="sxs-lookup"><span data-stu-id="c34f2-103">Form states</span></span>

<span data-ttu-id="c34f2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c34f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c34f2-105">Les objets Form peuvent être dans l'un des cinq États distincts, en fonction des méthodes qui ont été appelées et si des erreurs se sont produites lors de l'exécution de ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c34f2-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="c34f2-106">Les États sont décrits dans les rubriques suivantes:</span><span class="sxs-lookup"><span data-stu-id="c34f2-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="c34f2-107">État non initialisé</span><span class="sxs-lookup"><span data-stu-id="c34f2-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="c34f2-108">État normal</span><span class="sxs-lookup"><span data-stu-id="c34f2-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="c34f2-109">État noScribble</span><span class="sxs-lookup"><span data-stu-id="c34f2-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="c34f2-110">État HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="c34f2-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="c34f2-111">État HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="c34f2-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="c34f2-112">Les États sont principalement liés à l'état des données dans l'objet Form.</span><span class="sxs-lookup"><span data-stu-id="c34f2-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="c34f2-113">Les différents États indiquent si les données doivent être enregistrées, si l'objet Form doit autoriser les modifications apportées aux données et le moment où se trouve le formulaire.</span><span class="sxs-lookup"><span data-stu-id="c34f2-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="c34f2-114">En tant que telles, les États de formulaire et les transitions entre eux ont davantage à faire avec l'implémentation de IPersistMessage Server de votre serveur de formulaires: les méthodes d'interface [IUnknown](ipersistmessageiunknown.md) que n'importe quel autre.</span><span class="sxs-lookup"><span data-stu-id="c34f2-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="c34f2-115">La connaissance de ces États est très utile pour mettre en œuvre correctement les interfaces de formulaire MAPI que votre serveur de formulaire doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="c34f2-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="c34f2-116">Les rubriques de cette section décrivent les différents États, ainsi que les actions autorisées entraînant des transitions vers d'autres États.</span><span class="sxs-lookup"><span data-stu-id="c34f2-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="c34f2-117">Les transitions non répertoriées dans les rubriques ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="c34f2-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="c34f2-118">Si vos objets de formulaire effectuent des transitions non autorisées entre les États, ils ne se comportent pas de la façon dont les clients de messagerie attendent et peuvent entraîner un comportement imprévisible du client ou de l'objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="c34f2-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c34f2-119">Certaines transitions d'État dépendent des informations des États précédents.</span><span class="sxs-lookup"><span data-stu-id="c34f2-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="c34f2-120">Votre serveur de formulaire devra probablement implémenter un indicateur dans ses objets de formulaire pour indiquer si les valeurs des propriétés du message ont été modifiées afin de faciliter les modifications ultérieures à l'État.</span><span class="sxs-lookup"><span data-stu-id="c34f2-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c34f2-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c34f2-121">See also</span></span>

- [<span data-ttu-id="c34f2-122">Développement de serveurs de formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="c34f2-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

