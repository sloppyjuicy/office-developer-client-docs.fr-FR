---
title: Afficher les alertes et boîtes de dialogue à l’aide du modèle objet InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, displaying dialog boxes,form templates [InfoPath 2007], displaying dialog boxes,alerts, displaying in InfoPath 2003-compatible form templates,dialog boxes, displaying in InfoPath 2003-compatible form templates,InfoPath 2003-compatible form templates, displaying alerts
localization_priority: Normal
ms.assetid: 721ac58e-56d9-4e3b-93f1-849e0c94d010
description: Lorsque vous écrivez du code pour développer les fonctionnalités d'un modèle de formulaire utilisant le modèle objet InfoPath 2003, il est souvent utile de communiquer des informations aux utilisateurs par l'intermédiaire de boîtes de dialogue.
ms.openlocfilehash: 1cc0f4c7a6696eae2d3b7058898b4119cede79e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782367"
---
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a><span data-ttu-id="32962-104">Afficher les alertes et boîtes de dialogue à l’aide du modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="32962-104">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="32962-p101">Lorsque vous écrivez du code pour développer les fonctionnalités d'un modèle de formulaire utilisant le modèle objet InfoPath 2003, il est souvent utile de communiquer des informations aux utilisateurs par l'intermédiaire de boîtes de dialogue. L'affichage par programme d'une boîte de dialogue et des éléments de l'interface utilisateur dans InfoPath se fait au moyen des méthodes de l'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="32962-p101">When writing code to extend the functionality of a form template that uses the InfoPath 2003 object model, it is often useful to provide the user with information in a dialog box. Programmatically displaying a dialog box and related user interface elements is accomplished in InfoPath by using the methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
## <a name="overview-of-the-uiobject-interface"></a><span data-ttu-id="32962-107">Vue d'ensemble de l'interface UIObject</span><span class="sxs-lookup"><span data-stu-id="32962-107">Overview of the UIObject Interface</span></span>

<span data-ttu-id="32962-108">L'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) fournit aux développeurs de formulaires les méthodes suivantes pour l'affichage de plusieurs types de boîtes de dialogue destinées aux utilisateurs InfoPath qui remplissent un formulaire.</span><span class="sxs-lookup"><span data-stu-id="32962-108">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface provides the following methods, which form developers can use to have different types of dialog boxes displayed to InfoPath users as they are filling out a form.</span></span> 
  
|<span data-ttu-id="32962-109">Name</span><span class="sxs-lookup"><span data-stu-id="32962-109">Name</span></span>|<span data-ttu-id="32962-110">Description</span><span class="sxs-lookup"><span data-stu-id="32962-110">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="32962-111">Alerte</span><span class="sxs-lookup"><span data-stu-id="32962-111">Alert</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |<span data-ttu-id="32962-112">Affiche une boîte de message simple contenant une chaîne de message spécifiée.</span><span class="sxs-lookup"><span data-stu-id="32962-112">Displays a simple message box that contains a specified message string.</span></span> <span data-ttu-id="32962-113">Cette méthode doit être utilisée lorsque aucune intervention n’est requise de l’utilisateur et qu’un message doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="32962-113">This method should be used when no input is required from the user and only a message needs to be displayed.</span></span> <span data-ttu-id="32962-114">Affichée la boîte de dialogue est fermée en cliquant sur le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="32962-114">The dialog box displayed is closed by clicking the **OK** button.</span></span>  <br/> |
|[<span data-ttu-id="32962-115">Confirmer</span><span class="sxs-lookup"><span data-stu-id="32962-115">Confirm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |<span data-ttu-id="32962-116">Affiche un message dont les boutons permettent aux utilisateurs d'effectuer des entrées.</span><span class="sxs-lookup"><span data-stu-id="32962-116">Displays a message box with buttons for input from a user.</span></span> <span data-ttu-id="32962-117">La valeur renvoyée est une des constantes énumérées [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) .</span><span class="sxs-lookup"><span data-stu-id="32962-117">The value that is returned is one of the [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) enumerated constants.</span></span>  <br/> |
|[<span data-ttu-id="32962-118">SetSaveAsDialogFileName</span><span class="sxs-lookup"><span data-stu-id="32962-118">SetSaveAsDialogFileName</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |<span data-ttu-id="32962-119">Définit le nom de fichier par défaut pour un formulaire dans la boîte de dialogue **Enregistrer sous** .</span><span class="sxs-lookup"><span data-stu-id="32962-119">Sets the default file name for a form in the **Save As** dialog box.</span></span>  <br/> |
|[<span data-ttu-id="32962-120">SetSaveAsDialogLocation</span><span class="sxs-lookup"><span data-stu-id="32962-120">SetSaveAsDialogLocation</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |<span data-ttu-id="32962-121">Définit l’emplacement initial à partir de laquelle la boîte de dialogue **Enregistrer sous** commence à parcourir lors de son ouverture.</span><span class="sxs-lookup"><span data-stu-id="32962-121">Sets the initial location at which the **Save As** dialog box starts to browse when it is opened.</span></span>  <br/> |
|[<span data-ttu-id="32962-122">ShowMailItem</span><span class="sxs-lookup"><span data-stu-id="32962-122">ShowMailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |<span data-ttu-id="32962-123">Crée un nouveau message électronique dans l’application de messagerie par défaut, avec le formulaire actuellement ouvert joint au message.</span><span class="sxs-lookup"><span data-stu-id="32962-123">Creates a new email message in the default email application, with the currently open form attached to the message.</span></span>  <br/> |
|[<span data-ttu-id="32962-124">ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="32962-124">ShowModalDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |<span data-ttu-id="32962-125">Affiche la boîte de dialogue modale, en fonction des arguments de position et fichier .html spécifié.</span><span class="sxs-lookup"><span data-stu-id="32962-125">Displays a modal dialog box, based on the specified .html file and positional arguments.</span></span> <span data-ttu-id="32962-126">Cette méthode doit être utilisée si vous souhaitez afficher plus d’un message simple à l’utilisateur et que vous devez obtenir des données à partir de l’utilisateur (au-delà de la confirmation simple qui est fournie par **Oui**</span><span class="sxs-lookup"><span data-stu-id="32962-126">This method should be used if you want to display more than a simple message to the user and you need to get back some data from the user (beyond the simple confirmation that is provided by the **Yes**</span></span> | <span data-ttu-id="32962-127">**Non**</span><span class="sxs-lookup"><span data-stu-id="32962-127">**No**</span></span> | <span data-ttu-id="32962-128">**Annuler** les boutons affichés par la méthode **Confirm** ).</span><span class="sxs-lookup"><span data-stu-id="32962-128">**Cancel** buttons displayed by the **Confirm** method).</span></span>  <br/> |
|[<span data-ttu-id="32962-129">ShowSignatureDialog</span><span class="sxs-lookup"><span data-stu-id="32962-129">ShowSignatureDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |<span data-ttu-id="32962-130">Affiche la boîte de dialogue **Signatures numériques** intégrée.</span><span class="sxs-lookup"><span data-stu-id="32962-130">Displays the built-in **Digital Signatures** dialog box.</span></span>  <br/> |
   
## <a name="using-the-uiobject-interface"></a><span data-ttu-id="32962-131">Utilisation de l'interface UIObject</span><span class="sxs-lookup"><span data-stu-id="32962-131">Using the UIObject Interface</span></span>

<span data-ttu-id="32962-p105">L'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) est accessible par le biais de la propriété [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) de l'interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , elle-même accessible par le biais de la variable  `thisXDocument` initialisée dans la méthode  `_Startup` de la classe du code du formulaire. L'exemple ci-dessous illustre l'utilisation des méthodes [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) et [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) de l'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="32962-p105">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface is accessed through the [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, which itself is accessed through the  `thisXDocument` variable that is initialized in the  `_Startup` method of the form code class. The following example demonstrates using the [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) and [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
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

## <a name="using-the-showmodaldialog-method"></a><span data-ttu-id="32962-134">Utilisation de la méthode ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="32962-134">Using the ShowModalDialog Method</span></span>

<span data-ttu-id="32962-135">Cet exemple illustre l'utilisation de la méthode [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) de l'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) pour afficher une boîte de dialogue personnalisée définie dans le fichier HTML show.html.</span><span class="sxs-lookup"><span data-stu-id="32962-135">This example demonstrates how to use the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface to display a custom dialog box defined in the HTML file show.html.</span></span> 
  
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

<span data-ttu-id="32962-p106">Les exemples Visual C# et Visual Basic s'appuient sur un fichier HTML appelé « show.html » qui définit la boîte de dialogue appelée par la méthode [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) . Ce fichier HTML affiche certaines données du formulaire et affiche une zone de texte dans laquelle l'utilisateur peut entrer une valeur. La valeur de cette zone de texte est renvoyée au formulaire lors de la fermeture de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="32962-p106">Both the Visual C# and Visual Basic samples depend on an HTML file named "show.html" that defines the dialog box that is invoked by the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method. This HTML file displays some data from the form and shows a text box for the user to fill in a value. The value in the textbox is returned to the form when the dialog box is closed.</span></span> 
  
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
> <span data-ttu-id="32962-139">La méthode [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) nécessite une confiance totale pour pouvoir être exécuté ou afficher un aperçu.</span><span class="sxs-lookup"><span data-stu-id="32962-139">The [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method requires Full Trust to run or preview.</span></span> <span data-ttu-id="32962-140">Pour plus d’informations, voir [prévisualiser et déboguer les modèles de formulaires qui nécessitent une confiance totale](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="32962-140">For more information, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  

