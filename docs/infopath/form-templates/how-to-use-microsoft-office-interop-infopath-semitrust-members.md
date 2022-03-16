---
title: Utilisez Microsoft. Office. Membres Interop.InfoPath.SemiTrust non compatibles avec InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modèles de formulaire compatibles infopath 2003, à l’aide des fonctionnalités infopath 2007
ms.localizationpriority: medium
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: Modèle objet fourni par Microsoft. Office. L’espace de noms Interop.InfoPath.SemiTrust inclut des objets et des membres qui fournissent de nouvelles fonctionnalités qui ont été ajoutées à Office InfoPath 2007 et InfoPath.
ms.openlocfilehash: d0da9d07d98ecddc008e7b7e1bd886c06d623ac2
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506322"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a>Utilisez Microsoft. Office. Membres Interop.InfoPath.SemiTrust non compatibles avec InfoPath

Lorsque vous ajoutez du code à un modèle de formulaire créé avec la Shared Computer Toolkit Microsoft Office InfoPath 2003 ou créez un modèle de formulaire compatible avec le modèle objet compatible InfoPath 2003 (comme décrit dans Créer un modèle de formulaire à l’aide du modèle objet [InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), Microsoft InfoPath utilise par défaut un sous-ensemble des objets et des membres fournis par [Microsoft. Office. Espace de noms Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) identique à celui utilisé par InfoPath 2003. Cela permet d'assurer la compatibilité avec InfoPath 2003. Toutefois, le modèle objet fourni par [Microsoft.Office. L’espace de noms Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) inclut des objets et des membres supplémentaires qui fournissent de nouvelles fonctionnalités qui ont été ajoutées à Office InfoPath 2007 et InfoPath.
  
Par exemple, les interfaces [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) et [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) fournissent de nouvelles fonctionnalités de gestion des droits d’information qui ne sont pas disponibles dans InfoPath 2003. Ces dernières, et d'autres objets entièrement nouveaux ajoutés à l'espace de noms Microsoft.Office.Interop.InfoPath.SemiTrust, ne sont pas disponibles par défaut lorsque vous ouvrez ou créez un modèle de formulaire avec code managé à l'aide du modèle objet compatible InfoPath 2003.
  
De même, l’interface [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) fournit les mêmes fonctionnalités qu’InfoPath 2003 ; [L’interface _XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) a été modifiée pour inclure des propriétés et des méthodes supplémentaires qui ont été ajoutées dans Office InfoPath 2007, et la [_XDocument4 a](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) été modifiée pour inclure des propriétés et des méthodes supplémentaires qui ont été ajoutées dans InfoPath.
  
Si vous souhaitez utiliser des objets et des membres ajoutés dans Office InfoPath 2007 ou InfoPath dans un projet de modèle de formulaire créé à l’aide du modèle objet fourni par **Microsoft.Office. Espace de noms Interop.InfoPath.SemiTrust**, vous pouvez le faire, mais le code qui utilise ces membres ne sera pas compatible avec InfoPath 2003.
  
> [!NOTE]
> Tous les modèles de formulaires avec une logique métier créée à l’aide du modèle objet fourni par **Microsoft.Office. L’espace de noms Interop.InfoPath.SemiTrust**, qu’il utilise des objets et des membres compatibles avec InfoPath ou non, n’est pas pris en charge pour les modèles de formulaires activés pour le navigateur déployés sur Microsoft SharePoint Server 2010 avec InfoPath Forms Services. La logique métier des modèles de formulaires activés pour le navigateur doit utiliser le nouveau modèle objet InfoPath avec code géré fourni par [Microsoft.Office. Espace de noms InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx).
  
## <a name="example"></a>Exemple

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a>Création d'une variable objet XDocument ou Application pour accéder aux nouveaux membres du modèle objet

Pour accéder aux nouveaux objets et membres qui sont disponibles dans l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust**, vous devez déclarer et forcer la conversion des variables objet dans la version correcte de l'interface qui implémente ces membres. Par défaut, les `thisXDocument` `thisApplication` variables et les variables accèdent aux versions compatibles InfoPath 2003 [des interfaces](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) _XDocument2 et _Application2 correspondantes. Pour accéder aux interfaces **_XDocument3** et [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) qui permettent d’accéder aux nouvelles fonctionnalités, vous devez déclarer une variable objet du type **_XDocument3** ou **_Application3** ,  `thisXDocument`  `thisApplication` puis caster l’objet renvoyé par la ou la variable au même type que dans les exemples suivants.
  
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

Une fois que vous avez créé une variable du type **_XDocument3** ou _ **_Application3** version ultérieure, vous pouvez l’utiliser pour accéder à un objet ou un membre qui fournit de nouvelles fonctionnalités InfoPath.
  
L’exemple suivant montre comment utiliser une variable objet de type **_XDocument3** avec la propriété [d’accesseur Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) pour accéder à la nouvelle interface **Permission** et à sa propriété [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) pour déterminer si les paramètres d’autorisation sont activés pour le formulaire.
  
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
  
Par exemple, l’objet [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) ne fournit pas l’accès à deux nouvelles propriétés qui sont uniquement disponibles lors de l’utilisation de l’objet [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) avec version : les propriétés [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) et [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) .
  
Pour accéder à ces propriétés, vous devez déclarer une variable objet de type **ViewInfo2** et caster l’objet renvoyé par la propriété [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) de la variable objet **_XDocument3** au type **ViewInfo2** , comme illustré dans l’exemple suivant.
  
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
