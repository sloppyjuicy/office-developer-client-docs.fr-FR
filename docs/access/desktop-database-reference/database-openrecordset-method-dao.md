---
title: Database.OpenRecordset, méthode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: a243bc79-cac4-fe12-768d-d3d017954e78
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820966(v=office.15)
ms:contentKeyID: 48546753
ms.date: 06/04/2019
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052939
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: b13abd7f3f2c856a0f1a1288717d6f8affb81252
ms.sourcegitcommit: 4a570873914c58dd4cdbe97b5d9ec41866dc797c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2019
ms.locfileid: "34675742"
---
# <a name="databaseopenrecordset-method-dao"></a>Database.OpenRecordset, méthode (DAO)

**S’applique à** : Access 2013 | Office 2013

Crée un objet **[Recordset](recordset-object-dao.md)** et l’ajoute à la collection **Recordsets**.

## <a name="syntax"></a>Syntaxe

*expression*.**OpenRecordset** (_Name_, _Type_, _Options_, _LockEdit_)

*expression* Variable qui représente un objet **Database**.

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
<td><p><em>Name</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Source des enregistrements du nouveau <strong>Recordset</strong>. La source peut être un nom de table, un nom de requête ou une instruction SQL qui renvoie des enregistrements. Pour les objets <strong>Recordset</strong> de type table dans les bases de données du moteur de base de données Microsoft Access, la source peut uniquement être un nom de table.</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> qui indique le type de <strong>Recordset</strong> à ouvrir.</p><p><strong>REMARQUE</strong> : si vous ouvrez un objet <strong>Recordset</strong> dans un espace de travail Microsoft Access et que vous n’indiquez aucun type, <strong>OpenRecordset</strong> crée un objet <strong>Recordset</strong> de type table, si possible. If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Combinaison de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> qui indiquent les caractéristiques du nouveau <strong>Recordset</strong>.</p><p><strong>REMARQUE</strong> : <strong>dbConsistent</strong> et <strong>dbInconsistent</strong> s’excluent mutuellement, et l’utilisation de ces deux constantes peut entraîner une erreur. Fournir un argument LockEdit lorsque Options utilise la constante <strong>dbReadOnly</strong> génère également une erreur.</p>
</td>
</tr>
<tr class="even">
<td><p><em>LockEdit</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> qui détermine le verrouillage du <strong>Recordset</strong>.</p><p><strong>REMARQUE</strong> : vous pouvez utiliser <strong>dbReadOnly</strong> dans l’argument Options ou l’argument LockedEdit, mais pas dans les deux. Si vous l’utilisez dans les deux arguments, une erreur d’exécution se produit.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

Recordset

## <a name="remarks"></a>Remarques

En règle générale, si l’utilisateur obtient cette erreur lors de la mise à jour d’un enregistrement, votre code doit actualiser le contenu des champs et récupérer les valeurs nouvellement modifiées. Si une erreur survient lors de la suppression d’un enregistrement, votre code peut afficher les données du nouvel enregistrement à l’utilisateur, ainsi qu’un message indiquant que les données ont récemment été modifiées. À ce stade, votre code peut demander une confirmation pour s’assurer que l’utilisateur souhaite toujours supprimer l’enregistrement.

Vous pouvez également utiliser la constante **dbSeeChanges** si vous ouvrez un **Recordset** dans un espace de travail ODBC connecté au moteur de base de données Microsoft Access par rapport à une table Microsoft SQL Server 6.0 (ou version ultérieure) qui comporte une colonne IDENTITY, sinon une erreur peut survenir.

L’ouverture de plusieurs objets **Recordset** sur une source de données ODBC peut échouer car la connexion est occupée par un appel **OpenRecordset** précédent. Pour éviter cela, vous pouvez remplir complètement l’objet **Recordset** à l’aide de la méthode **MoveLast** dès l’ouverture du **Recordset**.

La fermeture d’un **Recordset** avec la méthode **[Close](connection-close-method-dao.md)** le supprime automatiquement de la collection **Recordsets**.


> [!NOTE]
> Si l’argument *source* fait référence à une instruction SQL composée d’une chaîne concaténée avec une valeur non entière, et que les paramètres système spécifient un caractère décimal d’un format différent de celui des États-Unis, tel qu’une virgule (par exemple, strSQL = "PRICE &gt; " &amp; lngPrice, et lngPrice = 125,50), une erreur se produit lorsque vous essayez d’ouvrir l’objet **Recordset**. Cela s'explique par le fait que lors de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut du système et le langage SQL n'accepte que les caractères décimaux de la notation américaine.

**Lien fourni par** la communauté [UtterAccess](https://www.utteraccess.com). UtterAccess est un forum d’aide et wiki de Microsoft Access réputé.

- [Transfert de données entre Access et Excel](https://www.utteraccess.com/forum/transfer-data-access-ex-t1672619.html)

## <a name="example"></a>Exemple

L’exemple suivant montre comment ouvrir un objet Recordset basé sur une requête avec paramètres.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

L’exemple suivant montre comment ouvrir un Recordset basé sur un tableau ou une requête.

```vb 
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

L’exemple suivant montre comment ouvrir un Recordset basé sur une instruction SQL (Structured Query Language).

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

L’exemple suivant montre comment utiliser la propriété Filter pour déterminer les enregistrements à inclure dans un Recordset ouvert par la suite.

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rst = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```



