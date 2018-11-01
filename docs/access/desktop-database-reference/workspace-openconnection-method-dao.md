---
title: Workspace.OpenConnection Method (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 9d97f298-a2d5-3b91-2efd-57f06fbd4654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198249(v=office.15)
ms:contentKeyID: 48546628
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3fb625208e5d47f4107adac5c429257ae58e2eab
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882174"
---
# <a name="workspaceopenconnection-method-dao"></a><span data-ttu-id="2084b-102">Workspace.OpenConnection Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="2084b-102">Workspace.OpenConnection Method (DAO)</span></span>


<span data-ttu-id="2084b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2084b-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="2084b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2084b-104">Syntax</span></span>

<span data-ttu-id="2084b-105">*expression* . OpenConnection (***nom***, ***Options***, ***ReadOnly***, ***connecter***)</span><span class="sxs-lookup"><span data-stu-id="2084b-105">*expression* .OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="2084b-106">*expression* Variable qui représente un objet **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="2084b-106">*expression* A variable that represents a **Workspace** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="2084b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2084b-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2084b-108">Name</span><span class="sxs-lookup"><span data-stu-id="2084b-108">Name</span></span></p></th>
<th><p><span data-ttu-id="2084b-109">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="2084b-109">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="2084b-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="2084b-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="2084b-111">Description</span><span class="sxs-lookup"><span data-stu-id="2084b-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2084b-112">Name</span><span class="sxs-lookup"><span data-stu-id="2084b-112">Name</span></span></p></td>
<td><p><span data-ttu-id="2084b-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2084b-113">Required</span></span></p></td>
<td><p><span data-ttu-id="2084b-114"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="2084b-114"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2084b-p101">Expression sous forme de chaîne. Reportez-vous à la section sous Notes.</span><span class="sxs-lookup"><span data-stu-id="2084b-p101">A string expression. See the discussion under Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2084b-117">Options</span><span class="sxs-lookup"><span data-stu-id="2084b-117">Options</span></span></p></td>
<td><p><span data-ttu-id="2084b-118">Facultatif</span><span class="sxs-lookup"><span data-stu-id="2084b-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="2084b-119"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="2084b-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2084b-p102">Définit différentes options pour la connexion, selon les indications dans les notes. En fonction de cette valeur, le gestionnaire de pilotes ODBC invite l'utilisateur à indiquer les informations de connexion comme le nom de la source de données (DSN), le nom d'utilisateur et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="2084b-p102">sets various options for the connection, as specified in Remarks. Based on this value, the ODBC driver manager prompts the user for connection information such as data source name (DSN), user name, and password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2084b-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2084b-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="2084b-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="2084b-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="2084b-124"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="2084b-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2084b-125"><strong>True</strong> si la connexion doit être ouverte pour un accès en lecture seule et <strong>False</strong> si la connexion doit être ouverte pour un accès en lecture/écriture (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="2084b-125"><strong>True</strong> if the connection is to be opened for read-only access and <strong>False</strong> if the connection is to be opened for read/write access (default).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2084b-126">Connexion</span><span class="sxs-lookup"><span data-stu-id="2084b-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="2084b-127">Facultatif</span><span class="sxs-lookup"><span data-stu-id="2084b-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="2084b-128"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="2084b-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2084b-129">Une chaîne de connexion ODBC.</span><span class="sxs-lookup"><span data-stu-id="2084b-129">An ODBC connection string.</span></span> <span data-ttu-id="2084b-130">Voir la propriété <strong><a href="connection-connect-property-dao.md">Connect</a></strong> pour des éléments spécifiques et la syntaxe de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="2084b-130">See the <strong><a href="connection-connect-property-dao.md">Connect</a></strong> property for the specific elements and syntax of this string.</span></span> <span data-ttu-id="2084b-131">Un ajoutant au début &quot;ODBC ; &quot; est requis.</span><span class="sxs-lookup"><span data-stu-id="2084b-131">A prepended &quot;ODBC;&quot; is required.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="2084b-132">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2084b-132">Return value</span></span>

<span data-ttu-id="2084b-133">Connection</span><span class="sxs-lookup"><span data-stu-id="2084b-133">Connection</span></span>

## <a name="remarks"></a><span data-ttu-id="2084b-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="2084b-134">Remarks</span></span>

<span data-ttu-id="2084b-p104">Utilisez la méthode **OpenConnection** pour définir une connexion à une source de données ODBC à partir d'un espace de travail ODBCDirect. La méthode **OpenConnection** est similaire à la méthode **OpenDatabase**, mais elle n'y est pas équivalente. La différence principale est que la méthode **OpenConnection** est disponible dans un espace de travail ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="2084b-p104">Use the **OpenConnection** method to establish a connection to an ODBC data source from an ODBCDirect workspace. The **OpenConnection** method is similar but not equivalent to **OpenDatabase**. The main difference is that **OpenConnection** is available only in an ODBCDirect workspace.</span></span>

<span data-ttu-id="2084b-138">Si vous spécifiez un nom de source de données (DSN) ODBC inscrit dans l’argument connecter, l’argument nom peut être n’importe quelle chaîne valide et fournit également la propriété **Name** de l’objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="2084b-138">If you specify a registered ODBC data source name (DSN) in the connect argument, then the name argument can be any valid string, and will also provide the **Name** property for the **Connection** object.</span></span> <span data-ttu-id="2084b-139">Si un DSN valide n’est pas inclus dans l’argument connecter, nom doit faire référence à un DSN ODBC valide, qui sera également la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="2084b-139">If a valid DSN is not included in the connect argument, then name must refer to a valid ODBC DSN, which will also be the **Name** property.</span></span> <span data-ttu-id="2084b-140">Si nom ni se connecter contient un DSN valid, le Gestionnaire de pilote ODBC peut avoir (via l’argument options) pour inviter l’utilisateur pour les informations de connexion nécessaires.</span><span class="sxs-lookup"><span data-stu-id="2084b-140">If neither name nor connect contains a valid DSN, the ODBC driver manager can be set (via the options argument) to prompt the user for the required connection information.</span></span> <span data-ttu-id="2084b-141">Le nom DSN indiqué à l'invite fournit ensuite la propriété **Name**.</span><span class="sxs-lookup"><span data-stu-id="2084b-141">The DSN supplied through the prompt then provides the **Name** property.</span></span>

<span data-ttu-id="2084b-p106">L'argument options détermine si l'utilisateur doit être invité à établir la connexion, définit à quel moment cela doit avoir lieu, et décide si la connexion doit être ouverte ou non en mode asynchrone. Vous pouvez utiliser l'une des constantes ci-après.</span><span class="sxs-lookup"><span data-stu-id="2084b-p106">The options argument determines if and when to prompt the user to establish the connection, and whether or not to open the connection asynchronously. You can use one of the following constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2084b-144">Constant</span><span class="sxs-lookup"><span data-stu-id="2084b-144">Constant</span></span></p></th>
<th><p><span data-ttu-id="2084b-145">Description</span><span class="sxs-lookup"><span data-stu-id="2084b-145">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2084b-146"><strong>dbDriverNoPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="2084b-146"><strong>dbDriverNoPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="2084b-p107">Le gestionnaire de pilotes ODBC utilise la chaîne de connexion fournie dans <em>dbname</em> et <em>connect</em>. Si vous ne fournissez pas suffisamment d’informations, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="2084b-p107">The ODBC Driver Manager uses the connection string provided in <em>dbname</em> and <em>connect</em>. If you don't provide sufficient information, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2084b-149"><strong>dbDriverPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="2084b-149"><strong>dbDriverPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="2084b-p108">Le gestionnaire de pilotes ODBC affiche la boîte de dialogue <strong>Sources de données ODBC</strong>, qui affiche les informations pertinentes fournies dans <em>dbname</em> ou <em>connect</em>. La chaîne de connexion est composée du DSN que l'utilisateur sélectionné par le biais des boîtes de dialogue, ou, si l'utilisateur ne spécifie pas de DSN, c'est le DSN par défaut qui est utilisé.</span><span class="sxs-lookup"><span data-stu-id="2084b-p108">The ODBC Driver Manager displays the <strong>ODBC Data Sources</strong> dialog box, which displays any relevant information supplied in <em>dbname</em> or <em>connect</em>. The connection string is made up of the DSN that the user selects via the dialog boxes, or, if the user doesn't specify a DSN, the default DSN is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2084b-152"><strong>dbDriverComplete</strong></span><span class="sxs-lookup"><span data-stu-id="2084b-152"><strong>dbDriverComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="2084b-p109">Valeur par défaut. Si l'argument <em>connect</em> inclut toutes les informations nécessaires pour établir une connexion, le gestionnaire de pilotes ODBC utilise la chaîne dans <em>connect</em>. Autrement, il se comporte comme lorsque vous spécifiez <strong>dbDriverPrompt</strong>.</span><span class="sxs-lookup"><span data-stu-id="2084b-p109">Default. If the <em>connect</em> argument includes all the necessary information to complete a connection, the ODBC Driver Manager uses the string in <em>connect</em>. Otherwise it behaves as it does when you specify <strong>dbDriverPrompt</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2084b-156"><strong>dbDriverCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="2084b-156"><strong>dbDriverCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="2084b-157">Cette option se comporte comme <strong>dbDriverComplete</strong> sauf que le pilote ODBC désactive les invites pour les informations qui ne sont pas nécessaires à l'établissement de la connexion.</span><span class="sxs-lookup"><span data-stu-id="2084b-157">This option behaves like <strong>dbDriverComplete</strong> except the ODBC driver disables the prompts for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2084b-158"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="2084b-158"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="2084b-p110">Exécute la méthode en mode asynchrone. Cette constante peut être utilisée avec n'importe quelles autres constantes <em>options</em>.</span><span class="sxs-lookup"><span data-stu-id="2084b-p110">Execute the method asynchronously. This constant may be used with any of the other <em>options</em> constants.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2084b-p111">**OpenConnection** renvoie un objet **Connection** qui contient des informations relatives à la connexion. L'objet **Connection** est similaire à un objet **[Database](database-object-dao.md)**. La différence principale est qu'un objet **Database** représente généralement une base de données, même si elle peut être utilisée pour représenter une connexion à une source de données ODBC à partir d'un espace de travail Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2084b-p111">**OpenConnection** returns a **Connection** object which contains information about the connection. The **Connection** object is similar to a **[Database](database-object-dao.md)** object. The principal difference is that a **Database** object usually represents a database, although it can be used to represent a connection to an ODBC data source from a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="2084b-164">Exemple</span><span class="sxs-lookup"><span data-stu-id="2084b-164">Example</span></span>

<span data-ttu-id="2084b-165">Cet exemple utilise la méthode **OpenConnection** avec différents paramètres pour ouvrir trois objets **Connection** différents.</span><span class="sxs-lookup"><span data-stu-id="2084b-165">This example uses the **OpenConnection** method with different parameters to open three different **Connection** objects.</span></span>

```vb 
Sub OpenConnectionX() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim conPubs2 As Connection 
 Dim conPubs3 As Connection 
 Dim conLoop As Connection 
 
 ' Create ODBCDirect Workspace object. 
 Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Open Connection object using supplied information in 
 ' the connect string. If this information were 
 ' insufficient, you could trap for an error rather than 
 ' go to an ODBC Driver Manager dialog box. 
 MsgBox "Opening Connection1..." 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Connection1", _ 
 dbDriverNoPrompt, , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Open read-only Connection object based on information 
 ' you enter in the ODBC Driver Manager dialog box. 
 MsgBox "Opening Connection2..." 
 Set conPubs2 = wrkODBC.OpenConnection("Connection2", _ 
 dbDriverPrompt, True, "ODBC;DSN=Publishers;") 
 
 ' Open read-only Connection object by entering only the 
 ' missing information in the ODBC Driver Manager dialog 
 ' box. 
 MsgBox "Opening Connection3..." 
 Set conPubs3 = wrkODBC.OpenConnection("Connection3", _ 
 dbDriverCompleteRequired, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
 ' Enumerate the Connections collection. 
 For Each conLoop In wrkODBC.Connections 
 Debug.Print "Connection properties for " & _ 
 conLoop.Name & ":" 
 
 With conLoop 
 ' Print property values by explicitly calling each 
 ' Property object; the Connection object does not 
 ' support a Properties collection. 
 Debug.Print " Connect = " & .Connect 
 ' Property actually returns a Database object. 
 Debug.Print " Database[.Name] = " & _ 
 .Database.Name 
 Debug.Print " Name = " & .Name 
 Debug.Print " QueryTimeout = " & .QueryTimeout 
 Debug.Print " RecordsAffected = " & _ 
 .RecordsAffected 
 Debug.Print " StillExecuting = " & _ 
 .StillExecuting 
 Debug.Print " Transactions = " & .Transactions 
 Debug.Print " Updatable = " & .Updatable 
 End With 
 
 Next conLoop 
 
 conPubs.Close 
 conPubs2.Close 
 conPubs3.Close 
 wrkODBC.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="2084b-166">Cet exemple présente l'objet **Connection** et la collection **Connections** en ouvrant un objet Microsoft Access **Database** et deux objets ODBCDirect **Connection**, et en répertoriant les propriétés disponibles dans chaque objet.</span><span class="sxs-lookup"><span data-stu-id="2084b-166">This example demonstrates the **Connection** object and **Connections** collection by opening a Microsoft Access **Database** object and two ODBCDirect **Connection** objects and listing the properties available to each object.</span></span>

```vb 
Sub ConnectionObjectX() 
 
 Dim wrkAcc as Workspace 
 Dim dbsNorthwind As Database 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim conPubs2 As Connection 
 Dim conLoop As Connection 
 Dim prpLoop As Property 
 
 ' Open Microsoft Access Database object. 
 Set wrkAcc = CreateWorkspace("NewWorkspace", _ 
 "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' objects. 
 Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSNs referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Connection1", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Set conPubs2 = wrkODBC.OpenConnection("Connection2", , _ 
 True, "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Debug.Print "Database properties:" 
 
 With dbsNorthwind 
 ' Enumerate Properties collection of Database object. 
 For Each prpLoop In .Properties 
 On Error Resume Next 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop.Value 
 On Error GoTo 0 
 Next prpLoop 
 End With 
 
 ' Enumerate the Connections collection. 
 For Each conLoop In wrkODBC.Connections 
 Debug.Print "Connection properties for " & _ 
 conLoop.Name & ":" 
 
 With conLoop 
 ' Print property values by explicitly calling each 
 ' Property object; the Connection object does not 
 ' support a Properties collection. 
 Debug.Print " Connect = " & .Connect 
 ' Property actually returns a Database object. 
 Debug.Print " Database[.Name] = " & _ 
 .Database.Name 
 Debug.Print " Name = " & .Name 
 Debug.Print " QueryTimeout = " & .QueryTimeout 
 Debug.Print " RecordsAffected = " & _ 
 .RecordsAffected 
 Debug.Print " StillExecuting = " & _ 
 .StillExecuting 
 Debug.Print " Transactions = " & .Transactions 
 Debug.Print " Updatable = " & .Updatable 
 End With 
 
 Next conLoop 
 
 dbsNorthwind.Close 
 conPubs.Close 
 conPubs2.Close 
 wrkAcc.Close 
 wrkODBC.Close 
 
End Sub 
 
```

