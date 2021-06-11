---
title: Conception d’un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 19a8a939685c440901f3f57d72baf673a579e590
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404294"
---
# <a name="designing-a-message-service"></a><span data-ttu-id="bdb8c-103">Conception d’un service de messagerie</span><span class="sxs-lookup"><span data-stu-id="bdb8c-103">Designing a message service</span></span>

<span data-ttu-id="bdb8c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bdb8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bdb8c-105">Avant de commencer à écrire du code pour prendre en charge votre service de message, il est important de créer une conception.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-105">Before you begin to write code to support your message service, it is important to create a design.</span></span> <span data-ttu-id="bdb8c-106">Résolvez les problèmes suivants dans votre processus de conception :</span><span class="sxs-lookup"><span data-stu-id="bdb8c-106">Resolve the following issues in your design process:</span></span>
  
1. <span data-ttu-id="bdb8c-107">Déterminez le nombre de fournisseurs de services à inclure dans le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-107">Determine how many service providers should be included in the message service.</span></span> <span data-ttu-id="bdb8c-108">Incluez uniquement les fournisseurs de services associés (c’est-à-dire, les fournisseurs qui fonctionnent avec le même système de messagerie) dans votre service.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-108">Include only related service providers (that is, providers that work with the same messaging system) in your service.</span></span> <span data-ttu-id="bdb8c-109">Les fournisseurs de services non liés n’appartiennent pas au même service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-109">Unrelated service providers do not belong in the same message service.</span></span> <span data-ttu-id="bdb8c-110">Utilisez le profil pour l’intégration de fournisseurs de services et de services de messagerie non liés.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-110">Use the profile for integrating unrelated service providers and message services.</span></span>
    
2. <span data-ttu-id="bdb8c-111">Déterminez le type de fournisseur de services à inclure dans le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-111">Determine what type of service providers should be included in the message service.</span></span> <span data-ttu-id="bdb8c-112">La plupart des services de messge incluent un fournisseur de chacun des types courants.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-112">Most messge services include one provider of each of the common types.</span></span> <span data-ttu-id="bdb8c-113">Autrement dit, le service de messagerie classique dispose d’un fournisseur de carnet d’adresses, d’un fournisseur de magasins de messages et d’un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-113">That is, the typical message service has one address book provider, one message store provider, and one transport provider.</span></span>
    
3. <span data-ttu-id="bdb8c-114">Déterminez le nombre de DLLs qui doivent contenir le service de message.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-114">Determine how many DLLs should contain the message service.</span></span> <span data-ttu-id="bdb8c-115">Le nombre de DLL qu’un service de message utilise dépend des facteurs suivants :</span><span class="sxs-lookup"><span data-stu-id="bdb8c-115">The number of DLLs that a message service uses depends on the following:</span></span>
    
   - <span data-ttu-id="bdb8c-116">Degré de complexité que vous êtes prêt à gérer en tant qu’auteur du service de message.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-116">The degree of complexity that you as the writer of the message service are willing to handle.</span></span>
    
   - <span data-ttu-id="bdb8c-117">Type de fournisseurs de services dans le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-117">The type of service providers in the message service.</span></span>
    
   - <span data-ttu-id="bdb8c-118">Relation que le service de message peut avoir avec un autre service de message.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-118">The relationship that the message service might have with another message service.</span></span>
    
   <span data-ttu-id="bdb8c-119">Étant donné que MAPI stocke un seul point d’entrée pour chaque type de fournisseur, n’incluez pas plusieurs fournisseurs du même type dans une seule DLL.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-119">Because MAPI stores only one entry point for each provider type, do not include multiple providers of the same type in a single DLL.</span></span> <span data-ttu-id="bdb8c-120">S’il est logique d’inclure plusieurs fournisseurs d’un type, implémentez-les dans des DLL distinctes ou leur faire partager une fonction de point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-120">If it makes sense to include multiple providers of one type, either implement them in separate DLLs or have them share an entry point function.</span></span> <span data-ttu-id="bdb8c-121">Une autre option consiste à implémenter des services de message associés, ou des services de message qui peuvent utiliser le même code d’installation et de configuration et la même fonction de point d’entrée DLL, dans une DLL.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-121">Another option is to implement related message services, or message services that are able to use the same installation and configuration code and the same DLL entry point function, in one DLL.</span></span>
    
   <span data-ttu-id="bdb8c-122">Si possible, restez simple et utilisez une DLL qui contient l’implémentation de tous les fournisseurs de services dans le service de messagerie et tout le code pour installer et configurer le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-122">If possible, keep it simple and use one DLL that contains the implementation of all the service providers in the message service and all the code to install and configure the message service.</span></span> <span data-ttu-id="bdb8c-123">Si cela n’est pas possible, vous pouvez implémenter une DLL pour le code d’installation et de configuration et une seule DLL pour tous les fournisseurs de services ou une DLL pour chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-123">If this is not possible, you can implement one DLL for the installation and configuration code and either a single DLL for all of the service providers or one DLL for each provider.</span></span>
    
4. <span data-ttu-id="bdb8c-124">Déterminez un nom pour la DLL ou les DLL du service de message.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-124">Determine a name for the message service DLL or DLLs.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="bdb8c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdb8c-125">See also</span></span>

- [<span data-ttu-id="bdb8c-126">Implémentation du service de message</span><span class="sxs-lookup"><span data-stu-id="bdb8c-126">Message Service Implementation</span></span>](message-service-implementation.md)

