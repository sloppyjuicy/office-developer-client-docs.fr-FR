---
title: Visual Basic (référence de base de données de bureau Access)
TOCTitle: Visual Basic
ms:assetid: 9d153b6c-c860-7350-cb3c-b9bd08f75ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249714(v=office.15)
ms:contentKeyID: 48546616
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fe56644d4bfe307ac3b9e42af94e7566b2507c9d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593263"
---
# <a name="visual-basic"></a>Visual Basic


**S’applique à** : Access 2013, Office 2013

Pour gérer les événements ADO dans Microsoft Visual Basic, vous devez déclarer une variable au niveau du module à l'aide du mot-clé **WithEvents**. La variable ne peut être déclarée qu'au sein d'un module de classe et doit être déclarée au niveau du module. Ce n'est toutefois pas aussi restrictif qu'il n'y paraît car les objets **Form** Visual Basic sont également des classes. La manière la plus simple de gérer les événements ADO est de déclarer une variable avec **WithEvents**. L'exemple suivant gère l'événement **ConnectComplete** pour un objet **Connection**:

```vb 
 
' BeginEventExampleVB02 
Dim WithEvents connEvent As Connection 
Attribute connEvent.VB_VarHelpID = -1 
Dim strMsg As String 
 
Private Sub Form_Load() 
 On Error GoTo ErrHandler: 
 
 Dim strConn As String 
 
 ' Create a new object with event 
 ' handling enabled. 
 strConn = "Provider='sqloledb';" & _ 
 "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';" & _ 
 "Integrated Security='SSPI';" 
 Set connEvent = New ADODB.Connection 
 connEvent.Open strConn 
 
 Exit Sub 
 
ErrHandler: 
 MsgBox strMsg 
End Sub 
 
Private Sub connEvent_ConnectComplete(ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pConnection As ADODB.Connection) 
 
 If adStatus = adStatusErrorsOccurred Then 
 If Not pError Is Nothing Then 
 Select Case pError.Number 
 Case adErrOperationCancelled 
 ' The operation was cancelled in the 
 ' Will event. Notify the user and exit. 
 strMsg = "I'm sorry you can't connect right now." & vbCrLf 
 strMsg = strMsg & " Click OK to exit." 
 Unload Me 
 Case Else 
 strMsg = "Error " & Format(pError.Number) & vbCrLf 
 strMsg = strMsg & pError.Description 
 strMsg = strMsg & " Click OK to exit." 
 Unload Me 
 End Select 
 Else 
 strMsg = "Error occured. Click OK to exit." 
 Unload Me 
 End If 
 End If 
 'frmWait.btnOK.Enabled = True 
End Sub 
' EndEventExampleVB02 
```

L'objet **Connection** est déclaré au niveau **Form** avec le mot-clé **WithEvents** pour activer la gestion de l'événement. Le handler d’événements Form Load crée l’objet en attribuant un nouvel objet Connection à \_ *connEvent,* puis ouvre la connexion.  Bien entendu, une application réelle ferait plus de traitement dans le handler d’événements de chargement de formulaire \_ qu’elle n’en montre ici.

