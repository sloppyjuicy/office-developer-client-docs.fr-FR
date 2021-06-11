---
title: 'Walkthrough: Create and debug a basic form template using the InfoPath object model'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- form templates [infopath 2007], walkthroughs,form templates [InfoPath 2007], creating InfoPath 2003-compatible,InfoPath 2003-compatible form templates, walkthroughs
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: Cette rubrique fournit une procédure pas à pas de création d’un modèle de formulaire InfoPath avec code géré de base qui fonctionne avec le modèle objet compatible InfoPath 2003 fourni par Microsoft. Office espace de noms.Interop.InfoPath.SemiTrust.
ms.openlocfilehash: c559aedad5c62134c796196c63c1a84f70c4dc3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414339"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a><span data-ttu-id="5af80-104">Walkthrough: Create and debug a basic form template using the InfoPath object model</span><span class="sxs-lookup"><span data-stu-id="5af80-104">Walkthrough: Create and debug a basic form template using the InfoPath object model</span></span>

<span data-ttu-id="5af80-105">Cette rubrique fournit une procédure pas à pas de création d’un modèle de formulaire InfoPath avec code géré de base qui fonctionne avec le modèle objet compatible InfoPath 2003 fourni par l’espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx)</span><span class="sxs-lookup"><span data-stu-id="5af80-105">This topic provides a walkthrough of creating a basic InfoPath managed code form template that works with the InfoPath 2003-compatible object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
## <a name="hello-world"></a><span data-ttu-id="5af80-106">Hello World</span><span class="sxs-lookup"><span data-stu-id="5af80-106">Hello World</span></span>

<span data-ttu-id="5af80-107">Dans l’exemple suivant, vous allez apprendre à afficher une boîte de dialogue d’alerte simple à l’aide de la méthode [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) du modèle objet compatible InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="5af80-107">In the following example, you will learn how to display a simple alert dialog box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the InfoPath 2003-compatible object model.</span></span> 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a><span data-ttu-id="5af80-108">Création d'un nouveau modèle de formulaire InfoPath qui fonctionne avec le modèle objet compatible InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="5af80-108">Create a new InfoPath form template that works with the InfoPath 2003-compatible object model</span></span>

1. <span data-ttu-id="5af80-109">Créez un modèle de formulaire qui fonctionne avec le modèle objet compatible InfoPath 2003, comme décrit dans Créer un modèle de formulaire à l’aide du modèle objet [InfoPath 2003.](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)</span><span class="sxs-lookup"><span data-stu-id="5af80-109">Create a new form template that works with the InfoPath 2003-compatible object model, as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).</span></span>
    
2. <span data-ttu-id="5af80-110">Appelez le projet de modèle de formulaire HelloWorld et enregistrez-le.</span><span class="sxs-lookup"><span data-stu-id="5af80-110">Name the form template project HelloWorld and save it.</span></span> 
    
   <span data-ttu-id="5af80-p101">Le système de projet crée les fichiers de code et de projet, puis ouvre un modèle de formulaire vierge dans InfoPath en mode Création. Vous pouvez alors ajouter des gestionnaires d'événements.</span><span class="sxs-lookup"><span data-stu-id="5af80-p101">The project system creates code and project files, and then opens a blank form template in InfoPath design mode. You are now ready to add event handlers.</span></span>
    
### <a name="add-a-button-with-an-onclick-event-handler"></a><span data-ttu-id="5af80-113">Ajout d'un bouton avec un gestionnaire d'événements OnClick</span><span class="sxs-lookup"><span data-stu-id="5af80-113">Add a button with an OnClick event handler</span></span>

1. <span data-ttu-id="5af80-114">Dans la section **Contrôles** de l'onglet **Accueil**, cliquez sur le contrôle **Bouton** pour l'insérer dans la vue.</span><span class="sxs-lookup"><span data-stu-id="5af80-114">In the **Controls** section on the **Home** tab, click the **Button** control to insert it into the view.</span></span> 
    
2. <span data-ttu-id="5af80-115">Cliquez avec le bouton droit sur le contrôle, puis cliquez sur **Propriétés du bouton**.</span><span class="sxs-lookup"><span data-stu-id="5af80-115">Right-click the control, and then click **Button Properties**.</span></span>
    
3. <span data-ttu-id="5af80-116">Modifiez **l’étiquette en** Alerte.</span><span class="sxs-lookup"><span data-stu-id="5af80-116">Change the **Label** to Alert.</span></span>
    
4. <span data-ttu-id="5af80-117">Modifiez **l’ID en** AlertID.</span><span class="sxs-lookup"><span data-stu-id="5af80-117">Change the **ID** to AlertID.</span></span>
    
5. <span data-ttu-id="5af80-118">Cliquez sur **Modifier le code du formulaire**.</span><span class="sxs-lookup"><span data-stu-id="5af80-118">Click **Edit Form Code**.</span></span>
    
   <span data-ttu-id="5af80-119">Un squelette de handler d’événements pour l’événement [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) est créé et le focus se déplace vers l’éditeur de code dans Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="5af80-119">An event handler skeleton for the [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) event is created and the focus moves to the code editor in Visual Studio 2012.</span></span> <span data-ttu-id="5af80-120">Pour plus d’informations sur l’utilisation des handlers d’événements, voir [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="5af80-120">For more information on working with event handlers, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span> 
    
   <span data-ttu-id="5af80-121">Vous pouvez maintenant ajouter du code de formulaire au gestionnaire d'événements du bouton.</span><span class="sxs-lookup"><span data-stu-id="5af80-121">You are now ready to add form code to the event handler for the button.</span></span>
    
### <a name="add-form-code-to-the-event-handler"></a><span data-ttu-id="5af80-122">Ajout de code de formulaire au gestionnaire d'événements</span><span class="sxs-lookup"><span data-stu-id="5af80-122">Add form code to the event handler</span></span>

1. <span data-ttu-id="5af80-123">Dans le gestionnaire d'événements **OnClick**, tapez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="5af80-123">In the **OnClick** event handler, type the following code:</span></span> 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="5af80-p103">Notez qu'une liste déroulante Microsoft IntelliSense s'affiche chaque fois que vous entrez un point dans la ligne de code. Le gestionnaire d'événements entier devrait ressembler à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="5af80-p103">Note that a Microsoft IntelliSense drop-down list is displayed after you type each period in the line of code. The entire event handler should look like the following:</span></span>
    
   ```cs
    [InfoPathEventHandler(MatchPath="AlertID", EventType=InfoPathEventType.OnClick)]
    public void AlertID_OnClick(DocActionEvent e)
    {
        thisXDocument.UI.Alert("Hello World!");
    }
   ```

   ```vb
    <InfoPathEventHandler(MatchPath:="AlertID", EventType:=InfoPathEventType.OnClick)>
    Public Sub AlertID_OnClick(ByVal e As DocActionEvent)
        thisXDocument.UI.Alert("Hello World!")
    End Sub
   ```

   > [!NOTE]
   > <span data-ttu-id="5af80-126">Au lieu d'employer la méthode **Alert**, vous pouvez utiliser la méthode **MessageBox.Show** de l'espace de noms **System.Windows.Forms** pour afficher un message.</span><span class="sxs-lookup"><span data-stu-id="5af80-126">As an alternative to using the **Alert** method, you can use the **MessageBox.Show** method of the **System.Windows.Forms** namespace to display a message box.</span></span> <span data-ttu-id="5af80-127">Pour ce faire, vous devez ajouter une référence au système. Windows. Assembly de formulaires, ajout ou ajout aux directives au début de votre fichier de code, puis tapez une ligne de code telle que `using System.Windows.Forms;` `Imports System.Windows.Forms` la suivante :`MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span><span class="sxs-lookup"><span data-stu-id="5af80-127">To do so, you must add a reference to the System.Windows.Forms assembly, add  `using System.Windows.Forms;` or  `Imports System.Windows.Forms` to the directives at the beginning of your code file, and then type a line of code such as the following:  `MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span></span>
  
2. <span data-ttu-id="5af80-128">Basculez dans la fenêtre du mode Création d'InfoPath, puis cliquez sur le bouton **Aperçu** sous l'onglet **Accueil**.</span><span class="sxs-lookup"><span data-stu-id="5af80-128">Switch to the InfoPath design mode window, and then click the **Preview** button on the **Home** tab.</span></span> 
    
3. <span data-ttu-id="5af80-129">Dans la fenêtre **Aperçu**, cliquez sur le bouton **Alerte**.</span><span class="sxs-lookup"><span data-stu-id="5af80-129">In the **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="5af80-130">Un message s'affiche avec le texte « Hello World! ».</span><span class="sxs-lookup"><span data-stu-id="5af80-130">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="5af80-131">La procédure suivante illustre l'ajout de points d'arrêt pour le débogage dans le code de votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="5af80-131">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="5af80-132">Débogage de code de formulaire</span><span class="sxs-lookup"><span data-stu-id="5af80-132">Debug form code</span></span>

1. <span data-ttu-id="5af80-133">Dans l'Éditeur de code, cliquez sur la barre grise à droite de la ligne :</span><span class="sxs-lookup"><span data-stu-id="5af80-133">In the code editor, click the grey bar to the left of the line:</span></span>
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="5af80-134">Un cercle rouge s'affiche et la ligne de code est mise en surbrillance pour indiquer que l'exécution s'interrompra sur ce point d'arrêt.</span><span class="sxs-lookup"><span data-stu-id="5af80-134">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
2. <span data-ttu-id="5af80-135">Dans le menu **Débogage**, cliquez sur **Démarrer le débogage** ou appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="5af80-135">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
3. <span data-ttu-id="5af80-136">Dans la fenêtre **Aperçu** d'InfoPath, cliquez sur le bouton **Alerte**.</span><span class="sxs-lookup"><span data-stu-id="5af80-136">In the InfoPath **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="5af80-137">Le focus bascule sur l'Éditeur de code et la ligne où se trouve le point d'arrêt est mise en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="5af80-137">The code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
4. <span data-ttu-id="5af80-138">Dans le menu **Débogage**, cliquez sur **Pas à pas principal** (ou appuyez sur Maj+F8 pour continuer pas à pas dans le code).</span><span class="sxs-lookup"><span data-stu-id="5af80-138">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
   <span data-ttu-id="5af80-p105">Le code de la méthode **Alert** s'exécute et l'alerte « Hello World! » s'affiche dans la fenêtre **Aperçu** d'InfoPath.</span><span class="sxs-lookup"><span data-stu-id="5af80-p105">The **Alert** method code is executed, and the "Hello World!" alert is displayed in the InfoPath **Preview** window.</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="5af80-141">Récupération du nom d'utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="5af80-141">Getting the Current User's Name</span></span>

<span data-ttu-id="5af80-p106">Avec les classes .NET Framework, vous pouvez accéder aux fonctionnalités qui n'étaient pas facilement disponibles depuis un script. Dans cet exemple, vous allez apprendre comment utiliser les classes .NET Framework pour récupérer le nom de l'utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="5af80-p106">By using the .NET Framework classes, you can get access to functionality that was not easily available in script. In this example, you will learn how use the .NET Framework classes to retrieve the name of the current user.</span></span>
  
### <a name="add-an-onload-event-handler"></a><span data-ttu-id="5af80-144">Ajout d'un gestionnaire d'événements OnLoad</span><span class="sxs-lookup"><span data-stu-id="5af80-144">Add an OnLoad event handler</span></span>

1. <span data-ttu-id="5af80-145">Ouvrez le projet HelloWorld InfoPath que vous avez créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="5af80-145">Open the InfoPath HelloWorld project that you created earlier.</span></span>
    
2. <span data-ttu-id="5af80-146">Sous l'onglet **Affichage**, cliquez sur **Afficher les champs**.</span><span class="sxs-lookup"><span data-stu-id="5af80-146">On the **View** tab, click **Show Fields**.</span></span>
    
3. <span data-ttu-id="5af80-147">Cliquez avec le bouton droit sur le nœud **mesChamps**, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="5af80-147">Right-click the **myFields** node, and then click **Add**.</span></span>
    
4. <span data-ttu-id="5af80-148">Dans **Nom**, tapez **employé**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="5af80-148">In **Name**, type **employee**, then click **OK**.</span></span>
    
5. <span data-ttu-id="5af80-149">Faites glisser le nœud **employé** dans la vue.</span><span class="sxs-lookup"><span data-stu-id="5af80-149">Drag the **employee** node into the view.</span></span> 
    
6. <span data-ttu-id="5af80-150">Sous l'onglet **Développeur**, cliquez sur **Événement Sur chargement (OnLoad)**.</span><span class="sxs-lookup"><span data-stu-id="5af80-150">On the **Developer** tab, click **On Load Event**.</span></span>
    
   <span data-ttu-id="5af80-151">Cela crée un handler d’événements pour [l’événement OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) et le focus se déplace vers l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="5af80-151">This will create an event handler for the [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) event, and focus moves to the code editor.</span></span> <span data-ttu-id="5af80-152">Le code de ce gestionnaire d'événements sera appelé à chaque chargement du formulaire.</span><span class="sxs-lookup"><span data-stu-id="5af80-152">The code in this event handler will be called each time the form is loaded.</span></span> <span data-ttu-id="5af80-153">La procédure suivante illustre l'ajout d'un code de formulaire qui récupère le nom de l'utilisateur et le place dans le gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="5af80-153">The next procedure shows how to add form code that retrieves the user's name to the event handler.</span></span> 
    
### <a name="add-form-code"></a><span data-ttu-id="5af80-154">Ajout de code de formulaire </span><span class="sxs-lookup"><span data-stu-id="5af80-154">Add form code</span></span>

1. <span data-ttu-id="5af80-155">Dans le gestionnaire d'événements **OnLoad**, tapez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="5af80-155">In the **OnLoad** event handler, type the following code:</span></span> 
    
   ```cs
    // Store an XML DOM node as a local variable.
    IXMLDOMNode nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    if(nodeEmployee != null)
    {
        if(nodeEmployee.text == "")
        {
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName;
        }
    }
   ```

   ```vb
    // Store an XML DOM node as a local variable.
    Dim nodeEmployee As IXMLDOMNode
    nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    If Not(nodeEmployee Is Nothing) Then
        If(nodeEmployee.text = "") Then
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName
        End If
    End If
   ```

2. <span data-ttu-id="5af80-156">Compilez et affichez un aperçu du formulaire.</span><span class="sxs-lookup"><span data-stu-id="5af80-156">Compile and preview the form.</span></span>
    
   <span data-ttu-id="5af80-157">La zone de texte employé doit maintenant contenir votre nom d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5af80-157">The employee text box should now be populated with your username.</span></span> 
    
<span data-ttu-id="5af80-158">Pour plus d’informations sur le déploiement d’un modèle de formulaire avec code géré, voir Déployer des modèles de [formulaire InfoPath avec code.](how-to-deploy-infopath-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="5af80-158">For information about how to deploy a managed code form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> <span data-ttu-id="5af80-159">Pour plus d’informations sur le modèle objet InfoPath et les tâches de programmation courantes dans les modèles de formulaires avec code géré qui fonctionnent avec le modèle objet compatible InfoPath 2003, voir Présentation du modèle objet [InfoPath 2003.](understanding-the-infopath-2003-object-model.md)</span><span class="sxs-lookup"><span data-stu-id="5af80-159">For information on the InfoPath object model and common programming tasks in managed code form templates that work with the InfoPath 2003-compatible object model, see [Understanding the InfoPath 2003 Object Model](understanding-the-infopath-2003-object-model.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5af80-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5af80-160">See also</span></span>

- [<span data-ttu-id="5af80-161">Code d'initialisation et de nettoyage à l'aide du modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="5af80-161">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [<span data-ttu-id="5af80-162">Modèles objet compatibles avec InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="5af80-162">InfoPath 2003 Compatible Object Models</span></span>](infopath-2003-compatible-object-models.md)
- [<span data-ttu-id="5af80-163">Ajouter un handler d’événements à l’aide du modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="5af80-163">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

