---
title: Afficher des alertes et des boîtes de dialogue à l’aide du modèle objet InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, displaying dialog boxes,form templates [InfoPath 2007], displaying dialog boxes,alerts, displaying in InfoPath 2003-compatible form templates,dialog boxes, displaying in InfoPath 2003-compatible form templates,InfoPath 2003-compatible form templates, displaying alerts
localization_priority: Normal
ms.assetid: 721ac58e-56d9-4e3b-93f1-849e0c94d010
description: Lorsque vous écrivez du code pour développer les fonctionnalités d'un modèle de formulaire utilisant le modèle objet InfoPath 2003, il est souvent utile de communiquer des informations aux utilisateurs par l'intermédiaire de boîtes de dialogue.
ms.openlocfilehash: 12088747250037e53a3b7d8d0577936e30d6292c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409481"
---
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a><span data-ttu-id="a9113-104">Afficher des alertes et des boîtes de dialogue à l’aide du modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="a9113-104">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="a9113-p101">Lorsque vous écrivez du code pour développer les fonctionnalités d'un modèle de formulaire utilisant le modèle objet InfoPath 2003, il est souvent utile de communiquer des informations aux utilisateurs par l'intermédiaire de boîtes de dialogue. L'affichage par programme d'une boîte de dialogue et des éléments de l'interface utilisateur dans InfoPath se fait au moyen des méthodes de l'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a9113-p101">When writing code to extend the functionality of a form template that uses the InfoPath 2003 object model, it is often useful to provide the user with information in a dialog box. Programmatically displaying a dialog box and related user interface elements is accomplished in InfoPath by using the methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
## <a name="overview-of-the-uiobject-interface"></a><span data-ttu-id="a9113-107">Vue d'ensemble de l'interface UIObject</span><span class="sxs-lookup"><span data-stu-id="a9113-107">Overview of the UIObject Interface</span></span>

<span data-ttu-id="a9113-108">L'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) fournit aux développeurs de formulaires les méthodes suivantes pour l'affichage de plusieurs types de boîtes de dialogue destinées aux utilisateurs InfoPath qui remplissent un formulaire.</span><span class="sxs-lookup"><span data-stu-id="a9113-108">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface provides the following methods, which form developers can use to have different types of dialog boxes displayed to InfoPath users as they are filling out a form.</span></span> 
  
|<span data-ttu-id="a9113-109">Nom</span><span class="sxs-lookup"><span data-stu-id="a9113-109">Name</span></span>|<span data-ttu-id="a9113-110">Description</span><span class="sxs-lookup"><span data-stu-id="a9113-110">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9113-111">Alerte</span><span class="sxs-lookup"><span data-stu-id="a9113-111">Alert</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |<span data-ttu-id="a9113-p102">Affiche une boîte de message unique contenant une chaîne de message spécifiée. Cette méthode est recommandée lorsqu'aucune action de la part de l'utilisateur n'est requise et qu'un simple message doit être affiché. Cette boîte de dialogue se ferme lorsque l'utilisateur clique sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9113-p102">Displays a simple message box that contains a specified message string. This method should be used when no input is required from the user and only a message needs to be displayed. The dialog box displayed is closed by clicking the **OK** button.  </span></span><br/> |
|[<span data-ttu-id="a9113-115">Confirm</span><span class="sxs-lookup"><span data-stu-id="a9113-115">Confirm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |<span data-ttu-id="a9113-116">Affiche une boîte de message contenant des boutons qui permettent aux utilisateurs d'effectuer des entrées.</span><span class="sxs-lookup"><span data-stu-id="a9113-116">Displays a message box with buttons for input from a user.</span></span> <span data-ttu-id="a9113-117">La valeur renvoyée est l’une des constantes [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) éumées.</span><span class="sxs-lookup"><span data-stu-id="a9113-117">The value that is returned is one of the [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) enumerated constants.</span></span>  <br/> |
|[<span data-ttu-id="a9113-118">SetSaveAsDialogFileName</span><span class="sxs-lookup"><span data-stu-id="a9113-118">SetSaveAsDialogFileName</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |<span data-ttu-id="a9113-119">Définit le nom de fichier par défaut d'un formulaire dans la boîte de dialogue **Enregistrer sous**.</span><span class="sxs-lookup"><span data-stu-id="a9113-119">Sets the default file name for a form in the **Save As** dialog box.</span></span>  <br/> |
|[<span data-ttu-id="a9113-120">SetSaveAsDialogLocation</span><span class="sxs-lookup"><span data-stu-id="a9113-120">SetSaveAsDialogLocation</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |<span data-ttu-id="a9113-121">Définit l'emplacement de recherche initial de la boîte de dialogue **Enregistrer sous**, lors de son ouverture.</span><span class="sxs-lookup"><span data-stu-id="a9113-121">Sets the initial location at which the **Save As** dialog box starts to browse when it is opened.</span></span>  <br/> |
|[<span data-ttu-id="a9113-122">ShowMailItem</span><span class="sxs-lookup"><span data-stu-id="a9113-122">ShowMailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |<span data-ttu-id="a9113-123">Crée un message électronique dans l’application de messagerie par défaut, avec le formulaire actuellement ouvert joint au message.</span><span class="sxs-lookup"><span data-stu-id="a9113-123">Creates a new email message in the default email application, with the currently open form attached to the message.</span></span>  <br/> |
|[<span data-ttu-id="a9113-124">ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="a9113-124">ShowModalDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |<span data-ttu-id="a9113-125">Affiche une boîte de dialogue qui exige une réponse de l'utilisateur, sur la base du fichier HTML et des arguments de position spécifiés.</span><span class="sxs-lookup"><span data-stu-id="a9113-125">Displays a modal dialog box, based on the specified .html file and positional arguments.</span></span> <span data-ttu-id="a9113-126">Cette méthode doit être utilisée si vous souhaitez afficher plus qu’un simple message à l’utilisateur et que vous  devez obtenir des données de l’utilisateur (au-delà de la simple confirmation fournie par le oui</span><span class="sxs-lookup"><span data-stu-id="a9113-126">This method should be used if you want to display more than a simple message to the user and you need to get back some data from the user (beyond the simple confirmation that is provided by the **Yes**</span></span> | <span data-ttu-id="a9113-127">**Non**</span><span class="sxs-lookup"><span data-stu-id="a9113-127">**No**</span></span> | <span data-ttu-id="a9113-128">**Boutons d’annulation** affichés par la **méthode Confirm).**</span><span class="sxs-lookup"><span data-stu-id="a9113-128">**Cancel** buttons displayed by the **Confirm** method).</span></span>  <br/> |
|[<span data-ttu-id="a9113-129">ShowSignatureDialog</span><span class="sxs-lookup"><span data-stu-id="a9113-129">ShowSignatureDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |<span data-ttu-id="a9113-130">Affiche la boîte de dialogue intégrée **Signatures numériques**.</span><span class="sxs-lookup"><span data-stu-id="a9113-130">Displays the built-in **Digital Signatures** dialog box.</span></span>  <br/> |
   
## <a name="using-the-uiobject-interface"></a><span data-ttu-id="a9113-131">Utilisation de l'interface UIObject</span><span class="sxs-lookup"><span data-stu-id="a9113-131">Using the UIObject Interface</span></span>

<span data-ttu-id="a9113-p105">L'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) est accessible par le biais de la propriété [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) de l'interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , elle-même accessible par le biais de la variable  `thisXDocument` initialisée dans la méthode  `_Startup` de la classe du code du formulaire. L'exemple ci-dessous illustre l'utilisation des méthodes [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) et [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) de l'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a9113-p105">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface is accessed through the [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, which itself is accessed through the  `thisXDocument` variable that is initialized in the  `_Startup` method of the form code class. The following example demonstrates using the [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) and [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
```cs
thisXDocument.UI.ShowMailItem("someone@example.com","", "", 
   "Updated Form", "Here is the updated form that you requested.");
thisXDocument.UI.Alert("The email message has been created.");
```

```vb
thisXDocument.UI.ShowMailItem("someone@example.com", "", "", _
   "Updated Form", "Here is the updated form that you requested.")
thisXDocument.UI.Alert("The email message has been created.")
```

## <a name="using-the-showmodaldialog-method"></a><span data-ttu-id="a9113-134">Utilisation de la méthode ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="a9113-134">Using the ShowModalDialog Method</span></span>

<span data-ttu-id="a9113-135">Cet exemple illustre l'utilisation de la méthode [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) de l'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) pour afficher une boîte de dialogue personnalisée définie dans le fichier HTML show.html.</span><span class="sxs-lookup"><span data-stu-id="a9113-135">This example demonstrates how to use the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface to display a custom dialog box defined in the HTML file show.html.</span></span> 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Write your code here.
   thisXDocument.UI.ShowModalDialog(
      "show.html",(object)thisXDocument,200,450,50,50);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Write your code here.
   thisXDocument.UI.ShowModalDialog( _
      "show.html", _
      DirectCast(thisXDocument, Object), 200, 450, 50, 50)
End Sub

```

<span data-ttu-id="a9113-p106">Les exemples Visual C# et Visual Basic s'appuient sur un fichier HTML appelé « show.html » qui définit la boîte de dialogue appelée par la méthode [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) . Ce fichier HTML affiche certaines données du formulaire et affiche une zone de texte dans laquelle l'utilisateur peut entrer une valeur. La valeur de cette zone de texte est renvoyée au formulaire lors de la fermeture de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a9113-p106">Both the Visual C# and Visual Basic samples depend on an HTML file named "show.html" that defines the dialog box that is invoked by the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method. This HTML file displays some data from the form and shows a text box for the user to fill in a value. The value in the textbox is returned to the form when the dialog box is closed.</span></span> 
  
```html
<HTML>
   <HEAD>
      <script language="JScript">
function BtnClick()
{
   xdocument = window.dialogArguments;
   myXml = xdocument.DOM.xml
   aForm = oForm.elements;
   aForm.textBox.value = myXml;
}
      </script>
   </HEAD>
   <BODY>
      <H1><FONT face="Arial">This is a modal dialog box</FONT> &nbsp;
      </H1>
      <BUTTON onclick="BtnClick()" id="BUTTON1" type="button">
         Get XML DOM
      </BUTTON>
      <FORM ID="oForm">
         <INPUT Type="text" name="textBox">
      </FORM>
   </BODY>
</HTML>

```

> [!IMPORTANT]
> <span data-ttu-id="a9113-139">[!IMPORTANTE] La méthode [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) nécessite une confiance totale pour pouvoir être exécuté ou afficher un aperçu.</span><span class="sxs-lookup"><span data-stu-id="a9113-139">The [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method requires Full Trust to run or preview.</span></span> <span data-ttu-id="a9113-140">Pour plus d’informations, voir Les modèles de formulaires d’aperçu et de [débogage qui nécessitent une confiance totale.](how-to-preview-and-debug-form-templates-that-require-full-trust.md)</span><span class="sxs-lookup"><span data-stu-id="a9113-140">For more information, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  

