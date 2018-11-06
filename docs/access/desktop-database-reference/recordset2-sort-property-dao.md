---
title: Propriété Recordset2.Sort (DAO)
TOCTitle: Sort Property
ms:assetid: 523a8c29-46e2-564f-205d-03c214f277fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193917(v=office.15)
ms:contentKeyID: 48544842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 60d843773c00e7bd40e3e8e28997422fbda3c215
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998307"
---
# <a name="recordset2sort-property-dao"></a>Propriété Recordset2.Sort (DAO)

**S’applique à**: Access 2013, Office 2013 

Définit ou renvoie l'ordre de tri des enregistrements d'un objet **[Recordset](recordset-object-dao.md)** (espace de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . Tri

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Vous pouvez utiliser la propriété **Sort** avec feuille de réponse dynamique et instantané – objets **Recordset** de type.

Lorsque vous définissez cette propriété pour un objet, le tri est exécuté lorsqu'un autre objet **Recordset** est créé par la suite à partir de cet objet. Le paramètre de la propriété **Sort** remplace l'ordre de tri défini pour un objet **[QueryDef](querydef-object-dao.md)**.

Par défaut, l'ordre de tri est croissant (A à Z ou 0 à 100).

La propriété **Sort** ne s’applique aux objets **Recordset** de type table ou avant uniquement. Pour trier un objet **Recordset** de type table, utilisez la propriété **[Index](recordset2-index-property-dao.md)** .

> [!NOTE]
> [!REMARQUE] Dans la plupart des cas, il est plus rapide d'ouvrir un nouvel objet **Recordset** à l'aide d'une instruction SQL qui comprend les critères de tri.

## <a name="example"></a>Exemple

Cet exemple illustre la propriété **Sort** en modifiant sa valeur et en créant un nouvel objet **Recordset**. La fonction SortOutput est nécessaire à l'exécution de cette procédure.

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim rstSortEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     SortOutput "Original Recordset:", rstEmployees 
     .Sort = "LastName, FirstName" 
     ' Print report showing Sort property and record order. 
     SortOutput _ 
     "Recordset after changing Sort property:", _ 
     rstEmployees 
     ' Open new Recordset from current one. 
     Set rstSortEmployees = .OpenRecordset 
     ' Print report showing Sort property and record order. 
     SortOutput "New Recordset:", rstSortEmployees 
     rstSortEmployees.Close 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function SortOutput(strTemp As String, _ 
     rstTemp As Recordset) 
     
     With rstTemp 
     Debug.Print strTemp 
     Debug.Print " Sort = " & _ 
     IIf(.Sort <> "", .Sort, "[Empty]") 
     .MoveFirst 
     
     ' Enumerate Recordset. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & _ 
     ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Function 
```

<br/>

Lorsque vous savez quelles données sélectionner, il est généralement plus efficace de créer un objet **Recordset** avec une instruction SQL. Cet exemple montre comment créer un seul objet **Recordset** et obtenir les mêmes résultats que dans l'exemple précédent.

```vb
    Sub SortX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Open a Recordset from an SQL statement that specifies a 
     ' sort order. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("SELECT * " & _ 
     "FROM Employees ORDER BY LastName, FirstName", _ 
     dbOpenDynaset) 
     
     dbsNorthwind.Close 
     
    End Sub
```
