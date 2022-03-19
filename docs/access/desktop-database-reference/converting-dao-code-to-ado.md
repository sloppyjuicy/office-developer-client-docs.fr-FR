---
title: Convertir le code DAO en code ADO
TOCTitle: Convert DAO code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: ddd101f6b6eb226bd7984b5c63e1498c7168ba08
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626716"
---
# <a name="convert-dao-code-to-ado"></a>Convertir le code DAO en code ADO

**S’applique à** : Access 2013, Office 2013

> [!NOTE]
> Les versions de la bibliothèque DAO antérieures à 3.6 ne sont pas fournies ni prises en charge dans Access.

## <a name="dao-to-ado-object-map"></a>Mappage d'objet DAO en ADO

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p><strong>DAO</strong></p></th>
<th><p><strong>ADO (ADODB)</strong></p></th>
<th><p><strong>Remarque</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DBEngine</p></td>
<td><p>Aucun</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Workspace</p></td>
<td><p>Aucun</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Database</p></td>
<td><p>Connection</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Recordset</p></td>
<td><p>Recordset</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Dynaset-Type</p></td>
<td><p>Keyset</p></td>
<td><p>Extrait une série de pointeurs vers les enregistrements du jeu d'enregistrements.</p></td>
</tr>
<tr class="even">
<td><p>Snapshot-Type</p></td>
<td><p>Static</p></td>
<td><p>Tous deux extraient des enregistrements complets mais un jeu d'enregistrements Static est actualisable.</p></td>
</tr>
<tr class="odd">
<td><p>Table-Type</p></td>
<td><p>Keyset avec l'option adCmdTableDirect.</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Field</p></td>
<td><p>Field</p></td>
<td><p>Quand référencée dans un jeu d'enregistrements.</p></td>
</tr>
</tbody>
</table>


### <a name="dao"></a>DAO

#### <a name="open-a-recordset"></a>Ouvre un Recordset

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a>Modifie un Recordset

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a>ADO

#### <a name="open-a-recordset"></a>Ouvre un Recordset

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a>Modifie un Recordset

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> Le déplacement du curseur depuis l'enregistrement en cours via **MoveNext, MoveLast, MoveFirst, MovePrevious** sans utiliser préalablement la méthode **CancelUpdate** exécute implicitement la méthode **Update**.

### <a name="about-the-contributors"></a>À propos des collaborateurs

**Lien fourni par** la communauté [UtterAccess](https://www.utteraccess.com). UtterAccess est un forum d’aide et wiki de Microsoft Access réputé.

- [Choisir entre DAO et ADO](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)


