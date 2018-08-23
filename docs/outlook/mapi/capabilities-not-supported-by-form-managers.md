---
title: Fonctionnalités non prises en charge par les gestionnaires de formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a84c0a93f80080b71f6049e73f0a0094c38c28ef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566872"
---
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="c1e41-103">Fonctionnalités non prises en charge par les gestionnaires de formulaires</span><span class="sxs-lookup"><span data-stu-id="c1e41-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="c1e41-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1e41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1e41-105">Les fonctionnalités suivantes ne sont pas pris en charge par le Gestionnaire de formulaire par défaut pour des raisons de performances, mais peuvent être pris en charge par les responsables de formulaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c1e41-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="c1e41-106">Une hiérarchie qui permet les formes groupées ou de catégorie au sein d’une bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="c1e41-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="c1e41-107">Une bibliothèque de formulaires est une base de données de fichiers plats des formulaires.</span><span class="sxs-lookup"><span data-stu-id="c1e41-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="c1e41-108">Contrôle d’accès pour les catégories de formulaires, correspondant à des classes de message ou surclasse.</span><span class="sxs-lookup"><span data-stu-id="c1e41-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="c1e41-109">Prise en charge de plusieurs versions linguistiques du même formulaire dans une bibliothèque de formulaires unique.</span><span class="sxs-lookup"><span data-stu-id="c1e41-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="c1e41-110">Il s’agit des problèmes de mise en œuvre.</span><span class="sxs-lookup"><span data-stu-id="c1e41-110">These are implementation issues.</span></span> <span data-ttu-id="c1e41-111">Il n’a rien à empêcher un gestionnaire de formulaires personnalisés à partir de l’implémentation de ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="c1e41-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="c1e41-112">L’architecture de formulaire MAPI ne gère pas plusieurs responsables de formulaire qui s’exécutent simultanément.</span><span class="sxs-lookup"><span data-stu-id="c1e41-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="c1e41-113">Bien que MAPI prend en charge plusieurs fournisseurs de magasins message simultanés, fournisseurs de transport et fournisseurs de carnet d’adresses, seul un gestionnaire de formulaire unique est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c1e41-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="c1e41-114">Étant donné que le gestionnaire qu’un seul formulaire peut être exécuté à la fois, si vous implémentez un gestionnaire de formulaire personnalisé, vous devrez réimplémenter toutes les fonctionnalités du Gestionnaire de formulaire par défaut dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="c1e41-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="c1e41-115">Le Gestionnaire de votre formulaire personnalisé remplacera entièrement du Gestionnaire de formulaire par défaut, les fonctionnalités du Gestionnaire de formulaire par défaut ne seront pas disponibles, sauf si elles sont dupliqués dans le Gestionnaire de votre formulaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c1e41-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c1e41-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1e41-116">See also</span></span>



[<span data-ttu-id="c1e41-117">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="c1e41-117">MAPI Forms</span></span>](mapi-forms.md)

