---
title: Objet TableDef (DAO)
TOCTitle: TableDef Object
ms:assetid: 715146b6-c62a-abff-28ee-e6bbe3c08adf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195790(v=office.15)
ms:contentKeyID: 48545582
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef0a7c167321a45249fb022e0987a5f8d6364ea0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469123"
---
# <a name="tabledef-object-dao"></a>Objet TableDef (DAO)

**S’applique à**: Access 2013 | Office 2013

Un objet **TableDef** représente la définition stockée d'une table de base ou d'une table liée (espaces de travail Microsoft Access uniquement).

## <a name="remarks"></a>Remarques

Vous manipulez une définition de table à l'aide d'un objet **TableDef**, de ses méthodes et de ses propriétés. Par exemple, vous pouvez :

- Examiner la structure de champ et d'index d'une table locale, liée ou externe dans une base de données.

- Utiliser les propriétés **Connect** et **SourceTableName** pour définir ou renvoyer des informations sur les tables liées et utiliser la méthode **RefreshLink** pour mettre à jour les connexions aux tables liées.

- Utiliser les propriétés **ValidationRule** et **ValidationText** pour définir ou renvoyer les conditions de validation.

- Utilisez la méthode **OpenRecordset** pour créer une table, feuille de réponse dynamique, dynamique, instantané ou objet **Recordset** de type avant uniquement, en fonction de la définition de table.

Pour les tables de base, la propriété **RecordCount** contient le nombre d'enregistrements dans la table de base de données spécifiée. Tables liées, **la propriété RecordCount** est toujours -1.

Pour créer un objet **TableDef**, utilisez la méthode **[CreateTableDef](database-createtabledef-method-dao.md)**.

### <a name="to-add-a-field-to-a-table"></a>Pour ajouter un champ à une table

1.  Assurez-vous que les objets **[Recordset](recordset-object-dao.md)** basés sur la table sont tous fermés.

2.  Utilisez la méthode **CreateField** pour créer une variable d'objet **Field** et définir ses propriétés.

3.  Utilisez la méthode **Append** pour ajouter l'objet **Field** à la collection **Fields** de l'objet **TableDef**.

Vous pouvez supprimer un objet **Field** à partir d'une collection **TableDefs** si aucun index ne lui est attribué, mais vous perdrez les données du champ.

### <a name="to-create-a-table-that-is-ready-for-new-records-in-a-database"></a>Pour créer une table prête pour de nouveaux enregistrements dans une base de données

1.  Utilisez la méthode **CreateTableDef** pour créer un objet **TableDef**.

2.  Définissez ses propriétés.

3.  Pour chaque champ de la table, utilisez la méthode **CreateField** pour créer une variable d'objet **Field** et définir ses propriétés.

4.  Utilisez la méthode **Append** pour ajouter les champs à la collection **Fields** de l'objet **TableDef**.

5.  Utilisez la méthode **Append** pour ajouter le nouvel objet **TableDef** à la collection **TableDefs** de l'objet **Database**.

Une table liée est connectée à la base de données via les propriétés **SourceTableName** et **Connect** de l'objet **TableDef**.

### <a name="to-link-a-table-to-a-database"></a>Pour lier une table à une base de données

1.  Utilisez la méthode **CreateTableDef** pour créer un objet **TableDef**.

2.  Définissez les propriétés **Connect** et **SourceTableName** (et éventuellement, la propriété **Attributes** ).

3.  Utilisez la méthode **Append** pour ajouter cet objet à la collection **TableDefs** d'un objet **Database**.

Pour faire référence à un objet **TableDef** dans une collection par son nombre ordinal ou par son paramètre de propriété **Name**, utilisez l'une des formes de syntaxe suivantes :

**TableDefs**(0)

**TableDefs** (« nom »)

**TableDefs**\!\[nom\]

## <a name="example"></a>Exemple

Cet exemple crée un objet **TableDef** et l'ajoute à la collection **TableDefs** de l'objet de la base de données Northwind. Il énumère ensuite les collections **TableDefs** et **Properties** du nouvel objet **TableDef**.

```vb
    Sub TableDefX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfNew As TableDef 
       Dim tdfLoop As TableDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new TableDef object, append Field objects  
       ' to its Fields collection, and append TableDef  
       ' object to the TableDefs collection of the  
       ' Database object. 
       Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
       tdfNew.Fields.Append tdfNew.CreateField("Date", dbDate) 
       dbsNorthwind.TableDefs.Append tdfNew 
     
       With dbsNorthwind 
          Debug.Print .TableDefs.Count & _ 
             " TableDefs in " & .Name 
     
          ' Enumerate TableDefs collection. 
          For Each tdfLoop In .TableDefs 
             Debug.Print "  " & tdfLoop.Name 
          Next tdfLoop 
     
          With tdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new 
             ' TableDef object, only printing properties 
             ' with non-empty values. 
             For Each prpLoop In .Properties 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          End With 
     
          ' Delete new TableDef since this is a  
          ' demonstration. 
          .TableDefs.Delete tdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

Cet exemple crée un objet **TableDef** dans la base de données Northwind.

```vb 
Sub CreateTableDefX() 
 
   Dim dbsNorthwind As Database 
   Dim tdfNew As TableDef 
   Dim prpLoop As Property 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
   ' Create a new TableDef object. 
   Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
 
   With tdfNew 
      ' Create fields and append them to the new TableDef  
      ' object. This must be done before appending the  
      ' TableDef object to the TableDefs collection of the  
      ' Northwind database. 
      .Fields.Append .CreateField("FirstName", dbText) 
      .Fields.Append .CreateField("LastName", dbText) 
      .Fields.Append .CreateField("Phone", dbText) 
      .Fields.Append .CreateField("Notes", dbMemo) 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "before appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
      ' Append the new TableDef object to the Northwind  
      ' database. 
      dbsNorthwind.TableDefs.Append tdfNew 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "after appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
   End With 
 
   ' Delete new TableDef object since this is a  
   ' demonstration. 
   dbsNorthwind.TableDefs.Delete "Contacts" 
 
   dbsNorthwind.Close 
```

<br/>

L'exemple suivant montre comment créer un champ calculé. La méthode CreateField crée un champ nommé **FullName**. La propriété Expression est ensuite définie sur l'expression qui calcule la valeur du champ.

**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```
