---
title: Modèles objet compatibles avec InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, object model,InfoPath 2003-compatible object model,object models [InfoPath 2003], compatible with InfoPath 2007,object models [InfoPath 2007], InfoPath 2003 compatible
ms.localizationpriority: medium
ms.assetid: e4511af6-d7e7-44ad-a50d-1b7ee04f8215
description: Microsoft InfoPath est conçu comme une application COM (Component Object Model) et offre l'accès à ses interfaces de programmation à la fois pour l'automatisation externe et pour les scripts utilisés depuis des modèles de formulaires comme interfaces COM.
ms.openlocfilehash: 5037b18645d892b0506aaba101c7f7f719290154
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381676"
---
# <a name="infopath-2003-compatible-object-models"></a>Modèles objet compatibles avec InfoPath 2003

Microsoft InfoPath est conçu comme une application COM (Component Object Model) et offre l'accès à ses interfaces de programmation à la fois pour l'automatisation externe et pour les scripts utilisés depuis des modèles de formulaires comme interfaces COM. Pour permettre la création de solutions InfoPath qui utilisent les langages de code managé de Visual C# et Visual Basic, le programme d'installation d'InfoPath installe trois assemblys d'interopérabilité. Les assemblys d'interopérabilité sont des assemblys .NET qui font office de lien entre le code managé et le code non managé et mappent les membres des objets COM avec les membres managés .NET équivalents.
  
Les fichiers des trois assemblys d'interopérabilité installés par InfoPath sont les suivants :
  
- Microsoft.Office.Interop.InfoPath.dll
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
- Microsoft.Office.Interop.InfoPath.Xml.dll

Cette rubrique présente le modèle objet exposé dans l'assembly d'interopérabilité Microsoft.Office.Interop.InfoPath.SemiTrust, utilisé exclusivement pour la création et l'exécution d'une logique métier avec code managé depuis les modèles de formulaires InfoPath (.xsn).
  
Pour plus d’informations sur Microsoft. Office. Interop.InfoPath et Microsoft.Office.Interop.InfoPath.Xml assemblys, consultez la documentation de [Microsoft.Office. Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) et [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) espaces de noms.
  
## <a name="important-installation-information"></a>Informations d’installation importantes

Par défaut, l'option **Installation par défaut** du programme d'installation d'InfoPath installe des copies des assemblys Microsoft.Office.Interop.InfoPath.SemiTrust et Microsoft.Office.Interop.InfoPath.Xml dans le dossier C:\Program Files\Microsoft Office\Office14. Les assemblys Microsoft.Office.Interop.InfoPath et Microsoft.Office.Interop.InfoPath.Xml sont également installés dans le Global Assembly Cache (GAC) dont vous pouvez consulter le contenu dans le dossier C:\Windows\Assembly.
  
Si ces assemblys ne sont pas installés, vérifiez que Microsoft InfoPath a été correctement installé. Si .NET Framework 2.0 ou ultérieur est installé avant le démarrage du programme d'installation, l'option **Prise en charge de la programmabilité .NET** du programme d'installation d'InfoPath est définie sur **Exécuter à partir du disque dur** pour une **Installation par défaut** d'InfoPath. Si ces assemblys d'interopérabilité ne sont pas disponibles sur votre ordinateur, vérifiez que .NET Framework 2.0 ou ultérieur est installé, puis exécutez **Ajout/Suppression de programmes** depuis le **Panneau de configuration** et définissez l'option **Prise en charge de la programmabilité .NET** sur **Exécuter à partir du disque dur**.
  
Pour plus d’informations sur le téléchargement .NET Framework redistribuable 2.0, voir [.NET Framework 2.0 Redistributable.](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=0856eacb-4362-4b0d-8edd-aab15c5e04f5)
  
## <a name="the-microsoftofficeinteropinfopathsemitrust-namespace"></a>The Microsoft. Office. Espace de noms Interop.InfoPath.SemiTrust

Avant la sortie de Microsoft Office InfoPath 2003 Service Pack 1 et du kit de ressources Microsoft Office InfoPath 2003 pour Visual Studio® .NET, toute la logique de programmation pour les modèles de formulaires InfoPath était créée à l'aide de Microsoft JScript ou Microsoft VBScript écrit dans l'environnement de développement Microsoft Script Editor (MSE). Les scripts créés dans MSE sont interprétés à l'exécution et accèdent au modèle objet COM de la bibliothèque de liens dynamiques IPEDITOR.dll .
  
Pour prendre en charge la création de modèles de formulaires qui utilisent des langages avec code managé tels que Visual C# et Visual Basic pour la logique de programmation, une fonctionnalité a été ajoutée pour permettre à InfoPath d'accueillir le CLR (Common Language Runtime) et l'assembly d'interopérabilité Microsoft.Office.Interop.InfoPath.SemiTrust a été créé pour permettre au code managé d'interagir de manière sécurisée avec le modèle objet COM d'InfoPath. Pour plus d’informations sur le modèle de sécurité qui s’applique aux modèles de formulaire InfoPath avec code géré, voir À propos du modèle de sécurité pour les [modèles de formulaires avec code](about-the-security-model-for-form-templates-with-code.md).
  
Bien que le processus de création de code managé pour une tâche donnée dans un modèle de formulaire InfoPath reste très similaire à la tâche de programmation équivalente avec un script, le modèle objet compatible InfoPath 2003 exposé lors de l'affichage de l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust** dans l' **Explorateur d'objets** de Visual Studio 2012 paraît plus complexe. Ceci est dû au fait que la technologie d'interopérabilité .NET Framework utilisée pour prendre en charge le modèle objet compatible InfoPath 2003 nécessite un serveur COM pour exposer toutes ses interfaces publiques, ainsi que quelques constructions supplémentaires requises par .NET Framework.
  
### <a name="how-com-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>Comment les objets COM sont exposés au modèle objet compatible InfoPath 2003

Lorsque vous travaillez avec un serveur COM depuis un langage évolué tel que JScript, VBScript ou Visual Basic (mais pas la version .NET de Visual Basic et Visual C#), le modèle objet exposé est plus simple que les classes et interfaces COM sous-jacentes. Par exemple, dans ce cas, l'objet InfoPath **UI** expose sept méthodes, dont la méthode **Alert** pour l'affichage d'une boîte de dialogue de message pour l'utilisateur.
  
Cependant, les constructions COM sous-jacentes de l'objet **UI** sont en réalité composées de trois entités : deux interfaces appelées **UI** et **UI2** et une coclasse COM qui implémente les membres de ces deux interfaces. Ces deux versions de l'interface **UI** sont présentes car l'interface COM requiert que la définition d'une interface reste la même pour maintenir la compatibilité descendante pour les programmes et composants qui appellent une implémentation de cette interface.
  
Dans ce cas **, l’interface** utilisateur, qui a été définie pour la version initiale d’InfoPath, fournit quatre méthodes, y compris la **méthode Alert** . **L’interface UI2** peut être considérée comme une deuxième version de **l’interface utilisateur** et elle a été définie pour la version InfoPath Service Pack 1. **L’interface UI2** hérite des quatre méthodes de **l’interface utilisateur** d’origine et ajoute trois nouvelles méthodes, telles que **la méthode Confirm**. Bien que vous pouvez écrire une ligne de code dans un script ou dans du code géré qui appelle la méthode **Confirm** `XDocument.UI.Confirm`à l’aide de , le code sous-jacent appelle en fait la méthode **Confirm** de l’interface **UI2** à partir de l’implémentation de cette méthode dans la coclasse COM.
  
Le modèle objet tel qu'il est exposé pour la création de script cache ces détails, mais l'assembly d'interopérabilité expose publiquement à la fois la coclasse et les deux interfaces. Pour le seul objet **UI** utilisé dans l'environnement de création de scripts MSE, l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust** expose les trois éléments suivants :
  
- Interface [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI.aspx)
- Interface [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx)
- Interface de coclasse [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)

Bien que ces trois interfaces soient exposées dans l' **Explorateur d'objets** et qu'elles se trouvent dans la documentation Bibliothèque de classes de l'espace de noms, vous travaillez uniquement avec l'interface de coclasse **UIObject**, qui implémente l'objet **UI**, et les membres de l'interface **UI2**, qui est la version actuelle de l'interface implémentée par l'interface de la coclasse **UIObject**. Pour accéder comme dans un script à l'interface de la coclasse **UIObject** depuis son objet parent [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , utilisez la propriété d'accès [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) . Mis à part quelques exceptions, ceci est le modèle de tous les objets de la version originale d'InfoPath qui ont été mis à jour lors de la sortie d'InfoPath Service Pack 1.
  
Alors que le modèle est pratiquement le même, la situation est légèrement plus simple pour les nouveaux objets qui ont été ajoutés avec la sortie d'InfoPath Service Pack 1, par exemple l'objet **Certificat**. Dans ce cas, vous ne devez vous préoccuper que de deux choses : l'interface de la coclasse [CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) et les membres de l'interface [Certificate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Certificate.aspx) , qui est l'interface la plus récente et la seule implémentée par l'interface de la coclasse **CertificateObject**. De plus, comme pour l'utilisation d'objets COM d'InfoPath depuis un script, la propriété [Certificate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Certificate.aspx) permet d'accéder à l'objet depuis son parent.
  
Ce même modèle s'applique aux interfaces des collections, excepté que « Collection » est ajouté au nom de l'interface de coclasse d'une collection au lieu de « Object ». Par exemple, l'interface de coclasse de la collection COM **DataAdapters** porte le nom [DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) et l'interface qu'elle implémente est l'interface [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdapters.aspx) . De la même manière, la propriété [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) de l'objet parent **XDocument** permet d'accéder à la collection.
  
Ce modèle présente trois exceptions. Le nom des interfaces de coclasse des objets COM **Application** et **XDocument** ne comporte pas la mention « Object ». Leur nom est identique à celui des objets COM correspondants : [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) et **XDocument**. En outre, les noms des interfaces implémentées par les interfaces de coclasse **Application** et **XDocument** sont précédés du caractère de soulignement (_) : [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) et [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx). La troisième exception est l'objet COM **DataObject**. L'interface de coclasse de cet objet porte le nom [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) , mais comme n'importe quel autre objet COM d'InfoPath, l'interface qu'il implémente est l'interface [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.aspx) .
  
### <a name="how-microsoft-xml-core-services-msxml-50-for-microsoft-office-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>Comment Microsoft XML Core Services® (MSXML) 5.0 pour les objets Microsoft Office sont exposés au modèle objet compatible InfoPath 2003

Un sous-ensemble des objets et membres du modèle objet fourni par les services MSXML (Microsoft XML Core Services), qui est également un serveur COM, sont incorporés dans les interfaces exposées par l'assembly d'interopérabilité Microsoft.Office.Interop.InfoPath.SemiTrust. La raison pour laquelle ceci est nécessaire est que certains des membres du modèle objet COM d'InfoPath s'appuient sur MSXML et doivent être en mesure d'accéder à ces membres de manière sécurisée. Les noms des interfaces de l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust** qui incorpore les objets et les membres du modèle objet MSXML sont les mêmes que ceux exposés par le serveur COM MSXML. Dans la plupart des cas, ces noms sont précédés de « IXMLDOM » car ils sont utilisés avec le modèle DOM XML. Par exemple, la propriété [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) de l'interface **XDocument**, qui est utilisée pour renvoyer une référence au document XML sous-jacent d'un formulaire, renvoie l'interface [IXMLDOMDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.IXMLDOMDocument.aspx) qui est incorporée dans l'assembly d'interopérabilité Microsoft.Office.Interop.InfoPath.SemiTrust. Vous pouvez appeler et utiliser les membres de l'interface **IXMLDOMDocument** pratiquement de la même manière que lorsque vous utilisez un script dans un modèle de formulaire sans code managé.
  
Pour plus d'informations sur l'utilisation des membres du modèle objet MSXML (Microsoft XML Core Services) pour Microsoft Office dans des modèles de formulaires avec code managé, voir [Utilisation de MSXML et de System.Xml avec le modèle objet InfoPath 2003](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md).
  
### <a name="using-intellisense"></a>Utilisation d'IntelliSense

Pour la plupart du code que vous écrivez sur le modèle objet compatible InfoPath 2003 dans un modèle de formulaire avec code géré, `thisXDocument` `thisApplication` vous utiliserez les variables initialisées `_Startup` dans la méthode du fichier de classe FormCode.cs ou FormCode.vb par défaut. Vous pouvez utiliser les `thisXDocument` variables et les `thisApplication` variables pour accéder aux membres des interfaces de coclasse [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) et [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . Après avoir tapé le nom d'une variable, suivi d'un point, la fonction IntelliSense de saisie semi-automatique des instructions affiche la liste des membres de l'interface de coclasse correspondante. Vous pouvez continuer ainsi pour accéder au membre du modèle objet avec lequel vous voulez travailler.
  
L’exemple suivant montre un exemple simple `thisXDocument` qui utilise la variable pour accéder à la méthode [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) afin d’afficher la version de l’application InfoPath à l’aide de la propriété [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) accessible à partir de la  `thisApplication` variable.
  
```cs
thisXDocument.UI.Alert(thisApplication.Version);
```

```vb
thisXDocument.UI.Alert(thisApplication.Version)
```

### <a name="using-the-class-library-reference-documentation"></a>Utilisation de la documentation de référence de la bibliothèque de classes

L'organisation de l'espace de noms dans la documentation de référence de la Bibliothèque de classes **Microsoft.Office.Interop.InfoPath.SemiTrust** reflète les relations entre les interfaces de coclasse et les interfaces héritées qu'elles implémentent, tel que décrit dans la section « Comment les objets COM sont exposés au code managé » plus haut dans cette rubrique.
  
Bien que l'organisation et l'affectation des noms de la documentation de référence de l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust** paraissent confuses de prime abord, les rubriques sont en réalité organisées de la même manière que dans la référence du modèle objet InfoPath dans le Guide de référence du développeur d'InfoPath, inclus dans InfoPath. À l'exception des rubriques relatives aux interfaces **Application** et **XDocument**, toutes les rubriques des interfaces de coclasse COM correspondent aux rubriques « Object » et « Collection » équivalentes dans la référence sur les scripts d'InfoPath. Par exemple, les rubriques « UIObject Interface » et « WindowsCollection Interface » de la documentation de référence de l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust** correspondent à un contenu similaire dans les rubriques « UI Object » et « Windows Collection » de la référence sur les scripts du modèle objet InfoPath.
  
Toutefois, le lien vers les membres de l'interface de coclasse qui suit la description de l'interface en début de rubrique aboutit à une rubrique vide. Pour afficher la liste des membres implémentés par l'interface de coclasse, vous devez ouvrir la rubrique de la dernière interface héritée par la coclasse, puis ouvrir la table de ses membres. Un lien vers l'interface héritée est proposé au début de la section Remarques de la rubrique consacrée à l'interface de coclasse.
  
Lorsque vous appuyez sur la touche F1 dans l'Éditeur de code, le comportement est similaire, excepté que le membre pour lequel vous invoquez l'aide est affiché directement car vous travaillez le plus souvent avec des membres d'une interface. Cependant, le fait qu'un membre puisse être implémenté depuis une interface avec version peut paraître confus la première fois que vous y êtes confronté. Par exemple, si vous tapez `thisXDocument.UI.Alert` et placez `Alert` le curseur sur F1 et appuyez sur F1, une rubrique intitulée « UI2. Alert Method » s’affiche. Ceci est dû au fait que la méthode **Alert** est une implémentation d'un membre de l'interface **UI2**.
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Passage de paramètres facultatifs aux membres du modèle objet InfoPath

Si un membre du modèle objet compatible InfoPath 2003 contient un paramètre facultatif et que vous ne spécifiez pas de valeur pour ce paramètre, vous devez transmettre le champ **Type.Missing** de ce paramètre. Si vous ne transmettez pas le champ **Type.Missing** alors que la valeur est omise, cela provoque une erreur de compilation. Ceci se produit aussi bien pour le code écrit en Visual C# qu'en Visual Basic. Par exemple, la méthode [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) de l'interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) comprend deux paramètres facultatifs :  _varEndNode_ et  _varViewContext_. Une ligne de code dans laquelle les valeurs de ces deux paramètres ne sont pas spécifiées doit ressembler aux exemples suivants.
  
```cs
IXMLDOMNode group1 = 
   thisXDocument.DOM.selectSingleNode("/my:myFields/my:group1");
thisXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
Dim group1 As IXMLDOMNode = _
   thisXDocument.DOM.selectSingleNode("/my:myFields/my:group1")
thisXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

### <a name="about-common-language-specification-compliance"></a>À propos de la conformité des spécifications linguistiques communes

En interne, l'attribut **CLSCompliant** de toutes les interfaces et tous les membres de l'assembly Microsoft.Office.Interop.InfoPath.SemiTrust est défini sur **false**. Du fait que la documentation de référence est générée en partie à l'aide de **System.Reflection**, la chaîne « Interface/méthode/propriété non conforme CLS » est ajoutée à la description de chaque interface et de chaque membre. Cependant, la plupart des interfaces et des membres de l'espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) sont en réalité conformes CLS.
  
## <a name="see-also"></a>Voir aussi

- [Tâches courantes en matière de développement de modèles de formulaires utilisant le modèle objet InfoPath 2003](common-tasks-for-developing-form-templates-using-infopath-object-model.md)
- [À propos du modèle de sécurité pour les modèles de formulaires avec code](about-the-security-model-for-form-templates-with-code.md)
- [Création de modèles de formulaires à l’aide du modèle objet InfoPath 2003](creating-form-templates-using-the-infopath-2003-object-model.md)
- [Présentation du modèle objet InfoPath 2003](understanding-the-infopath-2003-object-model.md)
