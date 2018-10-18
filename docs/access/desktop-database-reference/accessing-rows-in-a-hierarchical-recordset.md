---
<<<<<<< Titre tête : accès aux lignes d’un TOCTitle de jeu d’enregistrements hiérarchique : accès aux lignes d’un jeu d’enregistrements hiérarchique de ms:assetid : db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl : https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID : ms.date 48548104 : 09/18 / mtps_version 2015 : v=office.15
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a>Accès aux lignes d'un jeu d'enregistrements hiérarchique

=== titre : accès aux lignes d’un Recordset TOCTitle hiérarchique : accès aux lignes d’un ms:assetid de jeu d’enregistrements hiérarchique : db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl : https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID : ms.date 48548104 : mtps_version 17/10/2018 : v = Office.15
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a>Accès aux lignes d’un jeu d’enregistrements hiérarchique
>>>>>>> master

**S’applique à**: Access 2013 | Office 2013

L'exemple suivant illustre les étapes nécessaires pour accéder aux lignes d'un objet [Recordset](recordset-object-ado.md) hiérarchique :

<<<<<<< Tête
1.  Les objets **Recordset** provenant des tables authors et titleauthor sont liés par l'ID d'auteur.

2.  La boucle externe affiche le prénom et le nom de chaque auteur, ainsi que son état et son identification.

3.  L'objet **Recordset** ajouté pour chaque ligne est extrait de la collection **Fields** et affecté à *rstTitleAuthor*.

4.  La boucle interne affiche quatre champs de chaque ligne dans l'objet **Recordset** ajouté.

<a name="the-stayinsyncstayinsync-property-adomd-property-is-set-to-false-for-purposes-of-illustration--so-you-can-see-the-chapter-change-explicitly-in-each-iteration-of-the-outer-loop-however-the-example-will-be-more-efficient-if-the-assignment-in-step-3-is-moved-before-the-first-line-in-step-2-so-that-the-assignment-is-performed-only-once-then-set-the-stayinsync-property-to-true-so-that-rsttitleauthor-will-implicitly-and-automatically-change-to-the-corresponding-chapter-whenever-rst-moves-to-a-new-row"></a>(La propriété [StayInSync](stayinsync-property-ado.md) a la valeur FALSE à des fins d’illustration, pour vous pouvez de voir le chapitre changer de manière explicite dans chaque itération de la boucle externe. Toutefois, l’exemple sera plus efficace si l’affectation à l’étape 3 est placée avant la première ligne à l’étape 2, afin que l’affectation est effectuée qu’une seule fois. Puis définir la propriété **StayInSync** sur TRUE, afin que *rstTitleAuthor* implicitement et automatiquement devient le chapitre correspondant *effectuée* qu’une nouvelle ligne.)
=======
1. Les objets **Recordset** provenant des tables authors et titleauthor sont liés par l'ID d'auteur.

2. La boucle externe affiche le prénom et le nom de chaque auteur, ainsi que son état et son identification.

3. L'objet **Recordset** ajouté pour chaque ligne est extrait de la collection **Fields** et affecté à *rstTitleAuthor*.

4. La boucle interne affiche quatre champs de chaque ligne dans l'objet **Recordset** ajouté.

> [!NOTE] 
> La propriété [StayInSync](stayinsync-property-ado.md) est définie sur FALSE à des fins d’illustration, vous pouvez voir le chapitre changer de manière explicite dans chaque itération de la boucle externe. Toutefois, l’exemple sera plus efficace si l’affectation à l’étape 3 est placée avant la première ligne à l’étape 2, afin que l’affectation est effectuée qu’une seule fois. Valeur TRUE, la propriété **StayInSync** afin que *rstTitleAuthor* implicitement et automatiquement devient le chapitre correspondant *effectuée* qu’une nouvelle ligne.
>>>>>>> master

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

