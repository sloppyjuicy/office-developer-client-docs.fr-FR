---
title: Programmation ADO en VBScript
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 781019e44248866f6926e58bb3f75e9b044c4e4e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593305"
---
# <a name="vbscript-ado-programming"></a>Programmation ADO VBScript


**S’applique à** : Access 2013, Office 2013 

## <a name="creating-an-ado-project"></a>Création d'un projet ADO

Microsoft Visual Basic Scripting Edition ne prend pas en charge les bibliothèque de types ; vous n'avez donc pas besoin de référencer ADO dans votre projet. Par conséquent, aucune fonctionnalité associée, telle que l'exécution des lignes de commande, n'est prise en charge. Enfin, les constantes énumérées ADO ne sont, par défaut, pas définies dans VBScript.

En revanche, ADO comporte deux fichiers contenant les définitions suivantes à utiliser avec VBScript :

  - Pour les scripts côté serveur, utilisez Adovbs.inc, qui est installé dans le dossier c: \\ Program Files Common Files System \\ \\ \\ ado par \\ défaut.

  - Pour les scripts côté client, utilisez Adcvbs.inc, qui est installé par défaut dans le dossier \\ \\ \\ \\ msdac du système de fichiers communs program \\ files.

Vous pouvez copier et coller des définitions de constantes de ces fichiers dans vos pages ASP ou, si vous faites des scripts côté serveur, copiez le fichier Adovbs.inc dans un dossier de votre site web et faites-le référencer à partir de votre page ASP comme ceci :

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a>Création d'objets ADO dans VBScript

Vous ne pouvez pas utiliser l'instruction **Dim** pour assigner des objets à un type spécifique dans VBScript. En outre, VBScript ne prend pas en charge la syntaxe **New** utilisée avec l'instruction **Dim** dans Visual Basic pour Applications. Vous devez donc utiliser à la place l'appel de fonction **CreateObject** :

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a>Exemples VBScript

Le code suivant est un exemple générique de programmation côté serveur en VBScript dans un fichier ASP (Active Server Page) :

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

La documentation ADO contient des exemples VBScript plus spécifiques. Pour plus d’informations, voir [des exemples de code ADO dans Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).

## <a name="differences-between-vbscript-and-visual-basic"></a>Différences entre VBScript et Visual Basic

À plusieurs égards, l'utilisation d'ADO avec VBScript ou avec Visual Basic présente de nombreuses similitudes, notamment dans la manière dont la syntaxe est utilisée. En revanche, des différences importantes existent :

- VBScript ne prend en charge que le type de données Variant qui peut contenir différents types de données. Vous pouvez stocker les données dont vous avez besoin dans un type de données Variant et elles fonctionneront correctement grâce au casting effectué par VBScript. Celui-ci reconnaît le type requis par ADO et convertit en conséquence la valeur dans le type Variant.

- Vous ne pouvez pas `on error goto <label>` l’utiliser dans VBScript.

- VBScript prend en charge certaines fonctions Visual Basic intégrées, telles que **Msgbox**, **Date** et **IsNumeric**. En revanche, dans la mesure où VBScript est un sous-ensemble de Visual Basic, toutes les fonctions intégrées ne sont pas prises en charge. Par exemple, VBScript ne prend pas en charge la fonction **Format** et les fonctions d'E/S de fichier.

