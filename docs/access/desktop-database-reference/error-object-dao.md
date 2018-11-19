---
title: Objet Error - accès aux données (DAO) des objets
TOCTitle: Error Object
ms:assetid: e2608bc9-bece-9b47-4562-7a2689601f75
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835711(v=office.15)
ms:contentKeyID: 48548289
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2c34f5c9041102ecdb1c3c789c0e7c1c5585b3a6
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026352"
---
# <a name="error-object-dao"></a>Error, objet (DAO)


**S’applique à**: Access 2013, Office 2013

L'objet **Error** contient des détails sur les erreurs d'accès aux données, chacune d'entre elle appartenant à une opération simple impliquant DAO.

## <a name="remarks"></a>Remarques

Toute opération impliquant DAO peut générer une ou plusieurs erreurs. Par exemple, un appel à un serveur ODBC peut entraîner une erreur au niveau du serveur de base de données, d'ODBC, et de DAO. Lorsque chacun de ces types d'erreur se produit, un objet **Error** est placé dans la collection **Errors** de l'objet **DBEngine**. Un événement simple peut alors entraîner l'apparition de plusieurs objets **Error** dans la collection **Errors**.

Lorsqu'une opération DAO suivante génère une erreur, la collection **Errors** est effacée, et un ou plusieurs nouveaux objets **Error** sont placés dans la collection **Errors**. Les opérations DAO qui ne génèrent pas d'erreur n'ont aucun effet sur la collection **Errors**.

L'ensemble d'objets **Error** dans la collection **Errors** décrit une erreur. Le premier objet **Error** correspond à l'erreur de niveau inférieur (erreur d'origine), le second objet correspond à l'erreur de niveau immédiatement supérieur, etc. Par exemple, si une erreur ODBC se produit lorsque vous tentez d'ouvrir un objet **[Recordset](recordset-object-dao.md)**, le premier objet **Error**, **Errors**(0), contient l'erreur ODBC de niveau inférieur. Les erreurs suivantes contiennent les erreurs ODBC renvoyées par les différentes couches d'ODBC. Dans ce cas, le gestionnaire de pilotes ODBC, et probablement le pilote proprement dit, renvoient des objets **Error** distincts. Le dernier objet **Error**, **Errors.Count-** 1, contient l'erreur DAO qui indique que l'objet n'a pas pu être ouvert.

L'énumération des erreurs spécifiques dans la collection **Errors** permet à vos programmes de traitement des erreurs de déterminer plus précisément la cause et l'origine d'une erreur, et entreprend la procédure appropriée pour effectuer la récupération. Vous pouvez lire les propriétés de l'objet **Error** afin d'obtenir des détails spécifiques sur chaque erreur, notamment :

  - La propriété **[Description](error-description-property-dao.md)**, qui contient le texte de l'alerte d'erreur qui va être affichée à l'écran si l'erreur n'est pas interceptée.

  - La propriété **[Number](error-number-property-dao.md)**, qui contient la valeur d'entier long de la constante d'erreur.

  - La propriété **[Source](error-source-property-dao.md)**, qui identifie l'objet qui a généré l'erreur. Cela s'avère particulièrement utile lorsque la collection **Errors** contient plusoeurs objets **Error** suite à une demande auprès d'une source de données ODBC.

  - Les propriétés **HelpFile** et **HelpContext**, qui indiquent respectivement le fichier d'aide et la rubrique d'aide Microsoft Windows appropriés (le cas échéant) pour l'erreur.
    

    > [!NOTE]
    > [!REMARQUE] Lors de la programmation dans Microsoft Visual Basic pour Applications (VBA), si vous utilisez le mot clé **New** pour créer un objet qui entraîne consécutivement une erreur avant que cet objet soit ajouté à une collection, la collection **Errors** de l'objet **DBEngine** ne contient pas d'entrée pour l'erreur de cet objet, car le nouvel objet est associé à l'objet **DBEngine**. Cependant, les informations d'erreur sont disponibles dans l'objet VBA **Err**. Le code de traitement des erreurs VBA doit examiner la collection **Errors** chaque fois que vous anticipez une erreur d'accès aux données. 
    > 
    > Si vous écrivez un gestionnaire d'erreur centralisé, testez l'objet VBA **Err** pour déterminer si les informations d'erreur dans la collection **Errors** sont valides. Si la propriété **Number** du dernier élément de la collection **Errors** (DBEngine.Errors.Count - 1) et la valeur de l’objet **Err** correspondent, vous pouvez ensuite utiliser une série d’instructions **Select Case** pour identifier les erreurs DAO ou erreurs qui se sont produites. Si elles ne correspondent pas, utilisez la méthode [Refresh](errors-refresh-method-dao.md) dans la collection **Errors**.



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
            "  " & .Description & vbCr 
         strError = strError & _ 
            "  (Source: " & .Source & ")" & vbCr 
         strError = strError & _ 
            "Press F1 to see topic " & .HelpContext & vbCr 
         strError = strError & _ 
            "  in the file " & .HelpFile & "." 
      End With 
      MsgBox strError 
   Next 
 
   Resume Next 
 
End Sub 
 
```

