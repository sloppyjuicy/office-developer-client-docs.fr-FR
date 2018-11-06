---
title: Méthode Recordset.Seek (DAO)
TOCTitle: Seek Method
ms:assetid: ef83d909-c962-b016-7d33-36eacdc25c2c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836416(v=office.15)
ms:contentKeyID: 48548585
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053061
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5df9c972095d61ff17fa2a405a6786c08dad74fc
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997776"
---
# <a name="recordsetseek-method-dao"></a>Méthode Recordset.Seek (DAO)

**S’applique à**: Access 2013, Office 2013

Localise l'enregistrement dans un objet **Recordset** de type table indexée en fonction des critères spécifiés pour l'index actuel et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . Seek (***comparaison***, ***touche1***, ***Key2***, ***Key3***, ***Touche4***, ***Touche5***, ***Touche6***, ***Touche7***, ***Touche8***, ***Touche9***, ***Touche10***, ***Touche11***, ***Touche12***, ***Touche13***)

*expression* Variable qui représente un objet **Recordset** .

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Requis/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Comparison</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>L'une des expressions de chaîne suivantes : &lt;, &lt;=, =, &gt;= ou &gt;.</p></td>
</tr>
<tr class="even">
<td><p><em>Key1, Key2...Key13</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Une ou plusieurs valeurs correspondant aux champs dans l'index actuel de l'objet <strong>Recordset</strong>, comme indiqué par son paramètre de propriété <strong>Index</strong>. Vous pouvez utiliser les arguments clés jusqu'à 13.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous devez définir l'index actuel via la propriété **Index** avant d'utiliser la méthode **Seek**. Si l'index identifie un champ de clé non unique, **Seek** localise le premier enregistrement correspondant aux critères.

La méthode **Seek** recherche dans les champs de clé spécifiées et recherche le premier enregistrement qui répond aux critères spécifiés par comparaison et touche1. Une fois l'enregistrement trouvé, il devient actif et la propriété **NoMatch** reçoit la valeur **False**. Si la méthode **Seek** ne parvient pas à trouver de correspondance, la propriété **NoMatch** est affectée de la valeur **True**, et l'enregistrement actif n'est pas défini.

Si la comparaison est égal (=), supérieur ou égal (\>=), supérieur ou (\>), **Seek** commence au début de l’index et de transférer des recherches.

Si la comparaison est inférieure à (\<) ou inférieur ou égal (\<=), **Seek** commence à la fin de l’index et de recherche vers l’arrière. Toutefois, s'il existe des doublons à la fin de l'index, la méthode **Seek** démarre arbitrairement à partir de l'un des doublons, puis effectue une recherche vers l'arrière.

Vous devez spécifier des valeurs pour tous les champs définis dans l'index. Si vous utilisez **Seek** avec un index à plusieurs colonnes, et que vous ne spécifiez pas de valeur de comparaison pour chaque champ de l'index, vous ne pouvez pas utiliser l'opérateur égal (=) dans la comparaison. C’est parce que certains des champs de critères (key2 key3 et ainsi de suite) par défaut Null, ce qui correspondra probablement pas. Par conséquent, l'opérateur égal ne fonctionnera correctement que s'il existe un enregistrement dont les valeurs sont toutes **null** hormis la clé que vous recherchez. Il est recommandé d’utiliser supérieur ou égal (\>=) opérateur à la place.

L’argument touche1 doit être du même type de données de champ que le champ correspondant dans l’index en cours. Par exemple, si l’index actuel fait référence à un champ numérique (par exemple, ID d’employé), l’argument touche1 doit être numérique. De même, si l’index actuel fait référence à un champ de texte (tel que le nom de famille), touche1 doit être une chaîne.

Il n'est pas nécessaire d'avoir un enregistrement actif pour utiliser **Seek**.

Vous pouvez utiliser la collection **[Indexes](indexes-collection-dao.md)** pour énumérer les index existants.

Pour rechercher un enregistrement dans un objet **Recordset** de type feuille de réponse dynamique ou instantané qui satisfasse à une condition spécifique non représentée par les index existants, utilisez la méthode **[Find](recordset-findfirst-method-dao.md)**. Pour inclure tous les enregistrements, et pas seulement ceux qui répondent à une condition spécifique, utilisez la méthode **[Move](recordset-movefirst-method-dao.md)** pour passer d'un enregistrement à un autre.

Vous ne pouvez pas appliquer la méthode **Seek** à une table liée, car les tables liées ne peuvent pas être ouvertes en tant qu'objets **Recordset** de type table. Cependant, si vous vous servez de la méthode **[OpenDatabase](dbengine-opendatabase-method-dao.md)** pour ouvrir directement une base de données ISAM installable (non ODBC), vous pouvez appliquer la méthode **Seek** aux tables de cette base de données.

## <a name="example"></a>Exemple

Cet exemple démontre la méthode **Seek** en permettant à l'utilisateur de rechercher un produit en fonction d'un numéro d'identification.

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim intFirst As Integer 
       Dim intLast As Integer 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' You must open a table-type Recordset to use an index,  
       ' and hence the Seek method. 
       Set rstProducts = _ 
          dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
       With rstProducts 
          ' Set the index. 
          .Index = "PrimaryKey" 
     
          ' Get the lowest and highest product IDs. 
          .MoveLast 
          intLast = !ProductID 
          .MoveFirst 
          intFirst = !ProductID 
     
          Do While True 
             ' Display current record information and ask user  
             ' for ID number. 
             strMessage = "Product ID: " & !ProductID & vbCr & _ 
                "Name: " & !ProductName & vbCr & vbCr & _ 
                "Enter a product ID between " & intFirst & _ 
                " and " & intLast & "." 
             strSeek = InputBox(strMessage) 
     
             If strSeek = "" Then Exit Do 
     
             ' Store current bookmark in case the Seek fails. 
             varBookmark = .Bookmark 
     
             .Seek "=", Val(strSeek) 
     
             ' Return to the current record if the Seek fails. 
             If .NoMatch Then 
                MsgBox "ID not found!" 
                .Bookmark = varBookmark 
             End If 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Cet exemple de code montre comment utiliser la propriété **NoMatch** pour déterminer si les opérations **Seek** et **FindFirst** ont abouti. Si ce n'est pas le cas, l'utilisateur en est informé de façon appropriée. Les procédures SeekMatch et FindMatch sont nécessaires à l'exécution de cette procédure.

```vb
    Sub NoMatchX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim rstCustomers As Recordset 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim strCountry As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' Default is dbOpenTable; required if Index property will  
       ' be used. 
       Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
       With rstProducts 
          .Index = "PrimaryKey" 
     
          Do While True 
             ' Show current record information; ask user for  
             ' input. 
             strMessage = "NoMatch with Seek method" & vbCr & _ 
                "Product ID: " & !ProductID & vbCr & _ 
                "Product Name: " & !ProductName & vbCr & _ 
                "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
                "Enter a product ID." 
             strSeek = InputBox(strMessage) 
             If strSeek = "" Then Exit Do 
     
             ' Call procedure that seeks for a record based on  
             ' the ID number supplied by the user. 
             SeekMatch rstProducts, Val(strSeek) 
          Loop 
     
          .Close 
       End With 
     
       Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
          "SELECT CompanyName, Country FROM Customers " & _ 
          "ORDER BY CompanyName", dbOpenSnapshot) 
     
       With rstCustomers 
     
          Do While True 
             ' Show current record information; ask user for  
             ' input. 
             strMessage = "NoMatch with FindFirst method" & _ 
                vbCr & "Customer Name: " & !CompanyName & _ 
                vbCr & "Country: " & !Country & vbCr & _ 
                "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
                "Enter country on which to search." 
             strCountry = Trim(InputBox(strMessage)) 
             If strCountry = "" Then Exit Do 
     
             ' Call procedure that finds a record based on  
             ' the country name supplied by the user. 
             FindMatch rstCustomers, _ 
                "Country = '" & strCountry & "'" 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset, _ 
       intSeek As Integer) 
     
       Dim varBookmark As Variant 
       Dim strMessage As String 
     
       With rstTemp 
          ' Store current record location. 
          varBookmark = .Bookmark 
          .Seek "=", intSeek 
     
          ' If Seek method fails, notify user and return to the  
          ' last current record. 
          If .NoMatch Then 
             strMessage = _ 
                "Not found! Returning to current record." & _ 
                vbCr & vbCr & "NoMatch = " & .NoMatch 
             MsgBox strMessage 
             .Bookmark = varBookmark 
          End If 
     
       End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
       strFind As String) 
     
       Dim varBookmark As Variant 
       Dim strMessage As String 
     
       With rstTemp 
          ' Store current record location. 
          varBookmark = .Bookmark 
          .FindFirst strFind 
     
          ' If Find method fails, notify user and return to the  
          ' last current record. 
          If .NoMatch Then 
             strMessage = _ 
                "Not found! Returning to current record." & _ 
                vbCr & vbCr & "NoMatch = " & .NoMatch 
             MsgBox strMessage 
             .Bookmark = varBookmark 
          End If 
     
       End With 
     
    End Sub 
```

<br/>

L'exemple suivant montre comment utiliser la méthode Seek pour rechercher un enregistrement dans une table liée.

**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
