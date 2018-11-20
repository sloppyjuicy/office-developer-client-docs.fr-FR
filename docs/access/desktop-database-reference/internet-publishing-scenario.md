---
title: Scénario de publication Internet
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f481c4bc5cf11f9345458b3859c099b40a79885
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026448"
---
# <a name="internet-publishing-scenario"></a><span data-ttu-id="87ee4-102">Scénario de publication Internet</span><span class="sxs-lookup"><span data-stu-id="87ee4-102">Internet publishing scenario</span></span>

<span data-ttu-id="87ee4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="87ee4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="87ee4-p101">Cet exemple de code illustre la façon dont ADO doit être utilisé avec le fournisseur Microsoft OLE DB pour la publication Internet. Ce scénario consiste à créer une application Visual Basic qui utilise des objets **Recordset**, **Record** et **Stream** pour afficher le contenu des ressources publiées à l'aide du fournisseur de la publication Internet.</span><span class="sxs-lookup"><span data-stu-id="87ee4-p101">This code example demonstrates how to use ADO with the Microsoft OLE DB Provider for Internet Publishing. In this scenario, you will create a Visual Basic application that uses **Recordset**, **Record**, and **Stream** objects to display the contents of resources published with the Internet Publishing Provider.</span></span>

<span data-ttu-id="87ee4-106">La création de ce scénario passe par l'exécution des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="87ee4-106">The following steps are necessary to create this scenario:</span></span> 

1. <span data-ttu-id="87ee4-107">Configurer le projet Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="87ee4-107">Set up the Visual Basic project.</span></span>
2. <span data-ttu-id="87ee4-108">Initialiser la zone de liste principale.</span><span class="sxs-lookup"><span data-stu-id="87ee4-108">Initialize the Main list box.</span></span>
3. <span data-ttu-id="87ee4-109">Remplir la zone de liste de champs.</span><span class="sxs-lookup"><span data-stu-id="87ee4-109">Populate the Fields list box.</span></span>
4. <span data-ttu-id="87ee4-110">Remplir la zone de texte Details.</span><span class="sxs-lookup"><span data-stu-id="87ee4-110">Populate the Details text box.</span></span>

## <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="87ee4-111">Étape 1 : Configurer le projet Visual Basic</span><span class="sxs-lookup"><span data-stu-id="87ee4-111">Step 1: Set up the Visual Basic project</span></span>

<span data-ttu-id="87ee4-112">Dans ce scénario, vous êtes censé avoir installé sur votre système Microsoft Visual Basic version 6.0 ou ultérieure, ADO version 2.5 ou ultérieure, et le fournisseur Microsoft OLE DB pour la publication Internet.</span><span class="sxs-lookup"><span data-stu-id="87ee4-112">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0 or later, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</span></span>

### <a name="create-an-ado-project"></a><span data-ttu-id="87ee4-113">Créer un projet ADO</span><span class="sxs-lookup"><span data-stu-id="87ee4-113">Create an ADO project</span></span>

1.  <span data-ttu-id="87ee4-114">Dans Microsoft Visual Basic, créez un nouveau projet EXE standard.</span><span class="sxs-lookup"><span data-stu-id="87ee4-114">In Microsoft Visual Basic, create a new Standard EXE project.</span></span>

2.  <span data-ttu-id="87ee4-115">Dans le menu **Projet**, choisissez **Références**.</span><span class="sxs-lookup"><span data-stu-id="87ee4-115">From the **Project** menu, choose **References**.</span></span>

3.  <span data-ttu-id="87ee4-116">Sélectionnez **Microsoft ActiveX Data Objects 2.5 Library**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="87ee4-116">Select **Microsoft ActiveX Data Objects 2.5 Library**, and then click **OK**.</span></span>

### <a name="insert-controls-on-the-main-form"></a><span data-ttu-id="87ee4-117">Insérer des contrôles dans le formulaire principal</span><span class="sxs-lookup"><span data-stu-id="87ee4-117">Insert controls on the main form</span></span>

1.  <span data-ttu-id="87ee4-118">Ajoutez un contrôle ListBox à Form1.</span><span class="sxs-lookup"><span data-stu-id="87ee4-118">Add a ListBox control to Form1.</span></span> <span data-ttu-id="87ee4-119">Sa propriété **Name** la valeur **lstMain**.</span><span class="sxs-lookup"><span data-stu-id="87ee4-119">Set its **Name** property to **lstMain**.</span></span>

2.  <span data-ttu-id="87ee4-120">Ajoutez un autre contrôle ListBox à Form1.</span><span class="sxs-lookup"><span data-stu-id="87ee4-120">Add another ListBox control to Form1.</span></span> <span data-ttu-id="87ee4-121">**Valeur lstDetails**, définissez sa propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="87ee4-121">Set its **Name** property to **lstDetails**.</span></span>

3.  <span data-ttu-id="87ee4-122">Ajoutez un contrôle TextBox à Form1.</span><span class="sxs-lookup"><span data-stu-id="87ee4-122">Add a TextBox control to Form1.</span></span> <span data-ttu-id="87ee4-123">Sa propriété **Name** la valeur **txtDetails**.</span><span class="sxs-lookup"><span data-stu-id="87ee4-123">Set its **Name** property to **txtDetails**.</span></span>

## <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="87ee4-124">Étape 2 : Initialiser la zone de liste principale</span><span class="sxs-lookup"><span data-stu-id="87ee4-124">Step 2: Initialize the Main list box</span></span>

### <a name="declare-global-record-and-recordset-objects"></a><span data-ttu-id="87ee4-125">Déclarer les objets Record et Recordset globaux</span><span class="sxs-lookup"><span data-stu-id="87ee4-125">Declare global Record and Recordset objects</span></span>

- <span data-ttu-id="87ee4-126">Insérez le code suivant dans (Général) (Déclarations) pour Form1 :</span><span class="sxs-lookup"><span data-stu-id="87ee4-126">Insert the following code into the (General) (Declarations) for Form1:</span></span>
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   <span data-ttu-id="87ee4-127">Ce code déclare des références pour les objets globaux **Record** et **Recordset** qui seront utilisés par la suite dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="87ee4-127">This code declares global object references for **Record** and **Recordset** objects that will be used later in this scenario.</span></span>

### <a name="connect-to-a-url-and-populate-lstmain"></a><span data-ttu-id="87ee4-128">Se connecter à une URL et remplir lstMain</span><span class="sxs-lookup"><span data-stu-id="87ee4-128">Connect to a URL and populate lstMain</span></span>

- <span data-ttu-id="87ee4-129">Insérez le code suivant dans le gestionnaire d'événements Form Load pour Form1 :</span><span class="sxs-lookup"><span data-stu-id="87ee4-129">Insert the following code into the Form Load event handler for Form1:</span></span>
    
   ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
   ```
    
   <span data-ttu-id="87ee4-130">Ce code instancie les objets **Record** et **Recordset** globaux.</span><span class="sxs-lookup"><span data-stu-id="87ee4-130">This code instantiates the global **Record** and **Recordset** objects.</span></span> <span data-ttu-id="87ee4-131">L' **enregistrement** `grec` est ouvert avec l’URL définie comme **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="87ee4-131">The **Record** `grec` is opened with a URL specified as the **ActiveConnection**.</span></span> <span data-ttu-id="87ee4-132">Si l'URL existe, elle est ouverte ; si elle n'existe pas encore, elle est créée.</span><span class="sxs-lookup"><span data-stu-id="87ee4-132">If the URL exists, it is opened; if it does not already exist, it is created.</span></span> 
   
   <span data-ttu-id="87ee4-133">Notez que vous devez remplacer `https://servername/foldername/` avec une URL valide de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="87ee4-133">Note that you should replace `https://servername/foldername/` with a valid URL from your environment.</span></span> 
   
   <span data-ttu-id="87ee4-134">Le **jeu d’enregistrements** `grs` est ouvert sur les enfants de l' **enregistrement** `grec`.</span><span class="sxs-lookup"><span data-stu-id="87ee4-134">The **Recordset** `grs` is opened on the children of the **Record** `grec`.</span></span> <span data-ttu-id="87ee4-135">La valeur lstMain est puis rempli avec les noms de fichier des ressources publiées à l’URL.</span><span class="sxs-lookup"><span data-stu-id="87ee4-135">The lstMain is then populated with the file names of the resources published to the URL.</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="87ee4-136">Étape 3 : Remplir la zone de liste de champs</span><span class="sxs-lookup"><span data-stu-id="87ee4-136">Step 3: Populate the Fields list box</span></span>

- <span data-ttu-id="87ee4-137">Insérez le code suivant dans le gestionnaire d'événements Click de lstMain :</span><span class="sxs-lookup"><span data-stu-id="87ee4-137">Insert the following code into the Click event handler of lstMain:</span></span>

   ```vb 
    
    Private Sub lstMain_Click() 
        Dim rec As Record 
        Dim rs As Recordset 
        Set rec = New Record 
        Set rs = New Recordset 
        grs.MoveFirst 
        grs.Move lstMain.ListIndex 
        lstDetails.Clear 
        rec.Open grs 
        Select Case rec.RecordType 
            Case adCollectionRecord: 
                Set rs = rec.GetChildren 
                While Not rs.EOF 
                    lstDetails.AddItem rs(0) 
                    rs.MoveNext 
                Wend 
            Case adSimpleRecord: 
                recFields rec, lstDetails, txtDetails 
                
            Case adStructDoc: 
        End Select 
        
    End Sub 
   ```

   <span data-ttu-id="87ee4-138">Ce code déclare et instancie les objets **Record** et **Recordset** locaux `rec` et `rs`respectivement.</span><span class="sxs-lookup"><span data-stu-id="87ee4-138">This code declares and instantiates local **Record** and **Recordset** objects `rec` and `rs`respectively.</span></span>

   <span data-ttu-id="87ee4-139">La ligne correspondant à la ressource sélectionnée dans lstMain devient la ligne en cours de `grs`.</span><span class="sxs-lookup"><span data-stu-id="87ee4-139">The row corresponding to the resource selected in lstMain is made the current row of `grs`.</span></span> <span data-ttu-id="87ee4-140">Zone de liste **Details** est ensuite effacée et `rec` est ouvert avec la ligne active de `grs` comme source.</span><span class="sxs-lookup"><span data-stu-id="87ee4-140">The **Details** list box is then cleared and `rec` is opened with the current row of `grs` as the source.</span></span>

   <span data-ttu-id="87ee4-141">Si la ressource est un enregistrement de collection (comme spécifié par **RecordType**), le **jeu d’enregistrements** de local `rs` est ouvert sur les enfants de `rec`.</span><span class="sxs-lookup"><span data-stu-id="87ee4-141">If the resource is a collection record (as specified by **RecordType**), the local **Recordset** `rs` is opened on the children of `rec`.</span></span> <span data-ttu-id="87ee4-142">lstDetails est ensuite rempli avec les valeurs des lignes de `rs`.</span><span class="sxs-lookup"><span data-stu-id="87ee4-142">lstDetails is then filled with the values from the rows of `rs`.</span></span>

   <span data-ttu-id="87ee4-143">Si la ressource est un enregistrement simple, `recFields` est appelée.</span><span class="sxs-lookup"><span data-stu-id="87ee4-143">If the resource is a simple record, `recFields` is called.</span></span> <span data-ttu-id="87ee4-144">Pour plus d’informations sur `recFields`, consultez l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="87ee4-144">For more information about `recFields`, see the next step.</span></span>

   <span data-ttu-id="87ee4-145">Si la ressource est un document structuré, aucun code n'est implémenté.</span><span class="sxs-lookup"><span data-stu-id="87ee4-145">No code is implemented if the resource is a structured document.</span></span>

## <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="87ee4-146">Étape 4 : Remplir la zone de texte Details</span><span class="sxs-lookup"><span data-stu-id="87ee4-146">Step 4: Populate the Details text box</span></span>

- <span data-ttu-id="87ee4-147">Créer une nouvelle sous-routine nommée `recFields` et insérez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="87ee4-147">Create a new subroutine named `recFields` and insert the following code:</span></span>

   ```vb 
    
    Sub recFields(r As Record, l As ListBox, t As TextBox) 
        Dim f As Field 
        Dim s As Stream 
        Set s = New Stream 
        Dim str As String 
        
        For Each f In r.Fields 
            l.AddItem f.Name & ": " & f.Value 
        Next 
        t.Text = "" 
        If r!RESOURCE_CONTENTCLASS = "text/plain" Then 
            s.Open r, adModeRead, adOpenStreamFromRecord 
            str = s.ReadText(1) 
            s.Position = 0 
            If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?" 
                s.Charset = "ascii" 
                s.Type = adTypeText 
            End If 
            t.Text = s.ReadText(adReadAll) 
        End If 
    End Sub 
   ```

   <span data-ttu-id="87ee4-148">Ce code remplit lstDetails avec les champs et les valeurs de l’enregistrement simple transmis à `recFields`.</span><span class="sxs-lookup"><span data-stu-id="87ee4-148">This code populates lstDetails with the fields and values of the simple record passed to `recFields`.</span></span> <span data-ttu-id="87ee4-149">Si la ressource est un fichier texte, un objet **Stream** de type texte est ouvert à partir de l'enregistrement de la ressource.</span><span class="sxs-lookup"><span data-stu-id="87ee4-149">If the resource is a text file, a text **Stream** is opened from the resource record.</span></span> <span data-ttu-id="87ee4-150">Le code détermine si le jeu de caractères est ASCII et copie le contenu du **flux** dans `txtDetails`.</span><span class="sxs-lookup"><span data-stu-id="87ee4-150">The code determines if the character set is ASCII, and copies the **Stream** contents into `txtDetails`.</span></span>

