---
title: 'Chapitre 12: didacticiel RDS (Remote Data Service)'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aca77ac08688e643327bdbf229ab6c1dec40d109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296478"
---
# <a name="chapter-12-remote-data-service-rds-tutorial"></a>Chapitre 12: didacticiel RDS (Remote Data Service)

**S’applique à** : Access 2013, Office 2013

Ce didacticiel illustre l'utilisation du modèle de programmation RDS pour interroger et mettre à jour une source de données. Dans un premier temps, il décrit les étapes à suivre pour accomplir cette tâche. Le didacticiel est ensuite répété dans Microsoft Visual Basic Scripting Edition et Microsoft Visual J++, avec ADO pour Windows Foundation classes (ADO/WFC).

Ce didacticiel est codé dans différents langages pour deux raisons :

- La documentation portant sur RDS part du principe que le lecteur code en Visual Basic. Si cette documentation s'avère utile pour les programmeurs qui codent en Visual Basic, elle l'est moins pour les programmeurs qui utilisent d'autres langages.

- Si vous avez un doute concernant une fonctionnalité RDS déterminée et que vous possédez certaines connaissances dans un autre langage, vous pouvez éventuellement résoudre votre problème en examinant cette même fonction exprimée dans un autre langage.

Ce didacticiel est basé sur le modèle de programmation RDS. Chaque étape du modèle de programmation y est abordée, avec en outre une illustration de chacune de ces étapes par un fragment de code Visual Basic.

L'exemple de code est reproduit dans les autres langages avec un minimum de détails. Chaque étape figurant dans le didacticiel d'un langage de programmation donné s'accompagne d'une mention de l'étape correspondante dans le modèle de programmation et le didacticiel descriptif. Servez-vous du numéro de l'étape pour accéder aux détails correspondants dans le didacticiel descriptif.

Le modèle de programmation RDS est indiqué ci-dessous. Référez-vous-y à mesure que vous avancez dans le didacticiel.

### <a name="rds-programming-model-with-objects"></a>Modèle de programmation RDS avec des objets

- Spécifiez le programme à appeler sur le serveur et obtenir un moyen (proxy) d'y faire référence à partir du client.

- Appelez le programme serveur. Transmettez les paramètres au programme serveur qui identifie la source de données et la commande à émettre.

- Le programme serveur obtient un objet [Recordset](recordset-object-ado.md) auprès de la source de données, généralement en utilisant ADO. L'objet **Recordset** peut éventuellement être traité sur le serveur.

- Le programme serveur retourne l'objet **Recordset** final à l'application cliente.

- Au niveau du client, l'objet **Recordset** est éventuellement placé dans un format facilement exploitable par des contrôles visuels.

- Les modifications apportées à l'objet **Recordset** sont renvoyées au serveur et utilisées pour la mise à jour de la source de données.

## <a name="step-1-specify-a-server-program"></a>Étape 1: spécifier un programme serveur

Dans la plupart des cas, utilisez la méthode [CreateObject](createobject-method-rds.md) de l’objet [RDS.DataSpace](dataspace-object-rds.md) pour spécifier le programme serveur par défaut, [RDSServer.DataFactory](datafactory-object-rdsserver.md), ou votre propre programme serveur personnalisé (objet métier). Un programme serveur est instancié sur le serveur et une référence à ce programme (ou *proxy*) est retournée.

Ce didacticiel utilise le programme serveur par défaut :

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a>Étape 2: appeler le programme serveur 

Lorsque vous appelez une méthode sur le *proxy* client, c'est le programme serveur qui exécute cette méthode. Au cours de cette étape, vous allez exécuter une requête sur le serveur.

### <a name="part-a"></a>1ère partie 

Si vous n’avez pas utilisé [RDSServer.DataFactory](datafactory-object-rdsserver.md) dans ce didacticiel, le moyen le plus simple d’exécuter cette étape est d’utiliser l’objet [RDS.DataControl](datacontrol-object-rds.md). **RDS.DataControl** combine l’étape précédente de création d’un proxy, et celle-ci, qui consiste à émettre une requête.

1. Définissez la valeur de l' **objet RDS. DataControl** , propriété du [serveur](server-property-rds.md) pour identifier l'emplacement où le programme serveur doit être instancié.

2. Définissez la propriété [Connect](connect-property-rds.md) pour spécifier la chaîne de connexion permettant d'accéder à la source de données.

3. Définir la propriété [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) pour spécifier le texte de la commande de requête. 

4. Émettez la méthode [Refresh](refresh-method-rds.md) pour faire en sorte que le programme serveur se connecte à la source de données, récupère les lignes spécifiées par la requête et renvoie un objet **Recordset** au client.

Ce didacticiel n'utilise pas l'objet **RDS.DataControl**, mais, si c'était le cas, le code ressemblerait à ce qui suit :

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<br/>

De même, le didacticiel n'appelle pas RDS avec les objets ADO, mais voici comment se présenterait le code dans le cas contraire :

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a>2ème partie 

En règle générale, cette étape consiste à appeler la méthode [Query](query-method-rds.md) de l’objet **RDSServer.DataFactory**. Cette méthode prend une chaîne de connexion, utilisée pour établir la connexion à une source de données, et un texte de commande, pour spécifier les lignes à retourner par la source de données.

Ce didacticiel utilise la méthode **Query** de l'objet **DataFactory**:

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a>Étape 3: le serveur obtient un objet Recordset 

Le programme serveur utilise la chaîne de connexion et le texte de commande pour interroger la source de données et obtenir les lignes souhaitées. ADO est généralement utilisé pour récupérer cet objet **Recordset** même s'il est possible d'utiliser d'autres interfaces d'accès aux données Microsoft, comme OLE DB.

Un programme serveur personnalisé peut ressembler à ce qui suit :

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a>Étape 4: le serveur retourne l'objet Recordset 

RDS convertit l'objet **Recordset** récupéré dans un format qui peut être renvoyé au client (autrement dit, il *marshale* l'objet **Recordset**). La forme exacte de la conversion et son mode d'envoi varient selon que le serveur réside sur Internet ou sur un intranet, sur un réseau local ou qu'il corresponde à une bibliothèque de liaison dynamique. Toutefois, ce détail n'est pas crucial ; l'important est que RDS renvoie l'objet **Recordset** au client.

Côté client, un objet **Recordset** est retourné et affecté à une variable locale.

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a>Étape 5: rendre l'DataControl utilisable 

L'objet **Recordset** retourné est disponible et peut être utilisé. Vous pouvez l'examiner, le parcourir ou le modifier comme n'importe quel autre objet **Recordset**. L'utilisation que vous pouvez faire de cet objet **Recordset** dépend de votre environnement. Visual Basic et Visual C++ intègrent des contrôles visuels qu'un objet **Recordset** peut utiliser directement ou indirectement à l'aide d'un contrôle d'activation de données.

Par exemple, si vous affichez une page Web dans Internet Explorer, vous pouvez afficher les données **** de l'objet Recordset dans un contrôle visuel. Les contrôles visuels sur une page Web ne **** peuvent pas accéder directement à un objet Recordset. However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md). The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.

Le paramètre **DATASRC** de l'objet de contrôle visuel doit être défini sur **RDS.DataControl**, et sa propriété **DATAFLD** sur un champ (colonne) de l'objet **Recordset**.

Dans ce didacticiel, définissez la propriété **SourceRecordset**:

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

## <a name="step-6-changes-are-sent-to-the-server"></a>Étape 6: les modifications sont envoyées au serveur

Si l'objet **Recordset** est modifié, les modifications correspondantes (p. ex., lignes ajoutées, modifiées ou supprimées) peuvent être renvoyées au serveur.

[!REMARQUE] Le comportement par défaut de RDS peut être appelé implicitement avec les objets ADO et le fournisseur d'accès à distance Microsoft OLE DB. Les requêtes peuvent renvoyer des **jeux d'enregistrements**et les **jeux d'enregistrements** modifiés peuvent mettre à jour la source de données. Ce didacticiel n'appelle pas RDS avec les objets ADO, mais, si c'était le cas, voici comment se présenterait le code :

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a>1ère partie 

Supposons dans cet exemple que vous n’avez utilisé que l’objet [RDS.DataControl](datacontrol-object-rds.md) et qu’un objet **Recordset** est maintenant associé à **RDS.DataControl**. La méthode [SubmitChanges](submitchanges-method-rds.md) met à jour la source de données en fonction des modifications apportées à l’objet **Recordset** si les propriétés [Server](server-property-rds.md) et [Connect](connect-property-rds.md) sont toujours définies.

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

### <a name="part-b"></a>2ème partie 

Vous pouvez également mettre à jour le serveur avec l’objet [RDSServer.DataFactory](datafactory-object-rdsserver.md) en définissant une connexion et un objet **Recordset**.

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```


## <a name="appendix-a-rds-tutorial-vbscript"></a>Annexe A: didacticiel RDS (VBScript)

Il s'agit du didacticiel RDS, écrit en Microsoft Visual Basic Scripting Edition. Pour obtenir une description de la finalité de ce didacticiel, consultez l'introduction à cette rubrique.

Dans ce didacticiel, [RDS. DataControl](datacontrol-object-rds.md) et [RDS. DataSpace](dataspace-object-rds.md) sont créés au moment de la conception; autrement dit, ils sont définis avec des balises Object. Il est également possible de les créer au moment de l'exécution à l'aide de la méthode **Server.CreateObject**. 

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

### <a name="step-1-specify-a-server-program"></a>Étape 1: spécifier un programme serveur

VBScript peut détecter le nom du serveur Web IIS sur lequel il s'exécute en accédant à la méthode **Request. ServerVariables** VBScript disponible pour les pages ASP:

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

Toutefois, pour ce didacticiel, utilisez le serveur imaginaire, «yourServer».

> [!NOTE]
> [!REMARQUE] Soyez attentif au type de données des arguments **ByRef**. VBScript ne vous autorisant pas à spécifier le type de variable, vous devez toujours transmettre un type Variant. Si vous utilisez HTTP, RDS vous autorise à transmettre un type Variant à une méthode qui n'attend pas ce type de données si vous l'appelez avec la méthode **CreateObject** de l'objet [RDS.DataSpace](createobject-method-rds.md). Si vous utilisez DCOM ou un serveur in-process, faites en sorte que les types de paramètres côté client et côté serveur correspondent sans quoi vous obtiendrez une erreur « Incompatibilité de type ».

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a>Étape 2, partie A: appelez le programme serveur avec RDS. RDS

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

Passez à l'étape suivante.

### <a name="step-4-server-returns-the-recordset"></a>Étape 4: le serveur retourne l'objet Recordset

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a>Étape 5: l'DataControl est rendu utilisable par les contrôles visuels

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a>Étape 6, partie A: les modifications sont envoyées au serveur à l'aide de RDS. RDS

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

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a>Étape 6, partie B: les modifications sont envoyées au serveur avec RDSServer. DataFactory

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a>Annexe B: didacticiel RDS (Visual J++)

ADO/WFC ne suit pas intégralement le modèle d'objet RDS en cela qu'il n'implémente pas l'objet [RDS.DataControl](datacontrol-object-rds.md). ADO/WFC implémente uniquement la classe côté client[RDS.DataSpace](dataspace-object-rds.md).

La classe **DataSpace** implémente une seule méthode, [CreateObject](createobject-method-rds.md), qui retourne un objet [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax). La classe **DataSpace** implémente également la propriété [InternetTimeout](internettimeout-property-rds.md).

La classe **ObjectProxy** implémente une seule méthode, call, qui peut appeler n'importe quel objet métier côté serveur.

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```



