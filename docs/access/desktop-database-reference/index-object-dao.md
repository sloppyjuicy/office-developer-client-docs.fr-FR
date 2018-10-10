---
title: Objet index - accès aux données (DAO) des objets
TOCTitle: Index Object
ms:assetid: 92c32cad-ec8a-1243-1d18-83f50b269ecb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197655(v=office.15)
ms:contentKeyID: 48546380
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e45356a09a6a625381ef9a39d40e7349234460ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471010"
---
# <a name="index-object-dao"></a>Index Object (DAO)

**S’applique à**: Access 2013 | Office 2013

Les objets **Index** déterminent l'ordre des enregistrements accessibles depuis les tables de base de données et indiquent si les enregistrements en double sont acceptés ou pas, ce qui optimise l'accès aux données. Dans le cas d'une base de données externe, les objets **Index** décrivent les index définis pour les tables externes (espaces de travail Microsoft Access uniquement).

## <a name="remarks"></a>Remarques

Le moteur de base de données Microsoft Access utilise des index pour joindre des tables et crée des objets **[Recordset](recordset-object-dao.md)**. Les index déterminent l'ordre selon lequel les objets **Recordset** de type table renvoient des enregistrements. Toutefois, ils n'indiquent pas l'ordre dans lequel le moteur de base de données Microsoft Access stocke les enregistrements dans la table de base, ni celui dans lequel les autres types d'objet **Recordset** renvoient les enregistrements.

Grâce à un objet **Index**, vous pouvez :

- Utiliser la propriété **Required** pour indiquer que les objets **[Field](field-object-dao.md)** de l'index nécessitent des valeurs qui ne sont pas Null, puis utiliser la propriété **IgnoreNulls** pour déterminer si les valeurs Null contiennent des entrées d'index.

- Utiliser les propriétés **Primary** et **Unique** pour déterminer l'ordre et le caractère unique de l'objet **Index**.

Le moteur de base de données Microsoft Access gère automatiquement tous les index de table de base. Il met à jour les index lorsque vous ajoutez, modifiez ou supprimez des enregistrements de la table de base. Après avoir créé la base de données, utilisez régulièrement la méthode **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** pour actualiser les statistiques relatives à l'index.

Lorsque vous accédez à un objet **Recordset** de type table, vous indiquez l'ordre des enregistrements à l'aide de la propriété **Index** de l'objet. Définissez cette propriété sur le paramètre **Name** d'un objet **Index** existant dans la collection **Indexes**. Cette collection figure dans l'objet **[TableDef](tabledef-object-dao.md)** sous-jacent à l'objet **Recordset** que vous remplissez.

> [!NOTE]
> <P>[!REMARQUE] Vous ne devez pas créer d'index pour une table. Toutefois, dans le cas d'une table volumineuse non indexée, l'accès à un enregistrement spécifique ou le traitement de jointures peuvent durer longtemps. Inversement, la présence d'un nombre d'index trop important peut ralentir la mise à jour de la base de données lors de la modification de chaque index de table.</P>

La propriété **[Attributes](field-attributes-property-dao.md)** de chaque objet **Field** de l'index détermine l'ordre des enregistrements renvoyés ainsi que les techniques d'accès à utiliser pour cet index.

Chaque objet **Field** de la collection **Fields** d'un objet **Index** constitue un composant de l'index. Pour définir un nouvel objet **Index**, paramétrez ses propriétés avant de l'ajouter à une collection. L'objet **Index** pourra ainsi être utilisé ultérieurement.

> [!NOTE]
> <P>[!REMARQUE] Vous ne pouvez modifier le paramètre de propriété <STRONG>Name</STRONG> d'un objet <STRONG>Index</STRONG> que si le paramètre <STRONG><A href="connection-updatable-property-dao.md">Updatable</A></STRONG> de l'objet conteneur <STRONG>TableDef</STRONG> a la valeur <STRONG>True</STRONG>.</P>

Si vous indiquez une clé primaire pour une table, le moteur de base de données Microsoft Access la définit automatiquement comme index primaire. Il s'agit d'un ou plusieurs champs qui identifient de manière unique tous les enregistrements d'une table dans un ordre prédéfini. Le champ d'index primaire devant être unique, le moteur de base de données Microsoft Access attribue automatiquement la valeur **True** à la propriété **Unique** de l'objet **Index**. Si l'index primaire comprend plusieurs champs, chaque champ peut contenir des valeurs en double, mais la combinaison de valeurs de tous les champs indexés doit être unique. Un index primaire est constitué d'une clé correspondant à la table et comprend toujours les mêmes champs que la clé primaire.

> [!IMPORTANT]
> [!IMPORTANTE] Assurez-vous que les données sont conformes aux attributs du nouvel index. Si l'index impose des valeurs uniques, veillez à ce que les enregistrements de données ne contiennent aucune valeur en double. En effet, le moteur de base de données Microsoft Access ne peut pas créer l'index s'il existe des valeurs en double. Une erreur interceptable se produit lorsque vous tentez d'utiliser la méthode Append sur le nouvel index.

Lors de la création d'une relation qui applique l'intégrité référentielle, le moteur de base de données Microsoft Access crée automatiquement un index à l'aide de la propriété **Foreign**, définie comme clé étrangère dans la table de référence. Une fois une relation de table définie, le moteur de base de données Microsoft Access empêche tout ajout ou toute modification dans la base de données contraire à cette relation. Si vous définissez la propriété **Attributes** de l'objet **[Relation](relation-object-dao.md)** afin d'autoriser les mises à jour en cascade et les suppressions en cascade, le moteur de base de données Microsoft Access met à jour ou supprime automatiquement les enregistrements des tables liées.

1.  Utilisez la méthode **CreateIndex** sur un objet **TableDef**.

2.  Utilisez la méthode **CreateField** sur l'objet **Index** pour créer un objet **Field** pour chaque champ (colonne) à inclure dans l'objet **Index**.

3.  Définissez les propriétés **Index** requises.

4.  Ajoutez l'objet **Field** à la collection **Fields**.

5.  Ajoutez l'objet **Index** à la collection **Indexes**.
    

    > [!NOTE]
    > <P>[!REMARQUE] La propriété <STRONG>Clustered</STRONG> est ignorée pour les bases de données qui utilisent le moteur de base de données Microsoft Access, qui ne prend pas en charge les index cluster.</P>



## <a name="example"></a>Exemple

Cet exemple crée un nouvel objet **Index**, l'ajoute à la collection **Indexes** de la **TableDef** Employees, puis énumère la collection **Indexes** de la **TableDef**. Enfin, il énumère un objet **Recordset**, d'abord à l'aide de l' **Index** primaire, ensuite à l'aide du nouvel objet **Index**. La procédure IndexOutput est requise pour exécuter cette opération.

```vb
    Sub IndexObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create new index, create and append Field 
     ' objects to its Fields collection. 
     Set idxNew = .CreateIndex("NewIndex") 
     
     With idxNew 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     
     ' Add new Index object to the Indexes collection 
     ' of the Employees table collection. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection of Employees 
     ' table. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Print report using old and new indexes. 
     IndexOutput rstEmployees, "PrimaryKey" 
     IndexOutput rstEmployees, idxNew.Name 
     rstEmployees.Close 
     
     ' Delete new Index because this is a 
     ' demonstration. 
     .Indexes.Delete idxNew.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub IndexOutput(rstTemp As Recordset, _ 
     strIndex As String) 
     ' Report function for FieldX. 
     
     With rstTemp 
     ' Set the index. 
     .Index = strIndex 
     .MoveFirst 
     Debug.Print "Recordset = " & .Name & _ 
     ", Index = " & .Index 
     Debug.Print " EmployeeID - Country - Name" 
     
     ' Enumerate the recordset using the specified 
     ' index. 
     Do While Not .EOF 
     Debug.Print " " & !EmployeeID & " - " & _ 
     !Country & " - " & !LastName & ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Sub 
```

<br/>

Cet exemple utilise la méthode **CreateIndex** pour créer deux nouveaux objets **Index** et les ajouter à la collection **Indexes** de l'objet **TableDef** Employees. Il énumère ensuite la collection **Indexes** de l'objet **TableDef**, la collection **Fields** des nouveaux objets **Index**, et la collection Properties des nouveaux objets **Index**. La fonction CreateIndexOutput est requise pour exécuter cette opération.

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
