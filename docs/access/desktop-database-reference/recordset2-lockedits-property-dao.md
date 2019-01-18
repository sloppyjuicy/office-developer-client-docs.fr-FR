---
title: Propriété Recordset2.LockEdits (DAO)
TOCTitle: LockEdits Property
ms:assetid: 77055f44-f8e9-ac64-ecc3-144ddb4a4558
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196045(v=office.15)
ms:contentKeyID: 48545716
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ff2db22dcb0119792eb57a971d3cf36e763d3049
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701122"
---
# <a name="recordset2lockedits-property-dao"></a>Propriété Recordset2.LockEdits (DAO)

**S’applique à**: Access 2013, Office 2013

Définit ou renvoie une valeur indiquant le type de verrouillage utilisé lors de l'édition.

## <a name="syntax"></a>Syntaxe

*expression* . LockEdits

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour indique le type de verrouillage, comme spécifié dans le tableau suivant.

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
<td><p>True</p></td>
<td><p>Par défaut. Le verrouillage pessimiste est activé. La page contenant l’enregistrement que vous modifiez est verrouillée dès que vous invoquez la méthode Edit.</p></td>
</tr>
<tr class="even">
<td><p>False</p></td>
<td><p>Verrouillage optimiste est activé pour modification. La page contenant l’enregistrement n’est pas verrouillée jusqu'à ce que la méthode de mise à jour est exécutée.</p></td>
</tr>
</tbody>
</table>


Vous pouvez utiliser la propriété **LockEdits** avec des objets **[Recordset](recordset-object-dao.md)** pouvant être mis à jour.

Si une page est verrouillée, aucun autre utilisateur ne peut modifier les enregistrements sur la même page. Si vous définissez **LockEdits** sur **True** et qu'un autre utilisateur a déjà verrouillé la page, une erreur survient lorsque vous utilisez la méthode **Edit**. Les autres utilisateurs peuvent lire les données des pages verrouillées.

Si vous définissez la propriété **LockEdits** sur **False** et utilisez ensuite la méthode **Update** alors qu'un autre utilisateur a verrouillé la page, une erreur survient. Pour voir les modifications apportées à votre enregistrement par un autre utilisateur, utilisez la méthode **[Move](recordset2-move-method-dao.md)** avec 0 comme argument ; ce faisant, vous perdez toutefois vos modifications.

Lorsque vous utilisez des sources de données ODBC connectées à un moteur de base de données Microsoft Access, la propriété **LockEdits** est toujours définie sur **False** ou verrouillage optimiste. Le moteur de base de données Microsoft Access ne contrôle pas les mécanismes de verrouillage utilisés par les serveurs de base de données externes.

> [!NOTE]
> Vous pouvez prédéfinir la valeur de **LockEdits** lorsque vous ouvrez pour la première fois le **jeu d’enregistrements** en définissant l’argument lockedits de la méthode **[OpenRecordset](connection-openrecordset-method-dao.md)** . Si l’argument lockedits **dbPessimistic** définit la propriété **LockEdits** sur **True**et lockedits paramètre pour toute autre valeur définit la propriété **LockEdits** sur **False**.

## <a name="example"></a>Exemple

Cet exemple illustre le verrouillage pessimiste en définissant la propriété **LockEdits** sur **True**, puis le verrouillage optimiste en définissant la propriété **LockEdits** sur False. Il illustre également le type de gestion des erreurs requis dans un environnement de base de données multi-utilisateurs dans le cadre de la modification d'un champ. Les fonctions PessimisticLock et OptimisticLock sont indispensables pour l'exécution de cette procédure.

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
