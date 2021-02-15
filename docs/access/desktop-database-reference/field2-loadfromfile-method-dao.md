---
title: Méthode Field2.LoadFromFile (DAO)
TOCTitle: LoadFromFile Method
ms:assetid: 8ffe4636-d4da-0579-f4b5-14f423647562
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197396(v=office.15)
ms:contentKeyID: 48546314
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101190
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: bdb1ba92c4a0f4fbee7204b2f4fee8a96c87cc1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292789"
---
# <a name="field2loadfromfile-method-dao"></a><span data-ttu-id="e8082-102">Méthode Field2.LoadFromFile (DAO)</span><span class="sxs-lookup"><span data-stu-id="e8082-102">Field2.LoadFromFile method (DAO)</span></span>

<span data-ttu-id="e8082-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8082-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8082-104">Charge le fichier de disque désigné.</span><span class="sxs-lookup"><span data-stu-id="e8082-104">Loads the specified file from disk.</span></span>

## <a name="version-information"></a><span data-ttu-id="e8082-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="e8082-105">Version information</span></span>

<span data-ttu-id="e8082-106">Version ajoutée : Access 2007</span><span class="sxs-lookup"><span data-stu-id="e8082-106">Version added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="e8082-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8082-107">Syntax</span></span>

<span data-ttu-id="e8082-108">*.* LoadFromFile(***FileName***)</span><span class="sxs-lookup"><span data-stu-id="e8082-108">*expression* .LoadFromFile(***FileName***)</span></span>

<span data-ttu-id="e8082-109">*expression* une variable qui représente une **champ2** objet.</span><span class="sxs-lookup"><span data-stu-id="e8082-109">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8082-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8082-110">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8082-111">Nom</span><span class="sxs-lookup"><span data-stu-id="e8082-111">Name</span></span></p></th>
<th><p><span data-ttu-id="e8082-112">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="e8082-112">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="e8082-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="e8082-113">Data type</span></span></p></th>
<th><p><span data-ttu-id="e8082-114">Description</span><span class="sxs-lookup"><span data-stu-id="e8082-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8082-115"><em>FileName</em></span><span class="sxs-lookup"><span data-stu-id="e8082-115"><em>FileName</em></span></span></p></td>
<td><p><span data-ttu-id="e8082-116">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e8082-116">Required</span></span></p></td>
<td><p><span data-ttu-id="e8082-117"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="e8082-117"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="e8082-118">Chemin d'accès complet du fichier à charger.</span><span class="sxs-lookup"><span data-stu-id="e8082-118">The fully qualified path of the file to that you want to load.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="e8082-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="e8082-119">Example</span></span>

<span data-ttu-id="e8082-120">L'extrait de code suivant utilise la méthode **LoadFromFile** pour charger la photo d'un employé à partir du disque.</span><span class="sxs-lookup"><span data-stu-id="e8082-120">The following code snippet uses the **LoadFromFile** method to load an employee's picture from disk.</span></span>

```vb 
   '  Instantiate the parent recordset.  
   Set rsEmployees = db.OpenRecordset("Employees") 
  
   … Code to move to desired employee 
  
   ' Activate edit mode. 
   rsEmployees.Edit 
  
   ' Instantiate the child recordset. 
   Set rsPictures = rsEmployees.Fields("Pictures").Value  
  
   ' Add a new attachment. 
   rsPictures.AddNew 
   rsPictures.Fields("FileData").LoadFromFile "EmpPhoto39392.jpg" 
   rsPictures.Update 
  
   ' Update the parent record 
   rsEmployees.Update 
```

<br/>

<span data-ttu-id="e8082-121">L’exemple suivant montre comment ajouter des fichiers à partir d’un chemin d’accès de dossier spécifié à un champ Pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="e8082-121">The following example shows how to add files from a specified folder path to an attachment field.</span></span>

<span data-ttu-id="e8082-122">**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="e8082-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Public Function LoadAttachments(strPath As String, Optional strPattern As String = "*.*") As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld  As DAO.Field2
        Dim strFile As String
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Load all attachments in the specified directory
            strFile = Dir(strPath & "\*.*")
            
            rst.Edit
            Do While Len(strFile) > 0
                'Add a new attachment that matches the pattern.
                'Pass "" to match all files.
                If strFile Like strPattern Then
                    rsA.AddNew
                    rsA("FileData").LoadFromFile strPath & "\" & strFile
                    rsA.Update
                    
                    'Increment the number of files added
                    LoadAttachments = LoadAttachments + 1
                End If
                strFile = Dir
            Loop
            rsA.Close
            
            rst.Update
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
