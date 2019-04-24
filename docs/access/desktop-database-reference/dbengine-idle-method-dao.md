---
title: DBEngine. Idle, méthode (DAO)
TOCTitle: Idle Method
ms:assetid: c90b565e-626e-139d-102a-0386601ce0c8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823202(v=office.15)
ms:contentKeyID: 48547666
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052978
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7a84e3cc4b35886a12b2e6b4cf92b7483fea293a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294329"
---
# <a name="dbengineidle-method-dao"></a>DBEngine. Idle, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Suspend le traitement des données, ce qui permet au moteur de base de données Microsoft Access de terminer les tâches en cours, telles que l’optimisation de la mémoire ou les expirations de délai des pages (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . InActif (***action***)

*expression* Variable qui représente un objet **DBEngine** .

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
<td><p><em>Action</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Spécifie l’action à effectuer. Il peut s'agir de l'une des constantes <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

La méthode **Idle** permet au moteur de base de données Microsoft Access d'effectuer des tâches en arrière-plan qui peuvent ne pas être à jour en raison de l'intensité du traitement des données. Cela est souvent le cas dans les environnements multi-utilisateur et multitâches qui ne disposent pas d'un délai de traitement en arrière-plan suffisant pour tenir à jour tous les enregistrements d'un objet **[Recordset](recordset-object-dao.md)**.

Habituellement, les verrous en lecture sont supprimés et les données présentes dans les objets **Recordset** de type feuille de réponse dynamique ne sont mises à jour qu'à partir du moment où aucune autre action (y compris les déplacements de souris) ne se produit. Si vous utilisez périodiquement la méthode **Idle**, le moteur de base de données Microsoft Access peut se consacrer au traitement des tâches en arrière-plan en supprimant les verrous en lecture inutiles.

Une fois spécifié, l'argument facultatif **dbRefreshCache** actualise la mémoire à partir uniquement des données de la base de données les plus récentes.

Vous n'avez pas besoin d'utiliser cette méthode dans les environnements mono-utilisateur à moins que plusieurs instances d'une même application soient exécutées. La méthode **Idle** est propre à accroître les performances dans un environnement mono-utilisateur dans la mesure où elle force le moteur de base de données à écrire les données sur disque, ce qui supprime les verrous au niveau de la mémoire.


> [!NOTE]
> [!REMARQUE] Vous pouvez également supprimer les verrous en lecture en intégrant les opérations à une transaction.

## <a name="example"></a>Exemple

Cet exemple de code montre comment utiliser la méthode **Idle** pour s'assurer qu'une procédure de sortie accède aux données les plus récentes à disposition dans la base de données. La procédure IdleOutput est nécessaire à l'exécution de cette procédure.

```vb 
Sub IdleX() 
 
 Dim dbsNorthwind As Database 
 Dim strCountry As String 
 Dim strSQL As String 
 Dim rstOrders As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Get name of country from user and build SQL statement 
 ' with it. 
 strCountry = Trim(InputBox("Enter country:")) 
 strSQL = "SELECT * FROM Orders WHERE ShipCountry = '" & _ 
 strCountry & "' ORDER BY OrderID" 
 
 ' Open Recordset object with SQL statement. 
 Set rstOrders = dbsNorthwind.OpenRecordset(strSQL) 
 
 ' Display contents of Recordset object. 
 IdleOutput rstOrders, strCountry 
 
 rstOrders.Close 
 dbsNorthwind.Close 
 
End Sub 
 
Sub IdleOutput(rstTemp As Recordset, strTemp As String) 
 
 ' Call the Idle method to release unneeded locks, force 
 ' pending writes, and refresh the memory with the current 
 ' data in the .mdb file. 
 DBEngine.Idle dbRefreshCache 
 
 ' Enumerate the Recordset object. 
 With rstTemp 
 Debug.Print "Orders from " & strTemp & ":" 
 Debug.Print , "OrderID", "CustomerID", "OrderDate" 
 Do While Not .EOF 
 Debug.Print , !OrderID, !CustomerID, !OrderDate 
 .MoveNext 
 Loop 
 End With 
 
End Sub 
 
```

