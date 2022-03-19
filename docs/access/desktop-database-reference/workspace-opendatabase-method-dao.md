---
title: Méthode Workspace.OpenDatabase (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: dbb93908-ec3e-f3ee-c4ea-cca48340b4d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835343(v=office.15)
ms:contentKeyID: 48548108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 0653a0f17e4324624850484d278b3defa47370ee
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63629642"
---
# <a name="workspaceopendatabase-method-dao"></a>Méthode Workspace.OpenDatabase (DAO)

**S’applique à** : Access 2013, Office 2013

Ouvre une base de données spécifiée dans un objet **[Workspace](workspace-object-dao.md)** et renvoie une référence à l’objet **[Database](database-object-dao.md)** qui le représente.

## <a name="syntax"></a>Syntaxe

*expression* . OpenDatabase(***Nom** _, _*_Options_*_, _*_en lecture seule_*_, _*_Connect_**)

*expression* Variable qui représente un objet **Workspace**.

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Nom d’un fichier de base de données de moteur de base de données Microsoft Access existant, ou nom de la source de données (DSN) d’une source de données ODBC. Pour plus d’informations sur la définition de cette valeur, reportez-vous à la propriété <strong><a href="connection-name-property-dao.md">Name</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Définit différentes options pour la base de données, selon les indications dans les notes.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>True</strong> si vous souhaitez ouvrir la base de données avec un accès en lecture seule, ou <strong>False</strong> (valeur par défaut) si vous souhaitez ouvrir la base de données avec un accès en lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Spécifie les différentes informations de connexion, dont les mots de passe.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

Database

## <a name="remarks"></a>Remarques

Vous pouvez utiliser les valeurs ci-dessous pour l’argument options.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Setting</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>True</strong></p></td>
<td><p>Ouvre la base de données en mode exclusif.</p></td>
</tr>
<tr class="even">
<td><p><strong>False</strong></p></td>
<td><p>(Valeur par défaut) Ouvre la base de données en mode partagé.</p></td>
</tr>
</tbody>
</table>


Lorsque vous ouvrez une base de données, elle est automatiquement ajoutée à la collection **Databases**.

Certaines considérations s’appliquent lorsque vous utilisez dbname :

- S'il s'agit d'une base de données déjà ouverte pour un accès par un autre utilisateur, une erreur se produit.

- S'il ne s'agit pas d'une base de données existante ou d'un nom de source de données ODBC valide, une erreur se produit.

- S’il s’agit d’une chaîne nulle ("") et si *connect* prend la valeur "ODBC;", une boîte de dialogue répertoriant tous les noms de source de données ODBC enregistrés s’affiche afin que l’utilisateur puisse sélectionner une base de données.

Pour fermer une base de données, et ainsi supprimer l’objet **Database** de la collection **Databases**, utilisez la méthode **[Close](connection-close-method-dao.md)** dans l’objet.

> [!NOTE]
> Lorsque vous accédez à une source de données ODBC connectée au moteur de base de données Microsoft Access, vous pouvez améliorer les performances de votre application en ouvrant un objet **Database** connecté à la source de données ODBC, plutôt qu’en liant des objets **[TableDef](tabledef-object-dao.md)** individuels à des tables spécifiques dans la source de données ODBC.

## <a name="example"></a>Exemple

Cet exemple utilise la méthode **OpenDatabase** pour ouvrir une base de données Microsoft Access et deux bases de données ODBC connectées par le moteur de base de données Microsoft Access.

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

