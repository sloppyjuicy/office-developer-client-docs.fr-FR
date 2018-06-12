---
title: Utilisation des membres Microsoft.Office.Interop.InfoPath.SemiTrust non compatibles avec InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, using infopath 2007 features
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: Le modèle d’objet fourni par l’espace de noms Microsoft.Office.Interop.InfoPath.SemiTrust inclut des objets et des membres qui fournissent de nouvelles fonctionnalités qui a été ajoutée à Office InfoPath 2007 et InfoPath.
ms.openlocfilehash: 3d0e9b450dab6a821af1f698d9859b21e85abf81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782369"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a>Utilisation des membres Microsoft.Office.Interop.InfoPath.SemiTrust non compatibles avec InfoPath

Lorsque vous ajoutez du code pour un modèle de formulaire qui a été créé avec Microsoft Office InfoPath 2003 Toolkit ou créez un nouveau modèle de formulaire qui fonctionne avec le modèle d’objet compatible InfoPath 2003 (tel que décrit dans [créer un modèle de formulaire à l’aide de l’objet 2003 InfoPath Modèle](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), par défaut, Microsoft InfoPath utilise un sous-ensemble des objets et membres fournis par l’espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) que sont identiques à ceux utilisés par InfoPath 2003. Cela permet d'assurer la compatibilité avec InfoPath 2003. Toutefois, le modèle objet fourni par l'espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) inclut des objets et des membres supplémentaires fournissant des nouvelles fonctionnalités qui ont été ajoutées à Office InfoPath 2007 et InfoPath. 
  
Par exemple, les interfaces [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) et [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) fournissent des fonctionnalités de gestion des droits relatifs à l'information entièrement nouvelles qui ne sont pas disponibles dans InfoPath 2003. Ces dernières, et d'autres objets entièrement nouveaux ajoutés à l'espace de noms Microsoft.Office.Interop.InfoPath.SemiTrust, ne sont pas disponibles par défaut lorsque vous ouvrez ou créez un modèle de formulaire avec code managé à l'aide du modèle objet compatible InfoPath 2003. 
  
De la même manière, alors que l'interface [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) offre les mêmes fonctionnalités qu'InfoPath 2003, une nouvelle version de l'interface [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) a été conçue pour inclure les propriétés et méthodes supplémentaires qui ont été ajoutées à Office InfoPath 2007, et une nouvelle version de l'interface [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) a été conçue pour inclure les propriétés et méthodes supplémentaires qui ont été ajoutées à InfoPath. 
  
Si vous voulez utiliser des objets et des membres qui ont été ajoutés à Office InfoPath 2007 ou InfoPath dans un projet de modèle de formulaire créé au moyen du modèle objet fourni par l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust**, vous pouvez le faire mais le code qui utilise ces membres ne sera pas compatible avec InfoPath 2003. 
  
> [!NOTE]
> [!REMARQUE] Tous les modèles de formulaires avec logique métier créés au moyen du modèle objet fourni par l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust**, qu'ils utilisent ou non des objets et des membres compatibles avec InfoPath, ne sont pas pris en charge par les modèles de formulaires activés pour le navigateur qui sont déployés sur Microsoft SharePoint Server 2010 avec InfoPath Forms Services. La logique métier pour les modèles de formulaires activés pour le navigateur doit utiliser le nouveau modèle objet InfoPath avec code managé fourni par l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . 
  
## <a name="example"></a>Exemple

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a>Création d'une variable objet XDocument ou Application pour accéder aux nouveaux membres du modèle objet

Pour accéder aux nouveaux objets et membres qui sont disponibles dans l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust**, vous devez déclarer et forcer la conversion des variables objet dans la version correcte de l'interface qui implémente ces membres. Par défaut, les variables  `thisXDocument` et  `thisApplication` accèdent aux versions compatibles InfoPath 2003 des interfaces **_XDocument2** et [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) correspondantes. Pour accéder aux interfaces **_XDocument3** et [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) qui fournissent accès aux nouvelles fonctionnalités, vous devez déclarer une variable objet du type **_XDocument3** ou **_Application3**, puis forcer la conversion de l'objet renvoyé par la variable  `thisXDocument` ou  `thisApplication` vers le même type que celui indiqué dans les exemples suivants. 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
```

```cs
// Declare an object variable of type _Application3 and
// cast the object returned by the thisApplication variable to
// the same type.
_Application3 thisApplication3 = (_Application3)thisXDocument;
```

```vb
' Declare an object variable of type _Application3 and
' cast the object returned by the thisXApplication variable to
' the same type.
Dim thisDocument As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
```

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a>Accès à un nouvel objet à partir de la variable objet XDocument ou Application au moyen d'une propriété d'accès

Après avoir créé une variable du type _ **XDocument3** ou **_Application3** de la dernière version, vous pouvez l'utiliser pour accéder à un objet ou un membre qui fournit de nouvelles fonctionnalités InfoPath. 
  
L'exemple suivant illustre comment utiliser la variable objet de type _ **XDocument3** avec la propriété d'accès [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) pour accéder à la nouvelle interface **Permission** et sa propriété [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) pour déterminer si les paramètres d'autorisation sont activés pour le formulaire. 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
// Use the object variable to access the later version object and
// property.
thisXDocument.UI.Alert(thisDocument3.Permission.Enabled.ToString());
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
' Use the object variable to access the later version object and
' property.
thisXDocument.UI.Alert(thisDocument3.Permission.Enabled.ToString())
```

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a>Accès à un objet avec version et conversion forcée au type avec version

Si un objet qui existait dans le modèle objet InfoPath 2003 comporte de nouvelles propriétés et méthodes qui lui ont été ajoutées, l'objet qui implémente ces nouveaux membres présentera un nom avec version.
  
Par exemple, l'objet [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) ne fournit pas accès aux deux nouvelles propriétés qui sont uniquement disponibles lors de l'utilisation de l'objet [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) avec version, à savoir les propriétés [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) et [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) . 
  
Pour accéder à ces propriétés, vous devez déclarer une variable objet de type **ViewInfo2** et forcer la conversion de l'objet renvoyé par la propriété [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) de la variable objet _ **XDocument3** dans le type **ViewInfo2** comme illustré dans l'exemple suivant. 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
// Declare an object variable of type ViewInfo2 and cast the object 
// returned by the ViewInfos property to that type.
ViewInfo2 thisView = (ViewInfo2)thisXDocument3.ViewInfos["View2"];
// Display the value of the new HideName property.
thisXDocument3.UI.Alert(thisView.HideName.ToString());
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
' Declare an object variable of type ViewInfo2 and cast the object 
' returned by the ViewInfos property to that type.
Dim thisView As ViewInfo2 = _
   DirectCast(thisXDocument3.ViewInfos("View2"), ViewInfo2)
' Display the value of the new HideName property.
thisXDocument3.UI.Alert(thisView.HideName.ToString())
```


