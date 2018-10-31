---
title: Erreurs d’ActiveX Data Objects (ADO)
TOCTitle: ADO Errors
ms:assetid: 02fcf563-ce2d-9ef7-b8ae-2795f667335a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248796(v=office.15)
ms:contentKeyID: 48542972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8b6b794daf7c03df26c186ac58b9a02ed4a7419
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861231"
---
# <a name="ado-errors"></a><span data-ttu-id="1c612-102">Erreurs ADO</span><span class="sxs-lookup"><span data-stu-id="1c612-102">ADO Errors</span></span>


<span data-ttu-id="1c612-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c612-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1c612-104">Les erreurs ADO sont signalées à votre programme comme des erreurs d'exécution.</span><span class="sxs-lookup"><span data-stu-id="1c612-104">ADO Errors are reported to your program as run-time errors.</span></span> <span data-ttu-id="1c612-105">Vous pouvez utiliser le mécanisme de récupération des erreurs associé à votre langage de programmation pour les récupérer et les gérer.</span><span class="sxs-lookup"><span data-stu-id="1c612-105">You can use the error-trapping mechanism of your programming language to trap and handle them.</span></span> <span data-ttu-id="1c612-106">Par exemple, dans Visual Basic, utilisez l'instruction **On Error**.</span><span class="sxs-lookup"><span data-stu-id="1c612-106">For example, in Visual Basic, use the **On Error** statement.</span></span> <span data-ttu-id="1c612-107">Dans Visual J++, utilisez un bloc **try/catch**.</span><span class="sxs-lookup"><span data-stu-id="1c612-107">In Visual J++, use a **try-catch** block.</span></span> <span data-ttu-id="1c612-108">Dans Visual C++, cela dépend de la méthode que vous utilisez pour accéder aux bibliothèques ADO.</span><span class="sxs-lookup"><span data-stu-id="1c612-108">In Visual C++, it depends on the method you are using to access the ADO libraries.</span></span> <span data-ttu-id="1c612-109">Avec \#d’importation, utilisez un bloc **try-catch** .</span><span class="sxs-lookup"><span data-stu-id="1c612-109">With \#import, use a **try-catch** block.</span></span> <span data-ttu-id="1c612-110">Dans les autres cas, les programmateurs C++ doivent extraire l'objet Error explicitement en appelant **GetErrorInfo**.</span><span class="sxs-lookup"><span data-stu-id="1c612-110">Otherwise, C++ programmers need to explicitly retrieve the error object by calling **GetErrorInfo**.</span></span> <span data-ttu-id="1c612-111">La procédure Sub Visual Basic suivante illustre la récupération d'une erreur ADO :</span><span class="sxs-lookup"><span data-stu-id="1c612-111">The following Visual Basic sub procedure demonstrates trapping an ADO error:</span></span>

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

<span data-ttu-id="1c612-112">Cela **formulaire\_charge** procédure événementielle crée intentionnellement une erreur lorsque vous essayez d’ouvrir le même objet **Connection** à deux reprises.</span><span class="sxs-lookup"><span data-stu-id="1c612-112">This **Form\_Load** event procedure intentionally creates an error by trying to open the same **Connection** object twice.</span></span> <span data-ttu-id="1c612-113">Lors du deuxième appel de la méthode **Open**, le gestionnaire d'erreurs est activé.</span><span class="sxs-lookup"><span data-stu-id="1c612-113">The second time the **Open** method is called, the error handler is activated.</span></span> <span data-ttu-id="1c612-114">Dans ce cas, l'erreur est de type **adErrObjectOpen** et le gestionnaire d'erreurs affiche alors le message suivant avant de reprendre l'exécution du programme :</span><span class="sxs-lookup"><span data-stu-id="1c612-114">In this case the error is of type **adErrObjectOpen**, so the error handler displays the following message before resuming program execution:</span></span>

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

<span data-ttu-id="1c612-p103">Le message d'erreur comprend toutes les informations fournies par l'objet **Err** Visual Basic, à l'exception de la valeur **LastDLLError**, non applicable dans ce cas-ci. Le numéro de l'erreur indique l'erreur qui s'est produite. Sa description est utile si vous ne souhaitez pas gérer l'erreur vous-même. Vous pouvez simplement la passer à l'utilisateur. Même si vous souhaitez utiliser dans la mesure du possible des messages personnalisés en fonction de votre application, vous ne pouvez pas anticiper toutes les erreurs ; leur description vous donnera des indices pour en déterminer la cause. Dans l'exemple de code, l'erreur a été signalée par l'objet **Connection**. Vous pouvez voir ici l'ID programmatique ou le type de l'objet  pas un nom de variable.</span><span class="sxs-lookup"><span data-stu-id="1c612-p103">The error message includes each piece of information provided by the Visual Basic **Err** object except for the **LastDLLError** value, which does not apply here. The error number tells you which error has occurred. The description is useful in cases in which you do not want to handle the error yourself. You can simply pass it along to the user. Although you will usually want to use messages customized for your application, you cannot anticipate every error; the description gives some clue as to what went wrong. In the sample code, the error was reported by the **Connection** object. You will see the object's type or programmatic ID here — not a variable name.</span></span>


> [!NOTE]
> <span data-ttu-id="1c612-p104">[!REMARQUE] L'objet Visual Basic **Err** contient uniquement des informations sur la dernière erreur. La collection ADO **Errors** de l'objet **Connection** contient un objet **Error** pour chaque erreur déclenchée par la dernière opération ADO. Utilisez la collection **Errors** plutôt que l'objet **Err** pour gérer plusieurs erreurs. Pour plus d'informations sur la collection **Errors**, consultez <A href="provider-errors.md">Erreurs de fournisseur</A>. Cependant, en l'absence d'un objet **Connection** valide, l'objet **Err** est la seule source d'informations sur les erreurs ADO.</span><span class="sxs-lookup"><span data-stu-id="1c612-p104">The Visual Basic **Err** object only contains information about the most recent error. The ADO **Errors** collection of the **Connection** object contains one **Error** object for each error raised by the most recent ADO operation. Use the **Errors** collection rather than the **Err** object to handle multiple errors. For more information about the **Errors** collection, see <A href="provider-errors.md">Provider Errors</A>. However, if there is no valid **Connection** object, the **Err** object is the only source for information about ADO errors.</span></span>

<span data-ttu-id="1c612-p105">Certaines opérations sont susceptibles d'entraîner des erreurs ADO. Parmi les erreurs ADO les plus courantes, citons l'ouverture d'un objet, tel que **Connection** ou **Recordset**, une tentative de mise à jour des données ou l'appel d'une méthode ou d'une propriété qui n'est pas prise en charge par votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1c612-p105">What kinds of operations are likely to cause ADO errors? Common ADO errors can involve opening an object such as a **Connection** or **Recordset**, attempting to update data, or calling a method or property that is not supported by your provider.</span></span>

<span data-ttu-id="1c612-p106">Les erreurs OLE DB peuvent également être passées à votre application en tant qu'erreurs d'exécution dans la collection **Errors**. Pour plus d'informations sur les numéros d'erreurs OLE DB, consultez le chapitre 16 du Guide de référence du programmeur OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1c612-p106">OLE DB errors can also be passed to your application as run-time errors in the **Errors** collection. For more information about OLE DB error numbers, see Chapter 16 of the OLE DB Programmer's Reference.</span></span>

