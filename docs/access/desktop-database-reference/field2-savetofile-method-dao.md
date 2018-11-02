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
# <a name="field2savetofile-method-dao"></a><span data-ttu-id="7f4af-102">Méthode Field2.SaveToFile (DAO)</span><span class="sxs-lookup"><span data-stu-id="7f4af-102">Field2.SaveToFile method (DAO)</span></span>

<span data-ttu-id="7f4af-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f4af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f4af-104">Enregistre la pièce jointe sur le disque.</span><span class="sxs-lookup"><span data-stu-id="7f4af-104">Saves an attachment to disk.</span></span>

## <a name="version-information"></a><span data-ttu-id="7f4af-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="7f4af-105">Version Information</span></span>

<span data-ttu-id="7f4af-106">Version ajoutée : Access 2007</span><span class="sxs-lookup"><span data-stu-id="7f4af-106">Version Added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="7f4af-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f4af-107">Syntax</span></span>

<span data-ttu-id="7f4af-108">*expression* . SaveToFile (***nom de fichier***)</span><span class="sxs-lookup"><span data-stu-id="7f4af-108">*expression* .SaveToFile(***FileName***)</span></span>

<span data-ttu-id="7f4af-109">*expression* Variable qui représente un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="7f4af-109">*expression* A variable that represents a **Field2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="7f4af-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f4af-110">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f4af-111">Name</span><span class="sxs-lookup"><span data-stu-id="7f4af-111">Name</span></span></p></th>
<th><p><span data-ttu-id="7f4af-112">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="7f4af-112">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="7f4af-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="7f4af-113">Data Type</span></span></p></th>
<th><p><span data-ttu-id="7f4af-114">Description</span><span class="sxs-lookup"><span data-stu-id="7f4af-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f4af-115">FileName</span><span class="sxs-lookup"><span data-stu-id="7f4af-115">FileName</span></span></p></td>
<td><p><span data-ttu-id="7f4af-116">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7f4af-116">Required</span></span></p></td>
<td><p><span data-ttu-id="7f4af-117"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="7f4af-117"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7f4af-118">Chemin d'accès complet du fichier à charger.</span><span class="sxs-lookup"><span data-stu-id="7f4af-118">The fully qualified path of the file to which you want to save the attachment.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="7f4af-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="7f4af-119">Example</span></span>

<span data-ttu-id="7f4af-120">L'extrait de code suivant montre comment utiliser la méthode **SaveToFile** pour enregistrer toutes les pièces jointes d'un employé sur le disque jointe.</span><span class="sxs-lookup"><span data-stu-id="7f4af-120">The following code snippet illustrates how to use the **SaveToFile** method to save all of the attachments for a specific employee to disk.</span></span>

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

<span data-ttu-id="7f4af-121">L’exemple suivant montre comment enregistrer les fichiers stockés dans un champ de pièce jointe sur le chemin d’accès du dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="7f4af-121">The following example shows how to save the files stored in an attachment field to the specified folder path.</span></span>

<span data-ttu-id="7f4af-122">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="7f4af-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
