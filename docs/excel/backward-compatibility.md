---
title: Compatibilité descendante
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compatibilité des versions [Excel 2007], compatibilité XLL [Excel 2007], compatibilité descendante [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301679"
---
# <a name="backward-compatibility"></a><span data-ttu-id="00c00-104">Compatibilité descendante</span><span class="sxs-lookup"><span data-stu-id="00c00-104">Backward compatibility</span></span>

<span data-ttu-id="00c00-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="00c00-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="00c00-106">Cette rubrique traite des problèmes de compatibilité XLL dans les différentes versions de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="00c00-106">This topic addresses issues of XLL compatibility in different versions of Microsoft Excel.</span></span>
  
## <a name="useful-constant-definitions"></a><span data-ttu-id="00c00-107">Définitions des constantes utiles</span><span class="sxs-lookup"><span data-stu-id="00c00-107">Useful constant definitions</span></span>

<span data-ttu-id="00c00-108">EnVisagez d'inclure des définitions similaires à celles-ci dans votre code de projet XLL et de remplacer toutes les instances de nombres littéraux utilisés dans ce contexte.</span><span class="sxs-lookup"><span data-stu-id="00c00-108">Consider including definitions similar to these in your XLL project code and replacing all instances of literal numbers used in this context.</span></span> <span data-ttu-id="00c00-109">Cela permet de clarifier le code dont la version est propre et de réduire les risques de bogues liés à la version sous la forme de numéros inoffensifs.</span><span class="sxs-lookup"><span data-stu-id="00c00-109">This will clarify code that is version specific, and reduce the likelihood of version-related bugs in the form of innocuous-looking numbers.</span></span>
  
```cpp
#define MAX_XL11_ROWS            65536
#define MAX_XL11_COLS              256
#define MAX_XL12_ROWS          1048576
#define MAX_XL12_COLS            16384
#define MAX_XL11_UDF_ARGS           30
#define MAX_XL12_UDF_ARGS          255
#define MAX_XL4_STR_LEN           255u
#define MAX_XL12_STR_LEN        32767u
```

## <a name="getting-the-running-version"></a><span data-ttu-id="00c00-110">Obtention de la version en cours d'exécution</span><span class="sxs-lookup"><span data-stu-id="00c00-110">Getting the running version</span></span>

<span data-ttu-id="00c00-111">Vous devez détecter quelle version est en cours `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`d'exécution `arg` à l'aide de, où est un **XLOPER** numérique défini sur 2 et version est une chaîne **XLOPER** qui peut ensuite être forcée sur un entier.</span><span class="sxs-lookup"><span data-stu-id="00c00-111">You should detect which version is running using  `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, where  `arg` is a numeric **XLOPER** set to 2 and version is a string **XLOPER** which can then be coerced to an integer.</span></span> <span data-ttu-id="00c00-112">Pour Microsoft Excel 2013, il s'agit de 15,0.</span><span class="sxs-lookup"><span data-stu-id="00c00-112">For Microsoft Excel 2013, this is 15.0.</span></span> <span data-ttu-id="00c00-113">Vous devez effectuer cette opération dans, ou à partir de, la fonction [xlAutoOpen](xlautoopen.md) .</span><span class="sxs-lookup"><span data-stu-id="00c00-113">You should do this in, or from, the [xlAutoOpen](xlautoopen.md) function.</span></span> <span data-ttu-id="00c00-114">Vous pouvez ensuite définir une variable globale qui informe tous les modules de votre projet de la version d'Excel qui est en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="00c00-114">You can then set a global variable that informs all of the modules in your project which version of Excel is running.</span></span> <span data-ttu-id="00c00-115">Votre code peut ensuite décider s'il faut appeler l'API C à l'aide de **Excel12** et de **XLOPER12**, ou en utilisant **Excel4** à l'aide de **XLOPER**s.</span><span class="sxs-lookup"><span data-stu-id="00c00-115">Your code can then decide whether to call the C API using **Excel12** and **XLOPER12**s, or using **Excel4** using **XLOPER**s.</span></span>
  
<span data-ttu-id="00c00-116">Vous pouvez appeler **XLCallVer** pour découvrir la version de l'API C, mais cela n'indique pas laquelle des versions antérieures d'Excel 2007 sont en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="00c00-116">You can call **XLCallVer** to discover the C API version, but this does not indicate which of the pre-Excel 2007 versions you are running.</span></span> 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a><span data-ttu-id="00c00-117">Création de compléments qui exportent des interfaces doubles</span><span class="sxs-lookup"><span data-stu-id="00c00-117">Creating add-ins that export dual interfaces</span></span>

<span data-ttu-id="00c00-118">Considérez une fonction XLL qui prend une chaîne et renvoie une valeur qui peut être n'importe quel type de données de feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="00c00-118">Consider an XLL function that takes a string and returns a value that can be any of the worksheet data types.</span></span> <span data-ttu-id="00c00-119">Vous pouvez exporter une fonction inscrite en tant que type «lib» et prototypée comme suit lorsque la chaîne est transmise sous la forme d'une chaîne d'octets de longueur comptée.</span><span class="sxs-lookup"><span data-stu-id="00c00-119">You could export a function registered as type "PD" and prototyped as follows where the string is passed as a length-counted byte string.</span></span>
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
<span data-ttu-id="00c00-120">Bien que cela fonctionne parfaitement bien, il existe plusieurs raisons pour lesquelles il ne s'agit pas de l'interface idéale pour votre code en commençant dans Excel 2007:</span><span class="sxs-lookup"><span data-stu-id="00c00-120">Although this works perfectly well, there are several reasons why this is not the ideal interface to your code starting in Excel 2007:</span></span>
  
- <span data-ttu-id="00c00-121">Elle est soumise aux limitations des chaînes d'octets de l'API C et ne peut pas accéder aux chaînes Unicode longues prises en charge à partir d'Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="00c00-121">It is subject to the limitations of C API byte strings and cannot access the long Unicode strings supported starting in Excel 2007.</span></span>
    
- <span data-ttu-id="00c00-122">Bien que, en commençant dans Excel 2007, Excel puisse transmettre et accepter des éléments **XLOPER**, en interne, il les convertit en éléments **XLOPER12**, de sorte qu'il existe une charge de conversion implicite en commençant par Excel 2007, lorsque le code s'exécute dans les versions antérieures d'Excel.</span><span class="sxs-lookup"><span data-stu-id="00c00-122">Although, starting in Excel 2007, Excel can pass and accept **XLOPER**s, internally it converts them to **XLOPER12**s, so there is an implicit conversion overhead starting in Excel 2007 that is not there when the code runs in earlier versions of Excel.</span></span>
    
- <span data-ttu-id="00c00-123">Cette fonction peut être rendue thread-safe, mais si la chaîne de `PD$`type est changée en, l'inscription échoue avant Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="00c00-123">It may be that this function can be made thread safe, but if the type string is changed to  `PD$`, registration fails in starting before Excel 2007.</span></span>
    
<span data-ttu-id="00c00-124">Pour ces raisons, dans l'idéal, en commençant dans Excel 2007, vous devez exporter une fonction pour les utilisateurs `QD%$`qui ont été enregistrés sous, en supposant que votre code est thread-safe et prototypée comme suit.</span><span class="sxs-lookup"><span data-stu-id="00c00-124">For these reasons, ideally, starting in Excel 2007 you should export a function for your users that was registered as  `QD%$`, assuming your code is thread safe and prototyped as follows.</span></span>
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
<span data-ttu-id="00c00-125">Une autre raison pour laquelle vous pouvez souhaiter enregistrer une fonction différente en commençant dans Excel 2007 est qu'elle permet aux fonctions XLL de prendre jusqu'à 255 arguments au lieu de la limite de 30 versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="00c00-125">Another reason why you might want to register a different function starting in Excel 2007 is that it permits XLL functions to take up to 255 arguments, instead of the 30 limit of earlier versions.</span></span>
  
<span data-ttu-id="00c00-126">Heureusement, vous pouvez bénéficier des avantages des deux en exportant les deux versions de votre projet.</span><span class="sxs-lookup"><span data-stu-id="00c00-126">Fortunately, you can have the benefits of both by exporting both versions from your project.</span></span> <span data-ttu-id="00c00-127">Vous pouvez ensuite détecter la version Excel en cours d'exécution et enregistrer de façon conditionnelle la fonction la plus appropriée.</span><span class="sxs-lookup"><span data-stu-id="00c00-127">You can then detect the running Excel version and conditionally register the most appropriate function.</span></span> <span data-ttu-id="00c00-128">Pour plus d'informations et pour obtenir un exemple d'implémentation, voir [developIng Add-ins (XLL) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).</span><span class="sxs-lookup"><span data-stu-id="00c00-128">For more information and an example implementation, see [Developing Add-ins (XLLs) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).</span></span>
  
<span data-ttu-id="00c00-129">Cette approche entraîne la possibilité qu'une feuille de calcul exécutée dans Excel 2003 puisse afficher des résultats différents de ceux de la même feuille en cours d'exécution dans Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="00c00-129">This approach leads to the possibility that a worksheet running in Excel 2003 could display different results than the same sheet running starting in Excel 2007.</span></span> <span data-ttu-id="00c00-130">Par exemple, Excel 2003 mappe une chaîne Unicode dans une cellule de feuille de calcul Excel 2003 à une chaîne ASCII Byte et la tronque avant de la transmettre à une fonction XLL.</span><span class="sxs-lookup"><span data-stu-id="00c00-130">For example, Excel 2003 would map a Unicode string in an Excel 2003 worksheet cell to an ASCII byte-string and truncate it before passing it to an XLL function.</span></span> <span data-ttu-id="00c00-131">À partir d'Excel 2007, Excel transmet une chaîne Unicode non convertie à une fonction XLL inscrite de la manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="00c00-131">Starting in Excel 2007, Excel will pass an unconverted Unicode string to an XLL function registered in the right way.</span></span> <span data-ttu-id="00c00-132">Cela peut entraîner un résultat différent.</span><span class="sxs-lookup"><span data-stu-id="00c00-132">This could lead to a different result.</span></span> <span data-ttu-id="00c00-133">Vous devez être conscient de cette possibilité et des conséquences pour vos utilisateurs, pas seulement dans la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="00c00-133">You should be aware of this possibility and the consequences to your users, not just in the upgrade.</span></span> <span data-ttu-id="00c00-134">Par exemple, certaines fonctions numériques intégrées ont été améliorées entre Excel 2000 et Excel 2003.</span><span class="sxs-lookup"><span data-stu-id="00c00-134">For example, some built-in numeric functions were improved between Excel 2000 and Excel 2003.</span></span>
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a><span data-ttu-id="00c00-135">Nouvelles fonctions de feuille de calcul et fonctions de l'utilitaire d'analyse</span><span class="sxs-lookup"><span data-stu-id="00c00-135">New Worksheet functions and Analysis Toolpak functions</span></span>

<span data-ttu-id="00c00-136">Les fonctions de l'utilitaire d'analyse (ATP) font partie d'Excel en commençant dans Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="00c00-136">Analysis Toolpak (ATP) functions are part of Excel starting in Excel 2007.</span></span> <span data-ttu-id="00c00-137">Auparavant, un XLL pouvait uniquement appeler une fonction ATP à l'aide de [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="00c00-137">Previously, an XLL could only call an ATP function by using [xlUDF](xludf.md).</span></span> <span data-ttu-id="00c00-138">À partir d'Excel 2007, les fonctions ATP doivent être appelées à l'aide des énumérations de fonction définies dans xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="00c00-138">Starting in Excel 2007, the ATP functions should be called using the function enumerations defined in xlcall.h.</span></span> <span data-ttu-id="00c00-139">L'exemple dans l'appel de fonctions définies par l'utilisateur à partir de dll illustre les deux méthodes.</span><span class="sxs-lookup"><span data-stu-id="00c00-139">The example in Calling User-defined Functions from DLLs demonstrates the two different methods.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="00c00-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00c00-140">See also</span></span>

- [<span data-ttu-id="00c00-141">Les fonctions de rappel de l'API C Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="00c00-141">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md) 
- [<span data-ttu-id="00c00-142">Programmation avec l�API�C dans Excel</span><span class="sxs-lookup"><span data-stu-id="00c00-142">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
- [<span data-ttu-id="00c00-143">Quelles sont les nouveaut�s de l'API C pour Excel 2013</span><span class="sxs-lookup"><span data-stu-id="00c00-143">What's New in the C API for Excel</span></span>](what-s-new-in-the-c-api-for-excel.md)

