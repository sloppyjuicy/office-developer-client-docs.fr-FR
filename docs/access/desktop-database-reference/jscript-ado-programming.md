---
title: Programmation ADO en Jscript
TOCTitle: JScript ADO Programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 167033c58b163ffcef7934b6f38b79323c6b58b1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470204"
---
# <a name="jscript-ado-programming"></a>Programmation ADO en Jscript


**S’applique à**: Access 2013 | Office 2013


## <a name="creating-an-ado-project"></a>Création d'un projet ADO

Microsoft JScript ne prend pas en charge les bibliothèque de types ; vous n'avez donc pas besoin de référencer ADO dans votre projet. Par conséquent, aucune fonctionnalité associée, telle que l'exécution des lignes de commande, n'est prise en charge. Enfin, les constantes énumérées ADO ne sont, par défaut, pas définies dans JScript.

En revanche, ADO comporte deux fichiers contenant les définitions suivantes à utiliser avec JScript :

- Pour côté serveur scripts, utilisez Adojavas.inc, installé dans le répertoire c:\\Program Files\\Common Files\\système\\ado\\ dossier par défaut.

- Pour côté client scripts, utilisez Adcjavas.inc, installé dans le répertoire c:\\Program Files\\Common Files\\système\\msdac\\ dossier par défaut.

Vous pouvez soit copier et coller les définitions des constantes de ces fichiers dans vos pages ASP ou, si vous effectuez des scripts côté serveur, copiez le fichier Adojavas.inc dans un dossier sur votre site Web et fait référence à partir de votre page ASP comme suit :

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a>Création d'objets ADO en JScript

Vous devez, pour cela, utiliser l'appel de fonction **CreateObject**:

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a>Exemple JScript

Le code suivant est un exemple générique de programmation côté serveur en JScript dans un fichier ASP (Active Server Page) qui ouvre un objet **Recordset**:

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

