---
title: Erreurs ActiveX Data Objects (ADO)
TOCTitle: ADO errors
ms:assetid: 02fcf563-ce2d-9ef7-b8ae-2795f667335a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248796(v=office.15)
ms:contentKeyID: 48542972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e06c0fd79c59e12fe8f7fa3beac65bba37123d56
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944171"
---
# <a name="ado-errors"></a>Erreurs ADO

**S’applique à**: Access 2013, Office 2013

Les erreurs ADO sont signalées à votre programme comme des erreurs d'exécution. Vous pouvez utiliser le mécanisme de récupération des erreurs associé à votre langage de programmation pour les récupérer et les gérer. Par exemple, dans Visual Basic, utilisez l'instruction **On Error**. Dans Visual J++, utilisez un bloc **try/catch**. Dans Visual C++, cela dépend de la méthode que vous utilisez pour accéder aux bibliothèques ADO. Avec \#d’importation, utilisez un bloc **try-catch** . Dans les autres cas, les programmateurs C++ doivent extraire l'objet Error explicitement en appelant **GetErrorInfo**. La procédure Sub Visual Basic suivante illustre la récupération d'une erreur ADO :

```vb 
 
' BeginErrorHandlingVB01 
Private Sub Form_Load() 
 ' Turn on error handling 
 On Error GoTo FormLoadError 
 
 'Open the database and the recordset for processing. 
 ' 
 Dim strCnn As String 
 strCnn = "Provider='sqloledb';" & _ 
 "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
 
 ' cnn is a Public Connection Object because 
 ' it was defined WithEvents 
 Set cnn = New ADODB.Connection 
 cnn.Open strCnn 
 
 ' The next line of code intentionally causes 
 ' an error by trying to open a connection 
 ' that has already been opened. 
 cnn.Open strCnn 
 
 ' rst is a Public Recordset because it 
 ' was defined WithEvents 
 Set rst = New ADODB.Recordset 
 rst.Open "Customers", cnn 
 
 Exit Sub 
 
' Error handler 
FormLoadError: 
 Dim strErr As String 
 Select Case Err 
 Case adErrObjectOpen 
 strErr = "Error #" & Err.Number & ": " & Err.Description & vbCrLf 
 strErr = strErr & "Error reported by: " & Err.Source & vbCrLf 
 strErr = strErr & "Help File: " & Err.HelpFile & vbCrLf 
 strErr = strErr & "Topic ID: " & Err.HelpContext 
 MsgBox strErr 
 Debug.Print strErr 
 Err.Clear 
 Resume Next 
 ' If some other error occurs that 
 ' has nothing to do with ADO, show 
 ' the number and description and exit. 
 Case Else 
 strErr = "Error #" & Err.Number & ": " & Err.Description & vbCrLf 
 MsgBox strErr 
 Debug.Print strErr 
 Unload Me 
 End Select 
End Sub 
' EndErrorHandlingVB01 
```

Cela **formulaire\_charge** procédure événementielle crée intentionnellement une erreur lorsque vous essayez d’ouvrir le même objet **Connection** à deux reprises. Lors du deuxième appel de la méthode **Open**, le gestionnaire d'erreurs est activé. Dans ce cas, l'erreur est de type **adErrObjectOpen** et le gestionnaire d'erreurs affiche alors le message suivant avant de reprendre l'exécution du programme :

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

Le message d'erreur comprend toutes les informations fournies par l'objet **Err** Visual Basic, à l'exception de la valeur **LastDLLError**, non applicable dans ce cas-ci. Le numéro de l'erreur indique l'erreur qui s'est produite. Sa description est utile si vous ne souhaitez pas gérer l'erreur vous-même. Vous pouvez simplement la passer à l'utilisateur. Même si vous souhaitez utiliser dans la mesure du possible des messages personnalisés en fonction de votre application, vous ne pouvez pas anticiper toutes les erreurs ; leur description vous donnera des indices pour en déterminer la cause. Dans l'exemple de code, l'erreur a été signalée par l'objet **Connection**. Vous pouvez voir ici l'ID programmatique ou le type de l'objet  pas un nom de variable.


> [!NOTE]
> [!REMARQUE] L'objet Visual Basic **Err** contient uniquement des informations sur la dernière erreur. La collection ADO **Errors** de l'objet **Connection** contient un objet **Error** pour chaque erreur déclenchée par la dernière opération ADO. Utilisez la collection **Errors** plutôt que l'objet **Err** pour gérer plusieurs erreurs. Pour plus d'informations sur la collection **Errors**, consultez <A href="provider-errors.md">Erreurs de fournisseur</A>. Cependant, en l'absence d'un objet **Connection** valide, l'objet **Err** est la seule source d'informations sur les erreurs ADO.

Certaines opérations sont susceptibles d'entraîner des erreurs ADO. Parmi les erreurs ADO les plus courantes, citons l'ouverture d'un objet, tel que **Connection** ou **Recordset**, une tentative de mise à jour des données ou l'appel d'une méthode ou d'une propriété qui n'est pas prise en charge par votre fournisseur.

Les erreurs OLE DB peuvent également être passées à votre application en tant qu'erreurs d'exécution dans la collection **Errors**. Pour plus d'informations sur les numéros d'erreurs OLE DB, consultez le chapitre 16 du Guide de référence du programmeur OLE DB.

