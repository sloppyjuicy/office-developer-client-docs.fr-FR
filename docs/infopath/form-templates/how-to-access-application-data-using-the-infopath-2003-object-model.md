---
title: Accéder aux données d’application à l’aide du modèle objet InfoPath 2003
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
# <a name="access-application-data-using-the-infopath-2003-object-model"></a>Accéder aux données d’application à l’aide du modèle objet InfoPath 2003

Le modèle objet compatible avec InfoPath 2003 fournit des objets et des collections permettant d'accéder aux informations sur l'application InfoPath, notamment des informations relatives au document XML sous-jacent d'un formulaire et au fichier de définition du formulaire (.xsf). Ces données sont accessibles via l'objet de niveau supérieur dans la hiérarchie du modèle objet d'InfoPath, qui est instancié via l'interface [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . 
  
Un projet de modèle de formulaire avec code managé compatible avec InfoPath 2003 créé à l'aide de Visual Studio 2012 initialise la variable  `thisApplication` de la méthode  `_Startup` de la classe du code du formulaire, qui peut être utilisée pour accéder aux membres de l'interface [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . Dans l'exemple qui suit, les propriétés [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) et [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) de l'interface [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) sont utilisées pour renvoyer le nom et le numéro de version de l'instance d'InfoPath en cours d'exécution. Cette information est affichée dans une boîte de message à l'aide de la méthode [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) de l'interface [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) . 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

Dans l'exemple Visual C#, la référence au caractère  `\n` dans la chaîne du message d'alerte est rendue par le code InfoPath non managé comme un saut de ligne standard qui coupe le texte et le place dans une nouvelle ligne dans la boîte de message. Pour utiliser de manière explicite la nouvelle valeur de ligne définie pour l'environnement et la plate-forme actuels, utilisez la propriété **Environment.NewLine** comme illustré dans l'exemple qui suit. 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a>Accès aux données du document XML sous-jacent d'un formulaire

Les développeurs peuvent utiliser l'interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) pour accéder aux informations sur le document XML sous-jacent d'un formulaire, notamment à une référence à un DOM (Document Object Model) XML contenant les données XML source du formulaire. 
  
Dans l'exemple ci-dessous, la première boîte de message affiche une partie des données disponibles pour l'interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , par exemple si le document XML sous-jacent a été modifié (à l'aide de la propriété [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) ) et s'il a été signé numériquement (à l'aide de la propriété [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) ). La deuxième boîte de message utilise dans interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) la propriété [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) pour afficher le XML source du document XML sous-jacent du formulaire. 
  
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

La propriété **xml** utilisée dans l'exemple précédent est une propriété du DOM XML. Pour plus d'informations à ce sujet, consultez la documentation du kit de développement MSXML 5.0. 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a>Accès aux données du fichier de définition d'un formulaire

L'interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) permet également d'accéder aux informations sur le fichier .xsf d'un formulaire, notamment une référence DOM XML aux données XML source qu'il contient. Ces informations sont accessibles via la propriété [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) , qui renvoie une référence à l'interface [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) . 
  
Dans l'exemple ci-dessous, le premier message affiche une partie des données disponibles via l'interface [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) , telles que son emplacement URI (Uniform Resource Identifier) (à l'aide de la propriété [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) ) et son numéro de version (à l'aide de la propriété [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) ). Le message suivant utilise la propriété [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) de l'interface [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) pour afficher le XML source du fichier .xsf. 
  
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


