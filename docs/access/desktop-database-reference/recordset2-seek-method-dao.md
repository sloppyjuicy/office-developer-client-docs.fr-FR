---
title: Recordset2.Seek, méthode (DAO)
TOCTitle: Seek Method
ms:assetid: 9871619b-a303-c97d-54c0-defc8d9b87f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197940(v=office.15)
ms:contentKeyID: 48546489
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 15a92844e568c69ad490eb612125eff26a4c081e
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462303"
---
# <a name="recordset2seek-method-dao"></a>Recordset2.Seek, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Localise l’enregistrement dans un objet **Recordset** de type table indexé qui correspond aux critères spécifiés pour l’index actuel et fait de cet enregistrement l’enregistrement actif (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* .Seek(***Comparison** _, _*_Key1_*_, _*_Key2_*_, _*_Key3_*_, _*_Key4_*_, _*_Key5_*_, _*_Key6_*_, _*_Key7_*_, _*_Key8_*_, _*_Key9_*_, _*_Key10_*_, _*_Key11_*_, _*_Key12_*_, _*_Key13_**)

*expression* Variable qui représente un **objet Recordset2** .

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
<td><p><em>Comparaison</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>L'une des expressions de chaîne suivantes : &lt;, &lt;=, =, &gt;= ou &gt;.</p></td>
</tr>
<tr class="even">
<td><p><em>Key1, Key2...Key13</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Une ou plusieurs valeurs correspondant aux champs dans l'index actuel de l'objet <strong>Recordset</strong>, comme indiqué par son paramètre de propriété <strong>Index</strong>. Vous pouvez utiliser jusqu'à 13 arguments clés.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous devez définir l’index actuel avec la propriété **Index** avant d’utiliser la méthode **Seek**. Si l’index identifie un champ de clé non unique, la méthode **Seek** localise le premier enregistrement qui correspond aux critères.

La méthode **Seek** effectue une recherche dans les champs clés spécifiés et recherche le premier enregistrement qui répond aux critères spécifiés par comparaison et key1. Une fois trouvé, il rend cet enregistrement actif et définit la propriété **NoMatch** sur **False**. Si la méthode **Seek** ne parvient pas à trouver une correspondance, la propriété **NoMatch** est définie sur **True** et l’enregistrement actuel n’est pas défini.

Si le paramètre de comparaison est égal (=), supérieur ou égal (\>=) ou supérieur à (\>), la méthode **Seek** commence au début de l’index et effectue une recherche vers l’avant.

Si la comparaison est inférieure à (\<) ou inférieure ou égale (\<=), **Seek** commence à la fin de l’index et effectue une recherche vers l’arrière. Toutefois, s’il existe des entrées d’index en double à la fin de l’index, **Seek** commence par une entrée arbitraire parmi les doublons, puis effectue une recherche vers l’arrière.

Vous devez spécifier des valeurs pour tous les champs définis dans l’index. Si vous utilisez **Seek** avec un index à plusieurs colonnes et que vous ne spécifiez pas de valeur de comparaison pour chaque champ de l’index, vous ne pouvez pas utiliser l’opérateur égal (=) dans la comparaison. Cela est dû au fait que certains champs de critères (key2, key3, etc.) ont la valeur Null par défaut, ce qui ne correspond probablement pas. Par conséquent, l’opérateur égal fonctionne correctement uniquement si vous avez un enregistrement qui est tout **null** à l’exception de la clé que vous recherchez. Il est recommandé d’utiliser à la place l’opérateur supérieur ou égal (\>=).

L'argument key1 doit être du même type de données que le champ correspondant dans l'index actuel. Par exemple, si l'index actuel fait référence à un champ de type Numérique (tel que le numéro d'identification de l'employé), key1 doit être numérique. De même, si l'index actuel fait référence à un champ de type Texte (par exemple, celui accueillant le nom de famille), key1 doit être une chaîne.

Il n’est pas obligatoire qu’un enregistrement soit actif lorsque vous utilisez la méthode **Seek**.

Vous pouvez utiliser la collection d’**[index](indexes-collection-dao.md)** pour énumérer les index existants.

Pour localiser un enregistrement dans un **Recordset** de type feuille de réponse dynamique ou capture instantanée qui répond à une condition spécifique non couverte pas les index existants, utilisez les méthodes **[Find](recordset2-findfirst-method-dao.md)**. Pour inclure tous les enregistrements, et pas uniquement ceux qui répondent à une condition spécifique, utilisez les méthodes **[Move](recordset-movefirst-method-dao.md)** pour passer d’un enregistrement à un autre.

Vous ne pouvez pas utiliser la méthode **Seek** sur une table liée, car vous ne pouvez pas ouvrir des tables liées en tant qu’objets **Recordset** de type table. Toutefois, si vous utilisez la méthode **[OpenDatabase](dbengine-opendatabase-method-dao.md)** pour ouvrir directement une base de données ISAM (non ODBC) installable, vous pouvez utiliser **Seek** sur les tables de cette base de données.

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
