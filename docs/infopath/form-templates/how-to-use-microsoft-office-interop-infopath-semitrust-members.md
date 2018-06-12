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
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a><span data-ttu-id="50be9-104">Utilisation des membres Microsoft.Office.Interop.InfoPath.SemiTrust non compatibles avec InfoPath</span><span class="sxs-lookup"><span data-stu-id="50be9-104">Use Microsoft.Office.Interop.InfoPath.SemiTrust members not compatible with InfoPath</span></span>

<span data-ttu-id="50be9-105">Lorsque vous ajoutez du code pour un modèle de formulaire qui a été créé avec Microsoft Office InfoPath 2003 Toolkit ou créez un nouveau modèle de formulaire qui fonctionne avec le modèle d’objet compatible InfoPath 2003 (tel que décrit dans [créer un modèle de formulaire à l’aide de l’objet 2003 InfoPath Modèle](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), par défaut, Microsoft InfoPath utilise un sous-ensemble des objets et membres fournis par l’espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) que sont identiques à ceux utilisés par InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="50be9-105">When you add code to a form template that was created with the Microsoft Office InfoPath 2003 Toolkit or create a new form template that works with the InfoPath 2003-compatible object model (as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), by default, Microsoft InfoPath will use a subset of the objects and members provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace that are identical to those used by InfoPath 2003.</span></span> <span data-ttu-id="50be9-106">Cela permet d'assurer la compatibilité avec InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="50be9-106">This is done to provide compatibility with InfoPath 2003.</span></span> <span data-ttu-id="50be9-107">Toutefois, le modèle objet fourni par l'espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) inclut des objets et des membres supplémentaires fournissant des nouvelles fonctionnalités qui ont été ajoutées à Office InfoPath 2007 et InfoPath.</span><span class="sxs-lookup"><span data-stu-id="50be9-107">However, the object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace includes additional objects and members that provide new functionality that was added to Office InfoPath 2007 and InfoPath.</span></span> 
  
<span data-ttu-id="50be9-p102">Par exemple, les interfaces [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) et [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) fournissent des fonctionnalités de gestion des droits relatifs à l'information entièrement nouvelles qui ne sont pas disponibles dans InfoPath 2003. Ces dernières, et d'autres objets entièrement nouveaux ajoutés à l'espace de noms Microsoft.Office.Interop.InfoPath.SemiTrust, ne sont pas disponibles par défaut lorsque vous ouvrez ou créez un modèle de formulaire avec code managé à l'aide du modèle objet compatible InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="50be9-p102">For example, the [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) and [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) interfaces provide new information rights management functionality that is not available in InfoPath 2003. This, and other new objects added to the Microsoft.Office.Interop.InfoPath.SemiTrust namespace are not available by default when you open or create managed code form template with InfoPath 2003-compatible object model.</span></span> 
  
<span data-ttu-id="50be9-110">De la même manière, alors que l'interface [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) offre les mêmes fonctionnalités qu'InfoPath 2003, une nouvelle version de l'interface [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) a été conçue pour inclure les propriétés et méthodes supplémentaires qui ont été ajoutées à Office InfoPath 2007, et une nouvelle version de l'interface [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) a été conçue pour inclure les propriétés et méthodes supplémentaires qui ont été ajoutées à InfoPath.</span><span class="sxs-lookup"><span data-stu-id="50be9-110">Similarly, while the [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) interface provides the same functionality as InfoPath 2003; the [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) interface has been versioned to include additional properties and methods that were added in Office InfoPath 2007, and the [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) has been versioned to include additional properties and methods that were added in InfoPath.</span></span> 
  
<span data-ttu-id="50be9-111">Si vous voulez utiliser des objets et des membres qui ont été ajoutés à Office InfoPath 2007 ou InfoPath dans un projet de modèle de formulaire créé au moyen du modèle objet fourni par l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust**, vous pouvez le faire mais le code qui utilise ces membres ne sera pas compatible avec InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="50be9-111">If you want to use objects and members that were added in Office InfoPath 2007 or InfoPath in a form template project created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you can do so, but code that uses these members will not be compatible with InfoPath 2003.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="50be9-p103">[!REMARQUE] Tous les modèles de formulaires avec logique métier créés au moyen du modèle objet fourni par l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust**, qu'ils utilisent ou non des objets et des membres compatibles avec InfoPath, ne sont pas pris en charge par les modèles de formulaires activés pour le navigateur qui sont déployés sur Microsoft SharePoint Server 2010 avec InfoPath Forms Services. La logique métier pour les modèles de formulaires activés pour le navigateur doit utiliser le nouveau modèle objet InfoPath avec code managé fourni par l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) .</span><span class="sxs-lookup"><span data-stu-id="50be9-p103">All form templates with business logic created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, whether they use objects and members compatible with InfoPath or not, are not supported for browser-enabled form templates deployed to Microsoft SharePoint Server 2010 with InfoPath Forms Services. Business logic for browser-enabled form templates must use the new InfoPath managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
## <a name="example"></a><span data-ttu-id="50be9-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="50be9-114">Example</span></span>

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a><span data-ttu-id="50be9-115">Création d'une variable objet XDocument ou Application pour accéder aux nouveaux membres du modèle objet</span><span class="sxs-lookup"><span data-stu-id="50be9-115">Creating an XDocument or Application Object Variable to Access New Object Model Members</span></span>

<span data-ttu-id="50be9-p104">Pour accéder aux nouveaux objets et membres qui sont disponibles dans l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust**, vous devez déclarer et forcer la conversion des variables objet dans la version correcte de l'interface qui implémente ces membres. Par défaut, les variables  `thisXDocument` et  `thisApplication` accèdent aux versions compatibles InfoPath 2003 des interfaces **_XDocument2** et [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) correspondantes. Pour accéder aux interfaces **_XDocument3** et [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) qui fournissent accès aux nouvelles fonctionnalités, vous devez déclarer une variable objet du type **_XDocument3** ou **_Application3**, puis forcer la conversion de l'objet renvoyé par la variable  `thisXDocument` ou  `thisApplication` vers le même type que celui indiqué dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="50be9-p104">To access the new objects and members that are available in the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you must declare and cast object variables to the correct version of the interface that implements these members. By default, the  `thisXDocument` and  `thisApplication` variables access the InfoPath 2003-compatible versions of the corresponding **_XDocument2** and [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) interfaces. To access the **_XDocument3** and [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) interfaces that provide access to new functionality, you must declare an object variable of the **_XDocument3** or **_Application3** type, and then cast the object returned by the  `thisXDocument` or  `thisApplication` variable to the same type as shown in the following examples.</span></span> 
  
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

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a><span data-ttu-id="50be9-119">Accès à un nouvel objet à partir de la variable objet XDocument ou Application au moyen d'une propriété d'accès</span><span class="sxs-lookup"><span data-stu-id="50be9-119">Accessing a New Object From The XDocument or Application Object Variable Using an Accessor Property</span></span>

<span data-ttu-id="50be9-120">Après avoir créé une variable du type _ **XDocument3** ou **_Application3** de la dernière version, vous pouvez l'utiliser pour accéder à un objet ou un membre qui fournit de nouvelles fonctionnalités InfoPath.</span><span class="sxs-lookup"><span data-stu-id="50be9-120">After you have created a variable of the later version _ **XDocument3** or **_Application3** type, you can use it to access an object or member that provides new InfoPath functionality.</span></span> 
  
<span data-ttu-id="50be9-121">L'exemple suivant illustre comment utiliser la variable objet de type _ **XDocument3** avec la propriété d'accès [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) pour accéder à la nouvelle interface **Permission** et sa propriété [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) pour déterminer si les paramètres d'autorisation sont activés pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="50be9-121">The following example shows how to use an object variable of type _ **XDocument3** with the [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) accessor property to access the new **Permission** interface and its [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) property to determine if permission settings are enabled for the form.</span></span> 
  
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

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a><span data-ttu-id="50be9-122">Accès à un objet avec version et conversion forcée au type avec version</span><span class="sxs-lookup"><span data-stu-id="50be9-122">Accessing a Versioned Object and Casting to the Versioned Type</span></span>

<span data-ttu-id="50be9-123">Si un objet qui existait dans le modèle objet InfoPath 2003 comporte de nouvelles propriétés et méthodes qui lui ont été ajoutées, l'objet qui implémente ces nouveaux membres présentera un nom avec version.</span><span class="sxs-lookup"><span data-stu-id="50be9-123">If an object that existed in the InfoPath 2003 object model has new properties or methods added to it, the object that implements those new members will have a name that is versioned.</span></span>
  
<span data-ttu-id="50be9-124">Par exemple, l'objet [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) ne fournit pas accès aux deux nouvelles propriétés qui sont uniquement disponibles lors de l'utilisation de l'objet [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) avec version, à savoir les propriétés [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) et [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) .</span><span class="sxs-lookup"><span data-stu-id="50be9-124">For example, the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) object does not provide access to two new properties that are only available when using the versioned [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) object: the [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) and [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) properties.</span></span> 
  
<span data-ttu-id="50be9-125">Pour accéder à ces propriétés, vous devez déclarer une variable objet de type **ViewInfo2** et forcer la conversion de l'objet renvoyé par la propriété [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) de la variable objet _ **XDocument3** dans le type **ViewInfo2** comme illustré dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="50be9-125">To access these properties, you must declare an object variable of type **ViewInfo2** and cast the object returned by the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) property of the _ **XDocument3** object variable to the **ViewInfo2** type as shown in the following example.</span></span> 
  
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


