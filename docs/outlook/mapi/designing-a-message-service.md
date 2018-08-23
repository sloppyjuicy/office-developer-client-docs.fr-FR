---
title: Conception d’un service de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b572ebcec0a33d2134f4cf19b88e3132cbd47117
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581999"
---
# <a name="designing-a-message-service"></a><span data-ttu-id="89a9c-103">Conception d’un service de message</span><span class="sxs-lookup"><span data-stu-id="89a9c-103">Designing a message service</span></span>

<span data-ttu-id="89a9c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89a9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89a9c-105">Avant de commencer à écrire du code pour prendre en charge votre service de message, il est important de créer une conception.</span><span class="sxs-lookup"><span data-stu-id="89a9c-105">Before you begin to write code to support your message service, it is important to create a design.</span></span> <span data-ttu-id="89a9c-106">Résoudre les problèmes dans votre processus de conception suivants :</span><span class="sxs-lookup"><span data-stu-id="89a9c-106">Resolve the following issues in your design process:</span></span>
  
1. <span data-ttu-id="89a9c-107">Déterminer le nombre de fournisseurs de services doivent être inclus dans le service de message.</span><span class="sxs-lookup"><span data-stu-id="89a9c-107">Determine how many service providers should be included in the message service.</span></span> <span data-ttu-id="89a9c-108">Inclure uniquement les fournisseurs de service associées (autrement dit, les fournisseurs qui fonctionnent avec le même système de messagerie) dans votre service.</span><span class="sxs-lookup"><span data-stu-id="89a9c-108">Include only related service providers (that is, providers that work with the same messaging system) in your service.</span></span> <span data-ttu-id="89a9c-109">Fournisseurs de services indépendant n’appartiennent pas dans le même service de message.</span><span class="sxs-lookup"><span data-stu-id="89a9c-109">Unrelated service providers do not belong in the same message service.</span></span> <span data-ttu-id="89a9c-110">Utiliser le profil pour l’intégration de fournisseurs de services indépendants et les services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="89a9c-110">Use the profile for integrating unrelated service providers and message services.</span></span>
    
2. <span data-ttu-id="89a9c-111">Déterminer le type de fournisseurs de services doit être inclus dans le service de message.</span><span class="sxs-lookup"><span data-stu-id="89a9c-111">Determine what type of service providers should be included in the message service.</span></span> <span data-ttu-id="89a9c-112">La plupart des services volante inclut un fournisseur de chacun des types courants.</span><span class="sxs-lookup"><span data-stu-id="89a9c-112">Most messge services include one provider of each of the common types.</span></span> <span data-ttu-id="89a9c-113">Autrement dit, le service de message par défaut a fournisseur de carnet d’adresses d’un fournisseur de magasins d’un message et fournisseur de transport d’un seul.</span><span class="sxs-lookup"><span data-stu-id="89a9c-113">That is, the typical message service has one address book provider, one message store provider, and one transport provider.</span></span>
    
3. <span data-ttu-id="89a9c-114">Déterminer le nombre de DLL doit contenir le service de message.</span><span class="sxs-lookup"><span data-stu-id="89a9c-114">Determine how many DLLs should contain the message service.</span></span> <span data-ttu-id="89a9c-115">Le nombre de DLL qui utilise un service de message dépend des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="89a9c-115">The number of DLLs that a message service uses depends on the following:</span></span>
    
   - <span data-ttu-id="89a9c-116">Degré de complexité en tant que l’auteur du message du service de message sont prêts à gérer.</span><span class="sxs-lookup"><span data-stu-id="89a9c-116">The degree of complexity that you as the writer of the message service are willing to handle.</span></span>
    
   - <span data-ttu-id="89a9c-117">Le type de fournisseurs de services dans le service de message.</span><span class="sxs-lookup"><span data-stu-id="89a9c-117">The type of service providers in the message service.</span></span>
    
   - <span data-ttu-id="89a9c-118">La relation dont le service de message avec un autre service de message.</span><span class="sxs-lookup"><span data-stu-id="89a9c-118">The relationship that the message service might have with another message service.</span></span>
    
   <span data-ttu-id="89a9c-119">Étant donné que MAPI stocke le point d’une seule entrée pour chaque type de fournisseur, n’incluez pas plusieurs fournisseurs du même type dans une DLL unique.</span><span class="sxs-lookup"><span data-stu-id="89a9c-119">Because MAPI stores only one entry point for each provider type, do not include multiple providers of the same type in a single DLL.</span></span> <span data-ttu-id="89a9c-120">S’il convient d’inclure plusieurs fournisseurs d’un type, les implémenter dans des DLL distinctes ou demandez-leur de partager une fonction de point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="89a9c-120">If it makes sense to include multiple providers of one type, either implement them in separate DLLs or have them share an entry point function.</span></span> <span data-ttu-id="89a9c-121">Une autre option consiste à implémenter des services de messagerie connexes ou message les services qui sont en mesure d’utiliser la même installation et le code de configuration et la même DLL point d’entrée fonction dans une DLL.</span><span class="sxs-lookup"><span data-stu-id="89a9c-121">Another option is to implement related message services, or message services that are able to use the same installation and configuration code and the same DLL entry point function, in one DLL.</span></span>
    
   <span data-ttu-id="89a9c-122">Si possible, la simplicité et utiliser une DLL qui contient l’implémentation de tous les fournisseurs de service dans le service de message et tout le code pour installer et configurer le service de message.</span><span class="sxs-lookup"><span data-stu-id="89a9c-122">If possible, keep it simple and use one DLL that contains the implementation of all the service providers in the message service and all the code to install and configure the message service.</span></span> <span data-ttu-id="89a9c-123">Si ce n’est pas possible, vous pouvez implémenter une DLL de code de l’installation et la configuration et une DLL unique pour tous les fournisseurs de services ou une DLL pour chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="89a9c-123">If this is not possible, you can implement one DLL for the installation and configuration code and either a single DLL for all of the service providers or one DLL for each provider.</span></span>
    
4. <span data-ttu-id="89a9c-124">Déterminer un nom pour le service de message DLL ou la DLL.</span><span class="sxs-lookup"><span data-stu-id="89a9c-124">Determine a name for the message service DLL or DLLs.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="89a9c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89a9c-125">See also</span></span>

- [<span data-ttu-id="89a9c-126">Implémentation du service de messagerie</span><span class="sxs-lookup"><span data-stu-id="89a9c-126">Message Service Implementation</span></span>](message-service-implementation.md)

