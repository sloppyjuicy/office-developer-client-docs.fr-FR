---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- fonction tempmissing [Excel 2007], fonction TempMissing12 [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 37c127b2252f18643b34dfc72fd9929885a68d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435956"
---
# <a name="tempmissingtempmissing12"></a><span data-ttu-id="b79aa-104">TempMissing/TempMissing12</span><span class="sxs-lookup"><span data-stu-id="b79aa-104">TempMissing/TempMissing12</span></span>

 <span data-ttu-id="b79aa-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b79aa-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b79aa-106">Fonction de bibliothèque d'infrastructure qui crée une**XLOPER12** **XLOPER**/ temporaire de type **xltypeMissing**.</span><span class="sxs-lookup"><span data-stu-id="b79aa-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** of type **xltypeMissing**.</span></span>
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a><span data-ttu-id="b79aa-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b79aa-107">Parameters</span></span>

<span data-ttu-id="b79aa-108">Cette fonction n’utilise aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b79aa-108">This function takes no parameters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="b79aa-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b79aa-109">Return value</span></span>

<span data-ttu-id="b79aa-110">Renvoie un pointeur vers une expression **XLOPER**/ \*\*\*\* **xltypeMissing** .</span><span class="sxs-lookup"><span data-stu-id="b79aa-110">Returns a pointer to an **xltypeMissing** **XLOPER**/ **XLOPER12**.</span></span>
  
## <a name="example"></a><span data-ttu-id="b79aa-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="b79aa-111">Example</span></span>

<span data-ttu-id="b79aa-112">Cet exemple utilise **TempMissing12** pour fournir trois arguments manquants à **xlcWorkspace** suivi d'une valeur **booléenne** **false** pour supprimer l'affichage des barres de défilement de feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="b79aa-112">This example uses **TempMissing12** to provide three missing arguments to **xlcWorkspace** followed by a **Boolean** **FALSE** to suppress the display of worksheet scroll bars.</span></span> <span data-ttu-id="b79aa-113">Les trois premiers arguments correspondent à d'autres paramètres d'espace de travail qui ne sont pas affectés.</span><span class="sxs-lookup"><span data-stu-id="b79aa-113">The first three arguments correspond to other workspace settings which are unaffected.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="b79aa-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b79aa-114">See also</span></span>



[<span data-ttu-id="b79aa-115">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="b79aa-115">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

