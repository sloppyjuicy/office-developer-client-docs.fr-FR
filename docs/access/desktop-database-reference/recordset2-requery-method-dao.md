---
title: Recordset2. Requery, méthode (DAO)
TOCTitle: Requery Method
ms:assetid: d063c1e0-2fb7-b5cf-4d98-6f77a5a13cec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834712(v=office.15)
ms:contentKeyID: 48547837
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052940
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 44f573d179c26677fc801dac82e0deecc3874fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307209"
---
# <a name="recordset2requery-method-dao"></a>Recordset2. Requery, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Met à jour les données d'un objet **[Recordset](recordset-object-dao.md)** en réexécutant la requête sur laquelle l'objet est basé.

## <a name="syntax"></a>Syntaxe

*expression* . Requery (***défnouvellerequête***)

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
<td><p><em>Défnouvellerequête</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Représente la valeur de la propriété <strong>Name</strong> d’un objet <strong><a href="querydef-object-dao.md">QueryDef</a></strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Cette méthode s'avère utile pour s'assurer qu'un objet **Recordset** contient les données les plus récentes. Cette méthode remplit à nouveau l' **objet Recordset** actif à l'aide des paramètres de requête actuels ou (dans un espace de travail Microsoft Access) des nouveaux paramètres fournis par l'argument défnouvellerequête.

Si vous ne spécifiez pas d'argument défnouvellerequête, l' **objet Recordset** est rempli en fonction de la définition de requête et des paramètres utilisés pour remplir initialement l' **objet Recordset**. Any changes to the underlying data will be reflected during this re-population. If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.

Si vous spécifiez l' **objet querydef** d'origine dans l'argument défnouvellerequête, l' **objet Recordset** est reinterrogé à l'aide des paramètres spécifiés par l' **objet querydef**. Les modifications apportées aux données sous-jacentes sont répercutées lors de ce nouveau remplissage. Pour répercuter les modifications apportées aux valeurs des paramètres de requête dans l' **objet Recordset**, vous devez spécifier l'argument défnouvellerequête.

If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.

Lorsque vous utilisez la méthode **Requery**, le premier enregistrement de l'objet **Recordset** devient l'enregistrement actif.

Vous ne pouvez pas appliquer la méthode **Requery** aux objets **Recordset** de type feuille de réponse dynamique ou instantané dont la propriété **[Restartable](recordset2-restartable-property-dao.md)** a la valeur **False**. Toutefois, si vous fournissez l'argument facultatif défnouvellerequête, **** la propriété Restartable est ignorée.

Si les propriétés **[BOF](recordset2-bof-property-dao.md)** et **[EOF](recordset2-eof-property-dao.md)** de l'objet **Recordset** ont toutes deux la valeur **True** après que vous ayez utilisé la méthode **Requery**, la requête ne renvoie aucun enregistrement et l'objet **Recordset** ne contient pas de données.

## <a name="example"></a>Exemple

Cet exemple de code montre comment la méthode **Requery** peut être utilisée pour actualiser une requête suite à la modification des données sous-jacentes.

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset2 
     Dim rstChange As Recordset2 
     
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
 Dim rstView As Recordset2 
 
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

