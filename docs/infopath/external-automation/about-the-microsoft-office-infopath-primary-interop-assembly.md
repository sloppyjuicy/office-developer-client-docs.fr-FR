---
title: À propos de l’assembly PIA (Primary Interop Assembly) InfoPath de Microsoft Office
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2007, primary interop assembly,InfoPath primary interop assembly,PIAs [InfoPath 2007],primary interop assemblies [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Pour prendre en charge la création de solutions InfoPath qui utilisent des langages de code géré tels que Visual C# et Visual Basic, l’option prise en charge de la programmabilité .NET dans le programme d’installation d’InfoPath installe trois assemblys d’interop.
ms.openlocfilehash: 51773ad46b1371c410c4249e13a489f0c5550cd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310135"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>À propos de l’assembly PIA (Primary Interop Assembly) InfoPath de Microsoft Office

L’application InfoPath est conçue en tant qu’application COM (Component Object Model) qui expose ses interfaces de programmabilité pour l’automatisation externe en tant qu’interfaces COM. Pour prendre en charge la création de solutions InfoPath qui utilisent des langages de code géré tels que Visual C# et Visual Basic, l’option Prise en charge de la **programmabilité .NET** dans le programme d’installation d’InfoPath installe trois assemblys d’interop. Les assemblys d'interopérabilité sont des assemblys .NET qui font office de lien entre le code managé et le code non managé et mappent les membres des objets COM avec les membres managés .NET équivalents. 
  
Les fichiers des trois assemblys d'interopérabilité installés par InfoPath sont les suivants :
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
Cette rubrique décrit le modèle objet exposé via l’assembly d’opation Microsoft.Office.Interop.InfoPath, qui est exclusivement utilisé pour le code d’automatisation externe. Pour plus d’informations sur l’assembly Microsoft.Office.Interop.InfoPath.SemiTrust, qui est exclusivement utilisé pour l’écriture et l’exécution de code géré qui s’exécute à partir de modèles de formulaire InfoPath (.xsn), voir Modèles objet compatibles [InfoPath 2003.](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx)
  
## <a name="important-installation-information"></a>Informations importantes concernant l'installation

L’option d’installation par défaut du programme d’installation d’InfoPath installe l’assembly Microsoft.Office.Interop.InfoPath dans le Global Assembly Cache (GAC), dont le contenu peut être affiché à partir du dossier C:\Windows\Assembly (ou dans C:\Windows\assembly\GAC_MSIL lors de l’affichage direct du système de fichiers). Cet assembly est appelé « assembly Microsoft Office InfoPath Primary Interop Assembly » et est souvent utilisé conjointement avec l’assembly Microsoft.Office.Interop.InfoPath.Xml, qui est également installé dans le GAC, pour automatiser l’application InfoPath à partir d’applications externes qui utilisent du code géré. Pour plus d’informations sur Microsoft.Office.Interop.InfoPath.Xml assembly, voir À propos de l’assembly d’opation [XML InfoPath.](about-the-infopath-xml-interop-assembly.md)
  
Si l’assembly Microsoft.Office.Interop.InfoPath n’est pas visible dans le GAC, vous devez vérifier qu’InfoPath a été installé correctement. Par défaut, l’option prise en charge de la  **programmabilité .NET** dans le programme d’installation est configurée pour s’exécuter à partir de Mon ordinateur tant que .NET Framework 1.1 Redistributable, .NET Framework 1.1 Software Development Kit (SDK) ou une version ultérieure de .NET Framework est installée avant d’exécuter le programme d’installation. Si ces assemblys d’interopation ne sont pas disponibles sur votre ordinateur, vous devez vérifier  que .NET  Framework 1.1 ou ultérieur est installé, puis utiliser programmes et fonctionnalités du Panneau de configuration pour modifier l’installation en paramétrage de l’option prise en charge de la **programmabilité .NET** sous **Microsoft Office InfoPath** à exécuter à partir du My **Computer**.
  
Pour plus d’informations sur le téléchargement de .NET Framework 1.1 Redistributable, voir [.NET Framework 1.1 Redistributable](https://www.microsoft.com/en-us/download/details.aspx?id=26).
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>Espace de noms Microsoft.Office.Interop.InfoPath

Bien que le processus d’écriture de code géré pour une tâche donnée soit très similaire à l’utilisation d’un langage tel que Visual Basic pour Applications ou JScript, le  modèle objet exposé lors de l’affichage de l’espace de noms **Microsoft.Office.Interop.InfoPath** à partir de l’Explorateur d’objets dans Microsoft Visual Studio semble plus complexe. En effet, l’interopérabilité avec .NET Framework nécessite un serveur COM pour exposer toutes ses interfaces publiques, ainsi que certaines constructions supplémentaires requises par .NET Framework lui-même. Pour plus d’informations sur la façon dont et pourquoi le modèle objet exposé par un assembly d’opation apparaît plus complexe, voir la section « Comment les objets COM sont exposés au code géré » de la rubrique Modèles objet compatibles [InfoPath 2003.](../form-templates/infopath-2003-compatible-object-models.md) 
  
### <a name="using-intellisense"></a>Utilisation d'IntelliSense

Les exemples de cette section supposent que vous avez établi des références aux assemblys Microsoft.Office.Interop.InfoPath et Microsoft.Office.Interop.InfoPath.Xml assemblys. Pour plus d’informations sur la façon de définir des références et d’autres exemples d’automatisation externe, voir [External Automation Scenarios and Examples](external-automation-scenarios-and-examples.md).
  
Avant de pouvoir utiliser l’achèvement de l’instruction Microsoft IntelliSense dans du code d’automatisation externe, vous devez créer une variable objet pour une instance de la classe [Application,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) comme illustré dans la ligne de code suivante. 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

Après avoir créé la variable objet, lorsque vous tapez le nom de la variable suivi d’un point, une liste de listes listes est affichée avec les membres de la classe **Application** à sélectionner. 
  
Pour travailler avec un formulaire InfoPath, déclarez une variable objet de type [XDocument,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) puis initialisez-la en ouvrant le formulaire à partir de la collection [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) de la variable objet **Application,** comme illustré dans la ligne de code suivante. 
  
```cs
XDocument myXDoc = myApp.XDocuments.Open(
    "c:\\temp\\Form1.xml",
    (int) XdDocumentVersionMode.xdFailOnVersionOlder);
```

```vb
Dim myXDoc As XDocument = myApp.XDocuments.Open( _
    "c:\\temp\\Form1.xml", _
    XdDocumentVersionMode.xdFailOnVersionOlder)
```

La liste IntelliSense’achèvement de l’instruction pour les membres de la classe **XDocument** s’affiche lorsque vous tapez le nom de la variable suivi d’un point. 
  
Pour utiliser le contenu du document XML sous-jacent du formulaire à l’aide de Microsoft XML Core Services® (MSXML), vous devez créer une variable de type [IXMLDOMDocument2,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) puis utiliser la propriété [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) de la classe **XDocument** pour affecter le DOM XML du formulaire à cette variable. 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

La liste IntelliSense liste de fin d’instruction pour les membres de la classe **IXMLDOMDocument2** s’affiche lorsque vous tapez le nom de la variable suivi d’un point, ce qui vous permet d’utiliser MSXML pour travailler avec le document XML. 
  
### <a name="using-the-class-library-reference-documentation"></a>Utilisation de la documentation de référence de la bibliothèque de classes

L’organisation de la documentation de référence de la bibliothèque de classes de l’espace de noms [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) reflète les relations entre les interfaces de coclasse et les interfaces héritées qu’elles implémentent. 
  
Lorsque vous ouvrez une rubrique pour une interface de coclasse, telle [qu’Application,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) le lien vers les membres de l’interface de coclasse qui suit la description de l’interface au début de la rubrique affiche une rubrique vide. Pour afficher la liste des membres implémentés par l'interface de coclasse, vous devez ouvrir la rubrique de la dernière interface héritée par la coclasse, puis ouvrir la table de ses membres. Un lien vers l'interface héritée est proposé au début de la section Remarques de la rubrique consacrée à l'interface de coclasse. 
  
Lorsque vous appuyez sur F1 dans l’Éditeur de code Visual Studio, le comportement est similaire, sauf que le membre sur lequel vous voquez l’aide F1 s’affiche directement, car vous travaillez généralement avec les membres d’une interface. Cependant, le fait qu'un membre puisse être implémenté depuis une interface avec version peut paraître confus la première fois que vous y êtes confronté. Par exemple, si vous tapez  `myXDocument.UI.Alert` puis que vous placez le curseur sur  `Alert` et que vous appuyez sur F1, une rubrique intitulée « UI2.Alert Method » s'affiche. Ceci est dû au fait que la méthode **Alert** est une implémentation d'un membre de l'interface **UI2**. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Transmission de paramètres facultatifs à des membres du modèle objet InfoPath

Si un membre du modèle objet InfoPath contient un paramètre facultatif et que vous ne spécifiez pas de valeur pour ce paramètre, vous devez transmettre le champ **Type.Missing** pour ce paramètre. Si vous ne transmettez pas le champ **Type.Missing** alors que la valeur est omise, cela provoque une erreur de compilation. Cela est vrai pour le code écrit en C# et Visual Basic. Par exemple, la méthode [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) de l'interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) comprend deux paramètres facultatifs :  _varEndNode_ et  _varViewContext_. Une ligne de code dans laquelle les valeurs de ces deux paramètres ne sont pas spécifiées doit ressembler aux exemples suivants.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>Voir aussi

- [Exemples et scénarios d’automatisation externe](external-automation-scenarios-and-examples.md)

