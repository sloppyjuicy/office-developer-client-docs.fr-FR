---
title: Propriété Recordset2.NoMatch (DAO)
TOCTitle: NoMatch Property
ms:assetid: 2d7a02ff-a2bf-5f0e-bd71-a6d42c25b13a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192114(v=office.15)
ms:contentKeyID: 48543972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 083e76ea4e2a0800153d50fa0c61d5acb7a29645
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922180"
---
# <a name="recordset2nomatch-property-dao"></a>Propriété Recordset2.NoMatch (DAO)


**S’applique à**: Access 2013, Office 2013

Indique si un enregistrement donné a été localisé à l'aide de la méthode **[Seek](recordset2-seek-method-dao.md)** ou de l'une des méthodes **[Find](recordset2-findfirst-method-dao.md)** (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . NoMatch

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Lorsque vous ouvrez ou que vous créez un objet **[Recordset](recordset-object-dao.md)**, sa propriété **NoMatch** a la valeur **False**.

Pour rechercher un enregistrement, utilisez la méthode **Seek** sur un objet **Recordset** de type table ou l'une des méthodes **Find** sur un objet **Recordset** de type feuille de réponse dynamique ou instantané. Vérifiez le paramètre de la propriété **NoMatch** pour voir si l'enregistrement a pu être localisé.

Si la méthode **Seek** ou **Find** ne donne aucun résultat et que la propriété **NoMatch** a la valeur **True**, l'enregistrement actif ne sera plus valide. Veillez à obtenir le signet de l'enregistrement actif avant d'utiliser la méthode **Seek** ou l'une des méthodes **Find** si vous devez revenir à cet enregistrement.


> [!NOTE]
> <P>[!REMARQUE] L'appel de l'une des méthodes <STRONG><A href="recordset-movefirst-method-dao.md">Move</A></STRONG> sur un objet <STRONG>Recordset</STRONG> n'a aucune incidence sur le paramètre de la propriété <STRONG>NoMatch</STRONG>.</P>



## <a name="example"></a>Exemple

Cet exemple de code montre comment utiliser la propriété **NoMatch** pour déterminer si les opérations **Seek** et **FindFirst** ont abouti. Si ce n'est pas le cas, l'utilisateur en est informé de façon appropriée. Les procédures SeekMatch et FindMatch sont nécessaires à l'exécution de cette procédure.

```vb
    Sub NoMatchX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim rstCustomers As Recordset2 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim strCountry As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Default is dbOpenTable; required if Index property will 
     ' be used. 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     With rstProducts 
     .Index = "PrimaryKey" 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with Seek method" & vbCr & _ 
     "Product ID: " & !ProductID & vbCr & _ 
     "Product Name: " & !ProductName & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter a product ID." 
     strSeek = InputBox(strMessage) 
     If strSeek = "" Then Exit Do 
     
     ' Call procedure that seeks for a record based on 
     ' the ID number supplied by the user. 
     SeekMatch rstProducts, Val(strSeek) 
     Loop 
     
     .Close 
     End With 
     
     Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
     "SELECT CompanyName, Country FROM Customers " & _ 
     "ORDER BY CompanyName", dbOpenSnapshot) 
     
     With rstCustomers 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with FindFirst method" & _ 
     vbCr & "Customer Name: " & !CompanyName & _ 
     vbCr & "Country: " & !Country & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter country on which to search." 
     strCountry = Trim(InputBox(strMessage)) 
     If strCountry = "" Then Exit Do 
     
     ' Call procedure that finds a record based on 
     ' the country name supplied by the user. 
     FindMatch rstCustomers, _ 
     "Country = '" & strCountry & "'" 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset2, _ 
     intSeek As Integer) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .Seek "=", intSeek 
     
     ' If Seek method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
     strFind As String) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .FindFirst strFind 
     
     ' If Find method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub
```
