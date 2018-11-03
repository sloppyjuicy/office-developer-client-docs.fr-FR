---
title: Didacticiel RDS (VBScript)
TOCTitle: RDS tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1c6b42d9560a30b45fb777bb4fd1de4351830a4
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936293"
---
# <a name="rds-tutorial-vbscript"></a><span data-ttu-id="9fe11-102">Didacticiel RDS (VBScript)</span><span class="sxs-lookup"><span data-stu-id="9fe11-102">RDS tutorial (VBScript)</span></span>

<span data-ttu-id="9fe11-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9fe11-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9fe11-104">Il s’agit du didacticiel RDS, écrit en Microsoft Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="9fe11-104">This is the RDS tutorial, written in Microsoft Visual Basic Scripting Edition.</span></span> <span data-ttu-id="9fe11-105">Pour obtenir une description de l’objectif de ce didacticiel, consultez le [didacticiel RDS](chapter-12-rds-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="9fe11-105">For a description of the purpose of this tutorial, see the [RDS tutorial](chapter-12-rds-tutorial.md).</span></span>

<span data-ttu-id="9fe11-106">Dans ce didacticiel, [RDS. DataControl](datacontrol-object-rds.md) et [RDS. DataSpace](dataspace-object-rds.md) sont créés au moment du design ; Autrement dit, ils sont définis avec des balises object.</span><span class="sxs-lookup"><span data-stu-id="9fe11-106">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time; that is, they are defined with object tags.</span></span> <span data-ttu-id="9fe11-107">Il est également possible de les créer au moment de l'exécution à l'aide de la méthode **Server.CreateObject**.</span><span class="sxs-lookup"><span data-stu-id="9fe11-107">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> 

<span data-ttu-id="9fe11-108">Par exemple, l'objet **RDS.DataControl** peut être créé de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="9fe11-108">For example, the **RDS.DataControl** object could be created like this:</span></span>

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

## <a name="step-1--specify-a-server-program"></a><span data-ttu-id="9fe11-109">Étape 1 : spécifier un programme serveur</span><span class="sxs-lookup"><span data-stu-id="9fe11-109">Step 1 — Specify a server program</span></span>

<span data-ttu-id="9fe11-110">VBScript peut détecter le nom du serveur web IIS qu'exécute en accédant à la méthode VBScript **Request.ServerVariables** disponible pour les Pages ASP :</span><span class="sxs-lookup"><span data-stu-id="9fe11-110">VBScript can discover the name of the IIS web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="9fe11-111">Toutefois, dans ce didacticiel, utilisez le serveur fictif « yourServer ».</span><span class="sxs-lookup"><span data-stu-id="9fe11-111">However, for this tutorial, use the imaginary server, "yourServer."</span></span>

> [!NOTE]
> <P><span data-ttu-id="9fe11-p103">[!REMARQUE] Soyez attentif au type de données des arguments <STRONG>ByRef</STRONG>. VBScript ne vous autorisant pas à spécifier le type de variable, vous devez toujours transmettre un type Variant. Si vous utilisez HTTP, RDS vous autorise à transmettre un type Variant à une méthode qui n'attend pas ce type de données si vous l'appelez avec la méthode <STRONG>CreateObject</STRONG> de l'objet <A href="createobject-method-rds.md">RDS.DataSpace</A>. Si vous utilisez DCOM ou un serveur in-process, faites en sorte que les types de paramètres côté client et côté serveur correspondent sans quoi vous obtiendrez une erreur « Incompatibilité de type ».</span><span class="sxs-lookup"><span data-stu-id="9fe11-p103">Pay attention to the data type of <STRONG>ByRef</STRONG> arguments. VBScript does not let you specify the variable type, so you must always pass a Variant. When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the <STRONG>RDS.DataSpace</STRONG> object <A href="createobject-method-rds.md">CreateObject</A> method. When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span></P>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

## <a name="step-2a--invoke-the-server-program-with-rdsdatacontrol"></a><span data-ttu-id="9fe11-116">Étape 2a : appeler le programme serveur avec RDS.DataControl</span><span class="sxs-lookup"><span data-stu-id="9fe11-116">Step 2a — Invoke the server program with RDS.DataControl</span></span>

<span data-ttu-id="9fe11-117">Cet exemple est simplement un commentaire illustrant le comportement par défaut de l'objet **RDS.DataControl**, qui consiste à exécuter la requête spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9fe11-117">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

## <a name="step-2b--invoke-the-server-program-with-rdsserverdatafactory"></a><span data-ttu-id="9fe11-118">Étape 2b : appeler le programme serveur avec RDSServer.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9fe11-118">Step 2b — Invoke the server program with RDSServer.DataFactory</span></span>

## <a name="step-3--server-obtains-a-recordset"></a><span data-ttu-id="9fe11-119">Étape 3 : le serveur obtient un objet Recordset</span><span class="sxs-lookup"><span data-stu-id="9fe11-119">Step 3 — Server obtains a Recordset</span></span>

## <a name="step-4--server-returns-the-recordset"></a><span data-ttu-id="9fe11-120">Étape 4 : le serveur retourne l'objet Recordset</span><span class="sxs-lookup"><span data-stu-id="9fe11-120">Step 4 — Server returns the Recordset</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

## <a name="step-5--datacontrol-is-made-usable-by-visual-controls"></a><span data-ttu-id="9fe11-121">Étape 5 : l'objet DataControl est rendu utilisable par les contrôles visuels</span><span class="sxs-lookup"><span data-stu-id="9fe11-121">Step 5 — DataControl is made usable by visual controls</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

## <a name="step-6a--changes-are-sent-to-the-server-with-rdsdatacontrol"></a><span data-ttu-id="9fe11-122">Étape 6 a : les modifications sont envoyées au serveur avec RDS. DataControl \*</span><span class="sxs-lookup"><span data-stu-id="9fe11-122">Step 6a — Changes are sent to the server with RDS.DataControl\*</span></span>

<span data-ttu-id="9fe11-123">Cet exemple est simplement un commentaire illustrant la façon dont **RDS.DataControl** effectue les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="9fe11-123">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

## <a name="step-6b--changes-are-sent-to-the-server-with-rdsserverdatafactory"></a><span data-ttu-id="9fe11-124">Étape 6b : les modifications sont envoyées au serveur à l'aide de l'objet RDSServer.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9fe11-124">Step 6b — Changes are sent to the server with RDSServer.DataFactory</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

<span data-ttu-id="9fe11-125">**Fin du didacticiel.**</span><span class="sxs-lookup"><span data-stu-id="9fe11-125">**This is the end of the tutorial.**</span></span>

