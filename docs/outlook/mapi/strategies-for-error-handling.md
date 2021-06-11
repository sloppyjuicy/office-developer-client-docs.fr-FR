---
title: Stratégies de gestion des erreurs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9e76ae3f292d8348b9dc64cb54bffae96b96e871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424146"
---
# <a name="strategies-for-error-handling"></a><span data-ttu-id="13a17-103">Stratégies de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="13a17-103">Strategies for Error Handling</span></span>

  
  
<span data-ttu-id="13a17-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13a17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13a17-105">Étant donné que les méthodes d’interface sont virtuelles, il n’est pas possible de connaître, en tant qu’appelant, l’ensemble complet des valeurs qui peuvent être renvoyées à partir d’un seul appel.</span><span class="sxs-lookup"><span data-stu-id="13a17-105">Because interface methods are virtual, it is not possible to know, as a caller, the full set of values that can be returned from any one call.</span></span> <span data-ttu-id="13a17-106">Une implémentation d’une méthode peut renvoyer cinq valeurs ; une autre peut renvoyer huit.</span><span class="sxs-lookup"><span data-stu-id="13a17-106">One implementation of a method might return five values; another might return eight.</span></span> <span data-ttu-id="13a17-107">Les entrées de référence dans la documentation MAPI indiquent quelques valeurs qui peuvent être renvoyées pour chaque méthode . Voici les valeurs que votre client ou fournisseur de services peut vérifier et gérer, car elles ont des significations spéciales.</span><span class="sxs-lookup"><span data-stu-id="13a17-107">The reference entries in the MAPI documentation list a few values that can be returned for each method; these are the values that your client or service provider can check for and handle because they have special meanings.</span></span> <span data-ttu-id="13a17-108">D’autres valeurs peuvent être renvoyées, mais comme elles ne sont pas significatives, un code spécial pour les gérer n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="13a17-108">Other values can be returned, but because they are not meaningful, special code to handle those is not necessary.</span></span> <span data-ttu-id="13a17-109">Une vérification simple de la réussite ou de l’échec est adéquate.</span><span class="sxs-lookup"><span data-stu-id="13a17-109">A simple check for success or failure is adequate.</span></span>
  
<span data-ttu-id="13a17-110">Quelques méthodes d’interface retournent des avertissements.</span><span class="sxs-lookup"><span data-stu-id="13a17-110">A few of the interface methods return warnings.</span></span> <span data-ttu-id="13a17-111">Si une méthode que votre client ou fournisseur de services appelle peut renvoyer un avertissement, utilisez la macro **HR_FAILED** pour tester la valeur de retour plutôt qu’une vérification de zéro ou non zéro.</span><span class="sxs-lookup"><span data-stu-id="13a17-111">If a method that your client or service provider calls can return a warning, use the **HR_FAILED** macro to test the return value rather than a check for zero or nonzero.</span></span> <span data-ttu-id="13a17-112">Les avertissements, bien qu’autres que zéro, diffèrent des codes d’erreur en ce qu’ils n’ont pas le bit élevé.</span><span class="sxs-lookup"><span data-stu-id="13a17-112">Warnings, although nonzero, differ from error codes in that they do not have the high bit set.</span></span> <span data-ttu-id="13a17-113">Si votre client ou fournisseur de services n’utilise pas la macro, il est probable qu’un avertissement soit confondu avec un échec.</span><span class="sxs-lookup"><span data-stu-id="13a17-113">If your client or service provider does not use the macro, it is likely that a warning might be mistaken for a failure.</span></span> 
  
<span data-ttu-id="13a17-114">Bien que la plupart des méthodes et fonctions d’interface retournent des valeurs HRESULT, certaines fonctions retournent des valeurs longues non signées.</span><span class="sxs-lookup"><span data-stu-id="13a17-114">Although most interface methods and functions return HRESULT values, some functions return unsigned long values.</span></span> <span data-ttu-id="13a17-115">En outre, certaines méthodes utilisées dans l’environnement MAPI proviennent de COM et retournent des valeurs d’erreur COM plutôt que des valeurs d’erreur MAPI.</span><span class="sxs-lookup"><span data-stu-id="13a17-115">Also, some methods used in the MAPI environment come from COM and return COM error values rather than MAPI error values.</span></span> <span data-ttu-id="13a17-116">Gardez à l’esprit les instructions suivantes lors des appels :</span><span class="sxs-lookup"><span data-stu-id="13a17-116">Keep in mind the following guidelines when making calls:</span></span>
  
- <span data-ttu-id="13a17-117">Ne vous appuyez jamais sur les valeurs de retour de **IUnknown::AddRef** ou **IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="13a17-117">Never rely on or use the return values from **IUnknown::AddRef** or **IUnknown::Release**.</span></span> <span data-ttu-id="13a17-118">Ces valeurs de retour sont uniquement à des fins de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="13a17-118">These return values are for diagnostic purposes only.</span></span> 
    
- <span data-ttu-id="13a17-119">**IUnknown::QueryInterface** renvoie toujours des erreurs COM génériques lorsque la FACILITY_NULL ou FACILITY_RPC, plutôt que des erreurs MAPI.</span><span class="sxs-lookup"><span data-stu-id="13a17-119">**IUnknown::QueryInterface** always returns generic COM errors where the facility is FACILITY_NULL or FACILITY_RPC, rather than MAPI errors.</span></span> 
    
- <span data-ttu-id="13a17-120">Toutes les autres méthodes d’interface retournent des erreurs d’interface MAPI avec une FACILITY_ITF ou des FACILITY_RPC ou FACILITY_NULL erreurs.</span><span class="sxs-lookup"><span data-stu-id="13a17-120">All other interface methods return MAPI interface errors with a facility of FACILITY_ITF, or FACILITY_RPC or FACILITY_NULL errors.</span></span>
    
<span data-ttu-id="13a17-121">Lorsqu’un appel est passé à une méthode MAPI non prise enupportée, l’une des quatre erreurs possibles peut être renvoyée :</span><span class="sxs-lookup"><span data-stu-id="13a17-121">When a call is made to an unsupported MAPI method, one of four possible errors can be returned:</span></span> 
  
<span data-ttu-id="13a17-122">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="13a17-122">MAPI_E_NO_SUPPORT</span></span>
  
<span data-ttu-id="13a17-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="13a17-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span>
  
<span data-ttu-id="13a17-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="13a17-124">MAPI_E_INVALID_PARAMETER</span></span>
  
<span data-ttu-id="13a17-125">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="13a17-125">MAPI_E_VERSION.</span></span> 
  

