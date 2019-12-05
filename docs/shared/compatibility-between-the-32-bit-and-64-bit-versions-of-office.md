---
title: Compatibilité entre les versions 32 bits et 64 bits d’Office
ms.date: 12/03/2019
ms.audience: ITPro
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Découvrez en quoi la version 32 bits d’Office est compatible avec la version 64 bits d’Office.
localization_priority: Priority
ms.openlocfilehash: a0accc9c4b0198ab18b999353762a016d52f6b39
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819252"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a><span data-ttu-id="a2b0d-103">Compatibilité entre les versions 32 bits et 64 bits d’Office</span><span class="sxs-lookup"><span data-stu-id="a2b0d-103">Compatibility between the 32-bit and 64-bit versions of Office</span></span>

<span data-ttu-id="a2b0d-104">Découvrez en quoi la version 32 bits d’Office est compatible avec la version 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-104">Find out how the 32-bit version of Office is compatible with the 64-bit version of Office.</span></span>
  
<span data-ttu-id="a2b0d-105">Les applications Office sont disponibles en versions 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-105">Office applications are available in 32-bit and 64-bit versions.</span></span> 
  
<span data-ttu-id="a2b0d-106">Les versions 64 bits d’Office vous permettent de déplacer davantage de données pour une fonctionnalité accrue, par exemple lorsque vous utilisez de grands nombres dans Microsoft Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-106">The 64-bit versions of Office enable you to move more data around for increased capability, for example when you work with large numbers in Microsoft Excel 2010.</span></span> <span data-ttu-id="a2b0d-107">Lorsque vous rédigez du code 32 bits, vous pouvez utiliser la version 64 bits d’Office sans apporter de modifications.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-107">When writing 32-bit code, you can use the 64-bit version of Office without any changes.</span></span> <span data-ttu-id="a2b0d-108">Toutefois, lorsque vous écrivez du code 64 bits, vous devez vérifier que votre code contient des mots-clés spécifiques et des constantes de compilation conditionnelle pour vous assurer que le code est compatible avec la version antérieure d’Office et que le code correct est en cours d’exécution si vous mélangez du code 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-108">However, when you write 64-bit code, you should ensure that your code contains specific keywords and conditional compilation constants to ensure that the code is backward compatible with earlier version of Office, and that the correct code is being executed if you mix 32-bit and 64-bit code.</span></span>
  
<span data-ttu-id="a2b0d-109">L’implémentation Visual Basic pour Applications 7.0 (VBA 7) est publiée dans les versions 64 bits d’Office, mais elle fonctionne avec les applications 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-109">Visual Basic for Applications 7.0 (VBA 7) is released in the 64-bit versions for Office, and it works with both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="a2b0d-110">Les modifications décrites dans cet article s’appliquent uniquement aux versions 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-110">The changes described in this article apply only to the 64-bit versions of Office.</span></span> <span data-ttu-id="a2b0d-111">Utiliser les versions 32 bits de Microsoft Office vous permet d’exploiter les solutions intégrées dans les versions précédentes d’Office sans apporter d’autres modifications.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-111">Using the 32-bit versions of Microsoft Office enable you to use solutions built in previous versions of Office without further modifications.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a2b0d-112">Par défaut, lorsque vous installez une version 64 bits d’Office, vous installez également la version 32 bits, ainsi que le système 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-112">By default, when you install a 64-bit version of Office, you also install the 32-bit version is installed along with the 64-bit system.</span></span> <span data-ttu-id="a2b0d-113">Vous devez explicitement sélectionner l’option d’installation de la version 64 bits de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-113">You must explicitly select the Microsoft Office 64-bit version installation option.</span></span> 
  
<span data-ttu-id="a2b0d-114">Dans VBA 7, vous devez mettre à jour les instructions API Windows existantes (instructions **Declare**) pour qu’elles fonctionnent avec la version 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-114">In VBA 7, you must update existing Windows API statements (**Declare** statements) to work with the 64-bit version.</span></span> <span data-ttu-id="a2b0d-115">De plus, vous devez mettre à jour les pointeurs d’adresse et afficher les handles de fenêtre dans les types définis par l’utilisateur utilisés par ces instructions.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-115">Additionally, you must update address pointers and display window handles in user-defined types that are used by these statements.</span></span> <span data-ttu-id="a2b0d-116">Ces questions sont abordées plus en détail dans cet article, ainsi que les problèmes de compatibilité entre les versions 32 bits et 64 bits et les solutions suggérées.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-116">This is discussed in more detail in this article as well as compatibility issues between the 32-bit and 64-bit versions and suggested solutions.</span></span> 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a><span data-ttu-id="a2b0d-117">Comparer des systèmes 32 bits et 64 bits</span><span class="sxs-lookup"><span data-stu-id="a2b0d-117">Comparing 32-bit and 64-bit systems</span></span>
<span data-ttu-id="a2b0d-118"><a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a></span><span class="sxs-lookup"><span data-stu-id="a2b0d-118"><a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a></span></span>

<span data-ttu-id="a2b0d-119">Les applications créées avec les versions 64 bits d’Office peuvent faire référence à de plus grands espaces d’adressage que ceux des versions 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-119">Applications built with the 64-bit versions of Office can reference larger address spaces than 32-bit versions.</span></span> <span data-ttu-id="a2b0d-120">Cela signifie que vous pouvez utiliser davantage de mémoire physique pour les données qu’auparavant, permettant éventuellement de réduire la charge liée aux transferts incessants de données sur une mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-120">This means you can use more physical memory for data than before, potentially reducing the overhead spent moving data in and out of physical memory</span></span>
  
<span data-ttu-id="a2b0d-121">En plus de faire référence à des emplacements spécifiques (ou pointeurs) dans la mémoire physique, vous pouvez également utiliser des adresses pour référencer des identificateurs de fenêtre d’affichage (ou handles).</span><span class="sxs-lookup"><span data-stu-id="a2b0d-121">In addition to referring specific locations (known as pointers) in physical memory, you can also use addresses to reference display window identifiers (known as handles).</span></span> <span data-ttu-id="a2b0d-122">La taille (en octets) du pointeur ou handle varie selon que vous utilisez un système 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-122">The size (in bytes) of the pointer or handle depends on whether you're using a 32-bit or 64-bit system.</span></span> 
  
<span data-ttu-id="a2b0d-123">Si vous voulez exécuter vos solutions existantes avec les versions 64 bits d’Office, tenez compte des points suivants :</span><span class="sxs-lookup"><span data-stu-id="a2b0d-123">If you want to run your existing solutions with the 64-bit versions of Office, be aware of the following:</span></span>
  
- <span data-ttu-id="a2b0d-124">Les processus 64 bits natifs d’Office ne peuvent pas charger les fichiers binaires 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-124">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="a2b0d-125">Il s’agit d’un problème courant lorsque vous avez des contrôles ActiveX Microsoft existants et des compléments existants.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-125">This is expected to be a common issue when you have existing Microsoft ActiveX controls and existing add-ins.</span></span>
    
- <span data-ttu-id="a2b0d-126">Auparavant, VBA ne disposait pas de type de données de pointeur. Vous deviez utiliser des variables 32 bits pour stocker les pointeurs et les handles.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-126">VBA previously didn't have a pointer data type, so you had to use 32-bit variables to store pointers and handles.</span></span> <span data-ttu-id="a2b0d-127">Ces variables tronquent désormais les valeurs 64 bits renvoyées par les appels d’API lors de l’utilisation des instructions **Declare**.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-127">These variables now truncate 64-bit values returned by API calls when using **Declare** statements.</span></span> 
    
## <a name="vba-7-code-base"></a><span data-ttu-id="a2b0d-128">Base de code VBA 7</span><span class="sxs-lookup"><span data-stu-id="a2b0d-128">VBA 7 code base</span></span>
<span data-ttu-id="a2b0d-129"><a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a></span><span class="sxs-lookup"><span data-stu-id="a2b0d-129"><a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a></span></span>

<span data-ttu-id="a2b0d-130">VBA 7 remplace la base de code VBA Office 2007 et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-130">VBA 7 replaces the VBA code base in Office 2007 and earlier versions.</span></span> <span data-ttu-id="a2b0d-131">Cette implémentation est disponible dans les versions 32 bits et 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-131">VBA 7 is available in both the 32-bit and 64-bit versions of Office.</span></span> <span data-ttu-id="a2b0d-132">Elle fournit deux constantes de compilation conditionnelle :</span><span class="sxs-lookup"><span data-stu-id="a2b0d-132">It provides two conditional compilation constants:</span></span> 
  
- <span data-ttu-id="a2b0d-133">**VBA7** : permet de garantir la compatibilité descendante de votre code en testant si votre application utilise VBA 7 ou la version antérieure de VBA.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-133">**VBA7** - Helps ensure the backward compatibility of your code by testing whether your application is using VBA 7 or the previous version of VBA.</span></span> 
    
- <span data-ttu-id="a2b0d-134">**Win64** : teste si le code est en cours d’exécution au format 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-134">**Win64** Tests whether code is running as 32-bit or 64-bit.</span></span> 
    
<span data-ttu-id="a2b0d-135">À quelques exceptions près, les macros d’un document qui fonctionnent dans la version 32 bits de l’application fonctionnent également dans la version 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-135">With certain exceptions, the macros in a document that work in the 32-bit version of the application also work in the 64-bit version.</span></span>
  
## <a name="activex-control-and-com-add-in-compatibility"></a><span data-ttu-id="a2b0d-136">Compatibilité des contrôles ActiveX et des compléments COM</span><span class="sxs-lookup"><span data-stu-id="a2b0d-136">ActiveX control and COM add-in compatibility</span></span>
<span data-ttu-id="a2b0d-137"><a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="a2b0d-137"><a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a></span></span>

<span data-ttu-id="a2b0d-138">Les contrôles ActiveX de 32 bits existants ne sont pas compatibles avec les versions 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-138">Existing 32-bit ActiveX controls, are not compatible with the 64-bit versions of Office.</span></span> <span data-ttu-id="a2b0d-139">Pour les contrôles ActiveX et les objets COM :</span><span class="sxs-lookup"><span data-stu-id="a2b0d-139">For ActiveX controls and COM objects:</span></span>
  
- <span data-ttu-id="a2b0d-140">Si vous disposez du code source, vous pouvez générer une version 64 bits vous-même.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-140">If you have the source code, generate a 64-bit version yourself.</span></span>
- <span data-ttu-id="a2b0d-141">Si vous n’avez pas le code source, contactez le fournisseur pour obtenir une version mise à jour.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-141">If you don't have the source code, contact the vendor for an updated version.</span></span>
    
<span data-ttu-id="a2b0d-142">Les processus 64 bits natifs d’Office ne peuvent pas charger les fichiers binaires 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-142">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="a2b0d-143">Cela inclut les contrôles communs de **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) et les contrôles de **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar).</span><span class="sxs-lookup"><span data-stu-id="a2b0d-143">This includes the common controls of **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) and the controls of **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar).</span></span> <span data-ttu-id="a2b0d-144">Ces contrôles ont été installés par les versions 32 bits d’Office antérieures à Office 2010.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-144">These controls were installed by 32-bit versions of Office earlier than Office 2010.</span></span> <span data-ttu-id="a2b0d-145">Lorsque vous migrez le code vers les versions 64 bits d’Office, vous devez trouver une alternative pour vos solutions VBA existantes qui utilisent ces contrôles.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-145">You'll need to find an alternative for your existing VBA solutions that use these controls when you migrate the code to the 64-bit versions of Office.</span></span> 
  
## <a name="api-compatibility"></a><span data-ttu-id="a2b0d-146">Compatibilité de l’API</span><span class="sxs-lookup"><span data-stu-id="a2b0d-146">API compatibility</span></span>
<span data-ttu-id="a2b0d-147"><a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="a2b0d-147"><a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a></span></span>

<span data-ttu-id="a2b0d-148">L’association de VBA et de bibliothèques de types vous offre de nombreuses fonctionnalités utiles pour créer des applications Office.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-148">The combination of VBA and type libraries gives you lots of functionality to create Office applications.</span></span> <span data-ttu-id="a2b0d-149">Cependant, vous devez parfois communiquer directement avec le système d’exploitation et d’autres composants de l’ordinateur, par exemple lorsque vous gérez la mémoire ou des processus, lorsque vous travaillez avec des éléments d’interface utilisateur comme des fenêtres et des contrôles ou lorsque vous modifiez le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-149">However, sometimes you must communicate directly with the computer's operating system and other components, such as when you manage memory or processes, when working with UI elements linke windows and controls, or when modifying the Windows registry.</span></span> <span data-ttu-id="a2b0d-150">Dans ces scénarios, votre meilleure option consiste à utiliser l’une des fonctions externes incorporées dans les fichiers DLL.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-150">In these scenarios, your best option is to use one of the external functions that are embedded in DLL files.</span></span> <span data-ttu-id="a2b0d-151">Vous pouvez le faire dans VBA en passant des appels d’API à l’aide des instructions **Declare**.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-151">You do this in VBA by making API calls using **Declare** statements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a2b0d-152">Microsoft fournit le fichier Win32API.txt qui contient 1 500 instructions Declare et un outil permettant de copier l’instruction **Declare** que vous souhaitez dans votre code.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-152">Microsoft provides a Win32API.txt file that contains 1,500 Declare statements and a tool to copy the **Declare** statement that you want into your code.</span></span> <span data-ttu-id="a2b0d-153">Cependant, ces instructions s’appliquent aux systèmes 32 bits et doivent être converties en 64 bits à l’aide des informations indiquées plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-153">However, these statements are for 32-bit systems and must be converted to 64-bit by using the information discussed later in this article.</span></span> <span data-ttu-id="a2b0d-154">Les instructions **Declare** existantes ne seront pas compilées dans VBA 64 bits avant d’avoir été indiquées comme fiables pour 64 bits à l’aide de l’attribut **PtrSafe**.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-154">Existing **Declare** statements won't compile in 64-bit VBA until they've been marked as safe for 64-bit by using the **PtrSafe** attribute.</span></span> <span data-ttu-id="a2b0d-155">Vous trouverez des exemples de ce type de conversion sur le site web de Jan Karel Pieterse, Excel MVP à l’adresse suivante [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp).</span><span class="sxs-lookup"><span data-stu-id="a2b0d-155">You can find examples of this type of conversion at Excel MVP Jan Karel Pieterse's website at [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp).</span></span> <span data-ttu-id="a2b0d-156">Le [guide d’utilisateur de l’inspecteur de compatibilité du code Office](https://docs.microsoft.com/previous-versions/office/office-2010/ee833946(v=office.14)) est un outil particulièrement utile pour examiner la syntaxe des instructions API **Declare** pour l’attribut **PtrSafe**, le cas échéant, et le type de renvoi approprié.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-156">The [Office Code Compatibility Inspector user's guide](https://docs.microsoft.com/previous-versions/office/office-2010/ee833946(v=office.14)) is a useful tool to inspect the syntax of API **Declare** statements for the **PtrSafe** attribute, if needed, and the appropriate return type.</span></span> 
  
<span data-ttu-id="a2b0d-157">Les instructions **Declare** ressemblent à ce qui suit, selon que vous appelez une sous-routine (qui n’a aucune valeur de retour) ou une fonction (qui a une valeur de retour).</span><span class="sxs-lookup"><span data-stu-id="a2b0d-157">**Declare** statements resemble one of the following, depending on whether you are calling a subroutine (which has no return value) or a function (which does have a return value).</span></span> 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

<span data-ttu-id="a2b0d-158">La fonction **SubName** ou **FunctionName** est remplacée par le vrai nom de la procédure décrite dans le fichier DLL et correspond au nom utilisé lorsque la procédure est appelée à partir du code VBA.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-158">The **SubName** function or **FunctionName** function is replaced by the actual name of the procedure in the DLL file and represents the name that is used when the procedure is called from VBA code.</span></span> <span data-ttu-id="a2b0d-159">Vous pouvez également spécifier un argument **AliasName** pour le nom de la procédure.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-159">You can also specify an **AliasName** argument for the name of the procedure.</span></span> <span data-ttu-id="a2b0d-160">Le nom du fichier DLL qui contient la procédure appelée suit le mot-clé **Lib**.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-160">The name of the DLL file that contains the procedure being called follows the **Lib** keyword.</span></span> <span data-ttu-id="a2b0d-161">Enfin, la liste d’arguments contient les paramètres et les types de données qui doivent être transmis à la procédure.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-161">And finally, the argument list contains the parameters and the data types that must be passed to the procedure.</span></span> 
  
<span data-ttu-id="a2b0d-162">L’instruction **Declare** suivante ouvre une *subkey* dans le Registre Windows et remplace sa valeur.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-162">The following **Declare** statement opens a  *subkey*  in the Windows registry and replaces its value.</span></span> 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

<span data-ttu-id="a2b0d-163">L’entrée Windows.h (handle de fenêtre) pour la fonction **RegOpenKeyA** est comme suit :</span><span class="sxs-lookup"><span data-stu-id="a2b0d-163">The Windows.h (window handle) entry for the **RegOpenKeyA** function is as follows:</span></span> 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

<span data-ttu-id="a2b0d-164">Dans Visual C et Microsoft Visual C++, l’exemple précédent compile correctement pour les versions 32 bits et 64 bits,</span><span class="sxs-lookup"><span data-stu-id="a2b0d-164">In Visual C and Microsoft Visual C++, the previous example compiles correctly for both 32-bit and 64-bit.</span></span> <span data-ttu-id="a2b0d-165">car HKEY se définit comme un pointeur dont la taille reflète la taille de la mémoire de la plateforme où le code est compilé.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-165">This is because HKEY is defined as a pointer, whose size reflects the memory size of the platform that the code is compiled in.</span></span>
  
<span data-ttu-id="a2b0d-166">Dans les versions précédentes de VBA, il n’existait aucun type de données de pointeur spécifique ; le type de données **Long** était par conséquent toujours utilisé.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-166">In previous versions of VBA, there was no specific pointer data type so the **Long** data type was used.</span></span> <span data-ttu-id="a2b0d-167">Le type de données **Long** étant toujours 32 bits, cela provoque un échec en cas d’utilisation sur un système doté d’une mémoire 64 bits car les 32 bits supérieurs peuvent être tronqués ou peuvent remplacer d’autres adresses mémoire.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-167">And because the **Long** data type is always 32-bits, this breaks when used on a system with 64-bit memory because the upper 32-bits might be truncated or might overwrite other memory addresses.</span></span> <span data-ttu-id="a2b0d-168">L’une ou l’autre de ces situations peut provoquer un comportement inattendu ou un blocage système.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-168">Either of these situations can result in unpredictable behavior or system crashes.</span></span> 
  
<span data-ttu-id="a2b0d-169">Pour résoudre ce problème, VBA inclut un véritable type de données *pointeur* : **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-169">To resolve this, VBA includes a true  *pointer*  data type: **LongPtr**.</span></span> <span data-ttu-id="a2b0d-170">Ce nouveau type de données vous permet d’écrire correctement l’instruction **Declare** d’origine comme suit :</span><span class="sxs-lookup"><span data-stu-id="a2b0d-170">This new data type enables you to write the original **Declare** statement correctly as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

<span data-ttu-id="a2b0d-171">Ce type de données et le nouvel attribut **PtrSafe** vous permettent d’utiliser cette instruction **Declare** sur les systèmes 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-171">This data type and the new **PtrSafe** attribute enable you to use this **Declare** statement on either 32-bit or 64-bit systems.</span></span> <span data-ttu-id="a2b0d-172">L’attribut **PtrSafe** indique au compilateur VBA que l’instruction **Declare** concerne la version 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-172">The **PtrSafe** attribute indicates to the VBA compiler that the **Declare** statement is targeted for the 64-bit version of Office.</span></span> <span data-ttu-id="a2b0d-173">Sans cet attribut, l’utilisation de l’instruction **Declare** dans un système 64 bits entraîne une erreur de compilation.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-173">Without this attribute, using the **Declare** statement in a 64-bit system will result in a compile-time error.</span></span> <span data-ttu-id="a2b0d-174">L’attribut **PtrSafe** est facultatif sur la version 32 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-174">The **PtrSafe** attribute is optional on the 32-bit version of Office.</span></span> <span data-ttu-id="a2b0d-175">Cela permet aux instructions **Declare** existantes de fonctionner comme elles l’ont toujours fait.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-175">This enables existing **Declare** statements to work as they always have.</span></span> 
  
<span data-ttu-id="a2b0d-176">Le tableau suivant fournit des informations supplémentaires sur le nouveau qualificateur et les nouveaux types de données, ainsi qu’un autre type de données, deux opérateurs de conversion et trois fonctions.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-176">The following table provides more information about the new qualifier and data typeas well as another data type, two conversion operators, and three functions.</span></span>
  
|<span data-ttu-id="a2b0d-177">Type</span><span class="sxs-lookup"><span data-stu-id="a2b0d-177">Type</span></span>|<span data-ttu-id="a2b0d-178">Item</span><span class="sxs-lookup"><span data-stu-id="a2b0d-178">Item</span></span>|<span data-ttu-id="a2b0d-179">Description</span><span class="sxs-lookup"><span data-stu-id="a2b0d-179">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a2b0d-180">Qualificateur</span><span class="sxs-lookup"><span data-stu-id="a2b0d-180">Qualifier</span></span>  <br/> |<span data-ttu-id="a2b0d-181">**PtrSafe**</span><span class="sxs-lookup"><span data-stu-id="a2b0d-181">**PtrSafe**</span></span> <br/> |<span data-ttu-id="a2b0d-p119">Indique que l’instruction **Declare** est compatible avec 64 bits. Cet attribut est obligatoire sur les systèmes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-p119">Indicates that the **Declare** statement is compatible with 64-bits. This attribute is mandatory on 64-bit systems.  </span></span><br/> |
|<span data-ttu-id="a2b0d-184">Type de données</span><span class="sxs-lookup"><span data-stu-id="a2b0d-184">Data Type</span></span>  <br/> |<span data-ttu-id="a2b0d-185">**LongPtr**</span><span class="sxs-lookup"><span data-stu-id="a2b0d-185">**LongPtr**</span></span> <br/> |<span data-ttu-id="a2b0d-186">Un type de données variables qui est un type de données 4 octets sur les versions 32 bits et un type de données de 8 octets sur les versions 64 bits de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-186">A variable data type which is a 4-bytes data type on 32-bit versions and an 8-byte data type on 64-bit versions of Microsoft Office.</span></span> <span data-ttu-id="a2b0d-187">Il s’agit de la méthode recommandée pour déclarer un pointeur ou une handle pour le nouveau code, mais également pour le code hérité si celui-ci doit s’exécuter dans la version 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-187">This is the recommended way of declaring a pointer or a handle for new code but also for legacy code if it has to run in the 64-bit version of Office.</span></span> <span data-ttu-id="a2b0d-188">Il est uniquement pris en charge dans le runtime VBA 7 sur 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-188">It is only supported in the VBA 7 runtime on 32-bit and 64-bit.</span></span> <span data-ttu-id="a2b0d-189">Notez que vous pouvez lui attribuer des valeurs numériques, mais pas des types numériques.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-189">Note that you can assign numeric values to it but not numeric types.</span></span>  <br/> |
|<span data-ttu-id="a2b0d-190">Type de données</span><span class="sxs-lookup"><span data-stu-id="a2b0d-190">Data Type</span></span>  <br/> |<span data-ttu-id="a2b0d-191">**LongLong**</span><span class="sxs-lookup"><span data-stu-id="a2b0d-191">**LongLong**</span></span> <br/> |<span data-ttu-id="a2b0d-192">Il s’agit d’un type de données de 8 octets qui est disponible uniquement dans les versions 64 bits de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-192">This is an 8-byte data type which is available only in 64-bit versions of Microsoft Office.</span></span> <span data-ttu-id="a2b0d-193">Vous pouvez lui attribuer des valeurs numériques, pas des types numériques (pour éviter la troncation).</span><span class="sxs-lookup"><span data-stu-id="a2b0d-193">You can assign numeric values but not numeric types (to avoid truncation).</span></span>  <br/> |
|<span data-ttu-id="a2b0d-194">Opérateur de conversion</span><span class="sxs-lookup"><span data-stu-id="a2b0d-194">Conversion Operator</span></span>  <br/> |<span data-ttu-id="a2b0d-195">**CLngPtr**</span><span class="sxs-lookup"><span data-stu-id="a2b0d-195">**CLngPtr**</span></span> <br/> |<span data-ttu-id="a2b0d-196">Convertit une expression simple en un type de données **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-196">Converts a simple expression to a **LongPtr** data type.</span></span>  <br/> |
|<span data-ttu-id="a2b0d-197">Opérateur de conversion</span><span class="sxs-lookup"><span data-stu-id="a2b0d-197">Conversion Operator</span></span>  <br/> |<span data-ttu-id="a2b0d-198">**CLngLng**</span><span class="sxs-lookup"><span data-stu-id="a2b0d-198">**CLngLng**</span></span> <br/> |<span data-ttu-id="a2b0d-199">Convertit une expression simple en un type de données **LongLong**.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-199">Converts a simple expression to a **LongLong** data type.</span></span>  <br/> |
|<span data-ttu-id="a2b0d-200">Fonction</span><span class="sxs-lookup"><span data-stu-id="a2b0d-200">Function</span></span>  <br/> |<span data-ttu-id="a2b0d-201">**VarPtr**</span><span class="sxs-lookup"><span data-stu-id="a2b0d-201">**VarPtr**</span></span> <br/> |<span data-ttu-id="a2b0d-p122">Convertisseur de variante. Renvoie un **LongPtr** sur les versions 64 bits et un **Long** sur les versions 32 bits (4 octets).</span><span class="sxs-lookup"><span data-stu-id="a2b0d-p122">Variant converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="a2b0d-204">Fonction</span><span class="sxs-lookup"><span data-stu-id="a2b0d-204">Function</span></span>  <br/> |<span data-ttu-id="a2b0d-205">**ObjPtr**</span><span class="sxs-lookup"><span data-stu-id="a2b0d-205">**ObjPtr**</span></span> <br/> |<span data-ttu-id="a2b0d-p123">Convertisseur d’objet. Renvoie un **LongPtr** sur les versions 64 bits et un **Long** sur les versions 32 bits (4 octets).</span><span class="sxs-lookup"><span data-stu-id="a2b0d-p123">Object converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="a2b0d-208">Fonction</span><span class="sxs-lookup"><span data-stu-id="a2b0d-208">Function</span></span>  <br/> |<span data-ttu-id="a2b0d-209">**StrPtr**</span><span class="sxs-lookup"><span data-stu-id="a2b0d-209">**StrPtr**</span></span> <br/> |<span data-ttu-id="a2b0d-p124">Convertisseur de chaîne. Renvoie un **LongPtr** sur les versions 64 bits et un **Long** sur les versions 32 bits (4 octets).</span><span class="sxs-lookup"><span data-stu-id="a2b0d-p124">String converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
   
<span data-ttu-id="a2b0d-212">L’exemple suivant montre comment utiliser certains de ces éléments dans une instruction **Declare**.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-212">The follow example shows how to use some of these items in a **Declare** statement.</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

<span data-ttu-id="a2b0d-213">Notez que les instructions **Declare** sans attribut **PtrSafe** sont considérées comme non compatibles avec la version 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-213">Note that **Declare** statements without the **PtrSafe** attribute are assumed not to be compatible with the 64-bit version of Office.</span></span> 
  
<span data-ttu-id="a2b0d-214">Il existe deux constantes de compilation conditionnelle : **VBA7** et **Win64**.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-214">There are two conditional compilation constants: **VBA7** and **Win64**.</span></span> <span data-ttu-id="a2b0d-215">Pour assurer la compatibilité descendante avec les versions antérieures de Microsoft Office, utilisez la constante **VBA7** (c’est le cas le plus typique) pour empêcher d’utiliser le code 64 bits dans la version antérieure d’Office.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-215">To ensure backward compatibility with previous versions of Microsoft Office, you use the **VBA7** constant (this is the more typical case) to prevent 64-bit code from being used in the earlier version of Office.</span></span> <span data-ttu-id="a2b0d-216">Pour le code qui est différent entre la version 32 bits et la version 64 bits, comme l’appel d’une API de mathématiques qui utilise **LongLong** pour sa version 64 bits et **Long** pour sa version 32 bits, utilisez la constante **Win64**.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-216">For code that is different between the 32-bit version and the 64-bit version, such as calling a math API that uses **LongLong** for its 64-bit version and **Long** for its 32-bit version, you use the **Win64** constant.</span></span> <span data-ttu-id="a2b0d-217">Le code suivant montre l’utilisation de ces deux constantes.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-217">The following code shows the use of these two constants.</span></span> 
  
```vb
#if Win64 then
   Declare PtrSafe Function MyMathFunc Lib "User32" (ByVal N As LongLong) As LongLong
#else
   Declare Function MyMathFunc Lib "User32" (ByVal N As Long) As Long
#end if
#if VBA7 then
   Declare PtrSafe Sub MessageBeep Lib "User32" (ByVal N AS Long)
#else
   Declare Sub MessageBeep Lib "User32" (ByVal N AS Long)
#end if
```

<span data-ttu-id="a2b0d-218">Pour résumer, si vous écrivez du code 64 bits et que vous comptez l’utiliser dans les versions précédentes d’Office, utilisez la constante de compilation conditionnelle **VBA7**.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-218">To summarize, if you write 64-bit code and intend to use it in previous versions of Office, you will want to use the **VBA7** conditional compilation constant.</span></span> <span data-ttu-id="a2b0d-219">Cependant, si vous écrivez du code 32 bits dans Office, ce code fonctionne tel quel dans les versions précédentes d’Office sans passer par la constante de compilation.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-219">However, if you write 32-bit code in Office, that code works as is in previous versions of Office without the need for the compilation constant.</span></span> <span data-ttu-id="a2b0d-220">Si vous voulez vérifier que vous utilisez les instructions 32 bits pour les versions 32 bits et les instructions 64 bits pour les versions 64 bits, votre meilleure option consiste à utiliser la constante de compilation conditionnelle **Win64**.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-220">If you want to ensure that you are using 32-bit statements for 32-bit versions and 64-bit statements for 64-bit versions, your best option is to use the **Win64** conditional compilation constant.</span></span> 
  
## <a name="using-conditional-compilation-attributes"></a><span data-ttu-id="a2b0d-221">Utilisation des attributs de compilation conditionnelle</span><span class="sxs-lookup"><span data-stu-id="a2b0d-221">Using conditional compilation attributes</span></span>
<span data-ttu-id="a2b0d-222"><a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a></span><span class="sxs-lookup"><span data-stu-id="a2b0d-222"><a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a></span></span>

<span data-ttu-id="a2b0d-223">L’exemple suivant montre le code VBA destiné aux versions 32 bits qui doit être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-223">The following example shows VBA code written for 32-bit that needs to be updated.</span></span> <span data-ttu-id="a2b0d-224">Notez que les types de données du code hérité sont mis à jour pour utiliser **LongPtr**, car ils font référence aux handles ou aux pointeurs.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-224">Notice the data types in the legacy code that are updated to use **LongPtr** because they refer to handles or pointers.</span></span> 
  
### <a name="vba-code-written-for-32-bit-versions"></a><span data-ttu-id="a2b0d-225">Code VBA destiné aux versions 32 bits</span><span class="sxs-lookup"><span data-stu-id="a2b0d-225">VBA code written for 32-bit versions</span></span>
  
```vb
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
  
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
```

### <a name="vba-code-rewritten-for-64-bit-versions"></a><span data-ttu-id="a2b0d-226">Code VBA réécrit pour les versions 64 bits</span><span class="sxs-lookup"><span data-stu-id="a2b0d-226">VBA code rewritten for 64-bit versions</span></span>
  
```vb
#if VBA7 then    ' VBA7 
Declare PtrSafe Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As LongPtr
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As LongPtr
  lParam As LongPtr
  iImage As Long
End Type
 
#else    ' Downlevel when using previous version of VBA7
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
 
#end if
Sub TestSHBrowseForFolder ()
    Dim bInfo As BROWSEINFO
    Dim pidList As Long
    bInfo.pidlRoot = 0&amp;
    bInfo.ulFlags = &amp;H1
    pidList = SHBrowseForFolder(bInfo)
End Sub
```

<span data-ttu-id="a2b0d-227"><a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a></span><span class="sxs-lookup"><span data-stu-id="a2b0d-227"><a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a></span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="a2b0d-228">Questions fréquemment posées</span><span class="sxs-lookup"><span data-stu-id="a2b0d-228">Frequently asked questions</span></span>

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a><span data-ttu-id="a2b0d-229">Quand dois-je utiliser la version 64 bits d’Office ?</span><span class="sxs-lookup"><span data-stu-id="a2b0d-229">When should I use the 64-bit version of Office?</span></span>
  
<span data-ttu-id="a2b0d-230">La question est plutôt de savoir quelle application hôte (Excel, Word, etc.) vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-230">This is more a matter of which host application (Excel, Word, and so forth) you are using.</span></span> <span data-ttu-id="a2b0d-231">Par exemple, Excel est en mesure de gérer des feuilles de calcul beaucoup plus grandes avec la version 64 bits de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-231">For example, Excel is able to handle much larger worksheets with the 64-bit version of Microsoft Office.</span></span>
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a><span data-ttu-id="a2b0d-232">Puis-je installer des versions 64 bits et 32 bits d’Office côte à côte ?</span><span class="sxs-lookup"><span data-stu-id="a2b0d-232">Can I install 64-bit and 32-bit versions of Office side-by-side?</span></span>
  
<span data-ttu-id="a2b0d-233">Non.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-233">No.</span></span>
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a><span data-ttu-id="a2b0d-234">Quand dois-je convertir des paramètres Long en LongPtr ?</span><span class="sxs-lookup"><span data-stu-id="a2b0d-234">When should I convert Long parameters to LongPtr?</span></span>
  
<span data-ttu-id="a2b0d-235">Vous devez vérifier la documentation de l’API Windows sur le Microsoft Developers Network pour la fonction que vous voulez appeler.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-235">You need to check the Windows API documentation on the Microsoft Developers Network for the function you want to call.</span></span> <span data-ttu-id="a2b0d-236">Les handles et les pointeurs doivent être convertis en **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-236">Handles and pointers need to be converted to **LongPtr**.</span></span> <span data-ttu-id="a2b0d-237">Par exemple, la documentation relative à [RegOpenKeyA](https://docs.microsoft.com/windows/win32/api/winreg/nf-winreg-regopenkeyexa) fournit la signature suivante :</span><span class="sxs-lookup"><span data-stu-id="a2b0d-237">As an example, the documentation for [RegOpenKeyA](https://docs.microsoft.com/windows/win32/api/winreg/nf-winreg-regopenkeyexa) provides the following signature:</span></span> 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

<span data-ttu-id="a2b0d-238">Les paramètres sont définis comme suit :</span><span class="sxs-lookup"><span data-stu-id="a2b0d-238">The parameters are defined as:</span></span>
  
|<span data-ttu-id="a2b0d-239">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2b0d-239">Parameter</span></span>|<span data-ttu-id="a2b0d-240">Description</span><span class="sxs-lookup"><span data-stu-id="a2b0d-240">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="a2b0d-241">hKey [dans]</span><span class="sxs-lookup"><span data-stu-id="a2b0d-241">hKey [in]</span></span>  <br/> |<span data-ttu-id="a2b0d-242">Une *handle* vers une clé de Registre ouverte.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-242">A  *handle*  to an open registry key.</span></span>  <br/> |
|<span data-ttu-id="a2b0d-243">lpSubKey [dans, facultatif]</span><span class="sxs-lookup"><span data-stu-id="a2b0d-243">lpSubKey [in, optional]</span></span>  <br/> |<span data-ttu-id="a2b0d-244">Le nom de la sous-clé de Registre à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-244">The name of the registry subkey to be opened.</span></span>  <br/> |
|<span data-ttu-id="a2b0d-245">ulOptions</span><span class="sxs-lookup"><span data-stu-id="a2b0d-245">ulOptions</span></span>  <br/> |<span data-ttu-id="a2b0d-246">Ce paramètre est réservé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-246">This parameter is reserved and must be zero.</span></span>  <br/> |
|<span data-ttu-id="a2b0d-247">samDesired [dans]</span><span class="sxs-lookup"><span data-stu-id="a2b0d-247">samDesired [in]</span></span>  <br/> |<span data-ttu-id="a2b0d-248">Masque qui spécifie les droits d’accès souhaités à la clé.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-248">A mask that specifies the desired access rights to the key.</span></span>  <br/> |
|<span data-ttu-id="a2b0d-249">phkResult [out]</span><span class="sxs-lookup"><span data-stu-id="a2b0d-249">phkResult [out]</span></span>  <br/> |<span data-ttu-id="a2b0d-250">Un *pointeur* vers une variable qui reçoit une handle vers la clé ouverte.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-250">A  *pointer*  to a variable that receives a handle to the opened key.</span></span>  <br/> |
   
<span data-ttu-id="a2b0d-251">Dans [Win32API_PtrSafe.txt](https://docs.microsoft.com/office/troubleshoot/office/win32api_ptrsafe-with-64-bit-support), l’instruction **Declare** se définit comme suit :</span><span class="sxs-lookup"><span data-stu-id="a2b0d-251">In [Win32API_PtrSafe.txt](https://docs.microsoft.com/office/troubleshoot/office/win32api_ptrsafe-with-64-bit-support), the **Declare** statement is defined as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a><span data-ttu-id="a2b0d-252">Dois-je convertir les pointeurs et les handles dans les structures ?</span><span class="sxs-lookup"><span data-stu-id="a2b0d-252">Should I convert pointers and handles in structures?</span></span>
  
<span data-ttu-id="a2b0d-253">Oui.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-253">Yes.</span></span> <span data-ttu-id="a2b0d-254">Observez le type **MSG** dans Win32API_PtrSafe.txt :</span><span class="sxs-lookup"><span data-stu-id="a2b0d-254">See the **MSG** type in Win32API_PtrSafe.txt:</span></span> 
  
```vb
Type MSG
    hwnd As LongPtr 
    message As Long
    wParam As LongPtr 
    lParam As LongPtr 
    time As Long
    pt As POINTAPI
End TypeF
```

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a><span data-ttu-id="a2b0d-255">Quand dois-je utiliser strptr, varpt et objptr ?</span><span class="sxs-lookup"><span data-stu-id="a2b0d-255">When should I use strptr, varpt, and objptr?</span></span>
  
<span data-ttu-id="a2b0d-256">Vous devez utiliser ces fonctions pour récupérer respectivement des pointeurs vers des chaînes, des variables et des objets.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-256">You should use these functions to retrieve pointers to strings, variables and objects, respectively.</span></span> <span data-ttu-id="a2b0d-257">Sur la version 64 bits d’Office, ces fonctions renvoient un **LongPtr** de 64 bits, qui peut être transféré à l’instruction **Declare**.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-257">On the 64-bit version of Office, these functions will return a 64-bit **LongPtr**, which can be passed to **Declare** statements.</span></span> <span data-ttu-id="a2b0d-258">L’utilisation de ces fonctions n’a pas changé des versions précédentes de VBA.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-258">The use of these functions has not changed from previous versions of VBA.</span></span> <span data-ttu-id="a2b0d-259">La seule différence est qu’elles renvoient désormais un **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="a2b0d-259">The only difference is that they now return a **LongPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a2b0d-260">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2b0d-260">See also</span></span>
<span data-ttu-id="a2b0d-261"><a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="a2b0d-261"><a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a></span></span>

- <span data-ttu-id="a2b0d-262">[Anatomie d’une instruction Declare](https://docs.microsoft.com/previous-versions/aa671659(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="a2b0d-262">[Anatomy of a Declare Statement](https://docs.microsoft.com/previous-versions/aa671659(v=vs.71))</span></span>
