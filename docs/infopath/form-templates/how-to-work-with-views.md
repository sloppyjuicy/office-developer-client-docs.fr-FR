---
title: Utilisation des vues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- view class [infopath 2007],InfoPath 2007, working with views,views [InfoPath 2007]
localization_priority: Normal
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: Lorsque vous utilisez un modèle de formulaire InfoPath, vous pouvez écrire du code permettant d'accéder aux vues du formulaire, puis effectuer une série d'actions sur les données figurant dans les vues. Le modèle d'objet InfoPath fourni par l'espace de noms Microsoft.Office.InfoPath prend en charge l'accès aux vues d'un formulaire par le biais de l'utilisation des membres de la classe View .
ms.openlocfilehash: 84c32244454e388e50433922c007d556fbef806a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782391"
---
# <a name="work-with-views"></a><span data-ttu-id="1afb8-105">Utilisation des vues</span><span class="sxs-lookup"><span data-stu-id="1afb8-105">Work with Views</span></span>

<span data-ttu-id="1afb8-p102">Lorsque vous utilisez un modèle de formulaire InfoPath, vous pouvez écrire du code permettant d'accéder aux vues du formulaire, puis effectuer une série d'actions sur les données figurant dans les vues. Le modèle d'objet InfoPath fourni par l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) prend en charge l'accès aux vues d'un formulaire par le biais de l'utilisation des membres de la classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1afb8-p102">When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain. The InfoPath object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace supports access to a form's views through the use of the members of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class.</span></span> 
  
## <a name="overview-of-the-view-class"></a><span data-ttu-id="1afb8-108">Présentation de la classe View</span><span class="sxs-lookup"><span data-stu-id="1afb8-108">Overview of the View Class</span></span>

<span data-ttu-id="1afb8-109">La classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) fournit aux développeurs de formulaires les méthodes et les propriétés ci-dessous pour interagir avec une vue InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1afb8-109">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class provides the following methods and properties, which form developers can use to interact with an InfoPath view.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1afb8-110">[!REMARQUE] Les méthodes et les propriétés de la classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) ne sont pas disponibles au cours de l'événement [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1afb8-110">The methods and properties of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class are not available during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
|<span data-ttu-id="1afb8-111">**Nom**</span><span class="sxs-lookup"><span data-stu-id="1afb8-111">**Name**</span></span>|<span data-ttu-id="1afb8-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="1afb8-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1afb8-113">Méthode [DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="1afb8-114">Désactive la synchronisation automatique entre le document XML sous-jacent d'un formulaire et la vue associée.</span><span class="sxs-lookup"><span data-stu-id="1afb8-114">Disables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="1afb8-115">Méthode [EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="1afb8-116">Active la synchronisation automatique entre le document XML sous-jacent d'un formulaire et la vue associée.</span><span class="sxs-lookup"><span data-stu-id="1afb8-116">Enables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="1afb8-117">Méthode [ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-117">[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="1afb8-118">Exécute une commande d'édition sur le document XML sous-jacent d'un formulaire, sur la base des données sélectionnées dans la vue.</span><span class="sxs-lookup"><span data-stu-id="1afb8-118">Executes an editing command against a form's underlying XML document, based on the data currently selected in the view.</span></span>  <br/> |
|<span data-ttu-id="1afb8-119">Méthode [ExecuteAction (ActionType, chaîne)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-119">[ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="1afb8-120">Exécute une commande d'édition sur le document XML sous-jacent d'un formulaire, sur la base du champ ou groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="1afb8-120">Executes an editing command against a form's underlying XML document, based on the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="1afb8-121">Méthode [Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-121">[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) method</span></span>  <br/> |<span data-ttu-id="1afb8-122">Exporte la vue vers un fichier au format spécifié.</span><span class="sxs-lookup"><span data-stu-id="1afb8-122">Exports the view to a file of the specified format.</span></span>  <br/> |
|<span data-ttu-id="1afb8-123">Méthode [ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-123">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="1afb8-124">Impose la synchronisation entre le document XML sous-jacent d'un formulaire et la vue associée.</span><span class="sxs-lookup"><span data-stu-id="1afb8-124">Forces synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="1afb8-125">Méthode [GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-125">[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="1afb8-126">Obtient une référence à un objet **XPathNodeIterator** qui se répète sur les nœuds XML renvoyés à partir du nœud spécifié.</span><span class="sxs-lookup"><span data-stu-id="1afb8-126">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes starting from the specified node.</span></span>  <br/> |
|<span data-ttu-id="1afb8-127">Méthode [GetContextNodes (XPathNavigator, chaîne)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-127">[GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="1afb8-128">Obtient une référence à un objet **XPathNodeIterator** qui se répète sur les nœuds XML renvoyés dans la sélection actuelle dans le contrôle lié au champ spécifié ou au groupe.</span><span class="sxs-lookup"><span data-stu-id="1afb8-128">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes in the current selection within the control bound to the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="1afb8-129">Méthode [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-129">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="1afb8-130">Obtient une référence à un objet **XPathNodeIterator** qui se répète sur tous les nœuds XML dans la sélection actuelle d’éléments dans un affichage.</span><span class="sxs-lookup"><span data-stu-id="1afb8-130">Gets a reference to an **XPathNodeIterator** object for iterating over all XML nodes in the current selection of items in a view.</span></span>  <br/> |
|<span data-ttu-id="1afb8-131">Méthode [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-131">[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="1afb8-132">Sélectionne une plage de nœuds dans une vue, sur la base du premier nœud XML spécifié. </span><span class="sxs-lookup"><span data-stu-id="1afb8-132">Selects a range of nodes in a view based on the specified starting XML node.</span></span>  <br/> |
|<span data-ttu-id="1afb8-133">Méthode [SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-133">[SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="1afb8-134">Sélectionne une plage de nœuds dans une vue, sur la base des premier et dernier nœuds XML spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1afb8-134">Selects a range of nodes in a view based on the specified starting XML node and ending XML node.</span></span>  <br/> |
|<span data-ttu-id="1afb8-135">Méthode [SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-135">[SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="1afb8-136">Sélectionne une plage de nœuds dans une vue, sur la base du nœud XML de départ, du nœud XML de fin et du contrôle spécifiés. </span><span class="sxs-lookup"><span data-stu-id="1afb8-136">Selects a range of nodes in a view based on the specified starting XML node, the ending XML node, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="1afb8-137">Méthode [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-137">[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="1afb8-138">Sélectionne le texte contenu dans un contrôle modifiable lié au nœud spécifié par l’objet **XPathNavigator** transmis à cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1afb8-138">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method.</span></span>  <br/> |
|<span data-ttu-id="1afb8-139">Méthode [SelectText (XPathNavigator, chaîne)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-139">[SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="1afb8-140">Sélectionne le texte contenu dans un contrôle modifiable lié au nœud spécifié par l’objet **XPathNavigator** transmis à cette méthode et le contrôle spécifié.</span><span class="sxs-lookup"><span data-stu-id="1afb8-140">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="1afb8-141">Méthode [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-141">[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) method</span></span>  <br/> |<span data-ttu-id="1afb8-142">Crée un message électronique contenant la vue active.</span><span class="sxs-lookup"><span data-stu-id="1afb8-142">Creates an email message containing the current view.</span></span>  <br/> |
|<span data-ttu-id="1afb8-143">Propriété [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx)</span><span class="sxs-lookup"><span data-stu-id="1afb8-143">[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) property</span></span>  <br/> |<span data-ttu-id="1afb8-144">Obtient une référence à un objet [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) associé à la vue.</span><span class="sxs-lookup"><span data-stu-id="1afb8-144">Gets a reference to a [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span>  <br/> |
|<span data-ttu-id="1afb8-145">[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) , propriété</span><span class="sxs-lookup"><span data-stu-id="1afb8-145">[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) property</span></span>  <br/> |<span data-ttu-id="1afb8-146">Obtient une référence à un objet [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) associé à la vue.</span><span class="sxs-lookup"><span data-stu-id="1afb8-146">Gets a reference to a [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) object associated with the view.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="1afb8-147">[!REMARQUE] Le modèle objet InfoPath fournit également les classes [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) et [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , qui peuvent être utilisées pour obtenir des informations concernant toutes les vues implémentées dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="1afb8-147">The InfoPath object model also provides the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) and [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) classes, which can be used to get information about all of the views implemented in a form.</span></span> 
  
## <a name="using-the-view-class"></a><span data-ttu-id="1afb8-148">Utilisation de la classe View</span><span class="sxs-lookup"><span data-stu-id="1afb8-148">Using the View Class</span></span>

<span data-ttu-id="1afb8-p103">La classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) est accessible par le biais de la propriété [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) , elle-même accessible au moyen du mot clé **this** (C#) ou **Me** (Visual Basic). Pour accéder au nom de la vue, vous devez accéder à l'objet [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) associé à la vue. L'exemple de code suivant indique comment afficher une boîte de message avec le nom de la vue active.</span><span class="sxs-lookup"><span data-stu-id="1afb8-p103">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class is accessed through the [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class, which is accessed using the **this** (C#) or **Me** (Visual Basic) keyword. To access the name of the view, you need to access the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view. The following example demonstrates how to display a message box with the name of the view that is currently active.</span></span> 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

<span data-ttu-id="1afb8-p104">Tous les modèles de formulaires InfoPath comportent au moins une vue par défaut. Toutefois, InfoPath prend également en charge la création de vues multiples d'un document XML sous-jacent du formulaire. Dans le cas de vues multiples, l'élément [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) permet d'utiliser toutes le vues implémentées dans le modèle de formulaire. Pour accéder à la collection [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) d'un modèle de formulaire, utilisez la propriété [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Par le biais de la programmation, vous pouvez changer la vue active au moyen de la méthode [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) de la collection [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , comme l'illustre l'exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="1afb8-p104">All InfoPath form templates contain at least one default view; however, InfoPath also supports the creation of multiple views of a form's underlying XML document. When you have multiple views, the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) can be used to work with all of the views implemented in the form template. To access the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) of a form template, use the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class. You can programmatically change the view that is currently active by using the [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) method of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , as the following code sample demonstrates.</span></span> 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

<span data-ttu-id="1afb8-p105">L'exemple précédent de basculement d'une vue fonctionne uniquement une fois le formulaire ouvert. Pour définir une vue par défaut au cours de l'événement [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , utilisez la propriété [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) de la classe [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , comme illustré dans l'exemple suivant. Notez, toutefois, que cette valeur ne prendra effet qu'après l'enregistrement et la réouverture du formulaire.</span><span class="sxs-lookup"><span data-stu-id="1afb8-p105">The previous example for switching a view will work only after the form is opened. To set a default view during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, use the [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) property of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) class as shown in the following example. Note, however, that this value will only take effect after the form is saved and re-opened.</span></span> 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a><span data-ttu-id="1afb8-159">Sélection des contrôles dans une vue</span><span class="sxs-lookup"><span data-stu-id="1afb8-159">Selecting Controls in a View</span></span>

<span data-ttu-id="1afb8-p106">InfoPath propose deux méthode de la classe [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , qui sont toutes deux surchargées, pour sélectionner, par le biais de la programmation, un contrôle dans la vue actuelle : les méthodes [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) et [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) . La méthode [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) est utilisée pour les contrôles d'entrée de données, comme **Zone de texte**, tandis que la méthode **SelectNodes** est utilisée pour les contrôles structurels, comme **Section facultative**. Pour sélectionner un contrôle en particulier dans la vue, vous devez fournir le nœud et, éventuellement, l'ID de contexte de vue du contrôle. Cet ID est nécessaire lorsque plusieurs contrôles sont liés au même nœud dans la source de données. InfoPath fournit les informations d'ID de contexte de vue lors de la conception du formulaire.</span><span class="sxs-lookup"><span data-stu-id="1afb8-p106">InfoPath provides two methods of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class, both of which are overloaded, to programmatically select a control in the current view: the [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) and [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods. The [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method is used for data entry controls, such as a **Text Box**, while the **SelectNodes** method is used for structural controls, such as an **Optional Section**. To select a particular control in the view, you need to provide the node and, optionally, the control's ViewContext ID. The ViewContext ID is needed when you have multiple controls bound to the same node in the data source. InfoPath provides the ViewContext ID information when you design the form.</span></span>
  
<span data-ttu-id="1afb8-165">L'ID de contexte de vue d'un contrôle s'affiche sous l'onglet **Avancé** de la boîte de dialogue Propriétés du contrôle, accessible en cliquant avec le bouton droit sur le contrôle, en cliquant sur  _ControlName_ **Propriétés**, puis en cliquant sur l'onglet **Avancé**. L'ID de contexte de vue du contrôle est répertorié dans la section **Code** de l'onglet **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="1afb8-165">A control's ViewContext ID is displayed on the **Advanced** tab of the control's properties dialog box, which is accessed by right-clicking the control, clicking  _ControlName_ **Properties**, and then clicking the **Advanced** tab. The ViewContext ID of the control is listed in the **Code** section of the **Advanced** tab.</span></span> 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a><span data-ttu-id="1afb8-166">Cas d'utilisation de SelectText et SelectNodes</span><span class="sxs-lookup"><span data-stu-id="1afb8-166">When to use SelectText and SelectNodes</span></span>

<span data-ttu-id="1afb8-167">Vous pouvez sélectionner, par le biais de la programmation, les contrôles d'entrée de données ci-dessous en utilisant la méthode [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) :</span><span class="sxs-lookup"><span data-stu-id="1afb8-167">You can programmatically select the following data entry controls by using the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method:</span></span> 
  
- <span data-ttu-id="1afb8-168">Zone de texte</span><span class="sxs-lookup"><span data-stu-id="1afb8-168">Text Box</span></span>
    
- <span data-ttu-id="1afb8-169">Zone de texte mis en forme</span><span class="sxs-lookup"><span data-stu-id="1afb8-169">Rich Text Box</span></span>
    
- <span data-ttu-id="1afb8-170">Sélecteur de dates</span><span class="sxs-lookup"><span data-stu-id="1afb8-170">Date Picker</span></span>
    
<span data-ttu-id="1afb8-171">Vous pouvez sélectionner, par le biais de la programmation, les contrôles structurels ci-dessous en utilisant la méthode [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) :</span><span class="sxs-lookup"><span data-stu-id="1afb8-171">You can programmatically select the following structural controls by using the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method:</span></span> 
  
- <span data-ttu-id="1afb8-172">Section facultative</span><span class="sxs-lookup"><span data-stu-id="1afb8-172">Optional Section</span></span>
    
- <span data-ttu-id="1afb8-173">Section de choix</span><span class="sxs-lookup"><span data-stu-id="1afb8-173">Choice Section</span></span>
    
- <span data-ttu-id="1afb8-174">Section extensible (éléments)</span><span class="sxs-lookup"><span data-stu-id="1afb8-174">Repeating Section (items)</span></span>
    
- <span data-ttu-id="1afb8-175">Tableau extensible (lignes)</span><span class="sxs-lookup"><span data-stu-id="1afb8-175">Repeating Table (rows)</span></span>
    
- <span data-ttu-id="1afb8-176">Section récursive extensible (éléments)</span><span class="sxs-lookup"><span data-stu-id="1afb8-176">Repeating Recursive Section (items)</span></span>
    
- <span data-ttu-id="1afb8-177">Liste à puces, numérotée et simple</span><span class="sxs-lookup"><span data-stu-id="1afb8-177">Bulleted, Numbered, and Plain List</span></span>
    
- <span data-ttu-id="1afb8-178">Tableau extensible horizontal</span><span class="sxs-lookup"><span data-stu-id="1afb8-178">Horizontal Repeating Table</span></span>
    
<span data-ttu-id="1afb8-179">Vous ne pouvez pas sélectionner ou activer, par le biais de la programmation, les contrôles suivants :</span><span class="sxs-lookup"><span data-stu-id="1afb8-179">You cannot programmatically select, or set focus to, the following controls:</span></span>
  
- <span data-ttu-id="1afb8-180">Zone de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="1afb8-180">Drop-Down List Box</span></span>
    
- <span data-ttu-id="1afb8-181">Zone de liste</span><span class="sxs-lookup"><span data-stu-id="1afb8-181">List Box</span></span>
    
- <span data-ttu-id="1afb8-182">Case à cocher</span><span class="sxs-lookup"><span data-stu-id="1afb8-182">Check Box</span></span>
    
- <span data-ttu-id="1afb8-183">Case d'option</span><span class="sxs-lookup"><span data-stu-id="1afb8-183">Option Button</span></span>
    
- <span data-ttu-id="1afb8-184">Bouton</span><span class="sxs-lookup"><span data-stu-id="1afb8-184">Button</span></span>
    
- <span data-ttu-id="1afb8-185">Image (liée ou incluse)</span><span class="sxs-lookup"><span data-stu-id="1afb8-185">Picture (linked or included)</span></span>
    
- <span data-ttu-id="1afb8-186">Image manuscrite</span><span class="sxs-lookup"><span data-stu-id="1afb8-186">Ink Picture</span></span>
    
- <span data-ttu-id="1afb8-187">Lien hypertexte</span><span class="sxs-lookup"><span data-stu-id="1afb8-187">Hyperlink</span></span>
    
- <span data-ttu-id="1afb8-188">Zone d'expression</span><span class="sxs-lookup"><span data-stu-id="1afb8-188">Expression Box</span></span>
    
- <span data-ttu-id="1afb8-189">Étiquette verticale</span><span class="sxs-lookup"><span data-stu-id="1afb8-189">Vertical Label</span></span>
    
- <span data-ttu-id="1afb8-190">Section ActiveX</span><span class="sxs-lookup"><span data-stu-id="1afb8-190">ActiveX Section</span></span>
    
- <span data-ttu-id="1afb8-191">Zone horizontale</span><span class="sxs-lookup"><span data-stu-id="1afb8-191">Horizontal Region</span></span>
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a><span data-ttu-id="1afb8-192">Utilisation des méthodes SelectText et SelectNodes</span><span class="sxs-lookup"><span data-stu-id="1afb8-192">Using the SelectText and SelectNodes Methods</span></span>

<span data-ttu-id="1afb8-193">Dans l'exemple ci-dessous, la surcharge [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) de la méthode **SelectText**, qui fournit un paramètre  _xmlNode_, permet de sélectionner un contrôle **Zone de texte** lié à « my:field1 ».</span><span class="sxs-lookup"><span data-stu-id="1afb8-193">In the following example, the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides one  _xmlNode_ parameter, is used to select a **Text Box** that is bound to "my:field1".</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

<span data-ttu-id="1afb8-p107">Si plusieurs contrôlés sont liés à « my:field1 », vous devez utiliser la surcharge [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) de la méthode **SelectText**, qui fournit un paramètre  _viewContext_ supplémentaire pour sélectionner un contrôle spécifique. L'exemple ci-dessous part du principe qu'il y a deux contrôles **Zone de texte** liés à « my:field1 », le premier contrôle possédant l'ID de contexte de vue « CTRL1 » et le second contrôle l'ID de contexte de vue « CTRL8 ». Le second contrôle est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1afb8-p107">If you have multiple controls bound to "my:field1", you must use the [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides an additional  _viewContext_ parameter to select a specific control. The following example assumes that there are two **Text Box** controls bound to "my:field1", with the first control having a ViewContext ID of "CTRL1" and the second control having a ViewContext ID of "CTRL8". The second control is selected.</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

<span data-ttu-id="1afb8-197">Dans l'exemple qui suit, la surcharge [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) de la méthode **SelectNodes**, qui fournit le seul paramètre  _startNode_, est utilisé pour sélectionner la première ligne d'un tableau extensif lié au groupe extensible « my:employee ».</span><span class="sxs-lookup"><span data-stu-id="1afb8-197">In the following example, the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides only one  _startNode_ parameter, is used to select the first row in a repeating table bound to the repeating group "my:employee".</span></span> 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

<span data-ttu-id="1afb8-p108">Vous pouvez également sélectionner plusieurs lignes dans un tableau extensible. Dans l'exemple qui suit, les trois premières lignes d'un tableau extensible lié au groupe extensible « my:employee » sont sélectionnées avec la surcharge [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) de la méthode **SelectNodes**, qui fournit les paramètres  _startNode_ et  _endNode_:</span><span class="sxs-lookup"><span data-stu-id="1afb8-p108">You can also select multiple rows in a repeating table. In the following example, the first three rows of a repeating table bound to the repeating group "my:employee" are selected using the [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides  _startNode_ and  _endNode_ parameters:</span></span> 
  
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


