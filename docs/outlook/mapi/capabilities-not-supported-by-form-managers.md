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
ms.openlocfilehash: e31eacaae54968fbdbd9fe0345130a8d09c3509f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419379"
---
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="d7edf-103">Fonctionnalités non prises en charge par les gestionnaires de formulaires</span><span class="sxs-lookup"><span data-stu-id="d7edf-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="d7edf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7edf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7edf-105">Les fonctionnalités suivantes ne sont pas prises en charge par le gestionnaire de formulaire par défaut pour des raisons de performances, mais peuvent être prises en charge par les gestionnaires de formulaires personnalisés.</span><span class="sxs-lookup"><span data-stu-id="d7edf-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="d7edf-106">Hiérarchie qui permet de regrouper ou de classer les formulaires dans une bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="d7edf-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="d7edf-107">Une bibliothèque de formulaires est une base de données de formulaires à fichier plat.</span><span class="sxs-lookup"><span data-stu-id="d7edf-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="d7edf-108">Contrôle d'accès pour les catégories de formulaires, correspondant aux classes de message ou aux superclasses.</span><span class="sxs-lookup"><span data-stu-id="d7edf-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="d7edf-109">Prise en charge de plusieurs versions linguistiques du même formulaire dans une seule bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="d7edf-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="d7edf-110">Il s'agit des problèmes d'implémentation.</span><span class="sxs-lookup"><span data-stu-id="d7edf-110">These are implementation issues.</span></span> <span data-ttu-id="d7edf-111">Il n'y a rien à empêcher un gestionnaire de formulaires personnalisés d'implémenter ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="d7edf-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="d7edf-112">L'architecture des formulaires MAPI ne prend pas en charge plusieurs gestionnaires de formulaires exécutés simultanément.</span><span class="sxs-lookup"><span data-stu-id="d7edf-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="d7edf-113">Bien que MAPI prenne en charge plusieurs fournisseurs de banques de messages simultanées, fournisseurs de transport et fournisseurs de carnet d'adresses, un seul gestionnaire de formulaires est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d7edf-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="d7edf-114">Étant donné qu'un seul gestionnaire de formulaires peut s'exécuter en même temps, si vous implémentez un gestionnaire de formulaires personnalisés, vous devrez réimplémenter toutes les fonctionnalités du gestionnaire de formulaires par défaut dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="d7edf-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="d7edf-115">Étant donné que votre gestionnaire de formulaires personnalisés remplacera entièrement le gestionnaire de formulaires par défaut, les fonctionnalités du gestionnaire de formulaires par défaut ne seront pas disponibles, sauf s'ils sont dupliqués dans votre gestionnaire de formulaires personnalisés.</span><span class="sxs-lookup"><span data-stu-id="d7edf-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d7edf-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7edf-116">See also</span></span>



[<span data-ttu-id="d7edf-117">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="d7edf-117">MAPI Forms</span></span>](mapi-forms.md)

