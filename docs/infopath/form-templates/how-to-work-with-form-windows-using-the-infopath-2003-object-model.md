---
title: Utiliser des formulaires Windows l’aide du modèle objet InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, form windows,form windows [InfoPath 2007], InfoPath 2003-compatible form templates
ms.localizationpriority: medium
ms.assetid: fbcf3a04-ee0f-40a6-8edd-583ae203e2e1
description: Lorsque vous programmez un formulaire InfoPath, vous pouvez écrire du code pour accéder aux fenêtres d'un formulaire, puis personnaliser certains des éléments qu'elles contiennent. Le modèle objet compatible InfoPath 2003 prend en charge l'accès aux fenêtres d'un formulaire grâce à l'utilisation de l'interface WindowObject en association avec l'interface WindowsCollection .
ms.openlocfilehash: b49007234d99edcf683e69fc94351e2bf4a5ffa2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557462"
---
# <a name="work-with-form-windows-using-the-infopath-2003-object-model"></a>Utiliser des formulaires Windows l’aide du modèle objet InfoPath 2003

Lorsque vous programmez un formulaire InfoPath, vous pouvez écrire du code pour accéder aux fenêtres d'un formulaire, puis personnaliser certains des éléments qu'elles contiennent. Le modèle objet compatible InfoPath 2003 prend en charge l'accès aux fenêtres d'un formulaire grâce à l'utilisation de l'interface [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) en association avec l'interface [WindowsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowsCollection.aspx) . 
  
Il existe deux types de fenêtres dans InfoPath :
  
- La fenêtre d'édition, qui est utilisée lorsqu'un utilisateur remplit un formulaire.
    
- La fenêtre de création, qui est utilisée lorsqu'un utilisateur créé un modèle de formulaire.
    
Lorsque vous écrivez du code dans un modèle de formulaire, c'est la fenêtre d'édition qui vous sera la plus utile, car elle vous permet d'utiliser une instance **WindowObject** qui lui est associée afin d'accéder à diverses propriétés et méthodes servant à personnaliser un formulaire. 
  
## <a name="overview-of-the-windowscollection-interface"></a>Vue d'ensemble de l'interface WindowsCollection

L'interface **WindowsCollection** fournit les propriétés suivantes, que les développeurs de modèles de formulaires peuvent utiliser pour gérer les instances **WindowObject** qu'elle contient. 
  
|**Name**|**Description**|
|:-----|:-----|
|Propriété [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Count.aspx)  <br/> |Renvoie le nombre d'objets **Window** que contient la collection.  <br/> |
|Propriété [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Item.aspx)  <br/> |Renvoie une référence à l'objet **Window** spécifié.  <br/> **REMARQUE**: Visual C# aux collections à l’aide d’un indexeur au lieu d’appeler la **propriété Item.** Par exemple : `thisApplication.Windows[0].Caption`.           |
   
## <a name="overview-of-the-window-object"></a>Vue d'ensemble de l'objet Window

L'interface **WindowObject** fournit aux développeurs les méthodes et propriétés suivantes pour interagir avec une fenêtre InfoPath. La prise en charge de ces méthodes et propriétés dépend du type de fenêtre ( [XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) ) que vous utilisez. Certaines méthodes et propriétés fonctionnent uniquement avec les fenêtres d'édition (**XdWindowType.xdEditorWindow**). Les autres méthodes et propriétés fonctionnent à la fois avec les fenêtres d'édition et les fenêtres de création (**XdWindowType.xdDesignerWindow**). Par ailleurs, comme pour tous les membres de modèles objets InfoPath, la prise en charge des méthodes et des propriétés varie selon le niveau de sécurité et les modalités de déploiement du formulaire lorsque cette prise en charge est appelée à partir d'un modèle de formulaire.
  
|**Name**|**Description**|**Prise en charge des types de fenêtres**|
|:-----|:-----|:-----|
|[Méthode Activate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Activate.aspx)  <br/> |Active la fenêtre.  <br/> |Les types **xdDesignWindow** et **xdEditorWindow**  <br/> |
|[Propriété](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Active.aspx) active  <br/> |Renvoie une valeur **Boolean** qui indique si la fenêtre est la fenêtre active.  <br/> |Types **xdDesignWindow** et **xdEditorWindow**  <br/> |
|[Caption,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Caption.aspx) propriété  <br/> |Propriété en lecture/écriture qui renvoie ou définit le texte de légende de la fenêtre représentée par l'objet **Window**.  <br/> |Uniquement le type **xdEditorWindow**  <br/> |
|Méthode [Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Close.aspx)  <br/> |Ferme une fenêtre.  <br/> |Uniquement le type **xdEditorWindow**  <br/> |
|[CommandBars,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.CommandBars.aspx) propriété  <br/> |Renvoie une référence à l'objet Microsoft Office **CommandBars**.  <br/> |Types **xdDesignWindow** et **xdEditorWindow**  <br/> |
|[Height,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Height.aspx) propriété  <br/> |Propriété en lecture/écriture de type entier long qui spécifie la hauteur en points de la fenêtre représentée par l'objet **Window**.  <br/> |Types **xdDesignWindow** et **xdEditorWindow**  <br/> |
|[Left,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Left.aspx) propriété  <br/> |Propriété en lecture/écriture de type entier long qui indique la position horizontale (en points) de la fenêtre représentée par l'objet **Window**.  <br/> |Types **xdDesignWindow** et **xdEditorWindow**  <br/> |
|[MailEnvelope,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.MailEnvelope.aspx) propriété  <br/> |Renvoie une référence à [l’objet MailEnvelopeObject.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MailEnvelopeObject.aspx)  <br/> |Uniquement le type **xdEditorWindow**  <br/> |
|[TaskPanes,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.TaskPanes.aspx) propriété  <br/> |Renvoie une référence à la collection [TaskPanesCollection.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.TaskPanesCollection.aspx)  <br/> |Types **xdDesignWindow** et **xdEditorWindow**  <br/> |
|[Top,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Top.aspx) propriété  <br/> |Propriété en lecture/écriture de type entier long qui indique la position verticale (en points) de la fenêtre représentée par l'objet **Window**.  <br/> |Types **xdDesignWindow** et **xdEditorWindow**  <br/> |
|[WindowType,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowType.aspx) propriété  <br/> |Renvoie un nombre indiquant le type de la fenêtre, en fonction de l’éumération [XdWindowType.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx)  <br/> |Types **xdDesignWindow** et **xdEditorWindow**  <br/> |
|[Width,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Width.aspx) propriété  <br/> |Propriété en lecture/écriture de type entier long qui indique la largeur (en points) de la fenêtre représentée par l'objet **Window**.  <br/> |Types **xdDesignWindow** et **xdEditorWindow**  <br/> |
|[WindowState,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowState.aspx) propriété  <br/> |Propriété en lecture/écriture de type [XdWindowState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowState.aspx) qui renvoie ou définit l’état de la fenêtre représentée par **l’objet Window.**  <br/> |Types **xdDesignWindow** et **xdEditorWindow**  <br/> |
|[XDocument,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.XDocument.aspx) propriété  <br/> |Renvoie une référence à [l’objet _XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.aspx) associé à la fenêtre.  <br/> |Uniquement le type **xdEditorWindow**  <br/> |
   
## <a name="using-the-windowscollection-and-window-interfaces"></a>Utilisation des interfaces WindowsCollection et Window

L'interface **WindowsCollection** est accessible via la propriété [Windows](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Windows.aspx) de l'interface [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . Lorsque vous utilisez l'interface **WindowsCollection** pour accéder aux fenêtres d'un formulaire, vous pouvez utiliser un indexeur (Visual C#) ou transmettre un entier long à la propriété **Item** (Visual Basic) pour renvoyer une référence à une instance de l'interface **WindowObject**. Par exemple, le code ci-dessous définit une référence à la première interface **WindowObject** contenue dans l'interface **WindowsCollection**.
  
```cs
WindowObject objWindow = thisApplication.Windows[0];
```

```vb
Dim objWindow As WindowObject = thisApplication.Windows(0)
```

Cependant, vous pouvez accéder directement à la fenêtre actuellement ouverte en utilisant la propriété [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.ActiveWindow.aspx) de l'interface **Application**, sans passer par la collection ** WindowsCollection **, comme démontré dans l'exemple qui suit.
  
```cs
WindowObject objWindow = thisApplication.ActiveWindow;
```

```vb
Dim objWindow As WindowObject = thisApplication.ActiveWindow
```

> [!NOTE]
> [!REMARQUE] Lors du débogage d'un projet InfoPath avec code managé, la propriété **ActiveWindow** renvoie toujours **null** car la fenêtre de débogage est active. 
  
Pour accéder à un objet **WindowObject**, vous devez utiliser la propriété [Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) de l'interface [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.aspx) associée au document XML sous-jacent d'un formulaire. La propriété **View** de l'interface **XDocument** est utilisée pour accéder à l'objet **View**. Par exemple, le code suivant définit une référence à l'objet **WindowObject** associé à la vue d'un document XML sous-jacent du formulaire. 
  
```cs
WindowObject objWindow = thisXDocument.View.Window;
```

```vb
Dim objWindow As WindowObject = thisXDocument.View.Window
```

> [!NOTE]
> [!REMARQUE] Certaines propriétés et méthodes de l'objet **Window** peuvent uniquement être utilisées dans la fenêtre d'édition et renverront une erreur si elles sont utilisées dans la fenêtre de création. Les propriétés et méthodes prises en charge par chaque type de fenêtre sont répertoriées dans le tableau plus haut dans cette rubrique. Vous pouvez utiliser dans votre code la propriété **WindowType** pour déterminer le type de fenêtre que vous utilisez. 
  

