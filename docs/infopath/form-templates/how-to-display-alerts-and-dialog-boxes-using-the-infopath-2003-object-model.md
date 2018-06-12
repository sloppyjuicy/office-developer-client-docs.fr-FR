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
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a>Afficher les alertes et boîtes de dialogue à l’aide du modèle objet InfoPath 2003

Lorsque vous écrivez du code pour développer les fonctionnalités d'un modèle de formulaire utilisant le modèle objet InfoPath 2003, il est souvent utile de communiquer des informations aux utilisateurs par l'intermédiaire de boîtes de dialogue. L'affichage par programme d'une boîte de dialogue et des éléments de l'interface utilisateur dans InfoPath se fait au moyen des méthodes de l'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) . 
  
## <a name="overview-of-the-uiobject-interface"></a>Vue d'ensemble de l'interface UIObject

L'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) fournit aux développeurs de formulaires les méthodes suivantes pour l'affichage de plusieurs types de boîtes de dialogue destinées aux utilisateurs InfoPath qui remplissent un formulaire. 
  
|Name|Description|
|:-----|:-----|
|[Alerte](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |Affiche une boîte de message simple contenant une chaîne de message spécifiée. Cette méthode doit être utilisée lorsque aucune intervention n’est requise de l’utilisateur et qu’un message doit être affichée. Affichée la boîte de dialogue est fermée en cliquant sur le bouton **OK** .  <br/> |
|[Confirmer](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |Affiche un message dont les boutons permettent aux utilisateurs d'effectuer des entrées. La valeur renvoyée est une des constantes énumérées [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) .  <br/> |
|[SetSaveAsDialogFileName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |Définit le nom de fichier par défaut pour un formulaire dans la boîte de dialogue **Enregistrer sous** .  <br/> |
|[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |Définit l’emplacement initial à partir de laquelle la boîte de dialogue **Enregistrer sous** commence à parcourir lors de son ouverture.  <br/> |
|[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |Crée un nouveau message électronique dans l’application de messagerie par défaut, avec le formulaire actuellement ouvert joint au message.  <br/> |
|[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |Affiche la boîte de dialogue modale, en fonction des arguments de position et fichier .html spécifié. Cette méthode doit être utilisée si vous souhaitez afficher plus d’un message simple à l’utilisateur et que vous devez obtenir des données à partir de l’utilisateur (au-delà de la confirmation simple qui est fournie par **Oui** | **Non** | **Annuler** les boutons affichés par la méthode **Confirm** ).  <br/> |
|[ShowSignatureDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |Affiche la boîte de dialogue **Signatures numériques** intégrée.  <br/> |
   
## <a name="using-the-uiobject-interface"></a>Utilisation de l'interface UIObject

L'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) est accessible par le biais de la propriété [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) de l'interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , elle-même accessible par le biais de la variable  `thisXDocument` initialisée dans la méthode  `_Startup` de la classe du code du formulaire. L'exemple ci-dessous illustre l'utilisation des méthodes [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) et [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) de l'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) . 
  
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

## <a name="using-the-showmodaldialog-method"></a>Utilisation de la méthode ShowModalDialog

Cet exemple illustre l'utilisation de la méthode [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) de l'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) pour afficher une boîte de dialogue personnalisée définie dans le fichier HTML show.html. 
  
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

Les exemples Visual C# et Visual Basic s'appuient sur un fichier HTML appelé « show.html » qui définit la boîte de dialogue appelée par la méthode [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) . Ce fichier HTML affiche certaines données du formulaire et affiche une zone de texte dans laquelle l'utilisateur peut entrer une valeur. La valeur de cette zone de texte est renvoyée au formulaire lors de la fermeture de la boîte de dialogue. 
  
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
> [!IMPORTANTE] La méthode [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) nécessite une confiance totale pour pouvoir être exécuté ou afficher un aperçu. Pour plus d’informations, voir [prévisualiser et déboguer les modèles de formulaires qui nécessitent une confiance totale](how-to-preview-and-debug-form-templates-that-require-full-trust.md). 
  

