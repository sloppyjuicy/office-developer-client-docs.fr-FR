---
title: À propos de l’assembly PIA (Primary Interop Assembly) InfoPath de Microsoft Office
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2007, assembly d'interopérabilité de base, assembly PIA InfoPath, assemblys PIA [InfoPath 2007], assemblys PIA [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Pour prendre en charge la création de solutions InfoPath qui utilisent des langages de code managé tels que Visual C# et Visual Basic, l'option prise en charge de la programmabilité .NET dans le programme d'installation d'InfoPath installe trois assemblys d'interopérabilité.
ms.openlocfilehash: 51773ad46b1371c410c4249e13a489f0c5550cd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310135"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>À propos de l’assembly PIA (Primary Interop Assembly) InfoPath de Microsoft Office

L'application InfoPath est construite en tant qu'application COM (Component Object Model) qui expose ses interfaces de programmabilité pour l'automatisation externe en tant qu'interfaces COM. Pour prendre en charge la création de solutions InfoPath qui utilisent des langages de code managé tels que Visual C# et Visual Basic, l'option **prise en charge** de la programmabilité .net dans le programme d'installation d'InfoPath installe trois assemblys d'interopérabilité. Les assemblys d'interopérabilité sont des assemblys .NET qui font office de lien entre le code managé et le code non managé et mappent les membres des objets COM avec les membres managés .NET équivalents. 
  
Les fichiers des trois assemblys d'interopérabilité installés par InfoPath sont les suivants :
  
- Microsoft. Office. Interop. InfoPath. dll
    
- Microsoft. Office. Interop. InfoPath. SemiTrust. dll
    
- Microsoft. Office. Interop. InfoPath. Xml. dll
    
Cette rubrique décrit le modèle objet exposé via l'assembly d'interopérabilité Microsoft. Office. Interop. InfoPath, qui est utilisé exclusivement pour le code d'automatisation externe. Pour plus d'informations sur l'assembly Microsoft. Office. Interop. InfoPath. SemiTrust, qui est utilisé exclusivement pour l'écriture et l'exécution de code managé exécuté à partir de modèles de formulaire InfoPath (. xsn), voir [modèles objet compatibles avec infopath 2003](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx).
  
## <a name="important-installation-information"></a>Informations importantes concernant l'installation

L'option d'installation par défaut du programme d'installation d'InfoPath installe l'assembly Microsoft. Office. Interop. InfoPath dans le global assembly cache (GAC), dont le contenu peut être affiché à partir du dossier C:\Windows\Assembly. (ou dans C:\Windows\assembly\GAC_ MSIL lors de l'affichage du système de fichiers directement). Cet assembly est appelé «assembly PIA Microsoft Office InfoPath» et est souvent utilisé conjointement avec l'assembly Microsoft. Office. Interop. InfoPath. xml, qui est également installé dans le GAC, pour automatiser l'application InfoPath à partir de applications externes qui utilisent du code managé. Pour plus d'informations sur l'assembly Microsoft. Office. Interop. InfoPath. xml, voir [à propos de l'assembly XML d'InfoPath Interop](about-the-infopath-xml-interop-assembly.md).
  
Si l'assembly Microsoft. Office. Interop. InfoPath n'est pas visible dans le GAC, vérifiez qu'InfoPath a été correctement installé. Par défaut, l'option **prise en charge** de la programmabilité .net dans le programme d'installation est définie sur **exécuter à partir du disque dur** tant que le .NET Framework 1,1 Redistributable, .NET Framework 1,1 le kit de développement logiciel (SDK) ou une version ultérieure de .NET Framework est installé avant d'exécuter le programme d'installation. Si ces assemblys d'interopérabilité ne sont pas disponibles sur votre ordinateur, vous devez confirmer que .NET Framework 1,1 ou une version ultérieure est installé, puis utiliser les **programmes et fonctionnalités** du **panneau** de configuration pour modifier l'installation en définissant la **Programmabilité .net Option prise en charge** sous **Microsoft Office InfoPath** à **exécuter à partir du disque dur**.
  
Pour plus d'informations sur le téléchargement de la version redistribuable de .NET Framework 1,1, voir [.net framework 1,1 Redistributable](https://www.microsoft.com/en-us/download/details.aspx?id=26).
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>Espace de noms Microsoft. Office. Interop. InfoPath

Bien que le processus d'écriture de code managé pour une tâche donnée soit très semblable à l'exécution de la même tâche à l'aide d'un langage tel que Visual Basic pour applications ou JScript, le modèle objet exposé lors de l'affichage de **Microsoft. Office. Interop. InfoPath** l'espace de noms de l' **Explorateur d'objets** dans Microsoft Visual Studio est plus complexe. Cela est dû au fait que l'interopérabilité avec .NET Framework requiert un serveur COM pour exposer toutes ses interfaces publiques, ainsi que d'autres constructions supplémentaires requises par .NET Framework lui-même. Pour plus d'informations sur la façon dont le modèle objet exposé par un assembly d'interopérabilité semble plus complexe, consultez la section «Comment les objets COM sont exposés à du code managé» de la rubrique [modèles objet compatibles avec InfoPath 2003](../form-templates/infopath-2003-compatible-object-models.md) . 
  
### <a name="using-intellisense"></a>Utilisation d'IntelliSense

Les exemples de cette section supposent que vous avez établi des références aux assemblys Microsoft. Office. Interop. InfoPath et Microsoft. Office. Interop. InfoPath. Xml. Pour plus d'informations sur la définition de références et d'exemples d'automation externe supplémentaires, consultez la rubrique [scénarios d'automatisation externe et exemples](external-automation-scenarios-and-examples.md).
  
Avant de pouvoir utiliser la saisie semi-automatique des instructions Microsoft IntelliSense dans du code d'automatisation externe, vous devez créer une variable d'objet pour une instance de la classe [application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , comme illustré dans la ligne de code suivante. 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

Après la création de la variable d'objet, lorsque vous tapez le nom de la variable suivi d'un point, une liste déroulante s'affiche avec les membres de la classe d' **application** à sélectionner. 
  
Pour utiliser un formulaire InfoPath, déclarez une variable d'objet de type [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) , puis initialisez-la en ouvrant le formulaire à partir de la collection [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) de la variable d'objet **application** , comme illustré dans la ligne de code suivante. 
  
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

La liste déroulante de saisie semi-automatique des instructions IntelliSense pour les membres de la classe **XDocument** s'affiche lorsque vous tapez le nom de la variable suivi d'un point. 
  
Pour utiliser le contenu du document XML sous-jacent pour le formulaire à l'aide de Microsoft XML Core Services (MSXML), vous devez créer une variable de type [IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) , puis utiliser la propriété [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) de la classe **XDOCUMENT** pour affecter le code XML Modèle DOM (Document Object Model) du formulaire à cette variable. 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

La liste déroulante de saisie semi-automatique des instructions IntelliSense pour les membres de la classe **IXMLDOMDocument2** s'affiche lorsque vous tapez le nom de la variable suivi d'un point, ce qui vous permet d'utiliser MSXML pour utiliser le document XML. 
  
### <a name="using-the-class-library-reference-documentation"></a>Utilisation de la documentation de référence de la bibliothèque de classes

L'organisation de la documentation de référence de la bibliothèque de classes de l'espace de noms [Microsoft. Office. Interop. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) reflète les relations entre les interfaces de coclasse et les interfaces héritées qu'elles implémentent. 
  
Lorsque vous ouvrez une rubrique pour une interface de coclasse, telle que [application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , le lien vers les membres de l'interface de coclasse qui suit la description de l'interface au début de la rubrique affiche une rubrique vide. Pour afficher la liste des membres implémentés par l'interface de coclasse, vous devez ouvrir la rubrique de la dernière interface héritée par la coclasse, puis ouvrir la table de ses membres. Un lien vers l'interface héritée est proposé au début de la section Remarques de la rubrique consacrée à l'interface de coclasse. 
  
Lorsque vous appuyez sur F1 dans l'éditeur de code Visual Studio, le comportement est similaire, mais le membre sur lequel vous appelez l'aide F1 s'affiche directement, car vous travaillez le plus souvent avec les membres d'une interface. Cependant, le fait qu'un membre puisse être implémenté depuis une interface avec version peut paraître confus la première fois que vous y êtes confronté. Par exemple, si vous tapez  `myXDocument.UI.Alert` puis que vous placez le curseur sur  `Alert` et que vous appuyez sur F1, une rubrique intitulée « UI2.Alert Method » s'affiche. Ceci est dû au fait que la méthode **Alert** est une implémentation d'un membre de l'interface **UI2**. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Transmission de paramètres facultatifs à des membres du modèle objet InfoPath

Si un membre du modèle objet InfoPath contient un paramètre facultatif, et que vous ne spécifiez pas de valeur pour ce paramètre, vous devez transmettre le champ **type. Missing** pour ce paramètre. Si vous ne transmettez pas le champ **Type.Missing** alors que la valeur est omise, cela provoque une erreur de compilation. Ceci est vrai pour le code écrit en C# et Visual Basic. Par exemple, la méthode [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) de l'interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) comprend deux paramètres facultatifs :  _varEndNode_ et  _varViewContext_. Une ligne de code dans laquelle les valeurs de ces deux paramètres ne sont pas spécifiées doit ressembler aux exemples suivants.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>Voir aussi

- [Exemples et scénarios d’automatisation externe](external-automation-scenarios-and-examples.md)

