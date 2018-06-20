---
title: Fonctions de rappel de l’API C Excel4, Excel12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- fonctions [excel 2007], de rappel de l’api c
localization_priority: Normal
ms.assetid: 0f3ae86d-329a-4177-a65b-6288c248297e
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 221ea4c9c706d11acd31d3f2870d326a7189d299
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782003"
---
# <a name="c-api-callback-functions-excel4-excel12"></a><span data-ttu-id="71c74-104">Fonctions de rappel de l’API C Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="71c74-104">C API Callback Functions Excel4, Excel12</span></span>

<span data-ttu-id="71c74-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="71c74-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="71c74-106">Les fonctions **Excel 4** et **Excel12** sont fournies pour permettre la DLL à appeler une fonction de feuille de calcul Microsoft Excel interne, la fonction de feuille macro ou commande, ou XLL seule fonction spéciale ou de commande.</span><span class="sxs-lookup"><span data-stu-id="71c74-106">The **Excel4** and **Excel12** functions are provided to enable DLLs to call an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command.</span></span> <span data-ttu-id="71c74-107">Toutes les versions récentes d’Excel prennent en charge la fonction **Excel4** .</span><span class="sxs-lookup"><span data-stu-id="71c74-107">All recent versions of Excel support the **Excel4** function.</span></span> <span data-ttu-id="71c74-108">Démarrage de la fonction **Excel12** dans Excel 2007 est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="71c74-108">Starting in Excel 2007 the **Excel12** function is supported.</span></span> <span data-ttu-id="71c74-109">Les deux fonctions sont fournies sous deux formes :</span><span class="sxs-lookup"><span data-stu-id="71c74-109">Both functions are provided in two forms:</span></span> 
  
- <span data-ttu-id="71c74-110">Un formulaire de liste d’arguments de longueur variable (**Excel4/Excel12**)</span><span class="sxs-lookup"><span data-stu-id="71c74-110">A variable-length argument list form (**Excel4/Excel12**)</span></span>
    
- <span data-ttu-id="71c74-111">Un formulaire tableau d’arguments (**Excel4v/Excel12v**)</span><span class="sxs-lookup"><span data-stu-id="71c74-111">An array-of-arguments form (**Excel4v/Excel12v**)</span></span>
    
<span data-ttu-id="71c74-112">À l’exception de celui dans lequel les arguments sont passés à ces rappels, les deux sont équivalents.</span><span class="sxs-lookup"><span data-stu-id="71c74-112">Except for the way in which arguments are passed to these callbacks, the two forms are functionally equivalent.</span></span> <span data-ttu-id="71c74-113">Les concepts de base pour les deux formes sont décrits en détail dans [Excel 4/Excel12](excel4-excel12.md).</span><span class="sxs-lookup"><span data-stu-id="71c74-113">The basic concepts for both forms are fully described in [Excel4/Excel12](excel4-excel12.md).</span></span> <span data-ttu-id="71c74-114">[Excel4v/Excel12v](excel4v-excel12v.md) couvre les autres problèmes sur ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="71c74-114">[Excel4v/Excel12v](excel4v-excel12v.md) covers other issues about this form.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="71c74-115">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="71c74-115">In this section</span></span>

[<span data-ttu-id="71c74-116">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="71c74-116">Excel4/Excel12</span></span>](excel4-excel12.md)
  
[<span data-ttu-id="71c74-117">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="71c74-117">Excel4v/Excel12v</span></span>](excel4v-excel12v.md)
  

