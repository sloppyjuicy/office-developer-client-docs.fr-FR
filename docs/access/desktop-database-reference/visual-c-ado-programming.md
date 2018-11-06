---
title: Programmation ADO C++ visuelle
TOCTitle: Visual C++ ADO programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5278a998363359f4bd2aad14881865505ce45633
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998412"
---
# <a name="visual-c-ado-programming"></a><span data-ttu-id="c28c3-102">Programmation ADO C++ visuelle</span><span class="sxs-lookup"><span data-stu-id="c28c3-102">Visual C++ ADO programming</span></span>

<span data-ttu-id="c28c3-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c28c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c28c3-104">La documentation Référence de l'API ADO décrit les fonctionnalités de l'interface de programmation d'application (API) ADO en employant une syntaxe similaire à celle de Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c28c3-104">The ADO API Reference describes the functionality of the ADO application programming interface (API) using a syntax similar to Microsoft Visual Basic.</span></span> <span data-ttu-id="c28c3-105">Bien qu’elle s’adresse à tous les utilisateurs, les programmeurs ADO utilisent divers langages tels que Visual Basic, Visual C++ (avec et sans le \*\* \#importer\*\* directive) et Visual J ++ (avec le package de classes ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="c28c3-105">Though the intended audience is all users, ADO programmers employ diverse languages such as Visual Basic, Visual C++ (with and without the **\#import** directive), and Visual J++ (with the ADO/WFC class package).</span></span>

<span data-ttu-id="c28c3-106">Pour répondre à cette diversité, les [index de la syntaxe ADO pour Visual C++](using-ado-with-microsoft-visual-c.md) proposent une syntaxe spécifique au langage Visual C++ avec des liens vers des descriptions communes de fonctionnalités, paramètres, comportements exceptionnels, etc. de la documentation Référence de l'API ADO.</span><span class="sxs-lookup"><span data-stu-id="c28c3-106">To accommodate this diversity, the [ADO for Visual C++ Syntax Indexes](using-ado-with-microsoft-visual-c.md) provide Visual C++ language-specific syntax with links to common descriptions of functionality, parameters, exceptional behaviors, and so on, in the API Reference.</span></span>

<span data-ttu-id="c28c3-p102">ADO est implémenté avec les interfaces COM (Component Object Model). Toutefois, pour les programmeurs, il est plus facile d'utiliser COM avec certains langages de programmation qu'avec d'autres. Par exemple, presque tous les détails liés à l'utilisation de COM sont gérés implicitement pour les programmeurs qui ont recours à Visual Basic, tandis que les programmeurs Visual C++ doivent gérer eux-mêmes ces détails.</span><span class="sxs-lookup"><span data-stu-id="c28c3-p102">ADO is implemented with COM (Component Object Model) interfaces. However, it is easier for programmers to work with COM in certain programming languages than others. For example, nearly all the details of using COM are handled implicitly for Visual Basic programmers, whereas Visual C++ programmers must attend to those details themselves.</span></span>

<span data-ttu-id="c28c3-110">Les sections suivantes résument les détails pour les programmeurs C et C++ à l’aide d’ADO et \*\* \#importer\*\* directive.</span><span class="sxs-lookup"><span data-stu-id="c28c3-110">The following sections summarize details for C and C++ programmers using ADO and the **\#import** directive.</span></span> <span data-ttu-id="c28c3-111">Elle porte sur les types de données spécifiques à COM (**Variant**, **BSTR**et **SafeArray**) et gestion des erreurs (\_com\_erreur).</span><span class="sxs-lookup"><span data-stu-id="c28c3-111">It focuses on data types specific to COM (**Variant**, **BSTR**, and **SafeArray**), and error handling (\_com\_error).</span></span>

## <a name="using-the-import-compiler-directive"></a><span data-ttu-id="c28c3-112">À l’aide de la \#importer la directive du compilateur</span><span class="sxs-lookup"><span data-stu-id="c28c3-112">Using the \#import compiler directive</span></span>

<span data-ttu-id="c28c3-113">Le \*\* \#importer\*\* directive du compilateur Visual C++ simplifie l’utilisation avec les méthodes et propriétés ADO.</span><span class="sxs-lookup"><span data-stu-id="c28c3-113">The **\#import** Visual C++ compiler directive simplifies working with the ADO methods and properties.</span></span> <span data-ttu-id="c28c3-114">La directive extrait le nom d'un fichier contenant une bibliothèque de types, telle que le fichier .dll ADO (Msado15.dll), et génère des fichiers d'en-tête contenant des déclarations typedef, des pointeurs intelligents pour les interfaces, ainsi que des constantes énumérées.</span><span class="sxs-lookup"><span data-stu-id="c28c3-114">The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants.</span></span> <span data-ttu-id="c28c3-115">Chaque interface est encapsulée dans une classe.</span><span class="sxs-lookup"><span data-stu-id="c28c3-115">Each interface is encapsulated, or wrapped, in a class.</span></span>

<span data-ttu-id="c28c3-p105">Pour chaque opération qui se produit à l'intérieur d'une classe (c'est-à-dire, un appel de méthode ou de propriété), il existe une déclaration permettant d'appeler directement l'opération (c'est-à-dire, la forme « brute » de l'opération), et une déclaration qui appelle l'opération brute et lève une exception COM si l'opération ne s'exécute pas correctement. Si l'opération est une propriété, il existe généralement une directive de compilateur qui crée une autre syntaxe si l'opération présente une syntaxe apparentée à Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c28c3-p105">For each operation within a class (that is, a method or property call), there is a declaration to call the operation directly (that is, the "raw" form of the operation), and a declaration to call the raw operation and throw a COM error if the operation fails to execute successfully. If the operation is a property, there is usually a compiler directive that creates an alternative syntax for the operation that has syntax like Visual Basic.</span></span>

<span data-ttu-id="c28c3-118">Les opérations qui extraient la valeur d’une propriété ont un nom du formulaire, \**obtenir \*\*\* propriété*.</span><span class="sxs-lookup"><span data-stu-id="c28c3-118">Operations that retrieve the value of a property have names of the form, \**Get\*\*\*Property*.</span></span> <span data-ttu-id="c28c3-119">Les opérations qui définissent la valeur d’une propriété ont un nom du formulaire, \**placer \*\*\* propriété*.</span><span class="sxs-lookup"><span data-stu-id="c28c3-119">Operations that set the value of a property have names of the form, \**Put\*\*\*Property*.</span></span> <span data-ttu-id="c28c3-120">Les opérations qui définissent la valeur d’une propriété avec un pointeur vers un objet ADO ont un nom du formulaire, \**PutRef \*\*\* propriété*.</span><span class="sxs-lookup"><span data-stu-id="c28c3-120">Operations that set the value of a property with a pointer to an ADO object have names of the form, \**PutRef\*\*\*Property*.</span></span>

<span data-ttu-id="c28c3-121">Vous pouvez obtenir ou définir une propriété avec des appels se présentant comme suit :</span><span class="sxs-lookup"><span data-stu-id="c28c3-121">You can get or set a property with calls of these forms:</span></span>

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a><span data-ttu-id="c28c3-122">À l’aide des directives de propriété</span><span class="sxs-lookup"><span data-stu-id="c28c3-122">Using property directives</span></span>

<span data-ttu-id="c28c3-123">Le \*\* \_ \_declspec(property...)\*\* directive du compilateur est une extension du langage C spécifique à Microsoft qui déclare une fonction utilisée en tant que propriété avec une syntaxe alternative.</span><span class="sxs-lookup"><span data-stu-id="c28c3-123">The **\_\_declspec(property...)** compiler directive is a Microsoft-specific C language extension that declares a function used as a property to have an alternative syntax.</span></span> <span data-ttu-id="c28c3-124">Par conséquent, vous pouvez définir ou obtenir les valeurs d'une propriété d'une façon similaire à Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c28c3-124">As a result, you can set or get values of a property in a way similar to Visual Basic.</span></span> <span data-ttu-id="c28c3-125">Par exemple, vous pouvez définir et obtenir une propriété comme suit :</span><span class="sxs-lookup"><span data-stu-id="c28c3-125">For example, you can set and get a property this way:</span></span>

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

<span data-ttu-id="c28c3-126">Notez qu'il n'est pas utile de coder les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c28c3-126">Notice you do not have to code:</span></span>

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

<span data-ttu-id="c28c3-127">Le compilateur génère le \*\*\*\*\* Get-\*, **Put**-, ou \**PutRef \*\*\* propriété* appel en fonction de la syntaxe alternative déclarée et si la propriété est en cours lu ou écrit.</span><span class="sxs-lookup"><span data-stu-id="c28c3-127">The compiler will generate the appropriate \**Get\*\*\*-*, **Put**-, or \**PutRef\*\*\*Property* call based on what alternative syntax is declared and whether the property is being read or written.</span></span>

<span data-ttu-id="c28c3-128">Le \*\* \_ \_declspec(property...)\*\* directive du compilateur peut déclarer uniquement **get**, **put**ou la syntaxe alternative **get** et **put** pour une fonction.</span><span class="sxs-lookup"><span data-stu-id="c28c3-128">The **\_\_declspec(property...)** compiler directive can only declare **get**, **put**, or **get** and **put** alternative syntax for a function.</span></span> <span data-ttu-id="c28c3-129">Les opérations en lecture seule ne peuvent avoir qu'une déclaration **get** et les opérations en écriture seule une déclaration **put**; les opérations en lecture et en écriture ont à la fois des déclarations **get** et **put**.</span><span class="sxs-lookup"><span data-stu-id="c28c3-129">Read-only operations only have a **get** declaration; write-only operations only have a **put** declaration; operations that are both read and write have both **get** and **put** declarations.</span></span>

<span data-ttu-id="c28c3-130">Seules deux déclarations sont possibles avec cette directive ; Toutefois, chaque propriété peut avoir trois fonctions de propriété : \**obtenir \*\*\* propriété*, \**placer \*\*\* propriété*, et \**PutRef \*\*\* propriété*.</span><span class="sxs-lookup"><span data-stu-id="c28c3-130">Only two declarations are possible with this directive; however, each property may have three property functions: \**Get\*\*\*Property*, \**Put\*\*\*Property*, and \**PutRef\*\*\*Property*.</span></span> <span data-ttu-id="c28c3-131">Dans ce cas, deux formes seulement de la propriété possèdent une syntaxe alternative.</span><span class="sxs-lookup"><span data-stu-id="c28c3-131">In that case, only two forms of the property have the alternative syntax.</span></span>

<span data-ttu-id="c28c3-132">Par exemple, la propriété **ActiveConnection** de l’objet **Command** est déclarée avec une syntaxe alternative pour \**obtenir \*\*\* ActiveConnection* et \**PutRef \*\*\* ActiveConnection*.</span><span class="sxs-lookup"><span data-stu-id="c28c3-132">For example, the **Command** object **ActiveConnection** property is declared with an alternative syntax for \**Get\*\*\*ActiveConnection* and \**PutRef\*\*\*ActiveConnection*.</span></span> <span data-ttu-id="c28c3-133">**PutRef**- syntaxe est un choix judicieux car en pratique, vous devez généralement placer un objet **Connection** ouvert (c'est-à-dire, un pointeur d’objet **Connection** ) dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c28c3-133">The **PutRef**- syntax is a good choice because in practice, you will typically want to put an open **Connection** object (that is, a **Connection** object pointer) in this property.</span></span> <span data-ttu-id="c28c3-134">En revanche, l’objet **Recordset** a **Get**-, **Put**-, et \**PutRef \*\*\* ActiveConnection* opérations, mais pas de syntaxe alternative.</span><span class="sxs-lookup"><span data-stu-id="c28c3-134">On the other hand, the **Recordset** object has **Get**-, **Put**-, and \**PutRef\*\*\*ActiveConnection* operations, but no alternative syntax.</span></span>

## <a name="collections-the-getitem-method-and-the-item-property"></a><span data-ttu-id="c28c3-135">Collections, méthode GetItem et la propriété Item</span><span class="sxs-lookup"><span data-stu-id="c28c3-135">Collections, the GetItem method, and the Item property</span></span>

<span data-ttu-id="c28c3-p111">ADO définit plusieurs collections, notamment **Fields**, **Parameters**, **Properties** et **Errors**. En Visual C++, la méthode **GetItem(***index***)** retourne un membre de la collection. *Index* est une valeur de type **Variant**, qui représente soit un index numérique du membre de la collection, soit une chaîne contenant le nom du membre.</span><span class="sxs-lookup"><span data-stu-id="c28c3-p111">ADO defines several collections, including **Fields**, **Parameters**, **Properties**, and **Errors**. In Visual C++, the **GetItem(***index***)** method returns a member of the collection. *Index* is a **Variant**, the value of which is either a numerical index of the member in the collection, or a string containing the name of the member.</span></span>

<span data-ttu-id="c28c3-139">Le \*\* \_ \_declspec(property...)\*\* directive du compilateur déclare la propriété **Item** comme une syntaxe alternative à la méthode **élémentaire GetItem()** de chaque collection.</span><span class="sxs-lookup"><span data-stu-id="c28c3-139">The **\_\_declspec(property...)** compiler directive declares the **Item** property as an alternative syntax to each collection's fundamental **GetItem()** method.</span></span> <span data-ttu-id="c28c3-140">La syntaxe alternative utilise des crochets droits et présente des similitudes avec une référence de matrice.</span><span class="sxs-lookup"><span data-stu-id="c28c3-140">The alternative syntax uses square brackets and looks similar to an array reference.</span></span> <span data-ttu-id="c28c3-141">En règle générale, les deux formes se présentent comme suit:</span><span class="sxs-lookup"><span data-stu-id="c28c3-141">In general, the two forms look like the following:</span></span>

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

<span data-ttu-id="c28c3-142">Par exemple, assigner une valeur à un champ d’un objet **Recordset** , nommé ***rs***, dérivé de la table **authors** de la base de données **pubs** .</span><span class="sxs-lookup"><span data-stu-id="c28c3-142">For example, assign a value to a field of a **Recordset** object, named ***rs***, derived from the **authors** table of the **pubs** database.</span></span> <span data-ttu-id="c28c3-143">Utilisez la propriété **Item()** pour accéder au troisième **champ** de la collection **Fields** de l’objet **Recordset** (les collections sont indexées à partir de zéro ; le troisième champ est nommé ***au\_fname***).</span><span class="sxs-lookup"><span data-stu-id="c28c3-143">Use the **Item()** property to access the third **Field** of the **Recordset** object **Fields** collection (collections are indexed from zero; assume the third field is named ***au\_fname***).</span></span> <span data-ttu-id="c28c3-144">Appelez ensuite la méthode **Value()** sur l'objet **Field** pour attribuer une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="c28c3-144">Then call the **Value()** method on the **Field** object to assign a string value.</span></span>

<span data-ttu-id="c28c3-145">Ceci peut être exprimé en Visual Basic avec les quatre variantes suivantes (les deux dernières sont propres à Visual Basic ; les autres langages n'ont pas d'équivalents) :</span><span class="sxs-lookup"><span data-stu-id="c28c3-145">This can be expressed in Visual Basic in the following four ways (the last two forms are unique to Visual Basic; other languages do not have equivalents):</span></span>

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

<span data-ttu-id="c28c3-146">En Visual C++, l'équivalent des deux premières variantes est :</span><span class="sxs-lookup"><span data-stu-id="c28c3-146">The equivalent in Visual C++ to the first two forms above is:</span></span>

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

<span data-ttu-id="c28c3-147">\-ou -(la syntaxe alternative de la propriété **Value** est également indiquée)</span><span class="sxs-lookup"><span data-stu-id="c28c3-147">\-or- (the alternative syntax for the **Value** property is also shown)</span></span>

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a><span data-ttu-id="c28c3-148">Types de données spécifiques à COM</span><span class="sxs-lookup"><span data-stu-id="c28c3-148">COM-specific data types</span></span>

<span data-ttu-id="c28c3-p114">En règle générale, les types de données Visual Basic que vous rencontrez dans la documentation Référence de l'API ADO possèdent un équivalent Visual C++. Il peut s'agir notamment des types de données standard **unsigned char** pour **Byte** en Visual Basic, **short** pour **Integer** et **long** pour **Long**. Consultez les index de la syntaxe pour savoir exactement quelles sont les exigences au niveau des opérandes d'une méthode ou d'une propriété donnée.</span><span class="sxs-lookup"><span data-stu-id="c28c3-p114">In general, any Visual Basic data type you find in the ADO API Reference has a Visual C++ equivalent. These include standard data types such as **unsigned char** for a Visual Basic **Byte**, **short** for **Integer**, and **long** for **Long**. Look in the Syntax Indexes to see exactly what is required for the operands of a given method or property.</span></span>

<span data-ttu-id="c28c3-152">Les exceptions à cette règle sont les types de données spécifiques à COM : **Variant**, **BSTR** et **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="c28c3-152">The exceptions to this rule are the data types specific to COM: **Variant**, **BSTR**, and **SafeArray**.</span></span>

### <a name="variant"></a><span data-ttu-id="c28c3-153">Variant</span><span class="sxs-lookup"><span data-stu-id="c28c3-153">Variant</span></span>

<span data-ttu-id="c28c3-154">Un **Variant** est un type de données structurées qui contient un membre de valeur et un membre de type de données.</span><span class="sxs-lookup"><span data-stu-id="c28c3-154">A **Variant** is a structured data type that contains a value member and a data type member.</span></span> <span data-ttu-id="c28c3-155">Un **Variant** peut contenir un large éventail d’autres types de données, y compris un autre type Variant, BSTR, Boolean, IDispatch ou IUnknown pointeur, devise, date et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="c28c3-155">A **Variant** may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on.</span></span> <span data-ttu-id="c28c3-156">COM fournit également des méthodes qui permettent de convertissent un type de données vers un autre.</span><span class="sxs-lookup"><span data-stu-id="c28c3-156">COM also provides methods that make it easy to convert one data type to another.</span></span>

<span data-ttu-id="c28c3-157">Le \*\* \_variante\_t\*\* classe encapsule et gère le type de données **Variant** .</span><span class="sxs-lookup"><span data-stu-id="c28c3-157">The **\_variant\_t** class encapsulates and manages the **Variant** data type.</span></span>

<span data-ttu-id="c28c3-158">Lors de la référence des API ADO indique qu’une méthode ou opérande propriété prend une valeur, cela signifie généralement que la valeur est passée dans un \*\* \_variante\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="c28c3-158">When the ADO API Reference says a method or property operand takes a value, it usually means the value is passed in a **\_variant\_t**.</span></span>

<span data-ttu-id="c28c3-p116">Cette règle est explicitement vraie lorsque la section **Parameters** des rubriques de la documentation Référence de l'API ADO indique qu'un opérande est de type **Variant**. Des exceptions sont possibles, notamment lorsque la documentation précise explicitement que l'opérande correspond à un type de données standard, tel que **Long** ou **Byte**, ou encore lorsque l'opérande correspond à un type de données **String**.</span><span class="sxs-lookup"><span data-stu-id="c28c3-p116">This rule is explicitly true when the **Parameters** section in the topics of the ADO API Reference says an operand is a **Variant**. One exception is when the documentation explicitly says the operand takes a standard data type, such as **Long** or **Byte**, or an enumeration. Another exception is when the operand takes a **String**.</span></span>

### <a name="bstr"></a><span data-ttu-id="c28c3-162">BSTR</span><span class="sxs-lookup"><span data-stu-id="c28c3-162">BSTR</span></span>

<span data-ttu-id="c28c3-p117">**BSTR** (**B**asic **STR**ing) est un type de données structuré qui contient une chaîne de caractères ainsi que la longueur de celle-ci. COM fournit des méthodes permettant d'allouer, manipuler et libérer un type **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="c28c3-p117">A **BSTR** (**B**asic **STR**ing) is a structured data type that contains a character string and the string's length. COM provides methods to allocate, manipulate, and free a **BSTR**.</span></span>

<span data-ttu-id="c28c3-165">Le \*\* \_bstr\_t\*\* classe encapsule et gère le type de données **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="c28c3-165">The **\_bstr\_t** class encapsulates and manages the **BSTR** data type.</span></span>

<span data-ttu-id="c28c3-166">Lorsque la référence des API ADO indique qu’une méthode ou une propriété prend une valeur de **type String** , cela signifie que de la valeur est sous la forme d’un \*\* \_bstr\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="c28c3-166">When the ADO API Reference says a method or property takes a **String** value, it means the value is in the form of a **\_bstr\_t**.</span></span>

#### <a name="casting-variantt-and-bstrt-classes"></a><span data-ttu-id="c28c3-167">Cast \_variant\_t et \_bstr\_classes t</span><span class="sxs-lookup"><span data-stu-id="c28c3-167">Casting \_variant\_t and \_bstr\_t classes</span></span>

<span data-ttu-id="c28c3-168">Fréquence à laquelle il n’est pas nécessaire de code explicitement une \*\* \_variante\_t\*\* ou \*\* \_bstr\_t\*\* dans un argument d’une opération.</span><span class="sxs-lookup"><span data-stu-id="c28c3-168">Often it is not necessary to explicitly code a **\_variant\_t** or **\_bstr\_t** in an argument to an operation.</span></span> <span data-ttu-id="c28c3-169">Si le \*\* \_variante\_t\*\* ou \*\* \_bstr\_t\*\* possède un constructeur correspondant au type de données de l’argument, puis le compilateur génère le \*\* \_variante\_t\*\* ou \*\* \_ BSTR\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="c28c3-169">If the **\_variant\_t** or **\_bstr\_t** class has a constructor that matches the data type of the argument, then the compiler will generate the appropriate **\_variant\_t** or **\_bstr\_t**.</span></span>

<span data-ttu-id="c28c3-170">Toutefois, si l'argument est ambigu, c'est-à-dire si le type de données de l'argument correspond à plusieurs constructeurs, vous devez attribuer à l'argument le type de données approprié pour appeler le constructeur correct.</span><span class="sxs-lookup"><span data-stu-id="c28c3-170">However, if the argument is ambiguous, that is, the argument's data type matches more than one constructor, you must cast the argument with the appropriate data type to invoke the correct constructor.</span></span>

<span data-ttu-id="c28c3-171">Par exemple, la déclaration pour la méthode **Recordset::Open** est :</span><span class="sxs-lookup"><span data-stu-id="c28c3-171">For example, the declaration for the **Recordset::Open** method is:</span></span>

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

<span data-ttu-id="c28c3-172">L’argument ActiveConnection prend une référence à un \*\* \_variante\_t\*\*, que vous pouvez coder comme une chaîne de connexion ou un pointeur vers un objet **Connection** ouvert.</span><span class="sxs-lookup"><span data-stu-id="c28c3-172">The ActiveConnection argument takes a reference to a **\_variant\_t**, which you may code as a connection string or a pointer to an open **Connection** object.</span></span>

<span data-ttu-id="c28c3-173">La bonne \*\* \_variante\_t\*\* sera construite implicitement si vous passez une chaîne telle que « DSN = pubs ; uid = sa ; pwd = ; », ou un pointeur tel que "(IDispatch \*) pConn ».</span><span class="sxs-lookup"><span data-stu-id="c28c3-173">The correct **\_variant\_t** will be constructed implicitly if you pass a string such as "DSN=pubs;uid=sa;pwd=;", or a pointer such as "(IDispatch \*) pConn".</span></span>

<span data-ttu-id="c28c3-174">Ou vous pouvez coder explicitement un \*\* \_variante\_t\*\* contenant un pointeur tel que «\_variant\_t ((IDispatch \*) pConn, true) ».</span><span class="sxs-lookup"><span data-stu-id="c28c3-174">Or you may explicitly code a **\_variant\_t** containing a pointer such as "\_variant\_t((IDispatch \*) pConn, true)".</span></span> <span data-ttu-id="c28c3-175">Le cast, (IDispatch \*), résout l’ambiguïté avec un autre constructeur qui prend un pointeur vers une interface IUnknown.</span><span class="sxs-lookup"><span data-stu-id="c28c3-175">The cast, (IDispatch \*), resolves the ambiguity with another constructor that takes a pointer to an IUnknown interface.</span></span>

<span data-ttu-id="c28c3-p120">Bien qu'il s'agisse d'un fait rarement mentionné, il est essentiel de rappeler qu'ADO est une interface IDispatch. Chaque fois qu'un pointeur d'objet ADO doit être passé en tant que **Variant**, ce pointeur doit être converti en pointeur vers une interface IDispatch.</span><span class="sxs-lookup"><span data-stu-id="c28c3-p120">It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface. Whenever a pointer to an ADO object must be passed as a **Variant**, that pointer must be cast as a pointer to an IDispatch interface.</span></span>

<span data-ttu-id="c28c3-178">Le dernier cas codes explicitement le deuxième argument booléen du constructeur avec sa valeur par défaut facultative de la valeur true.</span><span class="sxs-lookup"><span data-stu-id="c28c3-178">The last case explicitly codes the second boolean argument of the constructor with its optional, default value of true.</span></span> <span data-ttu-id="c28c3-179">Cet argument conduit le constructeur **Variant** à appeler la méthode () **AddRef**, qui pour ADO appeler automatiquement le \*\* \_variante\_t::Release\*\*méthode () lors de l’appel de méthode ou la propriété ADO.</span><span class="sxs-lookup"><span data-stu-id="c28c3-179">This argument causes the **Variant** constructor to call its **AddRef**() method, which compensates for ADO automatically calling the **\_variant\_t::Release**() method when the ADO method or property call completes.</span></span>

### <a name="safearray"></a><span data-ttu-id="c28c3-180">SafeArray</span><span class="sxs-lookup"><span data-stu-id="c28c3-180">SafeArray</span></span>

<span data-ttu-id="c28c3-181">**SafeArray** est un type de données structuré qui contient un tableau d'autres types de données.</span><span class="sxs-lookup"><span data-stu-id="c28c3-181">A **SafeArray** is a structured data type that contains an array of other data types.</span></span> <span data-ttu-id="c28c3-182">**SafeArray** est appelée *sans échec* car il contient des informations sur les limites de chaque dimension du tableau et limite l’accès aux éléments du tableau dans ces limites.</span><span class="sxs-lookup"><span data-stu-id="c28c3-182">A **SafeArray** is called *safe* because it contains information about the bounds of each array dimension, and limits access to array elements within those bounds.</span></span>

<span data-ttu-id="c28c3-183">Lorsque la documentation Référence de l'API ADO indique qu'une méthode ou une propriété prend ou retourne un tableau, cela signifie que la méthode ou la propriété prend ou retourne un type **SafeArray**, et non un tableau C/C++ natif.</span><span class="sxs-lookup"><span data-stu-id="c28c3-183">When the ADO API Reference says a method or property takes or returns an array, it means the method or property takes or returns a **SafeArray**, not a native C/C++ array.</span></span>

<span data-ttu-id="c28c3-184">Par exemple, le deuxième paramètre de la méthode **OpenSchema** de l’objet **connexion** requiert un tableau de valeurs **Variant** .</span><span class="sxs-lookup"><span data-stu-id="c28c3-184">For example, the second parameter of the **Connection** object **OpenSchema** method requires an array of **Variant** values.</span></span> <span data-ttu-id="c28c3-185">Ces valeurs **Variant** doivent être transmis en tant qu’éléments d’un **tableau SafeArray**, et ce **tableau SafeArray** doit être définie en tant que la valeur d’un autre **type Variant**.</span><span class="sxs-lookup"><span data-stu-id="c28c3-185">Those **Variant** values must be passed as elements of a **SafeArray**, and that **SafeArray** must be set as the value of another **Variant**.</span></span> <span data-ttu-id="c28c3-186">Il est cet autre **Variant** qui est transmis comme second argument de la **méthode OpenSchema**.</span><span class="sxs-lookup"><span data-stu-id="c28c3-186">It is that other **Variant** that is passed as the second argument of **OpenSchema**.</span></span>

<span data-ttu-id="c28c3-187">Pour prendre d'autres exemples, le premier argument de la méthode **Find** est un **Variant** dont la valeur est un tableau **SafeArray** unidimensionnel ; chacun des deux premiers arguments facultatifs de **AddNew** est un tableau **SafeArray** unidimensionnel ; et la valeur retournée par la méthode **GetRows** est un type **Variant** dont la valeur est un tableau **SafeArray** à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="c28c3-187">As further examples, the first argument of the **Find** method is a **Variant** whose value is a one-dimensional **SafeArray**; each of the optional first and second arguments of **AddNew** is a one-dimensional **SafeArray**; and the return value of the **GetRows** method is a **Variant** whose value is a two-dimensional **SafeArray**.</span></span>

## <a name="missing-and-default-parameters"></a><span data-ttu-id="c28c3-188">Paramètres manquants et par défaut</span><span class="sxs-lookup"><span data-stu-id="c28c3-188">Missing and default parameters</span></span>

<span data-ttu-id="c28c3-p124">Visual Basic autorise les paramètres manquants au niveau des méthodes. Par exemple, la méthode **Open** de l'objet **Recordset** présente cinq paramètres. Or, vous pouvez ignorer les paramètres intermédiaires et omettre les paramètres finaux. Ainsi, une valeur **BSTR** ou **Variant** par défaut leur sera substituée en fonction du type de données de l'opérande manquant.</span><span class="sxs-lookup"><span data-stu-id="c28c3-p124">Visual Basic allows missing parameters in methods. For example, the **Recordset** object **Open** method has five parameters, but you can skip intermediate parameters and leave off trailing parameters. A default **BSTR** or **Variant** will be substituted depending on the data type of the missing operand.</span></span>

<span data-ttu-id="c28c3-192">Dans le cas de C/C++, tous les opérandes doivent être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c28c3-192">In C/C++, all operands must be specified.</span></span> <span data-ttu-id="c28c3-193">Si vous souhaitez spécifier un paramètre manquant dont le type de données est une chaîne, spécifiez une \*\* \_bstr\_t\*\* contenant une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="c28c3-193">If you want to specify a missing parameter whose data type is a string, specify a **\_bstr\_t** containing a null string.</span></span> <span data-ttu-id="c28c3-194">Si vous souhaitez spécifier un paramètre manquant dont le type de données est un **Variant**, spécifiez une \*\* \_variante\_t\*\* avec une valeur d’ED\_E\_PARAMNOTFOUND et un type de VT\_erreur.</span><span class="sxs-lookup"><span data-stu-id="c28c3-194">If you want to specify a missing parameter whose data type is a **Variant**, specify a **\_variant\_t** with a value of DISP\_E\_PARAMNOTFOUND and a type of VT\_ERROR.</span></span> <span data-ttu-id="c28c3-195">Vous pouvez également spécifier l’équivalent \*\* \_variante\_t\*\* constante, **vtMissing**, qui est fourni par le \*\* \#importer\*\* directive.</span><span class="sxs-lookup"><span data-stu-id="c28c3-195">Alternatively, specify the equivalent **\_variant\_t** constant, **vtMissing**, which is supplied by the **\#import** directive.</span></span>

<span data-ttu-id="c28c3-p126">Il existe trois méthodes qui constituent des exceptions à l'utilisation habituelle de **vtMissing**. Il s'agit des méthodes **Execute** des objets **Connection** et **Command**, et de la méthode **NextRecordset** de l'objet **Recordset**. Voici leurs signatures :</span><span class="sxs-lookup"><span data-stu-id="c28c3-p126">Three methods are exceptions to the typical use of **vtMissing**. These are the **Execute** methods of the **Connection** and **Command** objects, and the **NextRecordset** method of the **Recordset** object. The following are their signatures:</span></span>

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

<span data-ttu-id="c28c3-p127">Les paramètres  *RecordsAffected* et *Parameters* sont des pointeurs vers un **Variant**.  *Parameters* est un paramètre d'entrée qui spécifie l'adresse d'un **Variant** contenant un paramètre unique, ou un tableau de paramètres, qui modifiera la commande exécutée.  *RecordsAffected* est un paramètre de sortie qui spécifie l'adresse d'un **Variant** lorsque le nombre de lignes affectées par la méthode est retourné.</span><span class="sxs-lookup"><span data-stu-id="c28c3-p127">The parameters, *RecordsAffected* and *Parameters*, are pointers to a **Variant**. *Parameters* is an input parameter which specifies the address of a **Variant** containing a single parameter, or array of parameters, that will modify the command being executed. *RecordsAffected* is an output parameter that specifies the address of a **Variant**, where the number of rows affected by the method is returned.</span></span>

<span data-ttu-id="c28c3-202">Dans l’objet **Command** méthode **Execute** , indiquer qu’aucun paramètre n’est spécifié en définissant les *paramètres* soit \&vtMissing (ce qui est recommandé) ou le pointeur null (c'est-à-dire, **NULL** ou zéro (0)).</span><span class="sxs-lookup"><span data-stu-id="c28c3-202">In the **Command** object **Execute** method, indicate that no parameters are specified by setting *Parameters* to either \&vtMissing (which is recommended) or to the null pointer (that is, **NULL** or zero (0)).</span></span> <span data-ttu-id="c28c3-203">Si le *paramètre* est défini sur le pointeur null, la méthode remplace en interne l’équivalent de **vtMissing**, puis termine l’opération.</span><span class="sxs-lookup"><span data-stu-id="c28c3-203">If *Parameters* is set to the null pointer, the method internally substitutes the equivalent of **vtMissing**, and then completes the operation.</span></span>

<span data-ttu-id="c28c3-204">Dans toutes les méthodes indiquent que le nombre d’enregistrements affectés ne doit pas être retourné en associant *RecordsAffected* au pointeur null.</span><span class="sxs-lookup"><span data-stu-id="c28c3-204">In all the methods, indicate that the number of records affected should not be returned by setting *RecordsAffected* to the null pointer.</span></span> <span data-ttu-id="c28c3-205">Dans ce cas, le pointeur Null ne représente pas réellement le paramètre manquant mais indique plutôt que la méthode doit ignorer le nombre d'enregistrements affectés.</span><span class="sxs-lookup"><span data-stu-id="c28c3-205">In this case, the null pointer is not so much a missing parameter as an indication that the method should discard the number of records affected.</span></span>

<span data-ttu-id="c28c3-206">Par conséquent, pour ces trois méthodes, le code suivant est approprié :</span><span class="sxs-lookup"><span data-stu-id="c28c3-206">Thus, for these three methods, it is valid to code something such as:</span></span>

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a><span data-ttu-id="c28c3-207">Gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="c28c3-207">Error handling</span></span>

<span data-ttu-id="c28c3-208">Dans COM, la plupart des opérations renvoient un code de retour HRESULT qui indique si une fonction a été correctement exécutée.</span><span class="sxs-lookup"><span data-stu-id="c28c3-208">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="c28c3-209">Le \*\* \#importer\*\* directive génère un code wrapper pour chaque méthode « brute » ou la propriété et vérifie le HRESULT renvoyé.</span><span class="sxs-lookup"><span data-stu-id="c28c3-209">The **\#import** directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="c28c3-210">Si HRESULT indique un échec, le code de wrapper génère une erreur COM en appelant \_com\_problème\_errorex() avec HRESULT retourner le code en tant qu’argument.</span><span class="sxs-lookup"><span data-stu-id="c28c3-210">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="c28c3-211">Les objets d'erreur COM peuvent être interceptés dans un bloc **try**-**catch**.</span><span class="sxs-lookup"><span data-stu-id="c28c3-211">COM error objects can be caught in a **try**-**catch** block.</span></span> <span data-ttu-id="c28c3-212">(Par souci d’efficacité, interceptez une référence à un \*\* \_com\_erreur\*\* objet.)</span><span class="sxs-lookup"><span data-stu-id="c28c3-212">(For efficiency's sake, catch a reference to a **\_com\_error** object.)</span></span>

<span data-ttu-id="c28c3-p131">Rappelez-vous qu'il s'agit d'erreurs ADO : elles sont le résultat de l'échec d'une opération ADO. Les erreurs retournées par le fournisseur sous-jacent apparaissent en tant qu'objets **Error** dans la collection **Errors** de l'objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="c28c3-p131">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object **Errors** collection.</span></span>

<span data-ttu-id="c28c3-215">Le \*\* \#importer\*\* directive crée des erreurs que les routines de gestion pour les méthodes et propriétés déclarées dans le fichier .dll ADO.</span><span class="sxs-lookup"><span data-stu-id="c28c3-215">The **\#import** directive creates only error handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="c28c3-216">Toutefois, vous pouvez tirer parti de ce même mécanisme de gestion des erreurs en écrivant votre propre fonction inline ou macro de détection d'erreurs.</span><span class="sxs-lookup"><span data-stu-id="c28c3-216">However, you can take advantage of this same error handling mechanism by writing your own error checking macro or inline function.</span></span> <span data-ttu-id="c28c3-217">Vous trouverez des exemples dans la rubrique [Extensions Visual C++ pour ADO](visual-c-extensions-for-ado.md), ou le code présenté dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="c28c3-217">See the topic, [Visual C++ Extensions](visual-c-extensions-for-ado.md), or the code in the following sections for examples.</span></span>

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a><span data-ttu-id="c28c3-218">Visual équivalents C++ des conventions Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c28c3-218">Visual C++ equivalents of Visual Basic conventions</span></span>

<span data-ttu-id="c28c3-219">Vous trouverez ci-dessous un récapitulatif de plusieurs conventions décrites dans la documentation ADO, codées en Visual Basic, ainsi que leurs équivalents en Visual C++.</span><span class="sxs-lookup"><span data-stu-id="c28c3-219">The following is a summary of several conventions in the ADO documentation, coded in Visual Basic, as well as their equivalents in Visual C++.</span></span>

### <a name="declaring-an-ado-object"></a><span data-ttu-id="c28c3-220">Déclaration d’un objet ADO</span><span class="sxs-lookup"><span data-stu-id="c28c3-220">Declaring an ADO object</span></span>

<span data-ttu-id="c28c3-221">En langage Visual Basic, une variable d'objet ADO (en l'occurrence, un objet **Recordset** ) est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="c28c3-221">In Visual Basic, an ADO object variable (in this case for a **Recordset** object) is declared as follows:</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
```

<span data-ttu-id="c28c3-222">La clause, « ADODB. Objet Recordset », est le ProgID de l’objet **Recordset** défini dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="c28c3-222">The clause, "ADODB.Recordset", is the ProgID of the **Recordset** object as defined in the Registry.</span></span> <span data-ttu-id="c28c3-223">Une nouvelle instance d'un objet **Record** est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="c28c3-223">A new instance of a **Record** object is declared as follows:</span></span>

```vb 
 
Dim rst As New ADODB.Recordset 
```

<span data-ttu-id="c28c3-224">\-ou -</span><span class="sxs-lookup"><span data-stu-id="c28c3-224">\-or-</span></span>

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

<span data-ttu-id="c28c3-225">Dans Visual C++, la \*\* \#importer\*\* directive génère des déclarations de type pointeur intelligent pour tous les objets ADO.</span><span class="sxs-lookup"><span data-stu-id="c28c3-225">In Visual C++, the **\#import** directive generates smart pointer-type declarations for all the ADO objects.</span></span> <span data-ttu-id="c28c3-226">Par exemple, une variable qui pointe vers un \*\* \_Recordset\*\* objet est de type \*\* \_RecordsetPtr\*\*et est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="c28c3-226">For example, a variable that points to a **\_Recordset** object is of type **\_RecordsetPtr**, and is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs; 
```

<span data-ttu-id="c28c3-227">Une variable qui pointe vers une nouvelle instance d’un \*\* \_Recordset\*\* objet est déclaré comme suit :</span><span class="sxs-lookup"><span data-stu-id="c28c3-227">A variable that points to a new instance of a **\_Recordset** object is declared as follows:</span></span>

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

<span data-ttu-id="c28c3-228">\-ou -</span><span class="sxs-lookup"><span data-stu-id="c28c3-228">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

<span data-ttu-id="c28c3-229">\-ou -</span><span class="sxs-lookup"><span data-stu-id="c28c3-229">\-or-</span></span>

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

<span data-ttu-id="c28c3-230">Une fois que la méthode **CreateInstance** a été appelée, la variable peut être utilisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="c28c3-230">After the **CreateInstance** method is called, the variable can be used as follows:</span></span>

```cpp 
 
rs->Open(...); 
```

<span data-ttu-id="c28c3-231">Notez que dans certains cas, la «. » opérateur est utilisé comme si la variable était une instance d’une classe (rs. (CreateInstance) et dans un autre cas, la «-\>« opérateur est utilisé comme si la variable était un pointeur vers une interface (rs -\>Open).</span><span class="sxs-lookup"><span data-stu-id="c28c3-231">Notice that in one case, the "." operator is used as if the variable were an instance of a class (rs.CreateInstance), and in another case, the "-\>" operator is used as if the variable were a pointer to an interface (rs-\>Open).</span></span>

<span data-ttu-id="c28c3-232">Une variable peut être utilisée de deux façons, car le «-\>» est surchargé pour permettre à une instance d’une classe de se comporter comme un pointeur vers une interface.</span><span class="sxs-lookup"><span data-stu-id="c28c3-232">One variable can be used in two ways because the "-\>" operator is overloaded to allow an instance of a class to behave like a pointer to an interface.</span></span> <span data-ttu-id="c28c3-233">Un membre de classe privée de la variable d’instance contient un pointeur vers le \*\* \_Recordset\*\* interface ; la «-\>« opérateur retourne ce pointeur ; et le pointeur retourné accède aux membres de le \*\* \_Recordset\*\* objet.</span><span class="sxs-lookup"><span data-stu-id="c28c3-233">A private class member of the instance variable contains a pointer to the **\_Recordset** interface; the "-\>" operator returns that pointer; and the returned pointer accesses the members of the **\_Recordset** object.</span></span>

### <a name="coding-a-missing-parameter"></a><span data-ttu-id="c28c3-234">Codage d’un paramètre manquant</span><span class="sxs-lookup"><span data-stu-id="c28c3-234">Coding a missing parameter</span></span>

#### <a name="string"></a><span data-ttu-id="c28c3-235">String</span><span class="sxs-lookup"><span data-stu-id="c28c3-235">String</span></span>

<span data-ttu-id="c28c3-236">Lorsque vous devez coder un opérande **String** manquant en Visual Basic, il vous suffit de l'omettre.</span><span class="sxs-lookup"><span data-stu-id="c28c3-236">When you need to code a missing **String** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="c28c3-237">En Visual C++, vous devez spécifier l'opérande.</span><span class="sxs-lookup"><span data-stu-id="c28c3-237">You must specify the operand in Visual C++.</span></span> <span data-ttu-id="c28c3-238">Code un \*\* \_bstr\_t\*\* qui est une chaîne vide en tant que valeur.</span><span class="sxs-lookup"><span data-stu-id="c28c3-238">Code a **\_bstr\_t** that has an empty string as a value.</span></span>

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a><span data-ttu-id="c28c3-239">Variante</span><span class="sxs-lookup"><span data-stu-id="c28c3-239">Variant</span></span>

<span data-ttu-id="c28c3-240">Lorsque vous devez coder un opérande **Variant** manquant en Visual Basic, il vous suffit de l'omettre.</span><span class="sxs-lookup"><span data-stu-id="c28c3-240">When you need to code a missing **Variant** operand in Visual Basic, you merely omit the operand.</span></span> <span data-ttu-id="c28c3-241">En Visual C++, vous devez spécifier tous les opérandes.</span><span class="sxs-lookup"><span data-stu-id="c28c3-241">You must specify all operands in Visual C++.</span></span> <span data-ttu-id="c28c3-242">Codez un paramètre **Variant** manquant avec un \*\* \_variante\_t\*\* la valeur spéciale, ED\_E\_VT PARAMNOTFOUND et le type\_erreur.</span><span class="sxs-lookup"><span data-stu-id="c28c3-242">Code a missing **Variant** parameter with a **\_variant\_t** set to the special value, DISP\_E\_PARAMNOTFOUND, and type, VT\_ERROR.</span></span> <span data-ttu-id="c28c3-243">Vous pouvez également spécifier **vtMissing**, qui est un équivalent constante prédéfini fournis par le \*\* \#importer\*\* directive.</span><span class="sxs-lookup"><span data-stu-id="c28c3-243">Alternatively, specify **vtMissing**, which is an equivalent pre-defined constant supplied by the **\#import** directive.</span></span>

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

<span data-ttu-id="c28c3-244">\-ou utilisez-</span><span class="sxs-lookup"><span data-stu-id="c28c3-244">\-or use -</span></span>

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a><span data-ttu-id="c28c3-245">Déclaration d’un variant</span><span class="sxs-lookup"><span data-stu-id="c28c3-245">Declaring a variant</span></span>

<span data-ttu-id="c28c3-246">En Visual Basic, un **Variant** est déclaré avec l'instruction **Dim** comme suit :</span><span class="sxs-lookup"><span data-stu-id="c28c3-246">In Visual Basic, a **Variant** is declared with the **Dim** statement as follows:</span></span>

```vb 
 
Dim VariableName As Variant 
```

<span data-ttu-id="c28c3-247">Dans Visual C++, déclarez une variable en tant que type \*\* \_variante\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="c28c3-247">In Visual C++, declare a variable as type **\_variant\_t**.</span></span> <span data-ttu-id="c28c3-248">Schéma quelques \*\* \_variante\_t\*\* déclarations sont présentées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c28c3-248">A few schematic **\_variant\_t** declarations are shown below.</span></span>

> [!NOTE]
> <span data-ttu-id="c28c3-p139">[!REMARQUE] Ces déclarations donnent simplement une idée globale du codage que vous effectueriez dans votre propre programme. Pour plus d'informations, consultez les exemples ci-dessous, ainsi que la documentation Visual C++.</span><span class="sxs-lookup"><span data-stu-id="c28c3-p139">These declarations merely give a rough idea of what you would code in your own program. For more information, see the examples below, and the Visual C++ documentation.</span></span>

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a><span data-ttu-id="c28c3-251">Utilisation de tableaux de variants</span><span class="sxs-lookup"><span data-stu-id="c28c3-251">Using arrays of variants</span></span>

<span data-ttu-id="c28c3-252">En langage Visual Basic, les tableaux de valeurs **Variant** peuvent être codés à l'aide de l'instruction **Dim**. Vous pouvez également utiliser la fonction **Array**, comme illustré dans l'exemple de code suivant :</span><span class="sxs-lookup"><span data-stu-id="c28c3-252">In Visual Basic, arrays of **Variants** can be coded with the **Dim** statement, or you may use the **Array** function, as demonstrated in the following example code:</span></span>

```vb 
 
Public Sub ArrayOfVariants 
Dim cn As ADODB.Connection 
Dim rs As ADODB.Recordset 
Dim fld As ADODB.Field 
 
cn.Open "DSN=pubs", "sa", "" 
rs = cn.OpenSchema(adSchemaColumns, _ 
 Array(Empty, Empty, "authors", Empty)) 
For Each fld in rs.Fields 
 Debug.Print "Name = "; fld.Name 
Next fld 
rs.Close 
cn.Close 
End Sub 
```

<span data-ttu-id="c28c3-253">L’exemple Visual C++ suivant illustre l’utilisation de **SafeArray** utilisé avec un \*\* \_variante\_t\*\*.</span><span class="sxs-lookup"><span data-stu-id="c28c3-253">The following Visual C++ example demonstrates using a **SafeArray** used with a **\_variant\_t**.</span></span>

> [!NOTE]
> <span data-ttu-id="c28c3-254">[!REMARQUE] Les remarques suivantes correspondent aux sections commentées dans l'exemple de code.</span><span class="sxs-lookup"><span data-stu-id="c28c3-254">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="c28c3-255">À nouveau, la fonction inline TESTHR() est définie pour tirer parti d'un mécanisme de gestion des erreurs existant.</span><span class="sxs-lookup"><span data-stu-id="c28c3-255">Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.</span></span>

2. <span data-ttu-id="c28c3-p140">Vous avez seulement besoin d'un tableau unidimensionnel pour pouvoir utiliser **SafeArrayCreateVector** à la place de la déclaration **SAFEARRAYBOUND** et de la fonction **SafeArrayCreate** à usage général. Voici comment se présenterait le code si vous utilisiez **SafeArrayCreate**:</span><span class="sxs-lookup"><span data-stu-id="c28c3-p140">You only need a one-dimensional array, so you can use **SafeArrayCreateVector**, instead of the general purpose **SAFEARRAYBOUND** declaration and **SafeArrayCreate** function. The following is what that code would look like using **SafeArrayCreate**:</span></span>
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. <span data-ttu-id="c28c3-258">Le schéma identifié par la constante énumérée **adSchemaColumns**est associé à quatre colonnes de contrainte : tableau\_catalogue, TABLE\_schéma, TABLE\_nom et la colonne\_nom.</span><span class="sxs-lookup"><span data-stu-id="c28c3-258">The schema identified by the enumerated constant, **adSchemaColumns**, is associated with four constraint columns: TABLE\_CATALOG, TABLE\_SCHEMA, TABLE\_NAME, and COLUMN\_NAME.</span></span> <span data-ttu-id="c28c3-259">Par conséquent, un tableau de valeurs **Variant** à quatre éléments est créé.</span><span class="sxs-lookup"><span data-stu-id="c28c3-259">Therefore, an array of **Variant** values with four elements is created.</span></span> <span data-ttu-id="c28c3-260">Puis une valeur de contrainte qui correspond à la troisième colonne, TABLE\_nom est spécifié.</span><span class="sxs-lookup"><span data-stu-id="c28c3-260">Then a constraint value that corresponds to the third column, TABLE\_NAME, is specified.</span></span> <span data-ttu-id="c28c3-261">Le **jeu d’enregistrements** renvoyé se compose de plusieurs colonnes, un sous-ensemble des colonnes de contrainte.</span><span class="sxs-lookup"><span data-stu-id="c28c3-261">The **Recordset** that is returned consists of several columns, a subset of which is the constraint columns.</span></span> <span data-ttu-id="c28c3-262">Les valeurs des colonnes de contrainte pour chaque ligne renvoyée doivent être la même que les valeurs de contrainte correspondantes.</span><span class="sxs-lookup"><span data-stu-id="c28c3-262">The values of the constraint columns for each returned row must be the same as the corresponding constraint values.</span></span>

4. <span data-ttu-id="c28c3-263">Ceux qui connaissent **SAFEARRAY** peuvent être surpris que **SafeArrayDestroy**() n’est pas appelé avant la sortie.</span><span class="sxs-lookup"><span data-stu-id="c28c3-263">Those familiar with **SafeArrays** may be surprised that **SafeArrayDestroy**() is not called before the exit.</span></span> <span data-ttu-id="c28c3-264">En fait, appel **SafeArrayDestroy**() dans ce cas entraînerait une exception d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c28c3-264">In fact, calling **SafeArrayDestroy**() in this case will cause a run-time exception.</span></span> <span data-ttu-id="c28c3-265">Parce que l’appel de destructeur SafeArrayDestroy **_variant_t**lors de la \*\* \_variante\_t\*\* est hors de portée, ce qui libère **SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="c28c3-265">The reason is that the destructor for vtCriteria will call **VariantClear**() when the **\_variant\_t** goes out of scope, which will free the **SafeArray**.</span></span> <span data-ttu-id="c28c3-266">L’appel de **SafeArrayDestroy**, sans suppression manuelle de la \*\* \_variant\_t\*\*, provoque le destructeur tenter d’effacer un pointeur **SafeArray** non valide.</span><span class="sxs-lookup"><span data-stu-id="c28c3-266">Calling **SafeArrayDestroy**, without manually clearing the **\_variant\_t**, would cause the destructor to try to clear an invalid **SafeArray** pointer.</span></span> <span data-ttu-id="c28c3-267">Si **SafeArrayDestroy** était appelé, le code se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="c28c3-267">If **SafeArrayDestroy** were called, the code would look like this:</span></span>
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   <span data-ttu-id="c28c3-268">Toutefois, il est beaucoup plus simple de laisser la \*\* \_variante\_t\*\* gérer le **tableau SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="c28c3-268">However, it is much simpler to let the **\_variant\_t** manage the **SafeArray**.</span></span>


```cpp 
 
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
    
    // Note 1 
    inline void TESTHR( HRESULT _hr ) 
    { if FAILED(_hr) _com_issue_error(_hr); } 
    
    void main(void) 
    { 
    CoInitialize(NULL); 
    try 
    { 
    _RecordsetPtr pRs("ADODB.Recordset"); 
    _ConnectionPtr pCn("ADODB.Connection"); 
    _variant_t vtTableName("authors"), 
    vtCriteria; 
    long ix[1]; 
    SAFEARRAY *pSa = NULL; 
    
    pCn->Open("DSN=pubs;User ID=MyUserId;pwd=MyPassword;Provider=MSDASQL;", "", "", 
    adConnectUnspecified); 
    // Note 2, Note 3 
    pSa = SafeArrayCreateVector(VT_VARIANT, 1, 4); 
    if (!pSa) _com_issue_error(E_OUTOFMEMORY); 
    
    // Specify TABLE_NAME in the third array element (index of 2). 
    
    ix[0] = 2; 
    TESTHR(SafeArrayPutElement(pSa, ix, &vtTableName)); 
    
    // There is no Variant constructor for a SafeArray, so manually set the 
    // type (SafeArray of Variant) and value (pointer to a SafeArray). 
    
    vtCriteria.vt = VT_ARRAY | VT_VARIANT; 
    vtCriteria.parray = pSa; 
    
    pRs = pCn->OpenSchema(adSchemaColumns, vtCriteria, vtMissing); 
    
    long limit = pRs->GetFields()->Count; 
    for (long x = 0; x < limit; x++) 
    printf("%d: %s\n", x+1, 
    ((char*) pRs->GetFields()->Item[x]->Name)); 
    // Note 4 
    pRs->Close(); 
    pCn->Close(); 
    } 
    catch (_com_error &e) 
    { 
    printf("Error:\n"); 
    printf("Code = %08lx\n", e.Error()); 
    printf("Code meaning = %s\n", (char*) e.ErrorMessage()); 
    printf("Source = %s\n", (char*) e.Source()); 
    printf("Description = %s\n", (char*) e.Description()); 
    } 
    CoUninitialize(); 
    } 
```

### <a name="using-property-getputputref"></a><span data-ttu-id="c28c3-269">À l’aide de la propriété Get/Put/PutRef</span><span class="sxs-lookup"><span data-stu-id="c28c3-269">Using property Get/Put/PutRef</span></span>

<span data-ttu-id="c28c3-270">En langage Visual Basic, le fait que le nom d'une propriété soit récupéré, attribué ou qu'une référence lui soit attribuée ne suffit pas à le qualifier.</span><span class="sxs-lookup"><span data-stu-id="c28c3-270">In Visual Basic, the name of a property is not qualified by whether it is retrieved, assigned, or assigned a reference.</span></span>

```vb
    Public Sub GetPutPutRef 
    Dim rs As New ADODB.Recordset 
    Dim cn As New ADODB.Connection 
    Dim sz as Integer 
    cn.Open "Provider=sqloledb;Data Source=yourserver;" & _ 
     "Initial Catalog=pubs;Integrated Security=SSPI;" 
    rs.PageSize = 10 
    sz = rs.PageSize 
    rs.ActiveConnection = cn 
    rs.Open "authors",,adOpenStatic 
    ' ... 
    rs.Close 
    cn.Close 
    End Sub
```

<span data-ttu-id="c28c3-271">Cet exemple Visual C++ illustre l' **obtenir**/**Put**/\**PutRef \*\*\* propriété*.</span><span class="sxs-lookup"><span data-stu-id="c28c3-271">This Visual C++ example demonstrates the **Get**/**Put**/\**PutRef\*\*\*Property*.</span></span>

> [!NOTE]
> <span data-ttu-id="c28c3-272">[!REMARQUE] Les remarques suivantes correspondent aux sections commentées dans l'exemple de code.</span><span class="sxs-lookup"><span data-stu-id="c28c3-272">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="c28c3-273">Cet exemple utilise deux formes d’un argument de chaîne manquante : une constante explicite, **strMissing**et une chaîne que le compilateur utilisera pour créer un fichier temporaire \*\* \_bstr\_t\*\* qui existent pour l’étendue de la méthode **Open** .</span><span class="sxs-lookup"><span data-stu-id="c28c3-273">This example uses two forms of a missing string argument: an explicit constant, **strMissing**, and a string that the compiler will use to create a temporary **\_bstr\_t** that will exist for the scope of the **Open** method.</span></span>

2. <span data-ttu-id="c28c3-274">Il n’est pas nécessaire d’effectuer un cast de l’opérande de rs -\>PutRefActiveConnection (CN) à (IDispatch \*), car le type de l’opérande est déjà (IDispatch \*).</span><span class="sxs-lookup"><span data-stu-id="c28c3-274">It isn't necessary to cast the operand of rs-\>PutRefActiveConnection(cn) to (IDispatch \*) because the type of the operand is already (IDispatch \*).</span></span>
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr cn("ADODB.Connection"); 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _bstr_t strMissing(L""); 
     long oldPgSz = 0, 
     newPgSz = 5; 
     
    // Note 1 
     cn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     strMissing, "", 
     adConnectUnspecified); 
     
     oldPgSz = rs->GetPageSize(); 
     // -or- 
     oldPgSz = rs->PageSize; 
     
     rs->PutPageSize(newPgSz); 
     // -or- 
     rs->PageSize = newPgSz; 
     
    // Note 2 
     rs->PutRefActiveConnection( cn ); 
     rs->Open("authors", vtMissing, adOpenStatic, adLockReadOnly, 
     adCmdTable); 
     printf("Original pagesize = %d, new pagesize = %d\n", oldPgSz, 
     rs->GetPageSize()); 
     rs->Close(); 
     cn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = %s\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="using-getitemx-and-itemx"></a><span data-ttu-id="c28c3-275">À l’aide de GetItem (x) et un élément\[x\]</span><span class="sxs-lookup"><span data-stu-id="c28c3-275">Using GetItem(x) and Item\[x\]</span></span>

<span data-ttu-id="c28c3-276">Cet exemple Visual Basic illustre la syntaxe standard et alternative de **Item**().</span><span class="sxs-lookup"><span data-stu-id="c28c3-276">This Visual Basic example demonstrates the standard and alternative syntax for **Item**().</span></span>

```vb 
 
Public Sub GetItemItem 
Dim rs As New ADODB.Recordset 
Dim name as String 
rs = rs.Open "authors", "DSN=pubs;", adOpenDynamic, _ 
 adLockBatchOptimistic, adTable 
name = rs(0) 
' -or- 
name = rs.Fields.Item(0) 
rs(0) = "Test" 
rs.UpdateBatch 
' Restore name 
rs(0) = name 
rs.UpdateBatch 
rs.Close 
End Sub 
```

<span data-ttu-id="c28c3-277">Cet exemple Visual C++ illustre **Item**.</span><span class="sxs-lookup"><span data-stu-id="c28c3-277">This Visual C++ example demonstrates **Item**.</span></span>

> [!NOTE]
> <span data-ttu-id="c28c3-278">[!REMARQUE] La remarque suivante correspond aux sections commentées dans l'exemple de code.</span><span class="sxs-lookup"><span data-stu-id="c28c3-278">The following note corresponds to commented sections in the code example.</span></span>

1. <span data-ttu-id="c28c3-279">Lorsque l'accès à la collection s'effectue avec **Item**, l'index **2** doit être casté en **long** pour permettre l'appel d'un constructeur approprié.</span><span class="sxs-lookup"><span data-stu-id="c28c3-279">When the collection is accessed with **Item**, the index, **2**, must be cast to **long** so an appropriate constructor will be invoked.</span></span>
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try { 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _variant_t vtFirstName; 
     
     rs->Open("authors", 
     "Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     adOpenStatic, adLockOptimistic, adCmdTable); 
     rs->MoveFirst(); 
     
    // Note 1. Get a field. 
     vtFirstName = rs->Fields->GetItem((long)2)->GetValue(); 
     // -or- 
     vtFirstName = rs->Fields->Item[(long)2]->Value; 
     
     printf( "First name = '%s'\n", (char*) ((_bstr_t) vtFirstName)); 
     
     rs->Fields->GetItem((long)2)->Value = L"TEST"; 
     rs->Update(vtMissing, vtMissing); 
     
     // Restore name 
     rs->Fields->GetItem((long)2)->PutValue(vtFirstName); 
     // -or- 
     rs->Fields->GetItem((long)2)->Value = vtFirstName; 
     rs->Update(vtMissing, vtMissing); 
     rs->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
   ```

### <a name="casting-ado-object-pointers-with-idispatch-"></a><span data-ttu-id="c28c3-280">Conversion de pointeurs d'objet ADO à l'aide de (IDispatch \*)</span><span class="sxs-lookup"><span data-stu-id="c28c3-280">Casting ADO object pointers with (IDispatch \*)</span></span>

<span data-ttu-id="c28c3-281">L'exemple Visual C++ suivant illustre l'utilisation de (IDispatch \*) pour effectuer un cast des pointeurs d'objet ADO.</span><span class="sxs-lookup"><span data-stu-id="c28c3-281">The following Visual C++ example demonstrates using (IDispatch \*) to cast ADO object pointers.</span></span>

> [!NOTE]
> <span data-ttu-id="c28c3-282">[!REMARQUE] Les remarques suivantes correspondent aux sections commentées dans l'exemple de code.</span><span class="sxs-lookup"><span data-stu-id="c28c3-282">The following notes correspond to commented sections in the code example.</span></span>

1. <span data-ttu-id="c28c3-283">Spécifiez un objet **Connection** ouvert dans un **Variant** explicitement codé.</span><span class="sxs-lookup"><span data-stu-id="c28c3-283">Specify an open **Connection** object in an explicitly coded **Variant**.</span></span> <span data-ttu-id="c28c3-284">Effectuer un cast avec (IDispatch \*) afin que le constructeur approprié est appelé.</span><span class="sxs-lookup"><span data-stu-id="c28c3-284">Cast it with (IDispatch \*) so the correct constructor will be invoked.</span></span> <span data-ttu-id="c28c3-285">En outre, définir explicitement la seconde \*\* \_variante\_t\*\* sur la valeur par défaut de **la valeur true**, afin que le décompte de références d’objet soit correct lors de l’opération **Recordset::Open** .</span><span class="sxs-lookup"><span data-stu-id="c28c3-285">Also, explicitly set the second **\_variant\_t** parameter to the default value of **true**, so the object reference count will be correct when the **Recordset::Open** operation ends.</span></span>

2. <span data-ttu-id="c28c3-286">L’expression, (\_bstr\_t), n’est pas un cast, mais un \*\* \_variante\_t\*\* opérateur qui extrait une \*\* \_bstr\_t\*\* chaîne de **type Variant** retourné par **valeur**.</span><span class="sxs-lookup"><span data-stu-id="c28c3-286">The expression, (\_bstr\_t), is not a cast, but a **\_variant\_t** operator that extracts a **\_bstr\_t** string from the **Variant** returned by **Value**.</span></span> <span data-ttu-id="c28c3-287">L’expression (char\*), n’est pas un cast, mais un \*\* \_bstr\_t\*\* opérateur qui extrait un pointeur vers la chaîne encapsulé dans un \*\* \_bstr\_t\*\* objet.</span><span class="sxs-lookup"><span data-stu-id="c28c3-287">The expression, (char\*), is not a cast, but a **\_bstr\_t** operator that extracts a pointer to the encapsulated string in a **\_bstr\_t** object.</span></span> <span data-ttu-id="c28c3-288">Cette section de code illustre certains comportements utiles de \*\* \_variante\_t\*\* et \*\* \_bstr\_t\*\* opérateurs.</span><span class="sxs-lookup"><span data-stu-id="c28c3-288">This section of code demonstrates some of the useful behaviors of **\_variant\_t** and **\_bstr\_t** operators.</span></span>
    
   ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
     
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr pConn("ADODB.Connection"); 
     _RecordsetPtr pRst("ADODB.Recordset"); 
     
     pConn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     "", "", adConnectUnspecified); 
    // Note 1. 
     pRst->Open( 
     "authors", 
     _variant_t((IDispatch *) pConn, true), 
     adOpenStatic, 
     adLockReadOnly, 
     adCmdTable); 
     pRst->MoveLast(); 
    // Note 2. 
     printf("Last name is '%s %s'\n", 
     (char*) ((_bstr_t) pRst->GetFields()->GetItem("au_fname")->GetValue()), 
     (char*) ((_bstr_t) pRst->Fields->Item["au_lname"]->Value)); 
     
     pRst->Close(); 
     pConn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
    ::CoUninitialize(); 
    } 
   ```

