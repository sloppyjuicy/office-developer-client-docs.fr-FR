---
title: Programmation ADO en VBScript
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7e91eedbb790eabd49cfacc83b37a9db8cfad720
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867670"
---
# <a name="vbscript-ado-programming"></a><span data-ttu-id="8347e-102">Programmation ADO en VBScript</span><span class="sxs-lookup"><span data-stu-id="8347e-102">VBScript ADO Programming</span></span>


<span data-ttu-id="8347e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8347e-103">**Applies to**: Access 2013, Office 2013</span></span> 

## <a name="creating-an-ado-project"></a><span data-ttu-id="8347e-104">Création d'un projet ADO</span><span class="sxs-lookup"><span data-stu-id="8347e-104">Creating an ADO Project</span></span>

<span data-ttu-id="8347e-p101">Microsoft Visual Basic Scripting Edition ne prend pas en charge les bibliothèque de types ; vous n'avez donc pas besoin de référencer ADO dans votre projet. Par conséquent, aucune fonctionnalité associée, telle que l'exécution des lignes de commande, n'est prise en charge. Enfin, les constantes énumérées ADO ne sont, par défaut, pas définies dans VBScript.</span><span class="sxs-lookup"><span data-stu-id="8347e-p101">Microsoft Visual Basic, Scripting Edition does not support type libraries, so you do not need to reference ADO in your project. Consequently, no associated features such as command line completion are supported. Also, by default, ADO enumerated constants are not defined in VBScript.</span></span>

<span data-ttu-id="8347e-108">En revanche, ADO comporte deux fichiers contenant les définitions suivantes à utiliser avec VBScript :</span><span class="sxs-lookup"><span data-stu-id="8347e-108">However, ADO provides you with two include files containing the following definitions to be used with VBScript:</span></span>

  - <span data-ttu-id="8347e-109">Pour côté serveur script, utilisez Adovbs.inc qui est installé dans le répertoire c:\\Program Files\\Common Files\\système\\ado\\ dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="8347e-109">For server-side scripting use Adovbs.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

  - <span data-ttu-id="8347e-110">Pour côté client script, utilisez Adcvbs.inc qui est installé dans le répertoire c:\\Program Files\\Common Files\\système\\msdac\\ dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="8347e-110">For client-side scripting use Adcvbs.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="8347e-111">Vous pouvez soit copier et coller les définitions des constantes de ces fichiers dans vos pages ASP ou, si vous effectuez des scripts côté serveur, copiez fichier Adovbs.inc dans un dossier sur votre site Web et son référencement dans votre page ASP comme suit :</span><span class="sxs-lookup"><span data-stu-id="8347e-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adovbs.inc file to a folder on your website and referencing it from your ASP page like this:</span></span>

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a><span data-ttu-id="8347e-112">Création d'objets ADO dans VBScript</span><span class="sxs-lookup"><span data-stu-id="8347e-112">Creating ADO Objects in VBScript</span></span>

<span data-ttu-id="8347e-p102">Vous ne pouvez pas utiliser l'instruction **Dim** pour assigner des objets à un type spécifique dans VBScript. En outre, VBScript ne prend pas en charge la syntaxe **New** utilisée avec l'instruction **Dim** dans Visual Basic pour Applications. Vous devez donc utiliser à la place l'appel de fonction **CreateObject**:</span><span class="sxs-lookup"><span data-stu-id="8347e-p102">You cannot use the **Dim** statement to assign objects to a specific type in VBScript. Also, VBScript does not support the **New** syntax used with the **Dim** statement in Visual Basic for Applications. You must instead use the **CreateObject** function call:</span></span>

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a><span data-ttu-id="8347e-116">Exemples VBScript</span><span class="sxs-lookup"><span data-stu-id="8347e-116">VBScript Examples</span></span>

<span data-ttu-id="8347e-117">Le code suivant est un exemple générique de programmation côté serveur en VBScript dans un fichier ASP (Active Server Page) :</span><span class="sxs-lookup"><span data-stu-id="8347e-117">The following code is a generic example of VBScript server-side programming in an Active Server Page (ASP) file:</span></span>

```vb 
 
<%  @LANGUAGE="VBSCRIPT" %> 
<%  Option Explicit %> 
<!--#include File="adovbs.inc"--> 
<HTML> 
    <BODY BGCOLOR="White" topmargin="10" leftmargin="10"> 
 
    <!-- Your ASP Code goes here --> 
<% 
Dim Source 
Dim Connect 
Dim Rs1 
     
Source = "SELECT * FROM Authors" 
Connect = "Provider=sqloledb;Data Source=srv;" & _ 
    "Initial Catalog=Pubs;Integrated Security=SSPI;" 
 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
Rs1.Open Source, Connect, adOpenForwardOnly 
Response.Write("Success!") 
%> 
    </BODY> 
</HTML> 
```

<span data-ttu-id="8347e-118">La documentation ADO contient des exemples VBScript plus spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8347e-118">More specific VBScript examples are included with the ADO documentation.</span></span> <span data-ttu-id="8347e-119">Pour plus d’informations, voir [exemples de code ADO en Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).</span><span class="sxs-lookup"><span data-stu-id="8347e-119">For more information, see [ADO code examples in Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).</span></span>

## <a name="differences-between-vbscript-and-visual-basic"></a><span data-ttu-id="8347e-120">Différences entre VBScript et Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8347e-120">Differences Between VBScript and Visual Basic</span></span>

<span data-ttu-id="8347e-p104">À plusieurs égards, l'utilisation d'ADO avec VBScript ou avec Visual Basic présente de nombreuses similitudes, notamment dans la manière dont la syntaxe est utilisée. En revanche, des différences importantes existent :</span><span class="sxs-lookup"><span data-stu-id="8347e-p104">Using ADO with VBScript is similar to using ADO with Visual Basic in many ways, including how syntax is used. However, some significant differences exist:</span></span>

- <span data-ttu-id="8347e-p105">VBScript ne prend en charge que le type de données Variant qui peut contenir différents types de données. Vous pouvez stocker les données dont vous avez besoin dans un type de données Variant et elles fonctionneront correctement grâce au casting effectué par VBScript. Celui-ci reconnaît le type requis par ADO et convertit en conséquence la valeur dans le type Variant.</span><span class="sxs-lookup"><span data-stu-id="8347e-p105">VBScript supports only the Variant data type, which can hold different types of data. You can store the data you need in a Variant data type, and the data will function appropriately due to casting performed by VBScript. It recognizes the type required by ADO, and converts the value in the Variant accordingly.</span></span>

- <span data-ttu-id="8347e-126">Vous ne pouvez pas utiliser `on error goto <label>` dans VBScript.</span><span class="sxs-lookup"><span data-stu-id="8347e-126">You cannot use `on error goto <label>` within VBScript.</span></span>

- <span data-ttu-id="8347e-p106">VBScript prend en charge certaines fonctions Visual Basic intégrées, telles que **Msgbox**, **Date** et **IsNumeric**. En revanche, dans la mesure où VBScript est un sous-ensemble de Visual Basic, toutes les fonctions intégrées ne sont pas prises en charge. Par exemple, VBScript ne prend pas en charge la fonction **Format** et les fonctions d'E/S de fichier.</span><span class="sxs-lookup"><span data-stu-id="8347e-p106">VBScript supports some of the built-in Visual Basic functions such as **Msgbox**, **Date**, and **IsNumeric**. However, because VBScript is a subset of Visual Basic, not all built-in functions are supported. For example, VBScript does not support the **Format** function and the file I/O functions.</span></span>

