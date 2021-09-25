---
title: Recordset2.LockEdits, propriété (DAO)
TOCTitle: LockEdits Property
ms:assetid: 77055f44-f8e9-ac64-ecc3-144ddb4a4558
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196045(v=office.15)
ms:contentKeyID: 48545716
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4f55353eafb38f6d2ef2749da4788c3f288b2cd9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572801"
---
# <a name="recordset2lockedits-property-dao"></a>Recordset2.LockEdits, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur indiquant le type de verrouillage appliqué pendant l’opération de modification.

## <a name="syntax"></a>Syntaxe

*.* LockEdits

*expression* Variable qui représente un **objet Recordset2.**

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour indique le type de verrouillage, comme indiqué dans le tableau suivant.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Vrai</p></td>
<td><p>Par défaut. Le verrouillage pessimiste est activé. La page contenant l’enregistrement que vous modifiez est verrouillée dès que vous invoquez la méthode Edit.</p></td>
</tr>
<tr class="even">
<td><p>Faux</p></td>
<td><p>Le verrouillage optimiste est activé pour la modification. La page contenant l’enregistrement n’est pas verrouillée tant que la méthode Update n’est pas exécutée.</p></td>
</tr>
</tbody>
</table>


Vous pouvez utiliser la propriété **LockEdits** avec des objets **[Recordset](recordset-object-dao.md)** modifiables.

Si une page est verrouillée, aucun autre utilisateur ne peut modifier des enregistrements sur la même page. Si vous affectez à **LockEdits** la valeur **True** et qu'un autre utilisateur a déjà verrouillé la page, une erreur se produit lorsque vous utilisez la méthode **Edit**. Les autres utilisateurs peuvent néanmoins toujours lire les données des pages verrouillées.

Si vous affectez à la propriété **LockEdits** la valeur **False** et que vous utilisez par la suite la méthode **Update** alors qu'un autre utilisateur a verrouillé la page, une erreur est générée. Pour consulter les modifications apportées à votre enregistrement par un autre utilisateur, appelez la méthode **[Move](recordset2-move-method-dao.md)** avec un argument de valeur 0 ; toutefois, dans ce cas, sachez que vous perdrez vos modifications.

Lorsque vous utilisez des sources de données ODBC connectées au moteur de base de données Microsoft Access, la propriété **LockEdits** a toujours la valeur **False** (verrouillage optimiste). Le moteur de base de données Microsoft Access n'a aucun contrôle sur les mécanismes de verrouillage mis en œuvre sur des serveurs de base de données externes.

> [!NOTE]
> Vous pouvez prédéfiniter la valeur de  **LockEdits** lorsque vous ouvrez le jeu d’enregistrements pour la première fois en fixant l’argument lockedits de la **[méthode OpenRecordset.](connection-openrecordset-method-dao.md)** Le fait de définir l’argument verrouillermodifications sur **dbPessimistic** définit la propriété **LockEdits** sur **True** et le fait de définir verrouillermodifications sur toute autre valeur définit la propriété **LockEdits** sur **False**.

## <a name="example"></a>Exemple

Cet exemple illustre dans un premier temps le verrouillage pessimiste en affectant à la propriété **LockEdits** la valeur **True** et ensuite le verrouillage optimiste en affectant la valeur False à **LockEdits**. Il montre également le type de gestion d'erreurs requis dans un environnement de base de données multiutilisateur afin de modifier un champ. Les fonctions PessimisticLock et OptimisticLock sont nécessaires à l'exécution de la procédure.

```vb
    Sub LockEditsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCustomers As Recordset2 
     Dim strOldName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCustomers = _ 
     dbsNorthwind.OpenRecordset("Customers", _ 
     dbOpenDynaset) 
     
     With rstCustomers 
     ' Store original data. 
     strOldName = !CompanyName 
     
     If MsgBox("Pessimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with pessimistic locking 
     ' in effect. 
     If PessimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     If MsgBox("Optimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with optimistic locking 
     ' in effect. 
     If OptimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function PessimisticLock(rstTemp As Recordset2, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     PessimisticLock = True 
     
     With rstTemp 
     .LockEdits = True 
     
     ' When you set LockEdits to True, you trap for errors 
     ' when you call the Edit method. 
     On Error GoTo Err_Lock 
     .Edit 
     On Error GoTo 0 
     
     ' If the Edit is still in progress, then no errors 
     ' were triggered; you may modify the data. 
     If .EditMode = dbEditInProgress Then 
     fldTemp = strNew 
     .Update 
     .Bookmark = .LastModified 
     Else 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     PessimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function 
     
    Function OptimisticLock(rstTemp As Recordset, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     OptimisticLock = True 
     
     With rstTemp 
     .LockEdits = False 
     .Edit 
     fldTemp = strNew 
     
     ' When you set LockEdits to False, you trap for errors 
     ' when you call the Update method. 
     On Error GoTo Err_Lock 
     .Update 
     On Error GoTo 0 
     
     ' If there is no Edit in progress, then no errors were 
     ' triggered; you may modify the data. 
     If .EditMode = dbEditNone Then 
     ' Move current record pointer to the most recently 
     ' modified record. 
     .Bookmark = .LastModified 
     Else 
     .CancelUpdate 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     OptimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function
```
