---
title: 'Procédure pas à pas : Créer un modèle de formulaire de base avec du code'
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- '[infopath 2007] de modèles de formulaire, création de code managé, géré de modèles de formulaires [InfoPath 2007], création de code, de modèles [InfoPath 2007], procédures pas à pas, InfoPath 2007, procédures pas à pas'
localization_priority: Normal
ms.assetid: 0f55c8be-8641-476a-b0c8-c88adb2ac2b9
description: Dans Microsoft InfoPath, vous pouvez écrire une logique métier dans Visual Basic ou Visual C# en l’ouverture d’un modèle de formulaire dans le Concepteur InfoPath, puis en utilisant une des commandes de l’interface utilisateur pour ajouter un gestionnaire d’événements, afin d’ouvre l’environnement de développement Visual Studio 2012 pour écriture de votre code.
ms.openlocfilehash: 8c98d71c26f8e56c532b2a4467218c366072b2ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782483"
---
# <a name="walkthrough-create-a-basic-form-template-with-code"></a><span data-ttu-id="7984b-104">Procédure pas à pas : Créer un modèle de formulaire de base avec du code</span><span class="sxs-lookup"><span data-stu-id="7984b-104">Walkthrough: Create a basic form template with code</span></span>

<span data-ttu-id="7984b-105">Dans Microsoft InfoPath, vous pouvez écrire une logique métier dans Visual Basic ou Visual C# en l’ouverture d’un modèle de formulaire dans le Concepteur InfoPath, puis en utilisant une des commandes de l’interface utilisateur pour ajouter un gestionnaire d’événements, afin d’ouvre l’environnement de développement Visual Studio 2012 pour écriture de votre code.</span><span class="sxs-lookup"><span data-stu-id="7984b-105">In Microsoft InfoPath, you can write business logic in Visual Basic or C# by opening a form template in the InfoPath designer, and then using one of the user interface commands to add an event handler, which will open the Visual Studio 2012 development environment for writing your code.</span></span> <span data-ttu-id="7984b-106">Par défaut, les projets de modèle de formulaire créé à l’aide de Visual Studio 2012 travail par rapport au modèle objet de code managé fourni par l’espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7984b-106">By default, form template projects created using Visual Studio 2012 work against the managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
<span data-ttu-id="7984b-107">Cette procédure pas à pas vous montre tout d’abord comment créer une application Hello World simple à l’aide de c# ou Visual Basic dans l’environnement de développement Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="7984b-107">This walkthrough first shows you how to create a simple Hello World application using C# or Visual Basic in the Visual Studio 2012 development environment.</span></span> <span data-ttu-id="7984b-108">La procédure pas à pas se termine par un exemple de code qui montre comment utiliser la propriété [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) de la classe [d’utilisateurs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) pour récupérer le nom de l’utilisateur actuel et remplir un contrôle de **Zone de texte** avec cette valeur.</span><span class="sxs-lookup"><span data-stu-id="7984b-108">The walkthrough concludes with a code sample that shows you how to use the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to retrieve the current user's name and populate a **Text Box** control with that value.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="7984b-109">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="7984b-109">Prerequisites</span></span>

<span data-ttu-id="7984b-110">Pour pouvoir effectuer cette procédure à l’aide de l’environnement de développement Visual Studio 2012, vous aurez besoin :</span><span class="sxs-lookup"><span data-stu-id="7984b-110">In order to complete this walkthrough using the Visual Studio 2012 development environment, you will need:</span></span>
  
- <span data-ttu-id="7984b-111">Microsoft InfoPath avec Visual Studio 2012 est installé.</span><span class="sxs-lookup"><span data-stu-id="7984b-111">Microsoft InfoPath with Visual Studio 2012 installed.</span></span>
    
## <a name="hello-world-in-visual-studio-tools-for-applications"></a><span data-ttu-id="7984b-112">Créer l'application « Hello World » dans Visual Studio Tools for Applications</span><span class="sxs-lookup"><span data-stu-id="7984b-112">Hello World in Visual Studio Tools for Applications</span></span>

<span data-ttu-id="7984b-113">Dans la procédure suivante, vous allez découvrir comment écrire du code dans l’environnement de développement Visual Studio 2012 pour afficher une boîte de dialogue d’alerte simple en écrivant un gestionnaire d’événements pour l’événement [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) de la classe [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) , qui est associée avec le contrôle **bouton** .</span><span class="sxs-lookup"><span data-stu-id="7984b-113">In the following walkthrough, you will learn how to write code in the Visual Studio 2012 development environment to display a simple alert dialog box by writing an event handler for the [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) event of the [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) class, which is associated with the **Button** control.</span></span> 
  
### <a name="create-a-new-project-and-specify-the-programming-language"></a><span data-ttu-id="7984b-114">Créer un projet et spécifier le langage de programmation</span><span class="sxs-lookup"><span data-stu-id="7984b-114">Create a new project and specify the programming language</span></span>

1. <span data-ttu-id="7984b-115">Démarrez le Concepteur InfoPath, puis double-cliquez sur le modèle de formulaire **vide (éditeur InfoPath)** .</span><span class="sxs-lookup"><span data-stu-id="7984b-115">Start the InfoPath designer, and then double-click the **Blank (InfoPath Editor)** form template.</span></span> 
    
2. <span data-ttu-id="7984b-116">Pour spécifier le langage de programmation à utiliser, cliquez sur le **Bouton Office**et cliquez sur **Options de formulaire**, cliquez sur la **programmation** dans la liste **catégorie** , puis sélectionnez **Visual Basic** ou **Visual C#** dans le modèle de formulaire ** code de langue** liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="7984b-116">To specify which programming language to use, click the **Office Button**, click **Form Options**, click **Programming** in the **Category** list, and then select either **Visual Basic** or **C#** from the **Form template code language** drop-down list.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="7984b-117">Les autres options linguistiques programmation dans la liste déroulante **langue du modèle de formulaire code** assurent la compatibilité avec les versions précédentes d’InfoPath.</span><span class="sxs-lookup"><span data-stu-id="7984b-117">The other programming language options in the **Form template code language** drop-down list provide compatibility with previous versions of InfoPath.</span></span> <span data-ttu-id="7984b-118">Les options **(InfoPath 2007 Compatible) c#** et **Visual Basic (InfoPath 2007 Compatible)** fonctionne avec les procédures décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="7984b-118">The **C# (InfoPath 2007 Compatible)** and **Visual Basic (InfoPath 2007 Compatible)** options will work with the procedures in this topic.</span></span> <span data-ttu-id="7984b-119">Toutefois, pour utiliser les options **c# (compatible avec InfoPath 2003)** et **Visual Basic (compatible avec InfoPath 2003)** , voir [procédure pas à pas : création et débogage d’une base formulaire modèle à l’aide du modèle objet InfoPath 2003](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="7984b-119">However, to use the **C# (InfoPath 2003 Compatible)** and **Visual Basic (InfoPath 2003 Compatible)** options, see [Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md).</span></span> 
  
    <span data-ttu-id="7984b-120">Vous êtes maintenant prêt à ajouter un contrôle **bouton** et créer son gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="7984b-120">You are now ready to add a **Button** control and create its event handler.</span></span> 
    
### <a name="add-a-button-control-and-event-handler"></a><span data-ttu-id="7984b-121">Ajouter un contrôle Bouton et un gestionnaire d'événements</span><span class="sxs-lookup"><span data-stu-id="7984b-121">Add a Button control and event handler</span></span>

1. <span data-ttu-id="7984b-122">Dans le groupe **contrôles** , cliquez sur le contrôle **bouton** pour ajouter au formulaire.</span><span class="sxs-lookup"><span data-stu-id="7984b-122">In the **Controls** group, click the **Button** control to add it the form.</span></span> 
    
2. <span data-ttu-id="7984b-123">Double-cliquez sur le contrôle **bouton** , tapez Hello pour la propriété **Label** sous l’onglet **Propriétés** du ruban, puis cliquez sur **Code personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="7984b-123">Double-click the **Button** control, type Hello for the **Label** property on the **Properties** tab of the ribbon, and then click **Custom Code**.</span></span> <span data-ttu-id="7984b-124">Lorsque vous y êtes invité, enregistrez le formulaire et nommez-le HelloWorld.</span><span class="sxs-lookup"><span data-stu-id="7984b-124">When prompted, save the form and name it HelloWorld.</span></span>
    
   <span data-ttu-id="7984b-125">L’environnement **Visual Studio Tools for Applications** s’ouvre avec le curseur dans le gestionnaire pour l’événement [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) du **bouton** contrôle d’événements.</span><span class="sxs-lookup"><span data-stu-id="7984b-125">This will open the **Visual Studio Tools for Applications** environment with the cursor in the event handler for the [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) event of **Button** control.</span></span> 
    
   <span data-ttu-id="7984b-126">Vous pouvez maintenant ajouter du code de formulaire au gestionnaire d'événements du bouton. </span><span class="sxs-lookup"><span data-stu-id="7984b-126">You are now ready to add form code to the event handler for the button.</span></span> 
    
### <a name="add-hello-world-code-to-the-event-handler-and-preview-the-form"></a><span data-ttu-id="7984b-127">Ajouter le code « Hello World » au gestionnaire d'événements et afficher un aperçu du formulaire</span><span class="sxs-lookup"><span data-stu-id="7984b-127">Add "Hello World" code to the event handler and preview the form</span></span>

1. <span data-ttu-id="7984b-128">Dans le squelette du gestionnaire d'événements, tapez :</span><span class="sxs-lookup"><span data-stu-id="7984b-128">In the event handler skeleton, type:</span></span>
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   <span data-ttu-id="7984b-129">Le code de votre modèle de formulaire doit se présenter ainsi :</span><span class="sxs-lookup"><span data-stu-id="7984b-129">The code for your form template should look similar to the following:</span></span>
    
   ```cs
    using Microsoft.Office.InfoPath;
    using System;
    using System.Windows.Forms;
    using System.Xml;
    using System.Xml.XPath;
    namespace HelloWorld
    {
        public partial class FormCode
        {
            public void InternalStartup()
            {
            ((ButtonEvent)EventManager.ControlEvents["CTRL1_5"]).Clicked += new ClickedEventHandler(CTRL1_5_Clicked);
            }
            public void CTRL1_5_Clicked(object sender, ClickedEventArgs e)
            {
            MessageBox.Show("Hello World!");
            }
        }
    }
   ```

   ```vb
    Imports Microsoft.Office.InfoPath
    Imports System
    Imports System.Windows.Forms
    Imports System.Xml
    Imports System.Xml.XPath
    Namespace HelloWorld
        Public Class FormCode
            Private Sub InternalStartup(ByVal sender As Object, ByVal e As EventArgs) Handles Me.Startup
            AddHandler DirectCast(EventManager.ControlEvents("CTRL1_5"), ButtonEvent).Clicked, AddressOf CTRL1_5_Clicked
            End Sub
            Public Sub CTRL1_5_Clicked(ByVal sender As Object, ByVal e As ClickedEventArgs)
            MessageBox.Show("Hello World!")
            End Sub
        End Class
    End Namespace
   ```

2. <span data-ttu-id="7984b-130">Basculez dans la fenêtre Concepteur InfoPath.</span><span class="sxs-lookup"><span data-stu-id="7984b-130">Switch to the InfoPath designer window.</span></span>
    
3. <span data-ttu-id="7984b-131">Cliquez sur le bouton **Aperçu** sous l’onglet **accueil** .</span><span class="sxs-lookup"><span data-stu-id="7984b-131">Click the **Preview** button on the **Home** tab.</span></span> 
    
4. <span data-ttu-id="7984b-132">Cliquez sur le bouton Hello du formulaire.</span><span class="sxs-lookup"><span data-stu-id="7984b-132">Click the Hello button on the form.</span></span> 
    
   <span data-ttu-id="7984b-133">Un message s'affiche avec le texte « Hello World! ».</span><span class="sxs-lookup"><span data-stu-id="7984b-133">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="7984b-134">La procédure suivante illustre l'ajout de points d'arrêt pour le débogage dans le code de votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="7984b-134">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="7984b-135">Débogage de code de formulaire</span><span class="sxs-lookup"><span data-stu-id="7984b-135">Debug form code</span></span>

1. <span data-ttu-id="7984b-136">Revenez à la fenêtre de Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="7984b-136">Switch back to the Visual Studio 2012 window.</span></span>
    
2. <span data-ttu-id="7984b-137">Cliquez sur la barre grise située à gauche de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7984b-137">Click the grey bar to the left of the line:</span></span>
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   <span data-ttu-id="7984b-138">Un cercle rouge s'affiche et la ligne de code est mise en surbrillance pour indiquer que l'exécution marquera une pause à ce point d'arrêt dans votre code de formulaire.</span><span class="sxs-lookup"><span data-stu-id="7984b-138">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
3. <span data-ttu-id="7984b-139">Dans le menu **Débogage**, cliquez sur **Démarrer le débogage** ou appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="7984b-139">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
4. <span data-ttu-id="7984b-140">Dans la fenêtre **Aperçu** d’InfoPath, cliquez sur le bouton Hello du formulaire.</span><span class="sxs-lookup"><span data-stu-id="7984b-140">In the InfoPath **Preview** window, click the Hello button on the form.</span></span> 
    
5. <span data-ttu-id="7984b-141">L’éditeur de code Visual Studio 2012 reçoit le focus, et la ligne du point d’arrêt est mise en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="7984b-141">The Visual Studio 2012 code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
6. <span data-ttu-id="7984b-142">Dans le menu **Débogage**, cliquez sur **Pas à pas principal** (ou appuyez sur Maj+F8 pour continuer pas à pas dans le code).</span><span class="sxs-lookup"><span data-stu-id="7984b-142">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
7. <span data-ttu-id="7984b-p105">Le gestionnaire d'événements est exécuté, et le message « Hello World! » s'affiche. </span><span class="sxs-lookup"><span data-stu-id="7984b-p105">The event handler code is executed, and the "Hello World!" message is displayed.</span></span> 
    
8. <span data-ttu-id="7984b-145">Cliquez sur **OK** pour revenir à l’éditeur de code Visual Studio 2012, puis cliquez sur **Arrêter le débogage** dans le menu **débogage** (ou appuyez sur Ctrl + Alt + Attn).</span><span class="sxs-lookup"><span data-stu-id="7984b-145">Click **OK** to return to the Visual Studio 2012 code editor, and then click **Stop Debugging** on the **Debug** menu (or press Ctrl+Alt+Break).</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="7984b-146">Obtention du nom de l’utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="7984b-146">Getting the current user's name</span></span>

<span data-ttu-id="7984b-147">Dans l’exemple suivant, vous allez découvrir comment utiliser la propriété [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) de la classe [d’utilisateurs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) pour extraire le nom de l’utilisateur actuel et remplir la valeur d’un contrôle de **Zone de texte** à l’aide d’un gestionnaire d’événements pour l’événement de [chargement](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7984b-147">In the following example, you will learn how to use the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to retrieve the name of the current user and populate the value of a **Text Box** control by using an event handler for the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
<span data-ttu-id="7984b-148">Remplissage du contrôle de **Zone de texte** s’effectue à l’aide d’une instance de la classe [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) pour écrire le nom de l’utilisateur actuel dans le nœud XML auquel le contrôle est lié à.</span><span class="sxs-lookup"><span data-stu-id="7984b-148">Populating the **Text Box** control is accomplished by using an instance of the [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) class to write the current user's name to the XML node that the control is bound to.</span></span> 
  
<span data-ttu-id="7984b-149">La propriété [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) est d’abord appelée pour récupérer une instance de la classe [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) qui représente le document XML sous-jacent du formulaire.</span><span class="sxs-lookup"><span data-stu-id="7984b-149">First, the [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class is called to retrieve an instance of the [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) class that represents the underlying XML document of the form.</span></span> <span data-ttu-id="7984b-150">L’objet [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) appelle ensuite la méthode [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) , qui crée l’objet **XPathNavigator** et le place sur le nœud racine de la source de données principale du formulaire.</span><span class="sxs-lookup"><span data-stu-id="7984b-150">The [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) object then calls the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method, which creates the **XPathNavigator** object and positions it at the root node of the form's main data source.</span></span> 
  
<span data-ttu-id="7984b-151">La méthode [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) de la classe **XPathNavigator** est appelée pour sélectionner le champ employé dans la source de données du formulaire.</span><span class="sxs-lookup"><span data-stu-id="7984b-151">The [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) method of the **XPathNavigator** class is called to select the employee field in the form's data source.</span></span> <span data-ttu-id="7984b-152">Enfin, la méthode [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) est appelée pour définir la valeur du champ avec la propriété [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7984b-152">Finally, the [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) method is called to set the value of the field with the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property.</span></span> 
  
<span data-ttu-id="7984b-153">Pour plus d’informations sur l’utilisation de **System.Xml** dans les modèles de formulaires avec code managé, voir [utiliser les Classes XPathNavigator et XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7984b-153">For more information on working with **System.Xml** in managed code form templates, see [Work with the XPathNavigator and XPathNodeIterator Classes](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).</span></span>
  
### <a name="add-a-loading-event-handler"></a><span data-ttu-id="7984b-154">Ajouter un gestionnaire d'événements Chargement en cours (Loading) </span><span class="sxs-lookup"><span data-stu-id="7984b-154">Add a Loading event handler</span></span>

1. <span data-ttu-id="7984b-155">Ouvrez le modèle de formulaire HelloWorld que vous avez créé dans la procédure pas à pas précédente dans le Concepteur InfoPath.</span><span class="sxs-lookup"><span data-stu-id="7984b-155">Open the HelloWorld form template that you created in the previous walkthrough in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="7984b-156">Sous l’onglet **affichage** , sélectionnez **Afficher les champs**.</span><span class="sxs-lookup"><span data-stu-id="7984b-156">On the **View** tab, select **Show Fields**.</span></span>
    
3. <span data-ttu-id="7984b-157">Cliquez avec le bouton droit sur le dossier **mesChamps** , puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="7984b-157">Right click the **myFields** folder, and then click **Add**.</span></span>
    
4. <span data-ttu-id="7984b-158">Dans **nom**, tapez employé, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7984b-158">In **Name**, type employee, and then click **OK**.</span></span>
    
5. <span data-ttu-id="7984b-159">Faites glisser le champ employé sur l’affichage.</span><span class="sxs-lookup"><span data-stu-id="7984b-159">Drag the employee field onto the view.</span></span> 
    
6. <span data-ttu-id="7984b-160">Sous l’onglet **développeur** , cliquez sur **Événement chargement**.</span><span class="sxs-lookup"><span data-stu-id="7984b-160">On the **Developer** tab, click **Loading Event**.</span></span>
    
   <span data-ttu-id="7984b-161">Cela crée un gestionnaire d’événements pour l’événement de [chargement](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) et placer le focus sur ce gestionnaire d’événements dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="7984b-161">This will create an event handler for the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, and move the focus to that event handler in the code editor.</span></span> 
    
7. <span data-ttu-id="7984b-162">Dans l'éditeur de code, tapez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="7984b-162">In the code editor, type the following:</span></span>
    
   ```cs
    public void FormEvents_Loading(object sender, LoadingEventArgs e)
    {
        XPathNavigator dataSource;
        dataSource = this.MainDataSource.CreateNavigator();
        dataSource.SelectSingleNode(
            "/my:myFields/my:employee", NamespaceManager).SetValue(this.User.UserName);
    }
   ```
 
   ```vb
    Public Sub FormEvents_Loading(ByVal sender As Object, ByVal e As LoadingEventArgs)
        Dim dataSource As XPathNavigator
        dataSource = Me.MainDataSource.CreateNavigator
        dataSource.SelectSingleNode( _
            "/my:myFields/my:employee", NamespaceManager).SetValue(Me.User.UserName)
    End Sub
   ```

8. <span data-ttu-id="7984b-163">Basculer vers la fenêtre de création de formulaire InfoPath, puis cliquez sur le bouton **Aperçu** sous l’onglet **accueil** pour afficher un aperçu du formulaire.</span><span class="sxs-lookup"><span data-stu-id="7984b-163">Switch to the InfoPath form design window, and then click the **Preview** button on the **Home** tab to preview the form.</span></span> 
    
   <span data-ttu-id="7984b-164">Le champ employé doit être renseigné automatiquement votre nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7984b-164">The employee field should automatically fill in with your user name.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="7984b-165">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="7984b-165">Next steps</span></span>

- <span data-ttu-id="7984b-166">Pour plus d’informations sur l’utilisation des gestionnaires d’événements pour les autres contrôles et événements, voir [Ajouter un gestionnaire d’événements](how-to-add-an-event-handler.md).</span><span class="sxs-lookup"><span data-stu-id="7984b-166">For information about working with event handlers for other controls and events, see [Add an Event Handler](how-to-add-an-event-handler.md).</span></span>
    
- <span data-ttu-id="7984b-167">Pour plus d’informations sur l’aperçu et débogage de code dans les modèles de formulaires, voir [Aperçu et déboguer des modèles de formulaire InfoPath avec Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="7984b-167">For more information about previewing and debugging code in form templates, see [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
    
- <span data-ttu-id="7984b-168">Pour plus d’informations sur la façon de déployer un modèle de formulaire avec code managé, voir [Déployer des modèles de formulaire InfoPath avec Code](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="7984b-168">For information about how to deploy a managed-code form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span>
    
- <span data-ttu-id="7984b-169">Pour plus d’informations sur le modèle objet InfoPath et tâches de programmation courantes dans les modèles de formulaires avec code managé, voir [Présentation du modèle objet InfoPath et les tâches développeur courantes](understanding-the-infopath-object-model-and-common-developer-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="7984b-169">For information about the InfoPath object model and common programming tasks in managed-code form templates, see [Understanding the InfoPath Object Model and Common Developer Tasks](understanding-the-infopath-object-model-and-common-developer-tasks.md)</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7984b-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7984b-170">See also</span></span>

- [<span data-ttu-id="7984b-171">XmlForm</span><span class="sxs-lookup"><span data-stu-id="7984b-171">XmlForm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)

