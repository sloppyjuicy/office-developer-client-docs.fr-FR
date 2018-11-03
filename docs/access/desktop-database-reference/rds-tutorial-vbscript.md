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
# <a name="rds-tutorial-vbscript"></a>Didacticiel RDS (VBScript)

**S’applique à**: Access 2013, Office 2013

Il s’agit du didacticiel RDS, écrit en Microsoft Visual Basic Scripting Edition. Pour obtenir une description de l’objectif de ce didacticiel, consultez le [didacticiel RDS](chapter-12-rds-tutorial.md).

Dans ce didacticiel, [RDS. DataControl](datacontrol-object-rds.md) et [RDS. DataSpace](dataspace-object-rds.md) sont créés au moment du design ; Autrement dit, ils sont définis avec des balises object. Il est également possible de les créer au moment de l'exécution à l'aide de la méthode **Server.CreateObject**. 

Par exemple, l'objet **RDS.DataControl** peut être créé de la façon suivante :

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

## <a name="step-1--specify-a-server-program"></a>Étape 1 : spécifier un programme serveur

VBScript peut détecter le nom du serveur web IIS qu'exécute en accédant à la méthode VBScript **Request.ServerVariables** disponible pour les Pages ASP :

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

Toutefois, dans ce didacticiel, utilisez le serveur fictif « yourServer ».

> [!NOTE]
> <P>[!REMARQUE] Soyez attentif au type de données des arguments <STRONG>ByRef</STRONG>. VBScript ne vous autorisant pas à spécifier le type de variable, vous devez toujours transmettre un type Variant. Si vous utilisez HTTP, RDS vous autorise à transmettre un type Variant à une méthode qui n'attend pas ce type de données si vous l'appelez avec la méthode <STRONG>CreateObject</STRONG> de l'objet <A href="createobject-method-rds.md">RDS.DataSpace</A>. Si vous utilisez DCOM ou un serveur in-process, faites en sorte que les types de paramètres côté client et côté serveur correspondent sans quoi vous obtiendrez une erreur « Incompatibilité de type ».</P>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

## <a name="step-2a--invoke-the-server-program-with-rdsdatacontrol"></a>Étape 2a : appeler le programme serveur avec RDS.DataControl

Cet exemple est simplement un commentaire illustrant le comportement par défaut de l'objet **RDS.DataControl**, qui consiste à exécuter la requête spécifiée.

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

## <a name="step-2b--invoke-the-server-program-with-rdsserverdatafactory"></a>Étape 2b : appeler le programme serveur avec RDSServer.DataFactory

## <a name="step-3--server-obtains-a-recordset"></a>Étape 3 : le serveur obtient un objet Recordset

## <a name="step-4--server-returns-the-recordset"></a>Étape 4 : le serveur retourne l'objet Recordset

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

## <a name="step-5--datacontrol-is-made-usable-by-visual-controls"></a>Étape 5 : l'objet DataControl est rendu utilisable par les contrôles visuels

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

## <a name="step-6a--changes-are-sent-to-the-server-with-rdsdatacontrol"></a>Étape 6 a : les modifications sont envoyées au serveur avec RDS. DataControl *

Cet exemple est simplement un commentaire illustrant la façon dont **RDS.DataControl** effectue les mises à jour.

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

## <a name="step-6b--changes-are-sent-to-the-server-with-rdsserverdatafactory"></a>Étape 6b : les modifications sont envoyées au serveur à l'aide de l'objet RDSServer.DataFactory

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

**Fin du didacticiel.**

