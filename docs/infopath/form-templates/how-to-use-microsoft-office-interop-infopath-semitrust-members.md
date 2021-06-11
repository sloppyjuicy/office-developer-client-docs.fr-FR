---
title: Utilisez Microsoft. Office.Interop.InfoPath.SemiTrust non compatibles avec InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modèles de formulaire compatibles infopath 2003, à l’aide des fonctionnalités infopath 2007
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: Modèle objet fourni par Microsoft. Office’espace de noms .Interop.InfoPath.SemiTrust inclut des objets et des membres qui fournissent de nouvelles fonctionnalités qui ont été ajoutées à Office InfoPath 2007 et InfoPath.
ms.openlocfilehash: 45f7607aec8ccfd653780a550df0823730835a86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415340"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a><span data-ttu-id="8520d-104">Utilisez Microsoft. Office.Interop.InfoPath.SemiTrust non compatibles avec InfoPath</span><span class="sxs-lookup"><span data-stu-id="8520d-104">Use Microsoft.Office.Interop.InfoPath.SemiTrust members not compatible with InfoPath</span></span>

<span data-ttu-id="8520d-105">Lorsque vous ajoutez du code à un modèle de formulaire créé avec la Shared Computer Toolkit infopath 2003 Microsoft Office ou créez un modèle de formulaire compatible avec le modèle objet compatible InfoPath 2003 (comme décrit dans Créer un modèle de formulaire à l’aide du modèle objet [InfoPath 2003),](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)par défaut, Microsoft InfoPath utilise un sous-ensemble des objets et des membres fournis par l’espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) qui sont identiques à ceux utilisés par InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="8520d-105">When you add code to a form template that was created with the Microsoft Office InfoPath 2003 Toolkit or create a new form template that works with the InfoPath 2003-compatible object model (as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), by default, Microsoft InfoPath will use a subset of the objects and members provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace that are identical to those used by InfoPath 2003.</span></span> <span data-ttu-id="8520d-106">Cela permet d'assurer la compatibilité avec InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="8520d-106">This is done to provide compatibility with InfoPath 2003.</span></span> <span data-ttu-id="8520d-107">Toutefois, le modèle objet fourni par l’espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) inclut des objets et des membres supplémentaires qui fournissent de nouvelles fonctionnalités ajoutées à Office InfoPath 2007 et InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8520d-107">However, the object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace includes additional objects and members that provide new functionality that was added to Office InfoPath 2007 and InfoPath.</span></span> 
  
<span data-ttu-id="8520d-108">Par exemple, les interfaces [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) et [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) fournissent de nouvelles fonctionnalités de gestion des droits d’information qui ne sont pas disponibles dans InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="8520d-108">For example, the [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) and [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) interfaces provide new information rights management functionality that is not available in InfoPath 2003.</span></span> <span data-ttu-id="8520d-109">Ces dernières, et d'autres objets entièrement nouveaux ajoutés à l'espace de noms Microsoft.Office.Interop.InfoPath.SemiTrust, ne sont pas disponibles par défaut lorsque vous ouvrez ou créez un modèle de formulaire avec code managé à l'aide du modèle objet compatible InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="8520d-109">This, and other new objects added to the Microsoft.Office.Interop.InfoPath.SemiTrust namespace are not available by default when you open or create managed code form template with InfoPath 2003-compatible object model.</span></span> 
  
<span data-ttu-id="8520d-110">De même, l’interface [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) fournit les mêmes fonctionnalités qu’InfoPath 2003 ; [L’interface _XDocument3 a](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) été modifiée pour inclure des propriétés et des méthodes supplémentaires qui ont été ajoutées dans Office InfoPath 2007, et la _XDocument4 [a](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) été modifiée pour inclure des propriétés et des méthodes supplémentaires qui ont été ajoutées dans InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8520d-110">Similarly, while the [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) interface provides the same functionality as InfoPath 2003; the [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) interface has been versioned to include additional properties and methods that were added in Office InfoPath 2007, and the [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) has been versioned to include additional properties and methods that were added in InfoPath.</span></span> 
  
<span data-ttu-id="8520d-111">Si vous souhaitez utiliser des objets et des membres ajoutés dans Office InfoPath 2007 ou InfoPath dans un projet de modèle de formulaire créé à l’aide du modèle objet fourni par l’espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust,** vous pouvez le faire, mais le code qui utilise ces membres ne sera pas compatible avec InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="8520d-111">If you want to use objects and members that were added in Office InfoPath 2007 or InfoPath in a form template project created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you can do so, but code that uses these members will not be compatible with InfoPath 2003.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8520d-112">Tous les modèles de formulaires avec une logique métier créée à l’aide du modèle objet fourni par l’espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust,** qu’ils utilisent des objets et des membres compatibles avec InfoPath ou non, ne sont pas pris en charge pour les modèles de formulaire activés pour le navigateur déployés sur Microsoft SharePoint Server 2010 avec InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="8520d-112">All form templates with business logic created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, whether they use objects and members compatible with InfoPath or not, are not supported for browser-enabled form templates deployed to Microsoft SharePoint Server 2010 with InfoPath Forms Services.</span></span> <span data-ttu-id="8520d-113">La logique métier pour les modèles de formulaire activés pour le navigateur doit utiliser le nouveau modèle objet InfoPath avec code géré fourni par [Microsoft.Office. Espace de noms InfoPath.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx)</span><span class="sxs-lookup"><span data-stu-id="8520d-113">Business logic for browser-enabled form templates must use the new InfoPath managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8520d-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="8520d-114">Example</span></span>

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a><span data-ttu-id="8520d-115">Création d'une variable objet XDocument ou Application pour accéder aux nouveaux membres du modèle objet</span><span class="sxs-lookup"><span data-stu-id="8520d-115">Creating an XDocument or Application Object Variable to Access New Object Model Members</span></span>

<span data-ttu-id="8520d-116">Pour accéder aux nouveaux objets et membres qui sont disponibles dans l'espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust**, vous devez déclarer et forcer la conversion des variables objet dans la version correcte de l'interface qui implémente ces membres.</span><span class="sxs-lookup"><span data-stu-id="8520d-116">To access the new objects and members that are available in the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you must declare and cast object variables to the correct version of the interface that implements these members.</span></span> <span data-ttu-id="8520d-117">Par défaut, les variables et les variables accèdent aux `thisXDocument` `thisApplication` versions  compatibles [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) InfoPath 2003 des interfaces _XDocument2 et _Application2 correspondantes.</span><span class="sxs-lookup"><span data-stu-id="8520d-117">By default, the  `thisXDocument` and  `thisApplication` variables access the InfoPath 2003-compatible versions of the corresponding **_XDocument2** and [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) interfaces.</span></span> <span data-ttu-id="8520d-118">Pour accéder aux interfaces **_XDocument3** et [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) qui permettent d’accéder aux nouvelles fonctionnalités, vous devez déclarer une variable objet du type **_XDocument3** ou **_Application3,** puis caster l’objet renvoyé par la ou la variable au même type que dans les exemples `thisXDocument` suivants. `thisApplication`</span><span class="sxs-lookup"><span data-stu-id="8520d-118">To access the **_XDocument3** and [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) interfaces that provide access to new functionality, you must declare an object variable of the **_XDocument3** or **_Application3** type, and then cast the object returned by the  `thisXDocument` or  `thisApplication` variable to the same type as shown in the following examples.</span></span> 
  
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

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a><span data-ttu-id="8520d-119">Accès à un nouvel objet à partir de la variable objet XDocument ou Application au moyen d'une propriété d'accès</span><span class="sxs-lookup"><span data-stu-id="8520d-119">Accessing a New Object From The XDocument or Application Object Variable Using an Accessor Property</span></span>

<span data-ttu-id="8520d-120">Une fois que vous avez créé une variable du type _ **XDocument3** ou **_Application3** version ultérieure, vous pouvez l’utiliser pour accéder à un objet ou un membre qui fournit de nouvelles fonctionnalités InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8520d-120">After you have created a variable of the later version _ **XDocument3** or **_Application3** type, you can use it to access an object or member that provides new InfoPath functionality.</span></span> 
  
<span data-ttu-id="8520d-121">L’exemple suivant montre comment utiliser une variable objet de type _ **XDocument3** avec la propriété d’accesseur [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) pour accéder à la nouvelle interface **Permission** et à sa propriété [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) pour déterminer si les paramètres d’autorisation sont activés pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="8520d-121">The following example shows how to use an object variable of type _ **XDocument3** with the [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) accessor property to access the new **Permission** interface and its [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) property to determine if permission settings are enabled for the form.</span></span> 
  
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

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a><span data-ttu-id="8520d-122">Accès à un objet avec version et conversion forcée au type avec version</span><span class="sxs-lookup"><span data-stu-id="8520d-122">Accessing a Versioned Object and Casting to the Versioned Type</span></span>

<span data-ttu-id="8520d-123">Si un objet qui existait dans le modèle objet InfoPath 2003 comporte de nouvelles propriétés et méthodes qui lui ont été ajoutées, l'objet qui implémente ces nouveaux membres présentera un nom avec version.</span><span class="sxs-lookup"><span data-stu-id="8520d-123">If an object that existed in the InfoPath 2003 object model has new properties or methods added to it, the object that implements those new members will have a name that is versioned.</span></span>
  
<span data-ttu-id="8520d-124">Par exemple, l’objet [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) ne fournit pas l’accès à deux nouvelles propriétés qui sont uniquement disponibles lors de l’utilisation de l’objet [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) avec version : les propriétés [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) et [HideName.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx)</span><span class="sxs-lookup"><span data-stu-id="8520d-124">For example, the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) object does not provide access to two new properties that are only available when using the versioned [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) object: the [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) and [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) properties.</span></span> 
  
<span data-ttu-id="8520d-125">Pour accéder à ces propriétés, vous devez déclarer une variable objet de type **ViewInfo2** et caster l’objet renvoyé par la propriété [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) de la variable d’objet _ **XDocument3** au type **ViewInfo2,** comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="8520d-125">To access these properties, you must declare an object variable of type **ViewInfo2** and cast the object returned by the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) property of the _ **XDocument3** object variable to the **ViewInfo2** type as shown in the following example.</span></span> 
  
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


