---
title: Errors, collection (DAO)
TOCTitle: Errors Collection
ms:assetid: d42007b5-6410-14e9-baf9-9306fdef38f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834805(v=office.15)
ms:contentKeyID: 48547929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db6796d5777af12d1cd0a3e65647d7223f4423ba
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928921"
---
# <a name="errors-collection-dao"></a>Errors, collection (DAO)


**S’applique à**: Access 2013, Office 2013

Une collection **Errors** contient tous les objets **Error** stockés, chacun se rapportant à une opération unique impliquant DAO.

## <a name="remarks"></a>Remarques

Toute opération impliquant des objets DAO peut générer une ou plusieurs erreurs. À mesure que les erreurs surviennent, un ou plusieurs objets **Error** sont stockés dans la collection **Errors** de l'objet **DBEngine**. Lorsqu'une autre opération DAO génère une erreur, la collection **Errors** est effacée et le nouveau jeu d'objets **Error** est stocké dans la collection **Errors**. L'objet au numéro le plus élevé dans la collection **Errors **(DBEngine.Errors.Count - 1) correspond à l'erreur signalée par l'objet **Err** de Microsoft Visual Basic for Applications (VBA).

Les opérations DAO ne générant aucune erreur n'ont pas d'effets sur la collection **Errors**.

Les éléments de la collection **Errors** ne sont pas ajoutés comme ils le sont d'ordinaire avec les autres collections. Par conséquent, la collection **Errors** ne prend pas en charge les méthodes **Append** et **Delete**.

Le jeu d'objets **Error** de la collection **Errors** décrit une erreur. Le premier objet **Error** correspond à l'erreur de niveau le plus bas, le second au niveau immédiatement supérieur, etc. Par exemple, si une erreur ODBC survient lors de l'ouverture d'un objet **[Recordset](recordset-object-dao.md)**, le premier objet Error contient l'erreur ODBC de niveau le plus faible ; les erreurs suivantes contiennent les erreurs ODBC renvoyées par les différentes couches d'ODBC. Dans ce cas, le gestionnaire de pilote ODBC, voire le pilote lui-même, renvoient des objets **Error** séparés. Le dernier objet **Error** contient l'erreur DAO indiquant que l'objet n'a pas pu être ouvert.

L'énumération des différentes erreurs dans la collection **Errors** permet à vos routines de gestion des erreurs de déterminer de manière plus précise la cause et l'origine d'une erreur et de prendre les dispositions appropriées pour la résoudre.


> [!NOTE]
> [!REMARQUE] Si vous utilisez le mot clé **New** pour créer un objet à l'origine d'une erreur avant ou au moment d'être placé dans la collection **Errors**, cette dernière ne contient pas les informations d'erreur de cet objet, car le nouvel objet n'est pas associé à l'objet **DBEngine**. Toutefois, les informations d'erreur sont disponibles dans l'objet VBA **Err**.

## <a name="example"></a>Exemple

Cet exemple force une erreur, la capture et affiche les propriétés **Description**, **Number**, **Source**, **HelpContext** et **HelpFile** de l'objet **Error** qui en résulte.

```vb 
Sub DescriptionX() 
 
 Dim dbsTest As Database 
 
 On Error GoTo ErrorHandler 
 
 ' Intentionally trigger an error. 
 Set dbsTest = OpenDatabase("NoDatabase") 
 
 Exit Sub 
 
ErrorHandler: 
 Dim strError As String 
 Dim errLoop As Error 
 
 ' Enumerate Errors collection and display properties of 
 ' each Error object. 
 For Each errLoop In Errors 
 With errLoop 
 strError = _ 
 "Error #" & .Number & vbCr 
 strError = strError & _ 
 " " & .Description & vbCr 
 strError = strError & _ 
 " (Source: " & .Source & ")" & vbCr 
 strError = strError & _ 
 "Press F1 to see topic " & .HelpContext & vbCr 
 strError = strError & _ 
 " in the file " & .HelpFile & "." 
 End With 
 MsgBox strError 
 Next 
 
 Resume Next 
 
End Sub 
 
```

