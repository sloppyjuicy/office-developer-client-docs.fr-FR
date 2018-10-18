---
<span data-ttu-id="f15e6-101"><<<<<<< Titre tête : accès aux lignes d’un TOCTitle de jeu d’enregistrements hiérarchique : accès aux lignes d’un jeu d’enregistrements hiérarchique de ms:assetid : db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl : https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID : ms.date 48548104 : 09/18 / mtps_version 2015 : v=office.15</span><span class="sxs-lookup"><span data-stu-id="f15e6-101"><<<<<<< HEAD title: Accessing Rows in a Hierarchical Recordset TOCTitle: Accessing Rows in a Hierarchical Recordset ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: 48548104 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="f15e6-102">Accès aux lignes d'un jeu d'enregistrements hiérarchique</span><span class="sxs-lookup"><span data-stu-id="f15e6-102">Accessing Rows in a Hierarchical Recordset</span></span>

<span data-ttu-id="f15e6-103">=== titre : accès aux lignes d’un Recordset TOCTitle hiérarchique : accès aux lignes d’un ms:assetid de jeu d’enregistrements hiérarchique : db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl : https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID : ms.date 48548104 : mtps_version 17/10/2018 : v = Office.15</span><span class="sxs-lookup"><span data-stu-id="f15e6-103">======= title: Accessing rows in a hierarchical Recordset TOCTitle: Accessing rows in a hierarchical Recordset ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: 48548104 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="f15e6-104">Accès aux lignes d’un jeu d’enregistrements hiérarchique</span><span class="sxs-lookup"><span data-stu-id="f15e6-104">Accessing rows in a hierarchical Recordset</span></span>
>>>>>>> <span data-ttu-id="f15e6-105">master</span><span class="sxs-lookup"><span data-stu-id="f15e6-105">master</span></span>

<span data-ttu-id="f15e6-106">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f15e6-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f15e6-107">L'exemple suivant illustre les étapes nécessaires pour accéder aux lignes d'un objet [Recordset](recordset-object-ado.md) hiérarchique :</span><span class="sxs-lookup"><span data-stu-id="f15e6-107">The following example shows the steps necessary to access rows in a hierarchical [Recordset](recordset-object-ado.md):</span></span>

<span data-ttu-id="f15e6-108"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="f15e6-108"><<<<<<< HEAD</span></span>
1.  <span data-ttu-id="f15e6-109">Les objets **Recordset** provenant des tables authors et titleauthor sont liés par l'ID d'auteur.</span><span class="sxs-lookup"><span data-stu-id="f15e6-109">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2.  <span data-ttu-id="f15e6-110">La boucle externe affiche le prénom et le nom de chaque auteur, ainsi que son état et son identification.</span><span class="sxs-lookup"><span data-stu-id="f15e6-110">The outer loop displays each author's first and last name, state, and identification.</span></span>

3.  <span data-ttu-id="f15e6-111">L'objet **Recordset** ajouté pour chaque ligne est extrait de la collection **Fields** et affecté à *rstTitleAuthor*.</span><span class="sxs-lookup"><span data-stu-id="f15e6-111">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4.  <span data-ttu-id="f15e6-112">La boucle interne affiche quatre champs de chaque ligne dans l'objet **Recordset** ajouté.</span><span class="sxs-lookup"><span data-stu-id="f15e6-112">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

<a name="the-stayinsyncstayinsync-property-adomd-property-is-set-to-false-for-purposes-of-illustration--so-you-can-see-the-chapter-change-explicitly-in-each-iteration-of-the-outer-loop-however-the-example-will-be-more-efficient-if-the-assignment-in-step-3-is-moved-before-the-first-line-in-step-2-so-that-the-assignment-is-performed-only-once-then-set-the-stayinsync-property-to-true-so-that-rsttitleauthor-will-implicitly-and-automatically-change-to-the-corresponding-chapter-whenever-rst-moves-to-a-new-row"></a><span data-ttu-id="f15e6-113">(La propriété [StayInSync](stayinsync-property-ado.md) a la valeur FALSE à des fins d’illustration, pour vous pouvez de voir le chapitre changer de manière explicite dans chaque itération de la boucle externe.</span><span class="sxs-lookup"><span data-stu-id="f15e6-113">(The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration — so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="f15e6-114">Toutefois, l’exemple sera plus efficace si l’affectation à l’étape 3 est placée avant la première ligne à l’étape 2, afin que l’affectation est effectuée qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="f15e6-114">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="f15e6-115">Puis définir la propriété **StayInSync** sur TRUE, afin que *rstTitleAuthor* implicitement et automatiquement devient le chapitre correspondant *effectuée* qu’une nouvelle ligne.)</span><span class="sxs-lookup"><span data-stu-id="f15e6-115">Then set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.)</span></span>
=======
1. <span data-ttu-id="f15e6-116">Les objets **Recordset** provenant des tables authors et titleauthor sont liés par l'ID d'auteur.</span><span class="sxs-lookup"><span data-stu-id="f15e6-116">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2. <span data-ttu-id="f15e6-117">La boucle externe affiche le prénom et le nom de chaque auteur, ainsi que son état et son identification.</span><span class="sxs-lookup"><span data-stu-id="f15e6-117">The outer loop displays each author's first and last name, state, and identification.</span></span>

3. <span data-ttu-id="f15e6-118">L'objet **Recordset** ajouté pour chaque ligne est extrait de la collection **Fields** et affecté à *rstTitleAuthor*.</span><span class="sxs-lookup"><span data-stu-id="f15e6-118">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4. <span data-ttu-id="f15e6-119">La boucle interne affiche quatre champs de chaque ligne dans l'objet **Recordset** ajouté.</span><span class="sxs-lookup"><span data-stu-id="f15e6-119">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

> [!NOTE] 
> <span data-ttu-id="f15e6-120">La propriété [StayInSync](stayinsync-property-ado.md) est définie sur FALSE à des fins d’illustration, vous pouvez voir le chapitre changer de manière explicite dans chaque itération de la boucle externe.</span><span class="sxs-lookup"><span data-stu-id="f15e6-120">The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration, so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="f15e6-121">Toutefois, l’exemple sera plus efficace si l’affectation à l’étape 3 est placée avant la première ligne à l’étape 2, afin que l’affectation est effectuée qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="f15e6-121">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="f15e6-122">Valeur TRUE, la propriété **StayInSync** afin que *rstTitleAuthor* implicitement et automatiquement devient le chapitre correspondant *effectuée* qu’une nouvelle ligne.</span><span class="sxs-lookup"><span data-stu-id="f15e6-122">Set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.</span></span>
>>>>>>> <span data-ttu-id="f15e6-123">master</span><span class="sxs-lookup"><span data-stu-id="f15e6-123">master</span></span>

<span data-ttu-id="f15e6-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f15e6-124">**Example**</span></span>

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

