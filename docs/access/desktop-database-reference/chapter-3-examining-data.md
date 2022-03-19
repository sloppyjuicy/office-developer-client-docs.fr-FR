---
title: 'Chapitre 3 : Examen de données'
TOCTitle: 'Chapter 3: Examining data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 794b27e50abe0989e064b33244f6b3362d014210
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633623"
---
# <a name="chapter-3-examining-data"></a>Chapitre 3 : Examen de données

**S’applique à** : Access 2013, Office 2013

Le chapitre 2 vous a appris à récupérer des données à partir d'une source de données présentée sous la forme d'un objet **Recordset**. Ce chapitre décrit l'objet **Recordset** plus en détail et explique notamment comment naviguer dans un **Recordset** afin d'afficher ses données.

Les objets **Recordset** possèdent des méthodes et des propriétés qui vous permettent de les explorer et d'examiner leur contenu. Selon les fonctionnalités prises en charge par le fournisseur, certaines méthodes et propriétés des objets **Recordset** sont disponibles et d'autres ne le sont pas. Pour continuer à explorer l'objet **Recordset**, imaginez un **jeu d'enregistrements** renvoyé par la base de données exemple Northwind sur Microsoft SQL Server 2000, à l'aide du code suivant :

```vb 
 
'BeginRsTour 
Public Sub RecordsetTour() 
 On Error GoTo ErrHandler: 
 
 Dim objRs As New ADODB.Recordset 
 Dim strSQL As String 
 
 strSQL = "SELECT ProductID, ProductName, UnitPrice FROM Products " & _ 
 "WHERE CategoryID = 7" '7 = Produce 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, _ 
 adLockReadOnly, adCmdText 
 
 'Clean up 
 objRs.Close 
 Set objRs = Nothing 
 Exit Sub 
 
ErrHandler: 
 If Not objRs Is Nothing Then 
 If objRs.State = adStateOpen Then objRs.Close 
 Set objRs = Nothing 
 End If 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndRsTour 
```


Cette requête SQL renvoie un **jeu d'enregistrements** constitué de cinq lignes (enregistrements) et de trois colonnes (champs). Les valeurs de chaque ligne sont indiquées dans le tableau suivant.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>CHAMP 0<br />
Name = ProductID</p></th>
<th><p>CHAMP 1<br />
Name = ProductName</p></th>
<th><p>CHAMP 2<br />
Name = UnitPrice</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>7 </p></td>
<td><p>Pêches séchées bio Oncle Bob</p></td>
<td><p>30.0000</p></td>
</tr>
<tr class="even">
<td><p>14 </p></td>
<td><p>Tofu</p></td>
<td><p>23.2500</p></td>
</tr>
<tr class="odd">
<td><p>28</p></td>
<td><p>Choucroute Frau Kraut</p></td>
<td><p>45.6000</p></td>
</tr>
<tr class="even">
<td><p>51</p></td>
<td><p>Pommes séchées Manjimup</p></td>
<td><p>53.0000</p></td>
</tr>
<tr class="odd">
<td><p>74</p></td>
<td><p>Tofu LongVi</p></td>
<td><p>10.0000</p></td>
</tr>
</tbody>
</table>


La section suivante explique comment localiser la position actuelle du curseur dans cet exemple **de jeu d’enregistrements**.

Ce chapitre présente les rubriques suivantes :

- [Localisation de l’enregistrement actuel (ADO)](locating-the-current-record.md)
- [Navigation dans les données (ADO)](navigating-through-the-data.md)
- [Understanding Recordset structure (ADO)](understanding-recordset-structure.md)
