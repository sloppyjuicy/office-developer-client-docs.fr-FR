---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- fonction debugPrintf [Excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311003"
---
# <a name="debugprintf"></a><span data-ttu-id="02c86-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="02c86-104">debugPrintf</span></span>

<span data-ttu-id="02c86-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="02c86-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="02c86-106">Fonction de bibliothèque d'infrastructure qui écrit une chaîne d'octets terminée par un caractère null vers le débogueur actif via la fonction **OutputDebugStringA**du kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="02c86-106">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**.</span></span> <span data-ttu-id="02c86-107">Si l'application n'a pas de débogueur, le débogueur système affiche la chaîne.</span><span class="sxs-lookup"><span data-stu-id="02c86-107">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="02c86-108">Si l'application n'a pas de débogueur et que le débogueur système n'est pas actif, **debugPrintf** n'a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="02c86-108">If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="02c86-109">Cette fonction ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="02c86-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="02c86-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02c86-110">Parameters</span></span>

 <span data-ttu-id="02c86-111">_lpFormat (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="02c86-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="02c86-112">La chaîne de mise en forme, qui suit la syntaxe et les règles pour celles utilisées avec la fonction **sprintf** .</span><span class="sxs-lookup"><span data-stu-id="02c86-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="02c86-113">_arguments_</span><span class="sxs-lookup"><span data-stu-id="02c86-113">_arguments_</span></span>
  
<span data-ttu-id="02c86-114">Zéro ou plusieurs arguments correspondant à la chaîne de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="02c86-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="02c86-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="02c86-115">Example</span></span>

<span data-ttu-id="02c86-116">Cette fonction imprime une chaîne pour indiquer que le contrôle lui a été passé.</span><span class="sxs-lookup"><span data-stu-id="02c86-116">This function prints a string to show that control was passed to it.</span></span> <span data-ttu-id="02c86-117">L'indicateur _ DEBUG doit être défini avant la compilation, sinon cette fonction n'a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="02c86-117">The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a><span data-ttu-id="02c86-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02c86-118">See also</span></span>



[<span data-ttu-id="02c86-119">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="02c86-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

