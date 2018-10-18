---
<<<<<<< Titre tête : conversion du Code DAO vers ADO TOCTitle : conversion du Code DAO vers ADO ms:assetid : 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl : https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID : ms.date 48544585 : 18/09/2015 === titre : convertir de DAO code ADO TOCTitle : code DAO convertir ADO ms:assetid : 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl : https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID : ms.date 48544585 : 10/16/2018
>>>>>>> maître mtps_version : v=office.15 f1_keywords :
- vbaac10.chm5267115 f1_categories :
- Office.Version=v15
---

<<<<<<< Tête
# <a name="converting-dao-code-to-ado"></a>Conversion du code DAO vers ADO
=======
# <a name="convert-dao-code-to-ado"></a>Conversion du code DAO vers ADO
>>>>>>> master

**S’applique à**: Access 2013 | Office 2013

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
<<<<<<< Tête
<th><p><strong>ADO (ADODB)</strong></p></th>
=======
<th><p><strong>ADO (ADODB)</strong></p></th>
>>>>>>>forme de base
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
<<<<<<< Tête
<td><p>Extrait une série de pointeurs vers les enregistrements du jeu d'enregistrements</p></td>
=======
<td><p>Récupère un ensemble de pointeurs vers les enregistrements du jeu d’enregistrements.</p></td>
>>>>>>>forme de base
</tr>
<tr class="even">
<td><p>Snapshot-Type</p></td>
<td><p>Static</p></td>
<<<<<<< Tête
<td><p>Tous deux extraient des enregistrements complets mais un jeu d'enregistrements Static est actualisable.</p></td>
</tr>
<tr class="odd">
<td><p>Table-Type</p></td>
<td><p>Keyset avec l'option adCmdTableDirect</p></td>
=======
<td><p>Tous deux extraient des enregistrements complets mais un jeu d’enregistrements statique peut être mis à jour.</p></td>
</tr>
<tr class="odd">
<td><p>Table-Type</p></td>
<td><p>Keyset avec l’option adCmdTableDirect.</p></td>
>>>>>>>forme de base
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Champ</p></td>
<td><p>Champ</p></td>
<<<<<<< Tête
<td><p>Quand référencée dans un jeu d'enregistrements</p></td>
=======
<td><p>Quand référencée dans un jeu d’enregistrements.</p></td>
>>>>>>>forme de base
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
<<<<<<< Déplacement tête concentrer à partir de l’enregistrement en cours via **MoveNext, MoveLast, MoveFirst, MovePrevious** sans d’abord à l’aide de la méthode **CancelUpdate** exécutera implicitement la méthode **Update** .
> === Déplacement du curseur à partir de l’enregistrement en cours via **MoveNext, MoveLast, MoveFirst, MovePrevious** sans utiliser préalablement la méthode **CancelUpdate** implicitement exécute la méthode de **mise à jour** .
>>>>>>> master

### <a name="about-the-contributors"></a>À propos des collaborateurs

**Lien fourni par** la Communauté [UtterAccess](https://www.utteraccess.com) . UtterAccess est le premier forum d'aide et wiki de Microsoft Access.

- [Choix entre DAO et ADO](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<<<<<<< Tête

=======
<br/>
>>>>>>> master

