---
title: Accès à des lignes dans un recordset hiérarchique
TOCTitle: Accessing rows in a hierarchical Recordset
ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15)
ms:contentKeyID: 48548104
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fd50934eeaf91149f59262a45e9585602ffb73e3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586312"
---
# <a name="accessing-rows-in-a-hierarchical-recordset"></a>Accès à des lignes dans un recordset hiérarchique

**S’applique à** : Access 2013, Office 2013

L’exemple suivant illustre les étapes nécessaires pour accéder aux lignes d’un objet [Recordset](recordset-object-ado.md) hiérarchique :

1. Les objets **Recordset** provenant des tables authors et titleauthor sont liés par l'ID d'auteur.

2. La boucle externe affiche le prénom et le nom de chaque auteur, ainsi que son état et son identification.

3. L'objet **Recordset** ajouté pour chaque ligne est extrait de la collection **Fields** et affecté à *rstTitleAuthor*.

4. La boucle interne affiche quatre champs de chaque ligne dans l'objet **Recordset** ajouté.

> [!NOTE] 
> La [propriété StayInSync](stayinsync-property-ado.md) est définie sur FALSE à des fins d’illustration, afin que vous pouvez voir le changement de chapitre explicitement dans chaque itération de la boucle externe. Toutefois, l’exemple sera plus efficace si l’affectation à l’étape 3 est déplacée avant la première ligne de l’étape 2, afin que l’affectation ne soit effectuée qu’une seule fois. Définissez **la propriété StayInSync** sur TRUE, afin que *rstTitleAuthor* passe implicitement et automatiquement au chapitre correspondant chaque fois que *rst* passe à une nouvelle ligne.

**Exemple**

```vb 
 
Sub datashape() 
 Dim cnn As New ADODB.Connection 
 Dim rst As New ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 
 cnn.Provider = "MSDataShape" 
 cnn.Open "Data Provider=MSDASQL;" & _ 
 "Data Source=SRV;" & _ 
 "User Id=MyUserName;Password=MyPassword;Database=Pubs" 
' STEP 1 
 rst.StayInSync = FALSE 
 rst.Open "SHAPE {select * from authors} " & _ 
 "APPEND ({select * from titleauthor} " & _ 
 "RELATE au_id TO au_id) AS chapTitleAuthor", _ 
 cnn 
' STEP 2 
 While Not rst.EOF 
 Debug.Print rst("au_fname"), rst("au_lname"), _ 
 rst("state"), rst("au_id") 
' STEP 3 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
' STEP 4 
 While Not rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0), rstTitleAuthor(1), _ 
 rstTitleAuthor(2), rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Wend 
 rst.MoveNext 
 Wend 
End Sub 
```

