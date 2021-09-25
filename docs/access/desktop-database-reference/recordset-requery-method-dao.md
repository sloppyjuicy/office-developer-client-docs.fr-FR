---
title: Méthode Recordset.Requery (DAO)
TOCTitle: Requery Method
ms:assetid: a5d66eb5-499c-4133-f6c3-c7a1619a8a11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821155(v=office.15)
ms:contentKeyID: 48546840
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: ebcfcdb81899254b5e24496dff93f82fa626f7c6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572899"
---
# <a name="recordsetrequery-method-dao"></a>Méthode Recordset.Requery (DAO)

**S’applique à** : Access 2013, Office 2013

Met à jour les données dans un objet **[Recordset](recordset-object-dao.md)** en exécutant de nouveau la requête sur laquelle l’objet est basé.

## <a name="syntax"></a>Syntaxe

*expression* .Requery(***NewQueryDef***)

*expression* Variable qui représente un objet **Recordset**.

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
<td><p><em>NewQueryDef</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Représente la valeur de la propriété <strong>Name</strong> d’un objet <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Cette méthode s’avère utile pour s’assurer qu’un objet **Recordset** contient les données les plus récentes. Cette méthode remplit à nouveau l’objet **Recordset** actif à partir des paramètres de la requête actuelle ou (dans un espace de travail Microsoft Access) de ceux, nouveaux, fournis par l’argument défnouvellerequête.

Si vous ne spécifiez pas d’argument newquerydef, l’objet **Recordset** est de nouveau renseigné en fonction de la définition et des paramètres de requête déjà utilisés pour renseigner l’objet **Recordset** à l’origine. Toute modification à ces données sous-jacentes sera reflétée lors du nouveau remplissage. Si vous n’utilisez pas **QueryDef** pour créer **Recordset**, **Recorset** est créé à nouveau depuis le début.

Si vous spécifiez l'objet **QueryDef** d'origine dans l'argument newquerydef, **Recordset** fait l'objet d'une nouvelle requête basée sur les paramètres spécifiés par **QueryDef**. Les modifications apportées aux données sous-jacentes sont reflétées lors de ce nouveau remplissage. Pour répercuter les modifications effectuées au niveau de la valeur des paramètres de la requête dans l'objet **Recordset**, vous devez fournir l'argument newquerydef.

If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.

Lorsque vous utilisez la méthode **Requery**, le premier enregistrement de l'objet **Recordset** devient l'enregistrement actif.

Vous ne pouvez pas appliquer la méthode **Requery** aux objets **Recordset** de type feuille de réponse dynamique ou capture instantané dont la propriété **[Restartable](recordset-restartable-property-dao.md)** a la valeur **False**. Toutefois, si vous fournissez l'argument facultatif newquerydef, la propriété **Restartable** est ignorée.

Si les propriétés **[BOF](recordset-bof-property-dao.md)** et **[EOF](recordset-eof-property-dao.md)** de l'objet **Recordset** ont toutes deux la valeur **True** après que vous ayez utilisé la méthode **Requery**, la requête ne renvoie aucun enregistrement et l'objet **Recordset** ne contient pas de données.

## <a name="example"></a>Exemple

Cet exemple montre comment la méthode **Requery** peut être utilisée pour actualiser une requête après la modification des données sous-jacentes.

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset 
     Dim rstChange As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS ViewCountry Text; " & _ 
     "SELECT FirstName, LastName, Country FROM " & _ 
     "Employees WHERE Country = [ViewCountry] " & _ 
     "ORDER BY LastName") 
     
     qdfTemp.Parameters!ViewCountry = "USA" 
     Debug.Print "Data after initial query, " & _ 
     [ViewCountry] = USA" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Change underlying data. 
     Set rstChange = dbsNorthwind.OpenRecordset("Employees") 
     rstChange.AddNew 
     rstChange!FirstName = "Nina" 
     rstChange!LastName = "Roberts" 
     rstChange!Country = "USA" 
     rstChange.Update 
     
     rstView.Requery 
     Debug.Print "Requery after changing underlying data" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Restore original data because this is only a 
     ' demonstration. 
     rstChange.Bookmark = rstChange.LastModified 
     rstChange.Delete 
     rstChange.Close 
     
     rstView.Close 
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Cet exemple de code montre comment la méthode **Requery** peut être utilisée pour actualiser une requête suite à la modification de ses paramètres.

```vb 
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
 "PARAMETERS ViewCountry Text; " & _ 
 "SELECT FirstName, LastName, Country FROM " & _ 
 "Employees WHERE Country = [ViewCountry] " & _ 
 "ORDER BY LastName") 
 Set prmCountry = qdfTemp.Parameters!ViewCountry 
 
 qdfTemp.Parameters!ViewCountry = "USA" 
 Debug.Print "Data after initial query, " & _ 
 [ViewCountry] = USA" 
 Set rstView = qdfTemp.OpenRecordset 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 ' Change query parameter. 
 qdfTemp.Parameters!ViewCountry = "UK" 
 ' QueryDef argument must be included so that the 
 ' resulting Recordset reflects the change in the query 
 ' parameter. 
 rstView.Requery qdfTemp 
 Debug.Print "Requery after changing parameter, " & _ 
 "[ViewCountry] = UK" 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 rstView.Close 
 dbsNorthwind.Close 
 
End Sub 
 
```

