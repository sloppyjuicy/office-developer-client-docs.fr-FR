---
title: Propriété Recordset2.LockEdits (DAO)
TOCTitle: LockEdits Property
ms:assetid: 77055f44-f8e9-ac64-ecc3-144ddb4a4558
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196045(v=office.15)
ms:contentKeyID: 48545716
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f93924c579dc32e0841177eeb1068df64e12ab9b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931084"
---
# <a name="recordset2lockedits-property-dao"></a><span data-ttu-id="3b404-102">Propriété Recordset2.LockEdits (DAO)</span><span class="sxs-lookup"><span data-stu-id="3b404-102">Recordset2.LockEdits property (DAO)</span></span>


<span data-ttu-id="3b404-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b404-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b404-104">Définit ou renvoie une valeur indiquant le type de verrouillage utilisé lors de l'édition.</span><span class="sxs-lookup"><span data-stu-id="3b404-104">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b404-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b404-105">Syntax</span></span>

<span data-ttu-id="3b404-106">*expression* . LockEdits</span><span class="sxs-lookup"><span data-stu-id="3b404-106">*expression* .LockEdits</span></span>

<span data-ttu-id="3b404-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="3b404-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b404-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="3b404-108">Remarks</span></span>

<span data-ttu-id="3b404-109">Le paramètre ou la valeur de retour indique le type de verrouillage, comme spécifié dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3b404-109">The setting or return value indicates the type of locking, as specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b404-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b404-110">Value</span></span></p></th>
<th><p><span data-ttu-id="3b404-111">Description</span><span class="sxs-lookup"><span data-stu-id="3b404-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b404-112">True</span><span class="sxs-lookup"><span data-stu-id="3b404-112">True</span></span></p></td>
<td><p><span data-ttu-id="3b404-p101">Par défaut. Le verrouillage pessimiste est activé. La page contenant l’enregistrement que vous modifiez est verrouillée dès que vous invoquez la méthode Edit.</span><span class="sxs-lookup"><span data-stu-id="3b404-p101">Default. Pessimistic locking is in effect. The page containing the record you're editing is locked as soon as you call the Edit method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b404-116">False</span><span class="sxs-lookup"><span data-stu-id="3b404-116">False</span></span></p></td>
<td><p><span data-ttu-id="3b404-117">Verrouillage optimiste est activé pour modification.</span><span class="sxs-lookup"><span data-stu-id="3b404-117">Optimistic locking is in effect for editing.</span></span> <span data-ttu-id="3b404-118">La page contenant l’enregistrement n’est pas verrouillée jusqu'à ce que la méthode de mise à jour est exécutée.</span><span class="sxs-lookup"><span data-stu-id="3b404-118">The page containing the record is not locked until the Update method is executed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3b404-119">Vous pouvez utiliser la propriété **LockEdits** avec des objets **[Recordset](recordset-object-dao.md)** pouvant être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="3b404-119">You can use the **LockEdits** property with updatable **[Recordset](recordset-object-dao.md)** objects.</span></span>

<span data-ttu-id="3b404-p103">Si une page est verrouillée, aucun autre utilisateur ne peut modifier les enregistrements sur la même page. Si vous définissez **LockEdits** sur **True** et qu'un autre utilisateur a déjà verrouillé la page, une erreur survient lorsque vous utilisez la méthode **Edit**. Les autres utilisateurs peuvent lire les données des pages verrouillées.</span><span class="sxs-lookup"><span data-stu-id="3b404-p103">If a page is locked, no other user can edit records on the same page. If you set **LockEdits** to **True** and another user already has the page locked, an error occurs when you use the **Edit** method. Other users can read data from locked pages.</span></span>

<span data-ttu-id="3b404-p104">Si vous définissez la propriété **LockEdits** sur **False** et utilisez ensuite la méthode **Update** alors qu'un autre utilisateur a verrouillé la page, une erreur survient. Pour voir les modifications apportées à votre enregistrement par un autre utilisateur, utilisez la méthode **[Move](recordset2-move-method-dao.md)** avec 0 comme argument ; ce faisant, vous perdez toutefois vos modifications.</span><span class="sxs-lookup"><span data-stu-id="3b404-p104">If you set the **LockEdits** property to **False** and later use the **Update** method while another user has the page locked, an error occurs. To see the changes made to your record by another user, use the **[Move](recordset2-move-method-dao.md)** method with 0 as the argument; however, if you do this, you will lose your changes.</span></span>

<span data-ttu-id="3b404-p105">Lorsque vous utilisez des sources de données ODBC connectées à un moteur de base de données Microsoft Access, la propriété **LockEdits** est toujours définie sur **False** ou verrouillage optimiste. Le moteur de base de données Microsoft Access ne contrôle pas les mécanismes de verrouillage utilisés par les serveurs de base de données externes.</span><span class="sxs-lookup"><span data-stu-id="3b404-p105">When working with Microsoft Access database engine-connected ODBC data sources, the **LockEdits** property is always set to **False**, or optimistic locking. The Microsoft Access database engine has no control over the locking mechanisms used in external database servers.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3b404-127">Vous pouvez prédéfinir la valeur de <STRONG>LockEdits</STRONG> lorsque vous ouvrez pour la première fois le <STRONG>jeu d’enregistrements</STRONG> en définissant l’argument lockedits de la méthode <STRONG><A href="connection-openrecordset-method-dao.md">OpenRecordset</A></STRONG> .</span><span class="sxs-lookup"><span data-stu-id="3b404-127">You can preset the value of <STRONG>LockEdits</STRONG> when you first open the <STRONG>Recordset</STRONG> by setting the lockedits argument of the <STRONG><A href="connection-openrecordset-method-dao.md">OpenRecordset</A></STRONG> method.</span></span> <span data-ttu-id="3b404-128">Si l’argument lockedits <STRONG>dbPessimistic</STRONG> définit la propriété <STRONG>LockEdits</STRONG> sur <STRONG>True</STRONG>et lockedits paramètre pour toute autre valeur définit la propriété <STRONG>LockEdits</STRONG> sur <STRONG>False</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="3b404-128">Setting the lockedits argument to <STRONG>dbPessimistic</STRONG> will set the <STRONG>LockEdits</STRONG> property to <STRONG>True</STRONG>, and setting lockedits to any other value will set the <STRONG>LockEdits</STRONG> property to <STRONG>False</STRONG>.</span></span></P>



## <a name="example"></a><span data-ttu-id="3b404-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="3b404-129">Example</span></span>

<span data-ttu-id="3b404-p107">Cet exemple illustre le verrouillage pessimiste en définissant la propriété **LockEdits** sur **True**, puis le verrouillage optimiste en définissant la propriété **LockEdits** sur False. Il illustre également le type de gestion des erreurs requis dans un environnement de base de données multi-utilisateurs dans le cadre de la modification d'un champ. Les fonctions PessimisticLock et OptimisticLock sont indispensables pour l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="3b404-p107">This example demonstrates pessimistic locking by setting the **LockEdits** property to **True**, and then demonstrates optimistic locking by setting the **LockEdits** property to False. It also demonstrates what kind of error handling is required in a multiuser database environment in order to modify a field. The PessimisticLock and OptimisticLock functions are required for this procedure to run.</span></span>

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
