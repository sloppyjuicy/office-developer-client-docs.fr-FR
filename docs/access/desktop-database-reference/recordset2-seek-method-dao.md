---
title: Recordset2. Seek, méthode (DAO)
TOCTitle: Seek Method
ms:assetid: 9871619b-a303-c97d-54c0-defc8d9b87f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197940(v=office.15)
ms:contentKeyID: 48546489
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9510faab9035f2b2cbcccae0a8ddefa484a95cb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307188"
---
# <a name="recordset2seek-method-dao"></a>Recordset2. Seek, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Localise l’enregistrement dans un objet **Recordset** de type table indexé qui correspond aux critères spécifiés pour l’index actuel et fait de cet enregistrement l’enregistrement actif (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . Seek (***Comparison***, ***key1***, ***touche2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)

*expression* Variable qui représente un objet **Recordset2** .

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
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
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
<td><p>Une ou plusieurs valeurs correspondant aux champs dans l'index actuel de l'objet <strong>Recordset</strong>, comme indiqué par son paramètre de propriété <strong>Index</strong>. Vous pouvez utiliser jusqu’à 13 arguments key.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous devez définir l’index actuel avec la propriété **Index** avant d’utiliser la méthode **Seek**. Si l’index identifie un champ de clé non unique, la méthode **Seek** localise le premier enregistrement qui correspond aux critères.

La méthode **Seek** recherche dans les champs de clé spécifiés et localise le premier enregistrement qui correspond aux critères spécifiés par Comparison et key1. Une fois trouvé, cet enregistrement devient l’enregistrement actif et la propriété **NoMatch** est définie sur **False**. Si la méthode **Seek** ne trouve pas de correspondance, la propriété **NoMatch** est définie sur **True**, et l’enregistrement actif n’est pas défini.

Si comparaison est égal (=), supérieur ou égal (\>=) ou supérieur à (\>), la méthode **Seek** commence au début de l'index et effectue une recherche vers l'avant.

Si comparaison est inférieur à (\<) ou inférieur ou égal (\<=), la méthode **Seek** commence à la fin de l'index et effectue une recherche vers l'arrière. Toutefois, s'il existe des doublons à la fin de l'index, la méthode **Seek** démarre arbitrairement à partir de l'un des doublons, puis effectue une recherche vers l'arrière.

Vous devez spécifier des valeurs pour tous les champs définis dans l'index. Si vous utilisez la méthode **Seek** avec un index à plusieurs colonnes et que vous ne spécifiez pas de valeur de comparaison pour chaque champ de l’index, vous ne pouvez pas utiliser l’opérateur égal (=) dans la comparaison. Ceci est dû au fait que certains champs de critères (key2, key3, etc.) seront définis par défaut sur Null, et ne correspondront probablement pas. Par conséquent, l’opérateur égal ne fonctionnera correctement que si vous disposez d’un enregistrement entièrement **null**, à l’exception de la clé que vous recherchez. Il est recommandé d'utiliser à la place l'opérateur supérieur ou\>égal (=).

L’argument key1 doit être du même type de champ que le champ correspondant dans l’index actuel. Par exemple, si l’index actuel fait référence à un champ numérique (comme Employee ID), key1 doit être numérique. De même, si l’index actuel fait référence à un champ de texte (comme Last Name), key1 doit être une chaîne.

Il n'est pas nécessaire d'avoir un enregistrement actif pour utiliser **Seek**.

Vous pouvez utiliser la collection **[Indexes](indexes-collection-dao.md)** pour énumérer les index existants.

Pour rechercher un enregistrement dans un objet **Recordset** de type feuille de réponse dynamique ou instantané qui satisfasse à une condition spécifique non représentée par les index existants, utilisez la méthode **[Find](recordset2-findfirst-method-dao.md)**. Pour inclure tous les enregistrements, et pas seulement ceux qui répondent à une condition spécifique, utilisez la méthode **[Move](recordset-movefirst-method-dao.md)** pour passer d'un enregistrement à un autre.

Vous ne pouvez pas appliquer la méthode **Seek** à une table liée, car les tables liées ne peuvent pas être ouvertes en tant qu'objets **Recordset** de type table. Cependant, si vous vous servez de la méthode **[OpenDatabase](dbengine-opendatabase-method-dao.md)** pour ouvrir directement une base de données ISAM installable (non ODBC), vous pouvez appliquer la méthode **Seek** aux tables de cette base de données.

## <a name="example"></a>Exemple

Cet exemple illustre la méthode **Seek** en autorisant l’utilisateur à rechercher un produit avec un numéro d’identification.

```vb
    Sub SeekX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
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
     Dim rstProducts As Recordset2 
     Dim rstCustomers As Recordset2 
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
