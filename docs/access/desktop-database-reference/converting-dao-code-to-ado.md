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
ms.openlocfilehash: 60baeabfce93c2987cb9621c7cc877a7525a954c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876742"
---
# <a name="convert-dao-code-to-ado"></a>Convertir le code DAO en code ADO

**S’applique à**: Access 2013, Office 2013

> [!NOTE]
> Versions de la bibliothèque DAO antérieures à 3.6 ne sont pas fournies ou pris en charge dans Access.

## <a name="dao-to-ado-object-map"></a>DAO au mappage d’objets ADO

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td><p>Aucune</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Workspace</p></td>
<td><p>Aucune</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Base de données</p></td>
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
<td><p>Récupère un ensemble de pointeurs vers les enregistrements du jeu d’enregistrements.</p></td>
</tr>
<tr class="even">
<td><p>Snapshot-Type</p></td>
<td><p>Static</p></td>
<td><p>Tous deux extraient des enregistrements complets mais un jeu d’enregistrements statique peut être mis à jour.</p></td>
</tr>
<tr class="odd">
<td><p>Table-Type</p></td>
<td><p>Keyset avec l’option adCmdTableDirect.</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Champ</p></td>
<td><p>Champ</p></td>
<td><p>Quand référencée dans un jeu d’enregistrements.</p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a>DAO

#### <a name="open-a-recordset"></a>Ouvrir un jeu d'enregistrements

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a>Modifier un jeu d'enregistrements

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a>ADO

#### <a name="open-a-recordset"></a>Ouvrir un jeu d'enregistrements

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a>Modifier un jeu d'enregistrements

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> Le déplacement du curseur depuis l’enregistrement en cours via **MoveNext, MoveLast, MoveFirst, MovePrevious** sans utiliser préalablement la méthode **CancelUpdate** implicitement exécute la méthode de **mise à jour** .

### <a name="about-the-contributors"></a>À propos des collaborateurs

**Lien fourni par** la Communauté [UtterAccess](https://www.utteraccess.com) . UtterAccess est le premier forum d'aide et wiki de Microsoft Access.

- [Choix entre DAO et ADO](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

