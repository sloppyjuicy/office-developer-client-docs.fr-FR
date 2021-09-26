---
title: Field2.IsComplex, propriété (DAO)
TOCTitle: IsComplex Property
ms:assetid: ffc90e6e-e3ee-4f9b-ca6b-615199300d45
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837318(v=office.15)
ms:contentKeyID: 48548970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2bfec22e23aef53abe3a175a7647c2a0acaf58bb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618167"
---
# <a name="field2iscomplex-property-dao"></a>Field2.IsComplex, propriété (DAO)

**S’applique à** : Access 2013, Office 2013 

Renvoie une valeur **Boolean** qui indique si le champ défini est un type de données à plusieurs valeurs. En lecture seule.

## <a name="version-information"></a>Informations de version

Version ajoutée : Access 2007

## <a name="syntax"></a>Syntaxe

*.* IsComplex

*expression* une variable qui représente une **champ2** objet.

## <a name="example"></a>Exemple

L’exemple suivant montre comment naviguer dans un Recordset contenant un champ à valeurs multiples.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub PrintStudentsAndClasses()
        Dim dbs As DAO.Database
        Dim rsStudents As DAO.Recordset2  'Recordset for students
        Dim rsClasses As DAO.Recordset2  'Recordset for classes
        Dim fld As DAO.Field2
    
        'open the database
        Set dbs = CurrentDb()
    
        'get the table of students
        Set rsStudents = dbs.OpenRecordset("tblStudents")
    
        'loop through the students
        Do While Not rsStudents.EOF
            
            'get the classes field
            Set fld = rsStudents("Classes")
    
            'get the classes Recordset
            'make sure the field is a multi-valued field before
            'getting a Recordset object
            If fld.IsComplex Then
                Set rsClasses = fld.Value
            End If
    
            'access all records in the Recordset
            If Not (rsClasses.BOF And rsClasses.EOF) Then
                rsClasses.MoveLast
                rsClasses.MoveFirst
            End If
    
            'print the student and number of classes
            Debug.Print rsStudents("FirstName") & " " & rsStudents("LastName"), _
                "Number of classes: " & rsClasses.RecordCount
    
            'print the classes for this student
            Do While Not rsClasses.EOF
                Debug.Print , rsClasses("Value")
                rsClasses.MoveNext
            Loop
    
            'close the Classes Recordset
            rsClasses.Close
    
            'get the next student
            rsStudents.MoveNext
    
        Loop
        
        'cleanup
        rsStudents.Close
    
        Set fld = Nothing
        Set rsStudents = Nothing
        Set dbs = Nothing
    
    End Sub
```
