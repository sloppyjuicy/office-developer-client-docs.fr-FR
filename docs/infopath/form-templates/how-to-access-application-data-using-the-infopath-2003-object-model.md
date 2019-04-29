---
title: Accès aux données d'application à l'aide du modèle objet InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- form templates [infopath 2007], accessing data using 2003 object model,InfoPath 2003-compatible form templates, accessing application data
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: Le modèle objet compatible avec InfoPath 2003 fournit des objets et des collections permettant d'accéder aux informations sur l'application InfoPath, notamment des informations relatives au document XML sous-jacent d'un formulaire et au fichier de définition du formulaire (.xsf). Ces données sont accessibles via l'objet de niveau supérieur dans la hiérarchie du modèle objet d'InfoPath, qui est instancié via l'interface Application .
ms.openlocfilehash: 849882a97109d91a5807a6798d5a62457ab971fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437440"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a><span data-ttu-id="57da0-105">Accès aux données d'application à l'aide du modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="57da0-105">Access Application Data Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="57da0-p102">Le modèle objet compatible avec InfoPath 2003 fournit des objets et des collections permettant d'accéder aux informations sur l'application InfoPath, notamment des informations relatives au document XML sous-jacent d'un formulaire et au fichier de définition du formulaire (.xsf). Ces données sont accessibles via l'objet de niveau supérieur dans la hiérarchie du modèle objet d'InfoPath, qui est instancié via l'interface [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="57da0-p102">The InfoPath 2003-compatible object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file. This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface.</span></span> 
  
<span data-ttu-id="57da0-p103">Un projet de modèle de formulaire avec code managé compatible avec InfoPath 2003 créé à l'aide de Visual Studio 2012 initialise la variable  `thisApplication` de la méthode  `_Startup` de la classe du code du formulaire, qui peut être utilisée pour accéder aux membres de l'interface [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . Dans l'exemple qui suit, les propriétés [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) et [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) de l'interface [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) sont utilisées pour renvoyer le nom et le numéro de version de l'instance d'InfoPath en cours d'exécution. Cette information est affichée dans une boîte de message à l'aide de la méthode [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) de l'interface [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) .</span><span class="sxs-lookup"><span data-stu-id="57da0-p103">An InfoPath 2003-compatible managed code form template project created using Visual Studio 2012 initializes the  `thisApplication` variable in the  `_Startup` method of the form code class, which can be used to access the members of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface. In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface are used to return the name and version number of the running instance of InfoPath. This information is displayed in a message box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) interface.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

<span data-ttu-id="57da0-p104">Dans l'exemple Visual C#, la référence au caractère  `\n` dans la chaîne du message d'alerte est rendue par le code InfoPath non managé comme un saut de ligne standard qui coupe le texte et le place dans une nouvelle ligne dans la boîte de message. Pour utiliser de manière explicite la nouvelle valeur de ligne définie pour l'environnement et la plate-forme actuels, utilisez la propriété **Environment.NewLine** comme illustré dans l'exemple qui suit.</span><span class="sxs-lookup"><span data-stu-id="57da0-p104">In the Visual C# example, the reference to the  `\n` character in the string for the alert message is rendered by InfoPath unmanaged code as a standard new line feed that causes the text to break and be placed on a new line in the message box. To explicitly use the new line value defined for the current environment and platform, use the **Environment.NewLine** property instead, as shown in the following example.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a><span data-ttu-id="57da0-113">Accès aux données du document XML sous-jacent d'un formulaire</span><span class="sxs-lookup"><span data-stu-id="57da0-113">Accessing Data from the Underlying XML Document of a Form</span></span>

<span data-ttu-id="57da0-114">Les développeurs peuvent utiliser l'interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) pour accéder aux informations sur le document XML sous-jacent d'un formulaire, notamment à une référence à un DOM (Document Object Model) XML contenant les données XML source du formulaire.</span><span class="sxs-lookup"><span data-stu-id="57da0-114">Developers can use the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface to gain access to information about a form's underlying XML document, including a reference to an XML Document Object Model (DOM) that contains the source XML data of the form.</span></span> 
  
<span data-ttu-id="57da0-p105">Dans l'exemple ci-dessous, la première boîte de message affiche une partie des données disponibles pour l'interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , par exemple si le document XML sous-jacent a été modifié (à l'aide de la propriété [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) ) et s'il a été signé numériquement (à l'aide de la propriété [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) ). La deuxième boîte de message utilise dans interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) la propriété [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) pour afficher le XML source du document XML sous-jacent du formulaire.</span><span class="sxs-lookup"><span data-stu-id="57da0-p105">In the following example, the first message box displays some of the data that is available from the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, such as whether the underlying XML document has been changed (by using the [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) property) and whether it has been digitally signed (using the [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) property). The next message box uses the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface's [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) property to display the source XML of the form's underlying XML document.</span></span> 
  
```cs
thisXDocument.UI.Alert("\nIsDirty: " + thisXDocument.IsDirty +
   "\nIsDOMReadOnly: " + thisXDocument.IsDOMReadOnly +
   "\nIsNew: " + thisXDocument.IsNew +
   "\nIsReadOnly: " + thisXDocument.IsReadOnly +
   "\nIsSigned: " + thisXDocument.IsSigned);
thisXDocument.UI.Alert(thisXDocument.DOM.xml);
```

```vb
thisXDocument.UI.Alert("IsDirty: " &amp; thisXDocument.IsDirty &amp; vbNewLine &amp; _
   "IsDOMReadOnly: " &amp; thisXDocument.IsDOMReadOnly &amp; vbNewLine &amp; _
   "IsNew: " &amp; thisXDocument.IsNew &amp; vbNewLine &amp; _
   "IsReadOnly: " &amp; thisXDocument.IsReadOnly &amp; vbNewLine &amp; _
   "IsSigned: " &amp; thisXDocument.IsSigned)
thisXDocument.UI.Alert(thisXDocument.DOM.xml)
```

<span data-ttu-id="57da0-p106">La propriété **xml** utilisée dans l'exemple précédent est une propriété du DOM XML. Pour plus d'informations à ce sujet, consultez la documentation du kit de développement MSXML 5.0.</span><span class="sxs-lookup"><span data-stu-id="57da0-p106">The **xml** property used in the previous example is a property of the XML Document Object Model (DOM). For more information about the XML DOM, see the MSXML 5.0 SDK documentation.</span></span> 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a><span data-ttu-id="57da0-119">Accès aux données du fichier de définition d'un formulaire</span><span class="sxs-lookup"><span data-stu-id="57da0-119">Accessing Data from a Form's Form Definition File</span></span>

<span data-ttu-id="57da0-p107">L'interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) permet également d'accéder aux informations sur le fichier .xsf d'un formulaire, notamment une référence DOM XML aux données XML source qu'il contient. Ces informations sont accessibles via la propriété [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) , qui renvoie une référence à l'interface [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="57da0-p107">Information about a form's .xsf file, including an XML DOM reference to the source XML data that it contains, can also be accessed using the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface. This information is accessed using the [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) property, which returns a reference to the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface.</span></span> 
  
<span data-ttu-id="57da0-p108">Dans l'exemple ci-dessous, le premier message affiche une partie des données disponibles via l'interface [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) , telles que son emplacement URI (Uniform Resource Identifier) (à l'aide de la propriété [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) ) et son numéro de version (à l'aide de la propriété [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) ). Le message suivant utilise la propriété [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) de l'interface [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) pour afficher le XML source du fichier .xsf.</span><span class="sxs-lookup"><span data-stu-id="57da0-p108">In the following example, the first alert displays some of the data that is available through the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface, such as its Uniform Resource Identifier (URI) location (using the [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) property) and its version number (using the [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) property). The next alert uses the [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) property of the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface to display the source XML of the .xsf file.</span></span> 
  
```cs
thisXDocument.UI.Alert("PackageURL: " +
   thisXDocument.Solution.PackageURL +
   "\nURI: " + thisXDocument.Solution.URI +
   "\nVersion: " + thisXDocument.Solution.Version);
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml);
```

```vb
thisXDocument.UI.Alert("PackageURL: " &amp; _
   thisXDocument.Solution.PackageURL &amp; vbNewLine &amp; _
   "URI: " &amp; thisXDocument.Solution.URI &amp; vbNewLine &amp; _
   "Version: " &amp; thisXDocument.Solution.Version)
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml)
```


