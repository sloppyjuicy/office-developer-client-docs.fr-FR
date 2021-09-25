---
title: Travailler avec des affichages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- view class [infopath 2007],InfoPath 2007, working with views,views [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: Lorsque vous utilisez un modèle de formulaire InfoPath, vous pouvez écrire du code permettant d'accéder aux vues du formulaire, puis effectuer une série d'actions sur les données figurant dans les vues. Le modèle d'objet InfoPath fourni par l'espace de noms Microsoft.Office.InfoPath prend en charge l'accès aux vues d'un formulaire par le biais de l'utilisation des membres de la classe View .
ms.openlocfilehash: ac870441f2e8e6f780eaaa45dc0ee26e7c3cf25a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625832"
---
# <a name="work-with-views"></a>Travailler avec des affichages

Lorsque vous utilisez un modèle de formulaire InfoPath, vous pouvez écrire du code permettant d'accéder aux vues du formulaire, puis effectuer une série d'actions sur les données figurant dans les vues. Le modèle d'objet InfoPath fourni par l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) prend en charge l'accès aux vues d'un formulaire par le biais de l'utilisation des membres de la classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) . 
  
## <a name="overview-of-the-view-class"></a>Présentation de la classe View

La classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) fournit aux développeurs de formulaires les méthodes et les propriétés ci-dessous pour interagir avec une vue InfoPath. 
  
> [!NOTE]
> [!REMARQUE] Les méthodes et les propriétés de la classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) ne sont pas disponibles au cours de l'événement [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) . 
  
|**Name**|**Description**|
|:-----|:-----|
|[Méthode DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)  <br/> |Désactive la synchronisation automatique entre le document XML sous-jacent d'un formulaire et la vue associée.  <br/> |
|[Méthode EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)  <br/> |Active la synchronisation automatique entre le document XML sous-jacent d'un formulaire et la vue associée.  <br/> |
|[Méthode ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Exécute une commande d'édition sur le document XML sous-jacent d'un formulaire, sur la base des données sélectionnées dans la vue.  <br/> |
|[Méthode ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Exécute une commande d'édition sur le document XML sous-jacent d'un formulaire, sur la base du champ ou groupe spécifié.  <br/> |
|[Export,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) méthode  <br/> |Exporte la vue vers un fichier au format spécifié.  <br/> |
|[Méthode ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)  <br/> |Impose de synchroniser le document XML sous-jacent d'un formulaire avec la vue associée.  <br/> |
|[Méthode GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Obtient une référence à un objet **XPathNodeIterator** permettant d'effectuer des itérations dans les nœuds XML renvoyés à partir du nœud spécifié.  <br/> |
|[Méthode GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Obtient une référence à un objet **XPathNodeIterator** permettant d'effectuer des itérations dans les nœuds XML renvoyés dans la sélection active au sein du contrôle associé au champ ou groupe spécifié.  <br/> |
|[Méthode GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |Obtient une référence à un objet **XPathNodeIterator** permettant d'effectuer des itérations dans tous les nœuds XML dans la sélection active d'éléments d'une vue.  <br/> |
|[Méthode SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Sélectionne une plage de nœuds dans une vue, sur la base du premier nœud XML spécifié.  <br/> |
|[Méthode SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Sélectionne une plage de nœuds dans une vue, sur la base des premier et dernier nœuds XML spécifiés.  <br/> |
|[Méthode SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Sélectionne une plage de nœuds dans une vue, sur la base du nœud XML de départ, du nœud XML de fin et du contrôle spécifiés.  <br/> |
|[Méthode SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Sélectionne le texte contenu dans un contrôle modifiable lié au nœud spécifié par l'objet **XPathNavigator** transmis à cette méthode.  <br/> |
|[Méthode SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Sélectionne le texte contenu dans un contrôle modifiable lié au nœud spécifié par l'objet **XPathNavigator** transmis à cette méthode, et le contrôle spécifié.  <br/> |
|[Méthode ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)  <br/> |Crée un message électronique contenant l’affichage actuel.  <br/> |
|[ViewInfo,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) propriété  <br/> |Obtient une référence à un [objet ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) associé à l’affichage.  <br/> |
|[Window,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) propriété  <br/> |Obtient une référence à un [objet Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) associé à l’affichage.  <br/> |
   
> [!NOTE]
> [!REMARQUE] Le modèle objet InfoPath fournit également les classes [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) et [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , qui peuvent être utilisées pour obtenir des informations concernant toutes les vues implémentées dans un formulaire. 
  
## <a name="using-the-view-class"></a>Utilisation de la classe View

La classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) est accessible par le biais de la propriété [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) , elle-même accessible au moyen du mot clé **this** (C#) ou **Me** (Visual Basic). Pour accéder au nom de la vue, vous devez accéder à l'objet [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) associé à la vue. L'exemple de code suivant indique comment afficher une boîte de message avec le nom de la vue active. 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

Tous les modèles de formulaires InfoPath comportent au moins une vue par défaut. Toutefois, InfoPath prend également en charge la création de vues multiples d'un document XML sous-jacent du formulaire. Dans le cas de vues multiples, l'élément [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) permet d'utiliser toutes le vues implémentées dans le modèle de formulaire. Pour accéder à la collection [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) d'un modèle de formulaire, utilisez la propriété [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Par le biais de la programmation, vous pouvez changer la vue active au moyen de la méthode [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) de la collection [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , comme l'illustre l'exemple de code suivant. 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

L'exemple précédent de basculement d'une vue fonctionne uniquement une fois le formulaire ouvert. Pour définir une vue par défaut au cours de l'événement [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , utilisez la propriété [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) de la classe [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , comme illustré dans l'exemple suivant. Notez, toutefois, que cette valeur ne prendra effet qu'après l'enregistrement et la réouverture du formulaire. 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a>Sélection des contrôles dans une vue

InfoPath propose deux méthode de la classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , qui sont toutes deux surchargées, pour sélectionner, par le biais de la programmation, un contrôle dans la vue actuelle : les méthodes [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) et [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) . La méthode [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) est utilisée pour les contrôles d'entrée de données, comme **Zone de texte**, tandis que la méthode **SelectNodes** est utilisée pour les contrôles structurels, comme **Section facultative**. Pour sélectionner un contrôle en particulier dans la vue, vous devez fournir le nœud et, éventuellement, l'ID de contexte de vue du contrôle. Cet ID est nécessaire lorsque plusieurs contrôles sont liés au même nœud dans la source de données. InfoPath fournit les informations d'ID de contexte de vue lors de la conception du formulaire.
  
L'ID de contexte de vue d'un contrôle s'affiche sous l'onglet **Avancé** de la boîte de dialogue Propriétés du contrôle, accessible en cliquant avec le bouton droit sur le contrôle, en cliquant sur  _ControlName_ **Propriétés**, puis en cliquant sur l'onglet **Avancé**. L'ID de contexte de vue du contrôle est répertorié dans la section **Code** de l'onglet **Avancé**. 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a>Cas d'utilisation de SelectText et SelectNodes

Vous pouvez sélectionner, par le biais de la programmation, les contrôles d'entrée de données ci-dessous en utilisant la méthode [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) : 
  
- Zone de texte
    
- Zone de texte mis en forme
    
- Sélecteur de dates
    
Vous pouvez sélectionner, par le biais de la programmation, les contrôles structurels ci-dessous en utilisant la méthode [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) : 
  
- Section facultative
    
- Section de choix
    
- Section extensible (éléments)
    
- Tableau extensible (lignes)
    
- Section récursive extensible (éléments)
    
- Liste à puces, numérotée et simple
    
- Tableau extensible horizontal
    
Vous ne pouvez pas sélectionner ou activer, par le biais de la programmation, les contrôles suivants :
  
- Zone de liste déroulante
    
- Zone de liste
    
- Case à cocher
    
- Case d'option
    
- Bouton
    
- Image (liée ou incluse)
    
- Image manuscrite
    
- Lien hypertexte
    
- Zone d'expression
    
- Étiquette verticale
    
- Section ActiveX
    
- Zone horizontale
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a>Utilisation des méthodes SelectText et SelectNodes

Dans l'exemple ci-dessous, la surcharge [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) de la méthode **SelectText**, qui fournit un paramètre  _xmlNode_, permet de sélectionner un contrôle **Zone de texte** lié à « my:field1 ». 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

Si plusieurs contrôlés sont liés à « my:field1 », vous devez utiliser la surcharge [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) de la méthode **SelectText**, qui fournit un paramètre  _viewContext_ supplémentaire pour sélectionner un contrôle spécifique. L'exemple ci-dessous part du principe qu'il y a deux contrôles **Zone de texte** liés à « my:field1 », le premier contrôle possédant l'ID de contexte de vue « CTRL1 » et le second contrôle l'ID de contexte de vue « CTRL8 ». Le second contrôle est sélectionné. 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

Dans l'exemple qui suit, la surcharge [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) de la méthode **SelectNodes**, qui fournit le seul paramètre  _startNode_, est utilisé pour sélectionner la première ligne d'un tableau extensif lié au groupe extensible « my:employee ». 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

Vous pouvez également sélectionner plusieurs lignes dans un tableau extensible. Dans l'exemple qui suit, les trois premières lignes d'un tableau extensible lié au groupe extensible « my:employee » sont sélectionnées avec la surcharge [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) de la méthode **SelectNodes**, qui fournit les paramètres  _startNode_ et  _endNode_: 
  
```cs
// Create XPathNavigators to specify range of nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
XPathNavigator repeatingTableRow3 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:myemployee[3]", NamespaceManager);
// Select range of nodes in specified XPathNavigators.
CurrentView.SelectNodes(repeatingTableRow1, repeatingTableRow3);
```


