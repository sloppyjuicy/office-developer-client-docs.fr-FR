---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- fonction xlautoopen [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf02f71458f2f4d8514f69a6b6f0921b5318303a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406646"
---
# <a name="xlautoopen"></a><span data-ttu-id="98389-104">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="98389-104">xlAutoOpen</span></span>

 <span data-ttu-id="98389-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="98389-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="98389-106">Fonction de rappel qui doit être implémentée et exportée par chaque XLL valide.</span><span class="sxs-lookup"><span data-stu-id="98389-106">Callback function that must be implemented and exported by every valid XLL.</span></span> <span data-ttu-id="98389-107">La **fonction xlAutoOpen** est l’endroit recommandé où enregistrer les commandes et fonctions XLL, initialiser les structures de données, personnaliser l’interface utilisateur, etc.</span><span class="sxs-lookup"><span data-stu-id="98389-107">The **xlAutoOpen** function is the recommended place from where to register XLL functions and commands, initialize data structures, customize the user interface, and so on.</span></span> 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a><span data-ttu-id="98389-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98389-108">Parameters</span></span>

<span data-ttu-id="98389-109">Cette fonction ne prend aucun argument.</span><span class="sxs-lookup"><span data-stu-id="98389-109">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="98389-110">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="98389-110">Property value/Return value</span></span>

<span data-ttu-id="98389-111">Votre exécution de cette fonction doit renvoyer 1 (**ent**).</span><span class="sxs-lookup"><span data-stu-id="98389-111">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98389-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="98389-112">Remarks</span></span>

<span data-ttu-id="98389-113">Microsoft Excel **appelle xlAutoOpen** chaque fois que le XLL est activé.</span><span class="sxs-lookup"><span data-stu-id="98389-113">Microsoft Excel calls **xlAutoOpen** whenever the XLL is activated.</span></span> <span data-ttu-id="98389-114">Le XLL est activé dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="98389-114">The XLL is activated in the following situations:</span></span> 
  
- <span data-ttu-id="98389-115">Au début d’une session Excel si elle était active dans la dernière session Excel qui s’est terminée normalement.</span><span class="sxs-lookup"><span data-stu-id="98389-115">At the start of an Excel session if it was active in the last Excel session that ended normally.</span></span>
    
- <span data-ttu-id="98389-116">S’il est chargé au cours d Excel session.</span><span class="sxs-lookup"><span data-stu-id="98389-116">If loaded during an Excel session.</span></span>
    
- <span data-ttu-id="98389-117">Un XLL peut être chargé de plusieurs manières :</span><span class="sxs-lookup"><span data-stu-id="98389-117">An XLL can be loaded in several ways:</span></span>
    
- <span data-ttu-id="98389-118">En choisissant **Ouvrir** dans **le** menu Fichier (où la version de Excel prend en charge cette méthode de chargement des XL).</span><span class="sxs-lookup"><span data-stu-id="98389-118">By choosing **Open** on the **File** menu (where the version of Excel supports this method of loading XLLs).</span></span> 
    
- <span data-ttu-id="98389-119">À l’aide du Gestionnaire de compléments.</span><span class="sxs-lookup"><span data-stu-id="98389-119">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="98389-120">À partir d’une autre XLL qui appelle [xlfRegister](xlfregister-form-1.md) avec le nom de cette DLL comme seul argument.</span><span class="sxs-lookup"><span data-stu-id="98389-120">From another XLL that calls [xlfRegister](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="98389-121">À partir d’une feuille macro XLM qui appelle [REGISTER](xlfregister-form-1.md) avec le nom de cette DLL comme seul argument.</span><span class="sxs-lookup"><span data-stu-id="98389-121">From an XLM macro sheet that calls [REGISTER](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="98389-122">Si le add-in est désactivé et réactivé pendant une session Excel, cette fonction est appelée lors de la réactivation.</span><span class="sxs-lookup"><span data-stu-id="98389-122">If the add-in is deactivated and reactivated during an Excel session, this function is called on reactivation.</span></span>
    
### <a name="example"></a><span data-ttu-id="98389-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="98389-123">Example</span></span>

<span data-ttu-id="98389-124">Consultez les  `SAMPLES\EXAMPLE\EXAMPLE.C` fichiers  `SAMPLES\GENERIC\GENERIC.C` et, par exemple, les implémentations de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="98389-124">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C`, and for example implementations of this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98389-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98389-125">See also</span></span>



[<span data-ttu-id="98389-126">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="98389-126">xlAutoClose</span></span>](xlautoclose.md)
  
[<span data-ttu-id="98389-127">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="98389-127">xlAutoRegister/xlAutoRegister12</span></span>](xlautoregister-xlautoregister12.md)


[<span data-ttu-id="98389-128">Fonctions du Gestionnaire de compléments et de l’interface XLL</span><span class="sxs-lookup"><span data-stu-id="98389-128">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

