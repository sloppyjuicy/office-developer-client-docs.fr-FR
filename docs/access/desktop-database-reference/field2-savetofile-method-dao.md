---
title: Méthode Field2.SaveToFile (DAO)
TOCTitle: SaveToFile Method
ms:assetid: 250f9596-1a03-471d-96f9-718cd57dc94f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191852(v=office.15)
ms:contentKeyID: 48543776
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101191
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c73aa8f4023ea5d3a192608fad88bf336e6e858f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924798"
---
# <a name="field2savetofile-method-dao"></a>Méthode Field2.SaveToFile (DAO)

**S’applique à**: Access 2013, Office 2013

Enregistre la pièce jointe sur le disque.

## <a name="version-information"></a>Informations de version

Version ajoutée : Access 2007

## <a name="syntax"></a>Syntaxe

*expression* . SaveToFile (***nom de fichier***)

*expression* Variable qui représente un objet **Field2** .

### <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Obligatoire/Facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>FileName</p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Chaîne</strong></p></td>
<td><p>Chemin d'accès complet du fichier à charger.</p></td>
</tr>
</tbody>
</table>


## <a name="example"></a>Exemple

L'extrait de code suivant montre comment utiliser la méthode **SaveToFile** pour enregistrer toutes les pièces jointes d'un employé sur le disque jointe.

```vb
    '  Instantiate the parent recordset.  
       Set rsEmployees = db.OpenRecordset("Employees") 
      
       … Code to move to desired employee 
      
       ' Instantiate the child recordset. 
       Set rsPictures = rsEmployees.Fields("Pictures").Value  
     
       '  Loop through the attachments. 
       While Not rsPictures.EOF 
      
          '  Save current attachment to disk in the "My Documents" folder. 
          rsPictures.Fields("FileData").SaveToFile _ 
                      "C:\Documents and Settings\Username\My Documents" 
          rsPictures.MoveNext 
       Wend 
```

<br/>

L’exemple suivant montre comment enregistrer les fichiers stockés dans un champ de pièce jointe sur le chemin d’accès du dossier spécifié.

**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Public Function SaveAttachments(strPath As String, Optional strPattern As String = "*.*") As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld As DAO.Field2
        Dim strFullPath As String
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Save all attachments in the field
            Do While Not rsA.EOF
                If rsA("FileName") Like strPattern Then
                    strFullPath = strPath & "\" & rsA("FileName")
                    
                    'Make sure the file does not exist and save
                    If Dir(strFullPath) = "" Then
                        rsA("FileData").SaveToFile strFullPath
                    End If
                    
                    'Increment the number of files saved
                    SaveAttachments = SaveAttachments + 1
                End If
                
                'Next attachment
                rsA.MoveNext
            Loop
            rsA.Close
            
            'Next record
            rst.MoveNext
        Loop
        
        rst.Close
        dbs.Close
        
        Set fld = Nothing
        Set rsA = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Function
```
