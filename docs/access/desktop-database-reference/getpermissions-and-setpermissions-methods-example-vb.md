---
title: GetPermissions et SetPermissions, méthodes – Exemple (VB)
TOCTitle: GetPermissions and SetPermissions methods example (VB)
ms:assetid: 930d9b58-2fc8-efa9-edfe-05ef9039a74d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249649(v=office.15)
ms:contentKeyID: 48546390
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: dc932107a05015b2eea8f493ef4f8bc77295ed7e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581160"
---
# <a name="getpermissions-and-setpermissions-methods-example-vb"></a>GetPermissions et SetPermissions, méthodes – Exemple (VB)


**S’applique à** : Access 2013, Office 2013

Cet exemple illustre les méthodes [GetPermissions](getpermissions-method-adox.md) et [SetPermissions](setpermissions-method-adox.md). Le code suivant octroie à l'utilisateur « Admin » l'accès complet à la table « Orders ».

```vb 
 
' BeginGrantPermissionsVB 
Sub GrantPermissions() 
 On Error GoTo GrantPermissionsError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim lngPerm As Long 
 
 ' Opens a connection to the northwind database 
 ' using the Microsoft Jet 4.0 provider 
 cnn.Provider = "Microsoft.Jet.OLEDB.4.0" 
 cnn.Open "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" & _ 
 "jet oledb:system database=" & _ 
 "'c:\Program Files\Microsoft Office\Office\system.mdw'" 
 
 Set cat.ActiveConnection = cnn 
 
 ' Retrieve original permissions 
 lngPerm = cat.Users("admin").GetPermissions("Orders", adPermObjTable) 
 Debug.Print "Original permissions: " & Str(lngPerm) 
 
 ' Revoke all permissions 
 cat.Users("admin").SetPermissions "Orders", adPermObjTable, _ 
 adAccessRevoke, adRightFull 
 
 ' Display permissions 
 Debug.Print "Revoked permissions: " & _ 
 Str(cat.Users("admin").GetPermissions("Orders", adPermObjTable)) 
 
 ' Give the Admin user full rights on the orders object 
 cat.Users("admin").SetPermissions "Orders", adPermObjTable, _ 
 adAccessSet, adRightFull 
 
 ' Display permissions 
 Debug.Print "Full permissions: " & _ 
 Str(cat.Users("admin").GetPermissions("Orders", adPermObjTable)) 
 
 ' Restore original permissions 
 cat.Users("admin").SetPermissions "Orders", adPermObjTable, _ 
 adAccessSet, lngPerm 
 
 ' Display permissions 
 Debug.Print "Final permissions: " & _ 
 Str(cat.Users("admin").GetPermissions("Orders", adPermObjTable)) 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
GrantPermissionsError: 
 
 Set cat = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndGrantPermissionsVB 
```

