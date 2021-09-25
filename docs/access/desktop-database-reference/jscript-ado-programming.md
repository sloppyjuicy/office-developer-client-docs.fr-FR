---
title: Programmation ADO JScript
TOCTitle: JScript ADO programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0587f2d07342d97695524859ebca10248e70d931
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562600"
---
# <a name="jscript-ado-programming"></a>Programmation ADO JScript


**S’applique à** : Access 2013, Office 2013


## <a name="creating-an-ado-project"></a>Création d'un projet ADO

Microsoft JScript ne prend pas en charge les bibliothèque de types ; vous n'avez donc pas besoin de référencer ADO dans votre projet. Par conséquent, aucune fonctionnalité associée, telle que l'exécution des lignes de commande, n'est prise en charge. Enfin, les constantes énumérées ADO ne sont, par défaut, pas définies dans JScript.

En revanche, ADO comporte deux fichiers contenant les définitions suivantes à utiliser avec JScript :

- Pour les scripts côté serveur, utilisez Adojavas.inc, qui est installé dans le dossier c: \\ Program Files Common Files System \\ \\ \\ ado par \\ défaut.

- Pour les scripts côté client, utilisez Adcjavas.inc, qui est installé par défaut dans le dossier \\ \\ \\ \\ msdac du système de fichiers communs program \\ files.

Vous pouvez copier et coller des définitions de constantes de ces fichiers dans vos pages ASP, ou, si vous faites des scripts côté serveur, copiez le fichier Adojavas.inc dans un dossier de votre site web et référencez-le à partir de votre page ASP comme ceci :

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a>Création d'objets ADO en JScript

Vous devez, pour cela, utiliser l'appel de fonction **CreateObject** :

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a>Exemple JScript

Le code suivant est un exemple générique de programmation côté serveur en JScript dans un fichier ASP (Active Server Page) qui ouvre un objet **Recordset** :

```javascript 
 
<%  @LANGUAGE="JScript" %> 
<!--#include File="adojavas.inc"--> 
<HTML> 
<BODY BGCOLOR="White" topmargin="10" leftmargin="10"> 
<% 
var Source = "SELECT * FROM Authors"; 
var Connect =  "Provider=sqloledb;Data Source=srv;" + 
    "Initial Catalog=Pubs;Integrated Security=SSPI;" 
var Rs1 = Server.CreateObject( "ADODB.Recordset.2.5" ); 
Rs1.Open(Source,Connect,adOpenForwardOnly); 
Response.Write("Success!"); 
%> 
</BODY> 
</HTML> 
```

