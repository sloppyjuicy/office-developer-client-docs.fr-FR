---
title: Recordset2.LockEdits, propriété (DAO)
TOCTitle: LockEdits Property
ms:assetid: 77055f44-f8e9-ac64-ecc3-144ddb4a4558
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196045(v=office.15)
ms:contentKeyID: 48545716
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ff2db22dcb0119792eb57a971d3cf36e763d3049
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309645"
---
# <a name="recordset2lockedits-property-dao"></a><span data-ttu-id="56c35-102">Recordset2.LockEdits, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="56c35-102">Recordset2.LockEdits property (DAO)</span></span>

<span data-ttu-id="56c35-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56c35-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="56c35-104">Définit ou renvoie une valeur indiquant le type de verrouillage appliqué pendant l’opération de modification.</span><span class="sxs-lookup"><span data-stu-id="56c35-104">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="56c35-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56c35-105">Syntax</span></span>

<span data-ttu-id="56c35-106">*.* LockEdits</span><span class="sxs-lookup"><span data-stu-id="56c35-106">*expression* .LockEdits</span></span>

<span data-ttu-id="56c35-107">*expression* Variable qui représente un **objet Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="56c35-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="56c35-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="56c35-108">Remarks</span></span>

<span data-ttu-id="56c35-109">Le paramètre ou la valeur de retour indique le type de verrouillage, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="56c35-109">The setting or return value indicates the type of locking, as specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56c35-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="56c35-110">Value</span></span></p></th>
<th><p><span data-ttu-id="56c35-111">Description</span><span class="sxs-lookup"><span data-stu-id="56c35-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56c35-112">Vrai</span><span class="sxs-lookup"><span data-stu-id="56c35-112">True</span></span></p></td>
<td><p><span data-ttu-id="56c35-p101">Par défaut. Le verrouillage pessimiste est activé. La page contenant l’enregistrement que vous modifiez est verrouillée dès que vous invoquez la méthode Edit.</span><span class="sxs-lookup"><span data-stu-id="56c35-p101">Default. Pessimistic locking is in effect. The page containing the record you're editing is locked as soon as you call the Edit method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56c35-116">Faux</span><span class="sxs-lookup"><span data-stu-id="56c35-116">False</span></span></p></td>
<td><p><span data-ttu-id="56c35-117">Le verrouillage optimiste est activé pour la modification.</span><span class="sxs-lookup"><span data-stu-id="56c35-117">Optimistic locking is in effect for editing.</span></span> <span data-ttu-id="56c35-118">La page contenant l’enregistrement n’est pas verrouillée tant que la méthode Update n’est pas exécutée.</span><span class="sxs-lookup"><span data-stu-id="56c35-118">The page containing the record is not locked until the Update method is executed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="56c35-119">Vous pouvez utiliser la propriété **LockEdits** avec des objets **[Recordset](recordset-object-dao.md)** modifiables.</span><span class="sxs-lookup"><span data-stu-id="56c35-119">You can use the **LockEdits** property with updatable **[Recordset](recordset-object-dao.md)** objects.</span></span>

<span data-ttu-id="56c35-p103">Si une page est verrouillée, aucun autre utilisateur ne peut modifier des enregistrements sur la même page. Si vous affectez à **LockEdits** la valeur **True** et qu'un autre utilisateur a déjà verrouillé la page, une erreur se produit lorsque vous utilisez la méthode **Edit**. Les autres utilisateurs peuvent néanmoins toujours lire les données des pages verrouillées.</span><span class="sxs-lookup"><span data-stu-id="56c35-p103">If a page is locked, no other user can edit records on the same page. If you set **LockEdits** to **True** and another user already has the page locked, an error occurs when you use the **Edit** method. Other users can read data from locked pages.</span></span>

<span data-ttu-id="56c35-p104">Si vous affectez à la propriété **LockEdits** la valeur **False** et que vous utilisez par la suite la méthode **Update** alors qu'un autre utilisateur a verrouillé la page, une erreur est générée. Pour consulter les modifications apportées à votre enregistrement par un autre utilisateur, appelez la méthode **[Move](recordset2-move-method-dao.md)** avec un argument de valeur 0 ; toutefois, dans ce cas, sachez que vous perdrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="56c35-p104">If you set the **LockEdits** property to **False** and later use the **Update** method while another user has the page locked, an error occurs. To see the changes made to your record by another user, use the **[Move](recordset2-move-method-dao.md)** method with 0 as the argument; however, if you do this, you will lose your changes.</span></span>

<span data-ttu-id="56c35-p105">Lorsque vous utilisez des sources de données ODBC connectées au moteur de base de données Microsoft Access, la propriété **LockEdits** a toujours la valeur **False** (verrouillage optimiste). Le moteur de base de données Microsoft Access n'a aucun contrôle sur les mécanismes de verrouillage mis en œuvre sur des serveurs de base de données externes.</span><span class="sxs-lookup"><span data-stu-id="56c35-p105">When working with Microsoft Access database engine-connected ODBC data sources, the **LockEdits** property is always set to **False**, or optimistic locking. The Microsoft Access database engine has no control over the locking mechanisms used in external database servers.</span></span>

> [!NOTE]
> <span data-ttu-id="56c35-127">Vous pouvez prédéfiniter la valeur de  **LockEdits** lorsque vous ouvrez le jeu d’enregistrements pour la première fois en fixant l’argument lockedits de la **[méthode OpenRecordset.](connection-openrecordset-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="56c35-127">You can preset the value of **LockEdits** when you first open the **Recordset** by setting the lockedits argument of the **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span> <span data-ttu-id="56c35-128">Le fait de définir l’argument verrouillermodifications sur **dbPessimistic** définit la propriété **LockEdits** sur **True** et le fait de définir verrouillermodifications sur toute autre valeur définit la propriété **LockEdits** sur **False**.</span><span class="sxs-lookup"><span data-stu-id="56c35-128">Setting the lockedits argument to **dbPessimistic** will set the **LockEdits** property to **True**, and setting lockedits to any other value will set the **LockEdits** property to **False**.</span></span>

## <a name="example"></a><span data-ttu-id="56c35-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="56c35-129">Example</span></span>

<span data-ttu-id="56c35-p107">Cet exemple illustre dans un premier temps le verrouillage pessimiste en affectant à la propriété **LockEdits** la valeur **True** et ensuite le verrouillage optimiste en affectant la valeur False à **LockEdits**. Il montre également le type de gestion d'erreurs requis dans un environnement de base de données multiutilisateur afin de modifier un champ. Les fonctions PessimisticLock et OptimisticLock sont nécessaires à l'exécution de la procédure.</span><span class="sxs-lookup"><span data-stu-id="56c35-p107">This example demonstrates pessimistic locking by setting the **LockEdits** property to **True**, and then demonstrates optimistic locking by setting the **LockEdits** property to False. It also demonstrates what kind of error handling is required in a multiuser database environment in order to modify a field. The PessimisticLock and OptimisticLock functions are required for this procedure to run.</span></span>

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
