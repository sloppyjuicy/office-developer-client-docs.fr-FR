---
title: Fenêtres de formulaires
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- windowscollection [infopath 2007],form windows [InfoPath 2007],Window class [InfoPath 2007]
localization_priority: Normal
ms.assetid: 32ae2427-882b-45f8-8754-0e8c27fc23ba
description: Lorsque vous utilisez un formulaire InfoPath par programmation, vous pouvez écrire du code pour accéder à ses fenêtres et personnaliser certains éléments qu'elles contiennent. Le modèle objet InfoPath fourni par l'espace de noms Microsoft.Office.InfoPath prend en charge l'accès aux fenêtres d'un formulaire par le biais de la classe Window associée à la classe WindowCollection .
ms.openlocfilehash: 5b24798e92849a2d79bf836e12dd91845ee58942
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782387"
---
# <a name="work-with-form-windows"></a>Fenêtres de formulaires

Lorsque vous utilisez un formulaire InfoPath par programmation, vous pouvez écrire du code pour accéder à ses fenêtres et personnaliser certains éléments qu'elles contiennent. Le modèle objet InfoPath fourni par l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) prend en charge l'accès aux fenêtres d'un formulaire par le biais de la classe [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) associée à la classe [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) . 
  
> [!NOTE]
> [!REMARQUE] Les classes qui permettent d'utiliser des fenêtres de formulaire ne sont disponibles que lorsque vous utilisez un **Formulaire de l'Éditeur InfoPath**. Si le paramètre **Compatibilité** d'un modèle de formulaire est défini sur **Formulaire de navigateur Web**, ces classes ne sont pas disponibles. 
  
Il existe deux types de fenêtres dans InfoPath : 
  
- Fenêtre de modification utilisée lors du remplissage d'un formulaire.
    
- Fenêtre de conception utilisée lors de la conception d'un modèle de formulaire par l'utilisateur.
    
Lorsque vous écrivez du code dans un modèle de formulaire, celui-ci représente la fenêtre d'édition qui fournit les fonctionnalités les plus utiles, car vous pouvez utiliser un objet [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) qui fait référence à la fenêtre actuelle pour accéder aux différentes propriétés et méthodes qui permettent de personnaliser la mise en forme du formulaire. 
  
## <a name="overview-of-the-windowscollection-class"></a>Vue d'ensemble de la classe WindowsCollection

La classe [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) contient les propriétés ci-dessous destinées aux développeurs de modèles pour la gestion des objets [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) qu'elle contient. 
  
|**Nom**|**Description**|
|:-----|:-----|
|Propriété [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx)  <br/> |Obtient le nombre d’objets [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) contenus dans la collection.  <br/> |
|Propriété [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx)  <br/> |Obtient une référence à l’objet [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) spécifié.  <br/> |
   
## <a name="overview-of-the-window-class"></a>Vue d'ensemble de la classe Window

La classe [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) contient les méthodes et les propriétés suivantes destinées aux développeurs de formulaires pour interagir avec une fenêtre InfoPath. La prise en charge de ces méthodes et propriétés dépend du type de fenêtre ( [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) ) que vous utilisez. Certaines méthodes et propriétés fonctionnent uniquement avec le type de fenêtre Éditeur (**WindowType.Editor**). Les méthodes et les propriétés restantes fonctionnent avec le type de fenêtre Éditeur et le type de fenêtre du concepteur (**WindowType.Designer**). Par ailleurs, comme pour tous les membres de modèles objets InfoPath, la prise en charge des méthodes et des propriétés varie selon le niveau de sécurité et les modalités de déploiement du formulaire lorsque cette prise en charge est appelée à partir d'un modèle de formulaire.
  
|**Nom**|**Description**|**Prise en charge du Type de fenêtre**|
|:-----|:-----|:-----|
|Méthode [Activate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx)  <br/> |Active (concentre l'affichage sur) la fenêtre.   <br/> |Type de **Designer** et **Editor**  <br/> |
|[Active](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx) , propriété  <br/> |Obtient une valeur **Boolean** indiquant si la fenêtre est la fenêtre active.  <br/> |Type de **Designer** et **Editor**  <br/> |
|Propriété [Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx)  <br/> |Obtient ou définit le texte de légende de la fenêtre représentée par l’objet [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) .  <br/> |Type **Editor** uniquement  <br/> |
|Méthode [Close()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Ferme la fenêtre et vous invite à enregistrer les modifications effectuées dans un formulaire non enregistré, ou un formulaire qui comporte des modifications non enregistrées.  <br/> |Type **Editor** uniquement  <br/> |
|Méthode [Close(Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Ferme la fenêtre et force le cas échéant la fermeture sans enregistrement d'un formulaire non enregistré ou d'un formulaire qui contient des modifications non enregistrées.   <br/> |Type **Editor** uniquement  <br/> |
|[CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) , propriété  <br/> |Obtient une référence à la collection Microsoft Office **CommandBars** qui est associée à la fenêtre.  <br/> |Type de **Designer** et **Editor**  <br/> |
|[Height](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx) , propriété  <br/> |Obtient ou définit la hauteur de la fenêtre, mesurée en points.  <br/> |Type de **Designer** et **Editor**  <br/> |
|Propriété [Left](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx)  <br/> |Obtient ou définit la position horizontale de la fenêtre, mesurée en points.  <br/> |Type de **Designer** et **Editor**  <br/> |
|Propriété [MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx)  <br/> |Obtient une référence à la classe [MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx) .  <br/> |Type **Editor** uniquement  <br/> |
|[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx) , propriété  <br/> |Obtient une référence à la collection de la [collection TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) .  <br/> |Type de **Designer** et **Editor**  <br/> |
|Propriété [Top](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx)  <br/> |Obtient ou définit la position verticale de la fenêtre, mesurée en points.  <br/> |Type de **Designer** et **Editor**  <br/> |
|Propriété [Width](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx)  <br/> |Obtient ou définit la largeur de la fenêtre, mesurée en points.  <br/> |Type de **Designer** et **Editor**  <br/> |
|[WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx) , propriété  <br/> |Obtient ou définit l’état de la fenêtre sous forme de valeur [WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx) .  <br/> |Type de **Designer** et **Editor**  <br/> |
|Propriété [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx)  <br/> |Obtient le type de la fenêtre sous la forme d’une valeur d’énumération [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) .  <br/> |Type de **Designer** et **Editor**  <br/> |
|Propriété [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx)  <br/> |Renvoie une référence à l’objet [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) associé à la fenêtre.  <br/> |Type **Editor** uniquement  <br/> |
   
## <a name="using-the-windowscollection-and-window-classes"></a>Utilisation des classes WindowsCollection et Window

La classe [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) est accessible par le biais de la propriété [Windows](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . Lorsque vous utilisez la classe [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) pour accéder aux fenêtres d'un formulaire, vous utilisez un indexeur (pour Visual C#) ou passez un entier long à la propriété **Item** (pour Visual Basic) afin qu'elle renvoie une référence à une instance de l'objet [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) . Par exemple, le code suivant définit une référence au premier objet [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) contenu dans la collection [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) de la session InfoPath active. 
  
```cs
Window myWindow = this.Application.Windows[0];
```

```vb
Dim myWindow As Window = Me.Application.Windows(0)
```

Vous pouvez accéder directement à la fenêtre actuellement ouverte à l'aide de la propriété [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) , sans passer par la collection [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) , comme le représente la ligne de code suivante. 
  
```cs
Window myWindow = this.Application.ActiveWindow;
```

```vb
Dim myWindow As Window = Me.Application.ActiveWindow
```

Un objet [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) est également accessible à l'aide de la propriété [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) de la classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , qui représente l'affichage actuellement utilisé pour travailler sur le document XML sous-jacent du formulaire. La propriété [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) permet d'accéder à un objet [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , qui représente l'affichage actuel. Par exemple, le code suivant définit une référence à l'élément [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) associé à l'affichage actuel. 
  
```cs
Window myWindow = this.CurrentView.Window;
```

```vb
Dim myWindow As Window = Me.CurrentView.Window
```

> [!NOTE]
> [!REMARQUE] Certaines propriétés et méthodes de la classe [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) concernent uniquement le type de la fenêtre d'édition. Elles renvoient une erreur si elles sont utilisées avec le type de la fenêtre de conception. Les propriétés et les méthodes prises en charge pour chaque type de fenêtre sont répertoriées dans le tableau plus haut dans cette rubrique. Vous pouvez utiliser la propriété [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) dans le code pour déterminer le type de fenêtre utilisé. 
  

