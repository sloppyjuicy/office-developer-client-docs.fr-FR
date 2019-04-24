---
title: Fonctions de rappel de l'API C Excel4, Excel12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- fonctions [Excel 2007], rappel de l'API c
localization_priority: Normal
ms.assetid: 0f3ae86d-329a-4177-a65b-6288c248297e
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5fe5eb7486f12d75ce7e42ad57141480ec735c54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304178"
---
# <a name="c-api-callback-functions-excel4-excel12"></a><span data-ttu-id="0a9ff-104">Fonctions de rappel de l'API C Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="0a9ff-104">C API Callback Functions Excel4, Excel12</span></span>

<span data-ttu-id="0a9ff-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0a9ff-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0a9ff-106">Les fonctions **Excel4** et **Excel12** sont fournies pour permettre aux DLL d'appeler une fonction de feuille de calcul Microsoft Excel interne, une fonction de feuille de macro ou une commande, ou une fonction ou une commande spéciale XLL uniquement.</span><span class="sxs-lookup"><span data-stu-id="0a9ff-106">The **Excel4** and **Excel12** functions are provided to enable DLLs to call an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command.</span></span> <span data-ttu-id="0a9ff-107">Toutes les versions récentes d'Excel prennent en charge la fonction **Excel4** .</span><span class="sxs-lookup"><span data-stu-id="0a9ff-107">All recent versions of Excel support the **Excel4** function.</span></span> <span data-ttu-id="0a9ff-108">À partir d'Excel 2007, la fonction **Excel12** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0a9ff-108">Starting in Excel 2007 the **Excel12** function is supported.</span></span> <span data-ttu-id="0a9ff-109">Ces deux fonctions sont fournies sous deux formes:</span><span class="sxs-lookup"><span data-stu-id="0a9ff-109">Both functions are provided in two forms:</span></span> 
  
- <span data-ttu-id="0a9ff-110">Formulaire de liste d'arguments de longueur variable (**Excel4/Excel12**)</span><span class="sxs-lookup"><span data-stu-id="0a9ff-110">A variable-length argument list form (**Excel4/Excel12**)</span></span>
    
- <span data-ttu-id="0a9ff-111">Formulaire de tableau d'arguments (**Excel4v/Excel12v**)</span><span class="sxs-lookup"><span data-stu-id="0a9ff-111">An array-of-arguments form (**Excel4v/Excel12v**)</span></span>
    
<span data-ttu-id="0a9ff-112">À l'exception de la façon dont les arguments sont transmis à ces rappels, les deux formulaires sont équivalents.</span><span class="sxs-lookup"><span data-stu-id="0a9ff-112">Except for the way in which arguments are passed to these callbacks, the two forms are functionally equivalent.</span></span> <span data-ttu-id="0a9ff-113">Les concepts de base des deux formulaires sont décrits en détail dans [Excel4/Excel12](excel4-excel12.md).</span><span class="sxs-lookup"><span data-stu-id="0a9ff-113">The basic concepts for both forms are fully described in [Excel4/Excel12](excel4-excel12.md).</span></span> <span data-ttu-id="0a9ff-114">[Excel4v/Excel12v](excel4v-excel12v.md) aborde d'autres problèmes liés à ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="0a9ff-114">[Excel4v/Excel12v](excel4v-excel12v.md) covers other issues about this form.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="0a9ff-115">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="0a9ff-115">In this section</span></span>

[<span data-ttu-id="0a9ff-116">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="0a9ff-116">Excel4/Excel12</span></span>](excel4-excel12.md)
  
[<span data-ttu-id="0a9ff-117">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="0a9ff-117">Excel4v/Excel12v</span></span>](excel4v-excel12v.md)
  

