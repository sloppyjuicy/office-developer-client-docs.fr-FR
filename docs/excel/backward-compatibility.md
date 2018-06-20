---
title: Compatibilité descendante
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compatibilité des versions [excel 2007], compatibilité XLL [Excel 2007], [Excel 2007] de compatibilité descendante
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 095961fa909a67b354ed43a7e093b79a9ebb4f18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782017"
---
# <a name="backward-compatibility"></a><span data-ttu-id="23f41-104">Compatibilité descendante</span><span class="sxs-lookup"><span data-stu-id="23f41-104">Backward compatibility</span></span>

<span data-ttu-id="23f41-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="23f41-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="23f41-106">Cette rubrique traite des problèmes de compatibilité XLL dans différentes versions de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="23f41-106">This topic addresses issues of XLL compatibility in different versions of Microsoft Excel.</span></span>
  
## <a name="useful-constant-definitions"></a><span data-ttu-id="23f41-107">Définitions utiles</span><span class="sxs-lookup"><span data-stu-id="23f41-107">Useful constant definitions</span></span>

<span data-ttu-id="23f41-108">Envisager d’inclure des définitions similaires à celles-ci dans le code de votre projet XLL et remplacer toutes les instances de valeurs littérales utilisées dans ce contexte.</span><span class="sxs-lookup"><span data-stu-id="23f41-108">Consider including definitions similar to these in your XLL project code and replacing all instances of literal numbers used in this context.</span></span> <span data-ttu-id="23f41-109">Cela clarifier le code qui est la version spécifique et réduire les risques de bogues version sous la forme de nombres inoffensive.</span><span class="sxs-lookup"><span data-stu-id="23f41-109">This will clarify code that is version specific, and reduce the likelihood of version-related bugs in the form of innocuous-looking numbers.</span></span>
  
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

## <a name="getting-the-running-version"></a><span data-ttu-id="23f41-110">Obtention de la version en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="23f41-110">Getting the running version</span></span>

<span data-ttu-id="23f41-111">Vous devez détecter la version est en cours d’exécution à l’aide de `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, où `arg` numérique **XLOPER** la valeur 2 et la version est une chaîne **XLOPER** qui peut ensuite être converti en entier.</span><span class="sxs-lookup"><span data-stu-id="23f41-111">You should detect which version is running using  `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, where  `arg` is a numeric **XLOPER** set to 2 and version is a string **XLOPER** which can then be coerced to an integer.</span></span> <span data-ttu-id="23f41-112">Pour Microsoft Excel 2013, il s’agit 15.0.</span><span class="sxs-lookup"><span data-stu-id="23f41-112">For Microsoft Excel 2013, this is 15.0.</span></span> <span data-ttu-id="23f41-113">Vous devez procéder dans, ou à partir de la fonction [xlAutoOpen](xlautoopen.md) .</span><span class="sxs-lookup"><span data-stu-id="23f41-113">You should do this in, or from, the [xlAutoOpen](xlautoopen.md) function.</span></span> <span data-ttu-id="23f41-114">Vous pouvez ensuite définir une variable globale qui informe tous les modules dans votre projet de la version d’Excel est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="23f41-114">You can then set a global variable that informs all of the modules in your project which version of Excel is running.</span></span> <span data-ttu-id="23f41-115">Votre code peut ensuite décider s’il faut appeler l’API C en utilisant **Excel12** et **XLOPER12**s, ou **Excel4** à l’aide de s **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="23f41-115">Your code can then decide whether to call the C API using **Excel12** and **XLOPER12**s, or using **Excel4** using **XLOPER**s.</span></span>
  
<span data-ttu-id="23f41-116">Vous pouvez appeler **XLCallVer** pour découvrir la version de l’API C, mais cela n’indique pas les versions à Excel 2007 vous sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="23f41-116">You can call **XLCallVer** to discover the C API version, but this does not indicate which of the pre-Excel 2007 versions you are running.</span></span> 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a><span data-ttu-id="23f41-117">Création de compléments exportant des interfaces doubles</span><span class="sxs-lookup"><span data-stu-id="23f41-117">Creating add-ins that export dual interfaces</span></span>

<span data-ttu-id="23f41-118">Envisagez une fonction XLL qui accepte une chaîne et renvoie une valeur qui peut être un des types de données de feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="23f41-118">Consider an XLL function that takes a string and returns a value that can be any of the worksheet data types.</span></span> <span data-ttu-id="23f41-119">Vous pouvez exporter une fonction inscrit comme tapez « PD » et prototyper comme suit où la chaîne est transmise comme une chaîne d’octets.</span><span class="sxs-lookup"><span data-stu-id="23f41-119">You could export a function registered as type "PD" and prototyped as follows where the string is passed as a length-counted byte string.</span></span>
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
<span data-ttu-id="23f41-120">Bien que ce scénario fonctionne parfaitement, il existe plusieurs raisons pour lesquelles ce n’est pas l’interface idéale à votre code à compter d’Excel 2007 :</span><span class="sxs-lookup"><span data-stu-id="23f41-120">Although this works perfectly well, there are several reasons why this is not the ideal interface to your code starting in Excel 2007:</span></span>
  
- <span data-ttu-id="23f41-121">Il est soumis aux limitations de chaînes d’octets API C et ne peut pas accéder aux longues chaînes Unicode pris en charge à compter d’Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="23f41-121">It is subject to the limitations of C API byte strings and cannot access the long Unicode strings supported starting in Excel 2007.</span></span>
    
- <span data-ttu-id="23f41-122">Bien que, à compter d’Excel 2007, Excel peut passer et accepter **XLOPER**s, en interne il les convertit en **XLOPER12**s, donc il existe une surcharge de conversion implicite à compter d’Excel 2007 qui n’est pas il lorsque le code s’exécute dans les versions antérieures d’Excel.</span><span class="sxs-lookup"><span data-stu-id="23f41-122">Although, starting in Excel 2007, Excel can pass and accept **XLOPER**s, internally it converts them to **XLOPER12**s, so there is an implicit conversion overhead starting in Excel 2007 that is not there when the code runs in earlier versions of Excel.</span></span>
    
- <span data-ttu-id="23f41-123">Il peut s’avérer que cette fonction peut être rendue thread-safe, mais si la chaîne type est remplacée par `PD$`, l’enregistrement échoue lors du démarrage avant d’Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="23f41-123">It may be that this function can be made thread safe, but if the type string is changed to  `PD$`, registration fails in starting before Excel 2007.</span></span>
    
<span data-ttu-id="23f41-124">Pour ces raisons, dans l’idéal, compter d’Excel 2007, vous devez exporter une fonction pour vos utilisateurs qui a été enregistré en tant que `QD%$`, en supposant que votre code est thread-safe et prototyper comme suit.</span><span class="sxs-lookup"><span data-stu-id="23f41-124">For these reasons, ideally, starting in Excel 2007 you should export a function for your users that was registered as  `QD%$`, assuming your code is thread safe and prototyped as follows.</span></span>
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
<span data-ttu-id="23f41-125">Une autre raison pourquoi vous souhaiterez peut-être enregistrer une autre fonction à compter d’Excel 2007 est afin de permettre aux fonctions XLL d’accepter jusqu'à 255 arguments, au lieu de la limite des versions antérieures de 30.</span><span class="sxs-lookup"><span data-stu-id="23f41-125">Another reason why you might want to register a different function starting in Excel 2007 is that it permits XLL functions to take up to 255 arguments, instead of the 30 limit of earlier versions.</span></span>
  
<span data-ttu-id="23f41-126">Heureusement, vous pouvez avoir les avantages des deux en exportant les deux versions de votre projet.</span><span class="sxs-lookup"><span data-stu-id="23f41-126">Fortunately, you can have the benefits of both by exporting both versions from your project.</span></span> <span data-ttu-id="23f41-127">Vous pouvez ensuite détecter la version d’Excel en cours d’exécution et conditionnellement enregistrer la fonction la plus appropriée.</span><span class="sxs-lookup"><span data-stu-id="23f41-127">You can then detect the running Excel version and conditionally register the most appropriate function.</span></span> <span data-ttu-id="23f41-128">Pour plus d’informations et un exemple d’implémentation, voir [Developing compléments (XLL) dans Excel 2007](http://msdn.microsoft.com/en-us/library/aa730920.aspx).</span><span class="sxs-lookup"><span data-stu-id="23f41-128">For more information and an example implementation, see [Developing Add-ins (XLLs) in Excel 2007](http://msdn.microsoft.com/en-us/library/aa730920.aspx).</span></span>
  
<span data-ttu-id="23f41-129">Cette approche la possibilité qu’une feuille de calcul en cours d’exécution dans Excel 2003 peut afficher des résultats différents de la même feuille en cours d’exécution à compter d’Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="23f41-129">This approach leads to the possibility that a worksheet running in Excel 2003 could display different results than the same sheet running starting in Excel 2007.</span></span> <span data-ttu-id="23f41-130">Par exemple, Microsoft Excel 2003 souhaite mapper une chaîne Unicode dans une cellule de feuille de calcul Excel 2003 à une chaîne d’octets ASCII, tronqué avant de passer à une fonction XLL.</span><span class="sxs-lookup"><span data-stu-id="23f41-130">For example, Excel 2003 would map a Unicode string in an Excel 2003 worksheet cell to an ASCII byte-string and truncate it before passing it to an XLL function.</span></span> <span data-ttu-id="23f41-131">À compter d’Excel 2007, Excel passe une chaîne Unicode non convertie à une fonction XLL inscrite dans la bonne manière.</span><span class="sxs-lookup"><span data-stu-id="23f41-131">Starting in Excel 2007, Excel will pass an unconverted Unicode string to an XLL function registered in the right way.</span></span> <span data-ttu-id="23f41-132">Cela peut entraîner un résultat différent.</span><span class="sxs-lookup"><span data-stu-id="23f41-132">This could lead to a different result.</span></span> <span data-ttu-id="23f41-133">Vous devez être conscient de cette possibilité et les conséquences de vos utilisateurs, pas seulement dans la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="23f41-133">You should be aware of this possibility and the consequences to your users, not just in the upgrade.</span></span> <span data-ttu-id="23f41-134">Par exemple, certaines fonctions numériques intégrées ont été améliorées entre Excel 2000 et Excel 2003.</span><span class="sxs-lookup"><span data-stu-id="23f41-134">For example, some built-in numeric functions were improved between Excel 2000 and Excel 2003.</span></span>
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a><span data-ttu-id="23f41-135">Nouvelles fonctions de feuille de calcul et des fonctions de l’utilitaire d’analyse</span><span class="sxs-lookup"><span data-stu-id="23f41-135">New Worksheet functions and Analysis Toolpak functions</span></span>

<span data-ttu-id="23f41-136">Fonctions utilitaire d’analyse font partie d’Excel à compter d’Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="23f41-136">Analysis Toolpak (ATP) functions are part of Excel starting in Excel 2007.</span></span> <span data-ttu-id="23f41-137">Auparavant, un XLL pouvait appeler uniquement une fonction DAV à l’aide de [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="23f41-137">Previously, an XLL could only call an ATP function by using [xlUDF](xludf.md).</span></span> <span data-ttu-id="23f41-138">À compter d’Excel 2007, les fonctions DAV doivent être appelées à l’aide les énumérations de fonction définies dans xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="23f41-138">Starting in Excel 2007, the ATP functions should be called using the function enumerations defined in xlcall.h.</span></span> <span data-ttu-id="23f41-139">L’exemple de fonctions définies par l’utilisateur de l’appel à partir de DLL montre les deux méthodes différentes.</span><span class="sxs-lookup"><span data-stu-id="23f41-139">The example in Calling User-defined Functions from DLLs demonstrates the two different methods.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="23f41-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23f41-140">See also</span></span>

- [<span data-ttu-id="23f41-141">Les fonctions de rappel de l'API C Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="23f41-141">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md) 
- [<span data-ttu-id="23f41-142">Programmation avec l�API�C dans Excel</span><span class="sxs-lookup"><span data-stu-id="23f41-142">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
- [<span data-ttu-id="23f41-143">Quelles sont les nouveaut�s de l'API C pour Excel 2013</span><span class="sxs-lookup"><span data-stu-id="23f41-143">What's New in the C API for Excel</span></span>](what-s-new-in-the-c-api-for-excel.md)

