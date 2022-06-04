---
title: À propos de l’assembly PIA (Primary Interop Assembly) InfoPath de Microsoft Office
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2007, assembly d’interopérabilité principale, assembly d’interopérabilité principale InfoPath, PIAs [InfoPath 2007],assemblys d’interopérabilité primaire [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Pour prendre en charge la création de solutions InfoPath qui utilisent des langages de code managé tels que Visual C# et Visual Basic, l’option de prise en charge de la programmabilité .NET dans le programme d’installation d’InfoPath installe trois assemblys d’interopérabilité.
ms.openlocfilehash: 34bbd0472786ca20974cbff2bd1a44f93a154774
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894830"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>À propos de l’assembly PIA (Primary Interop Assembly) InfoPath de Microsoft Office

L’application InfoPath est générée en tant qu’application COM (Component Object Model) qui expose ses interfaces de programmabilité pour l’automatisation externe en tant qu’interfaces COM. Pour prendre en charge la création de solutions InfoPath qui utilisent des langages de code managé tels que Visual C# et Visual Basic, l’option **de prise en charge de la programmabilité .NET** dans le programme d’installation d’InfoPath installe trois assemblys d’interopérabilité. Les assemblys d'interopérabilité sont des assemblys .NET qui font office de lien entre le code managé et le code non managé et mappent les membres des objets COM avec les membres managés .NET équivalents.
  
Les fichiers des trois assemblys d'interopérabilité installés par InfoPath sont les suivants :
  
- Microsoft.Office.Interop.InfoPath.dll

- Microsoft.Office.Interop.InfoPath.SemiTrust.dll

- Microsoft.Office.Interop.InfoPath.Xml.dll

Cette rubrique décrit le modèle objet exposé via l’assembly d’interopérabilité Microsoft.Office.Interop.InfoPath, qui est utilisé exclusivement pour le code d’automatisation externe. Pour plus d’informations sur l’assembly Microsoft.Office.Interop.InfoPath.SemiTrust, qui est utilisé exclusivement pour l’écriture et l’exécution de code managé qui s’exécute à partir de modèles de formulaire InfoPath (.xsn), consultez [InfoPath 2003 Compatible Object Models](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx).
  
## <a name="important-installation-information"></a>Informations importantes concernant l'installation

L’option d’installation par défaut du programme d’installation d’InfoPath installe l’assembly Microsoft.Office.Interop.InfoPath dans le Global Assembly Cache (GAC), dont le contenu peut être affiché à partir du dossier C:\Windows\Assembly (ou dans C:\Windows\assembly\GAC_MSIL lors de l’affichage direct du système de fichiers). Cet assembly est appelé « Microsoft Office InfoPath Primary Interop Assembly » et est souvent utilisé conjointement avec l’assembly Microsoft.Office.Interop.InfoPath.Xml, qui est également installé dans le GAC, pour automatiser l’application InfoPath à partir d’applications externes qui utilisent du code managé. Pour plus d’informations sur l’assembly Microsoft.Office.Interop.InfoPath.Xml, consultez [À propos de l’assembly InfoPath XML Interop](about-the-infopath-xml-interop-assembly.md).
  
Si l’assembly Microsoft.Office.Interop.InfoPath n’est pas visible dans le GAC, vous devez confirmer qu’InfoPath a été installé correctement. Par défaut, l’option prise en charge de la **programmabilité .NET** dans le programme d’installation est définie sur **Exécuter à partir de Mon ordinateur** tant que le Kit de développement logiciel (SDK) .NET Framework 1.1 Redistributable 1.1 ou .NET Framework 1.1 ou une version ultérieure du .NET Framework est installé avant d’exécuter le programme d’installation. Si ces assemblys d’interopérabilité ne sont pas disponibles sur votre ordinateur, vous devez confirmer que .NET Framework 1.1 ou version ultérieure est installé, puis utiliser **les programmes et fonctionnalités** du **Panneau** de configuration pour modifier la configuration en définissant l’option **prise en charge de la programmabilité .NET** sous **Microsoft Office InfoPath** pour **exécuter à partir de mon ordinateur**.
  
Pour plus d’informations sur le téléchargement de .NET Framework 1.1 Redistributable, consultez [.NET Framework 1.1 Redistributable](/download/dotnet-framework).
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>Espace de noms Microsoft.Office.Interop.InfoPath

Bien que le processus d’écriture de code managé pour une tâche donnée soit très similaire à l’exécution de la même tâche à l’aide d’un langage tel que Visual Basic pour Applications ou JScript, le modèle objet exposé lors de l’affichage de l’espace de noms **Microsoft.Office.Interop.InfoPath** à partir de **l’Explorateur d’objets** dans Microsoft Visual Studio semble plus complexe. En effet, l’interopérabilité avec le .NET Framework nécessite un serveur COM pour exposer toutes ses interfaces publiques, ainsi que certaines constructions supplémentaires requises par le .NET Framework lui-même. Pour plus d’informations sur la façon dont et pourquoi le modèle objet exposé par un assembly d’interopérabilité semble plus complexe, consultez la section « Comment les objets COM sont exposés au code managé » de la rubrique [Modèles d’objets compatibles InfoPath 2003](../form-templates/infopath-2003-compatible-object-models.md) .
  
### <a name="using-intellisense"></a>Utilisation d'IntelliSense

Les exemples de cette section supposent que vous avez établi des références aux assemblys Microsoft.Office.Interop.InfoPath et Microsoft.Office.Interop.InfoPath.Xml. Pour plus d’informations sur la définition de références et d’autres exemples d’automatisation externe, consultez [Scénarios et exemples d’automatisation](external-automation-scenarios-and-examples.md) externe.
  
Avant de pouvoir utiliser la saisie semi-automatique de l’instruction Microsoft IntelliSense dans le code d’automatisation externe, vous devez créer une variable objet pour une instance de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , comme indiqué dans la ligne de code suivante.
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

Après avoir créé la variable d’objet, lorsque vous tapez le nom de la variable suivi d’un point, une liste déroulante s’affiche avec les membres de la classe **Application** à sélectionner.
  
Pour utiliser un formulaire InfoPath, déclarez une variable d’objet de type [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) , puis initialisez-la en ouvrant le formulaire à partir de la collection [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) de la variable d’objet **Application** , comme indiqué dans la ligne de code suivante.
  
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

La liste déroulante d’achèvement de l’instruction IntelliSense pour les membres de la classe **XDocument** s’affiche lorsque vous tapez le nom de la variable suivi d’un point.
  
Pour utiliser le contenu du document XML sous-jacent pour le formulaire à l’aide de Microsoft XML Core Services (MSXML), vous devez créer une variable de type [IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) , puis utiliser la propriété [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) de la classe **XDocument** pour affecter le modèle DOM (Document Object Model) XML du formulaire à cette variable.
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

La liste déroulante d’achèvement de l’instruction IntelliSense pour les membres de la classe **IXMLDOMDocument2** s’affiche lorsque vous tapez le nom de la variable suivi d’un point, ce qui vous permet d’utiliser MSXML pour travailler avec le document XML.
  
### <a name="using-the-class-library-reference-documentation"></a>Utilisation de la documentation de référence de la bibliothèque de classes

L’organisation de la documentation de référence de la bibliothèque de classes de l’espace de noms [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) reflète les relations entre les interfaces de coclasse et les interfaces héritées qu’elles implémentent.
  
Lorsque vous ouvrez une rubrique pour une interface de coclasse, telle que [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , le lien vers les membres de l’interface de coclasse suivant la description de l’interface au début de la rubrique affiche une rubrique vide. Pour afficher la liste des membres implémentés par l'interface de coclasse, vous devez ouvrir la rubrique de la dernière interface héritée par la coclasse, puis ouvrir la table de ses membres. Un lien vers l'interface héritée est proposé au début de la section Remarques de la rubrique consacrée à l'interface de coclasse.
  
Lorsque vous appuyez sur F1 dans l’éditeur Visual Studio Code, le comportement est similaire, sauf que le membre sur lequel vous tirez parti de l’aide F1 s’affiche directement, car vous travaillez généralement avec les membres d’une interface. Cependant, le fait qu'un membre puisse être implémenté depuis une interface avec version peut paraître confus la première fois que vous y êtes confronté. Par exemple, si vous tapez `myXDocument.UI.Alert` et placez le curseur et appuyez sur `Alert` F1, une rubrique intitulée « UI2. Méthode d’alerte » s’affiche. Ceci est dû au fait que la méthode **Alert** est une implémentation d'un membre de l'interface **UI2**.
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Transmission de paramètres facultatifs à des membres du modèle objet InfoPath

Si un membre de modèle objet InfoPath contient un paramètre facultatif et que vous ne spécifiez pas de valeur pour ce paramètre, vous devez transmettre le champ **Type.Missing** pour ce paramètre. Si vous ne transmettez pas le champ **Type.Missing** alors que la valeur est omise, cela provoque une erreur de compilation. Cela est vrai pour le code écrit en C# et Visual Basic. Par exemple, la méthode [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) de l’interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) inclut deux paramètres facultatifs : _varEndNode_ et _varViewContext_. Une ligne de code dans laquelle les valeurs de ces deux paramètres ne sont pas spécifiées doit ressembler aux exemples suivants.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>Voir aussi

- [Exemples et scénarios d’automatisation externe](external-automation-scenarios-and-examples.md)
