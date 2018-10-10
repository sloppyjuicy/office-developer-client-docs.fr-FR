---
title: Méthode Workspace.OpenDatabase (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: dbb93908-ec3e-f3ee-c4ea-cca48340b4d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835343(v=office.15)
ms:contentKeyID: 48548108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 05edf4979f7fe3a7084f2ab7a7b27f058447eac8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469892"
---
# <a name="workspaceopendatabase-method-dao"></a><span data-ttu-id="baf6f-102">Méthode Workspace.OpenDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="baf6f-102">Workspace.OpenDatabase Method (DAO)</span></span>

<span data-ttu-id="baf6f-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="baf6f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="baf6f-104">Ouvre une base de données spécifiée dans un objet **[Workspace](workspace-object-dao.md)** et renvoie une référence à l'objet **[Database](database-object-dao.md)** qui le représente.</span><span class="sxs-lookup"><span data-stu-id="baf6f-104">Opens a specified database in a **[Workspace](workspace-object-dao.md)** object and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="baf6f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="baf6f-105">Syntax</span></span>

<span data-ttu-id="baf6f-106">*expression* . OpenDatabase (***nom***, ***Options***, ***ReadOnly***, ***connecter***)</span><span class="sxs-lookup"><span data-stu-id="baf6f-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="baf6f-107">*expression* Variable qui représente un objet **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="baf6f-107">*expression* A variable that represents a **Workspace** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="baf6f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="baf6f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="baf6f-109">Name</span><span class="sxs-lookup"><span data-stu-id="baf6f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="baf6f-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="baf6f-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="baf6f-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="baf6f-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="baf6f-112">Description</span><span class="sxs-lookup"><span data-stu-id="baf6f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baf6f-113">Name</span><span class="sxs-lookup"><span data-stu-id="baf6f-113">Name</span></span></p></td>
<td><p><span data-ttu-id="baf6f-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="baf6f-114">Required</span></span></p></td>
<td><p><span data-ttu-id="baf6f-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="baf6f-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="baf6f-p101">Nom d'un fichier de base de données de moteur de base de données Microsoft Access existant, ou nom de la source de données (DSN) d'une source de données ODBC. Pour plus d'informations sur la définition de cette valeur, reportez-vous à la propriété <strong><a href="connection-name-property-dao.md">Name</a></strong>.  </span><span class="sxs-lookup"><span data-stu-id="baf6f-p101">the name of an existing Microsoft Access database engine database file, or the data source name (DSN) of an ODBC data source. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baf6f-118">Options</span><span class="sxs-lookup"><span data-stu-id="baf6f-118">Options</span></span></p></td>
<td><p><span data-ttu-id="baf6f-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="baf6f-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="baf6f-120"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="baf6f-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="baf6f-121">Définit différentes options pour la base de données, selon les indications dans les notes.</span><span class="sxs-lookup"><span data-stu-id="baf6f-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baf6f-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="baf6f-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="baf6f-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="baf6f-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="baf6f-124"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="baf6f-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="baf6f-125"><strong>True</strong> si vous souhaitez ouvrir la base de données avec un accès en lecture seule, ou <strong>False</strong> (valeur par défaut) si vous souhaitez ouvrir la base de données avec un accès en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="baf6f-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baf6f-126">Connexion</span><span class="sxs-lookup"><span data-stu-id="baf6f-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="baf6f-127">Facultatif</span><span class="sxs-lookup"><span data-stu-id="baf6f-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="baf6f-128"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="baf6f-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="baf6f-129">Spécifie les différentes informations de connexion, dont les mots de passe.</span><span class="sxs-lookup"><span data-stu-id="baf6f-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="baf6f-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="baf6f-130">Return Value</span></span>

<span data-ttu-id="baf6f-131">Base de données</span><span class="sxs-lookup"><span data-stu-id="baf6f-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="baf6f-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="baf6f-132">Remarks</span></span>

<span data-ttu-id="baf6f-133">Vous pouvez utiliser les valeurs ci-dessous pour l'argument options.</span><span class="sxs-lookup"><span data-stu-id="baf6f-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="baf6f-134">Paramètre</span><span class="sxs-lookup"><span data-stu-id="baf6f-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="baf6f-135">Description</span><span class="sxs-lookup"><span data-stu-id="baf6f-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baf6f-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="baf6f-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="baf6f-137">Ouvre la base de données en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="baf6f-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baf6f-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="baf6f-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="baf6f-139">(Valeur par défaut) Ouvre la base de données en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="baf6f-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="baf6f-140">Lorsque vous ouvrez une base de données, elle est automatiquement ajoutée à la collection **Databases**.</span><span class="sxs-lookup"><span data-stu-id="baf6f-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="baf6f-141">Certaines considérations s’appliquent lorsque vous utilisez NomBaseDonnées :</span><span class="sxs-lookup"><span data-stu-id="baf6f-141">Some considerations apply when you use dbname:</span></span>

- <span data-ttu-id="baf6f-142">S'il s'agit d'une base de données déjà ouverte pour un accès par un autre utilisateur, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="baf6f-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

- <span data-ttu-id="baf6f-143">S'il ne s'agit pas d'une base de données existante ou d'un nom de source de données ODBC valide, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="baf6f-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

- <span data-ttu-id="baf6f-144">S’il s’agit d’une chaîne de longueur nulle (« ») et *vous connecter* est « ODBC ; », une boîte de dialogue répertoriant les noms de source de données ODBC tous enregistrés s’affiche afin que l’utilisateur peut sélectionner une base de données.</span><span class="sxs-lookup"><span data-stu-id="baf6f-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="baf6f-145">Pour fermer une base de données, et ainsi supprimer l'objet **Database** de la collection **Databases**, utilisez la méthode **[Close](connection-close-method-dao.md)** dans l'objet.</span><span class="sxs-lookup"><span data-stu-id="baf6f-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>

> [!NOTE]
> <span data-ttu-id="baf6f-146">[!REMARQUE] Lorsque vous accédez à une source de données ODBC connectée au moteur de base de données Microsoft Access, vous pouvez améliorer les performances de votre application en ouvrant un objet **Database** connecté à la source de données ODBC, plutôt qu'en liant des objets **[TableDef](tabledef-object-dao.md)** individuels à des tables spécifiques dans la source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="baf6f-146">When you access a Microsoft access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual **[TableDef](tabledef-object-dao.md)** objects to specific tables in the ODBC data source.</span></span>

## <a name="example"></a><span data-ttu-id="baf6f-147">Exemple</span><span class="sxs-lookup"><span data-stu-id="baf6f-147">Example</span></span>

<span data-ttu-id="baf6f-148">Cet exemple utilise la méthode **OpenDatabase** pour ouvrir une base de données Microsoft Access et deux bases de données ODBC connectées par le moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="baf6f-148">This example uses the **OpenDatabase** method to open one Microsoft Access database and two Microsoft Access database engine-connected ODBC databases.</span></span>

```vb 
Sub OpenDatabaseX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsPubs As Database 
 Dim dbsPubs2 As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 ' Create Microsoft Access Workspace object. 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 
 ' Open Database object from saved Microsoft Access database 
 ' for exclusive use. 
 MsgBox "Opening Northwind..." 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb", _ 
 True) 
 
 ' Open read-only Database object based on information in 
 ' the connect string. 
 MsgBox "Opening pubs..." 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set dbsPubs = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverNoPrompt, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Open read-only Database object by entering only the 
 ' missing information in the ODBC Driver Manager dialog 
 ' box. 
 MsgBox "Opening second copy of pubs..." 
 Set dbsPubs2 = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverCompleteRequired, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 Debug.Print "Database properties for " & _ 
 dbsLoop.Name & ":" 
 
 On Error Resume Next 
 ' Enumerate the Properties collection of each Database 
 ' object. 
 For Each prpLoop In dbsLoop.Properties 
 If prpLoop.Name = "Connection" Then 
 ' Property actually returns a Connection object. 
 Debug.Print " Connection[.Name] = " & _ 
 dbsLoop.Connection.Name 
 Else 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 End If 
 Next prpLoop 
 On Error GoTo 0 
 
 Next dbsLoop 
 
 dbsNorthwind.Close 
 dbsPubs.Close 
 dbsPubs2.Close 
 wrkAcc.Close 
 
End Sub 
 
```

