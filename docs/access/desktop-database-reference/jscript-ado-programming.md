---
title: Programmation ADO JScript
TOCTitle: JScript ADO programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 88a84f6fa3604286ca27651cefc999c96ff41d0e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708970"
---
# <a name="jscript-ado-programming"></a><span data-ttu-id="097b2-102">Programmation ADO JScript</span><span class="sxs-lookup"><span data-stu-id="097b2-102">JScript ADO programming</span></span>


<span data-ttu-id="097b2-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="097b2-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="creating-an-ado-project"></a><span data-ttu-id="097b2-104">Création d'un projet ADO</span><span class="sxs-lookup"><span data-stu-id="097b2-104">Creating an ADO Project</span></span>

<span data-ttu-id="097b2-p101">Microsoft JScript ne prend pas en charge les bibliothèque de types ; vous n'avez donc pas besoin de référencer ADO dans votre projet. Par conséquent, aucune fonctionnalité associée, telle que l'exécution des lignes de commande, n'est prise en charge. Enfin, les constantes énumérées ADO ne sont, par défaut, pas définies dans JScript.</span><span class="sxs-lookup"><span data-stu-id="097b2-p101">Microsoft JScript does not support type libraries, so you do not need to reference ADO in your project. Consequently, no associated features such as command line completion are supported. Also, by default, ADO enumerated constants are not defined in JScript.</span></span>

<span data-ttu-id="097b2-108">En revanche, ADO comporte deux fichiers contenant les définitions suivantes à utiliser avec JScript :</span><span class="sxs-lookup"><span data-stu-id="097b2-108">However, ADO provides you with two include files containing the following definitions to be used with JScript:</span></span>

- <span data-ttu-id="097b2-109">Pour côté serveur scripts, utilisez Adojavas.inc, installé dans le répertoire c:\\Program Files\\Common Files\\système\\ado\\ dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="097b2-109">For server-side scripting use Adojavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

- <span data-ttu-id="097b2-110">Pour côté client scripts, utilisez Adcjavas.inc, installé dans le répertoire c:\\Program Files\\Common Files\\système\\msdac\\ dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="097b2-110">For client-side scripting use Adcjavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="097b2-111">Vous pouvez soit copier et coller les définitions des constantes de ces fichiers dans vos pages ASP ou, si vous effectuez des scripts côté serveur, copiez le fichier Adojavas.inc dans un dossier sur votre site Web et fait référence à partir de votre page ASP comme suit :</span><span class="sxs-lookup"><span data-stu-id="097b2-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adojavas.inc file to a folder on your website and references it from your ASP page like this:</span></span>

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a><span data-ttu-id="097b2-112">Création d'objets ADO en JScript</span><span class="sxs-lookup"><span data-stu-id="097b2-112">Creating ADO Objects in JScript</span></span>

<span data-ttu-id="097b2-113">Vous devez, pour cela, utiliser l'appel de fonction **CreateObject**:</span><span class="sxs-lookup"><span data-stu-id="097b2-113">You must instead use the **CreateObject** function call:</span></span>

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a><span data-ttu-id="097b2-114">Exemple JScript</span><span class="sxs-lookup"><span data-stu-id="097b2-114">JScript Example</span></span>

<span data-ttu-id="097b2-115">Le code suivant est un exemple générique de programmation côté serveur en JScript dans un fichier ASP (Active Server Page) qui ouvre un objet **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="097b2-115">The following code is a generic example of JScript server-side programming in an Active Server Page (ASP) file that opens a **Recordset** object:</span></span>

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

