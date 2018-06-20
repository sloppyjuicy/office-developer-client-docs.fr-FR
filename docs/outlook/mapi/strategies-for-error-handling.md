---
title: Stratégies de gestion des erreurs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e778df216d0fe9b901cd9f7136c8014a6b8f0d0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787260"
---
# <a name="strategies-for-error-handling"></a><span data-ttu-id="1de4a-103">Stratégies de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="1de4a-103">Strategies for Error Handling</span></span>

  
  
<span data-ttu-id="1de4a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1de4a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1de4a-105">Méthodes d’interface sont virtuelles, il n’est pas possible de savoir, en tant qu’un appelant, l’ensemble de valeurs qui peut être renvoyé à partir de n’importe quel un appel.</span><span class="sxs-lookup"><span data-stu-id="1de4a-105">Because interface methods are virtual, it is not possible to know, as a caller, the full set of values that can be returned from any one call.</span></span> <span data-ttu-id="1de4a-106">Une implémentation d’une méthode peut retourner les cinq valeurs ; un autre peut retourner huit.</span><span class="sxs-lookup"><span data-stu-id="1de4a-106">One implementation of a method might return five values; another might return eight.</span></span> <span data-ttu-id="1de4a-107">Les entrées de référence dans la documentation de MAPI répertorient quelques valeurs pouvant être renvoyés pour chaque méthode ; Voici les valeurs que votre client ou fournisseur de services peut rechercher et traiter, car elles ont une signification spéciale.</span><span class="sxs-lookup"><span data-stu-id="1de4a-107">The reference entries in the MAPI documentation list a few values that can be returned for each method; these are the values that your client or service provider can check for and handle because they have special meanings.</span></span> <span data-ttu-id="1de4a-108">Autres valeurs peuvent être renvoyées, mais, car ils ne sont pas significatives, code spécial pour gérer ces n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1de4a-108">Other values can be returned, but because they are not meaningful, special code to handle those is not necessary.</span></span> <span data-ttu-id="1de4a-109">Un contrôle simple pour la réussite ou l’échec est approprié.</span><span class="sxs-lookup"><span data-stu-id="1de4a-109">A simple check for success or failure is adequate.</span></span>
  
<span data-ttu-id="1de4a-110">Quelques méthodes de l’interface renvoient des avertissements.</span><span class="sxs-lookup"><span data-stu-id="1de4a-110">A few of the interface methods return warnings.</span></span> <span data-ttu-id="1de4a-111">Si une méthode qui appelle votre client ou fournisseur de services peut retourner un message d’avertissement, utilisez la macro **HR_FAILED** pour tester la valeur de retour plutôt que d’une vérification de zéro ou différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="1de4a-111">If a method that your client or service provider calls can return a warning, use the **HR_FAILED** macro to test the return value rather than a check for zero or nonzero.</span></span> <span data-ttu-id="1de4a-112">Avertissements, bien que différent de zéro, diffèrent des codes d’erreur en ce sens qu’ils n’ont pas le bit élevé à définir.</span><span class="sxs-lookup"><span data-stu-id="1de4a-112">Warnings, although nonzero, differ from error codes in that they do not have the high bit set.</span></span> <span data-ttu-id="1de4a-113">Si votre client ou fournisseur de services n’utilise pas de la macro, il est probable que d’avertissement peut être confondue avec une défaillance.</span><span class="sxs-lookup"><span data-stu-id="1de4a-113">If your client or service provider does not use the macro, it is likely that a warning might be mistaken for a failure.</span></span> 
  
<span data-ttu-id="1de4a-114">Bien que la plupart des méthodes d’interface et les fonctions renvoient des valeurs HRESULT, certaines fonctions renvoient des valeurs de type longs non signés.</span><span class="sxs-lookup"><span data-stu-id="1de4a-114">Although most interface methods and functions return HRESULT values, some functions return unsigned long values.</span></span> <span data-ttu-id="1de4a-115">En outre, certaines méthodes utilisés dans l’environnement MAPI provenant de COM et renvoyer les valeurs d’erreur COM plutôt que les valeurs d’erreur MAPI.</span><span class="sxs-lookup"><span data-stu-id="1de4a-115">Also, some methods used in the MAPI environment come from COM and return COM error values rather than MAPI error values.</span></span> <span data-ttu-id="1de4a-116">Gardez à l’esprit les instructions suivantes lors d’appels :</span><span class="sxs-lookup"><span data-stu-id="1de4a-116">Keep in mind the following guidelines when making calls:</span></span>
  
- <span data-ttu-id="1de4a-117">Ne jamais s’appuient sur ou utilisez les valeurs de retour de **IUnknown::AddRef** ou **IUnknown::Release**.</span><span class="sxs-lookup"><span data-stu-id="1de4a-117">Never rely on or use the return values from **IUnknown::AddRef** or **IUnknown::Release**.</span></span> <span data-ttu-id="1de4a-118">Ces valeurs renvoyées sont uniquement à des fins de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="1de4a-118">These return values are for diagnostic purposes only.</span></span> 
    
- <span data-ttu-id="1de4a-119">**IUnknown::QueryInterface** renvoie toujours les erreurs COM génériques où la fonctionnalité est FACILITY_NULL ou FACILITY_RPC, plutôt que des erreurs MAPI.</span><span class="sxs-lookup"><span data-stu-id="1de4a-119">**IUnknown::QueryInterface** always returns generic COM errors where the facility is FACILITY_NULL or FACILITY_RPC, rather than MAPI errors.</span></span> 
    
- <span data-ttu-id="1de4a-120">Toutes les autres méthodes d’interface retournent les erreurs de l’interface MAPI avec une installation de FACILITY_ITF ou FACILITY_RPC ou erreurs FACILITY_NULL.</span><span class="sxs-lookup"><span data-stu-id="1de4a-120">All other interface methods return MAPI interface errors with a facility of FACILITY_ITF, or FACILITY_RPC or FACILITY_NULL errors.</span></span>
    
<span data-ttu-id="1de4a-121">Lorsqu’un appel est effectué à une méthode MAPI non pris en charge, un des quatre erreurs possibles peut être renvoyé :</span><span class="sxs-lookup"><span data-stu-id="1de4a-121">When a call is made to an unsupported MAPI method, one of four possible errors can be returned:</span></span> 
  
<span data-ttu-id="1de4a-122">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1de4a-122">MAPI_E_NO_SUPPORT</span></span>
  
<span data-ttu-id="1de4a-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="1de4a-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span>
  
<span data-ttu-id="1de4a-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1de4a-124">MAPI_E_INVALID_PARAMETER</span></span>
  
<span data-ttu-id="1de4a-125">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="1de4a-125">MAPI_E_VERSION.</span></span> 
  

