---
title: Répondre aux événements de formulaire
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- order of events [infopath 207],events [InfoPath 2007], responding,events [InfoPath 2007], order,InfoPath 2007, reponding to events,EventArgs classes [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: 754db64b-179f-4385-8dd9-c20c9407b186
description: Vous pouvez écrire du code pour répondre à divers événements susceptibles de se produire pendant qu'un utilisateur remplit un formulaire. Pour utiliser les événements dans InfoPath, vous pouvez ajouter des gestionnaires d'événements lorsque vous travaillez sur un modèle de formulaire en mode Création.
ms.openlocfilehash: 2d835fce70bb7a882421509ff7dd950608226053
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62782821"
---
# <a name="respond-to-form-events"></a>Répondre aux événements de formulaire

Vous pouvez écrire du code pour répondre à divers événements susceptibles de se produire pendant qu'un utilisateur remplit un formulaire. Pour utiliser les événements dans InfoPath, vous pouvez ajouter des gestionnaires d'événements lorsque vous travaillez sur un modèle de formulaire en mode Création.
  
Les gestionnaires d'événements InfoPath doivent toujours être créés en mode Création, car InfoPath ajoute automatiquement la déclaration appropriée pour la réception de l'événement dans la méthode **InternalStartup** et insère le squelette du code du gestionnaire d'événements dans le fichier de code d'un formulaire (FormCode.cs ou FormCode.vb). Après avoir créé un gestionnaire d'événement, ne modifiez pas sa déclaration dans le fichier de code du formulaire. 
  
Pour plus d’informations sur la création des handlers d’événements InfoPath, voir [Add an Event Handler](how-to-add-an-event-handler.md).
  
## <a name="overview-of-the-event-classes"></a>Présentation des classes d'événements

Le modèle InfoPath fourni par l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) implémente trois classes qui mettent en œuvre les 12 événements pouvant survenir et être gérés par la logique métier du modèle de formulaire. Le tableau suivant contient la liste de tous les objets d'événements InfoPath, les événements auxquels ils sont associés et une description de leur fonction. 
  
|**Name**|**Événements**|**Description**|
|:-----|:-----|:-----|
|[ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) <br/> |[Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) <br/> |La classe **ButtonEvent** implémente l'événement **Clicked** lors d'un clic sur un contrôle **Bouton** dans un formulaire. |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) <br/> [Chargement](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) <br/> [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) <br/> [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) <br/> [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> [Envoyer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) <br/> [VersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.VersionUpgrade.aspx) <br/> [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) <br/> |La classe **FormEvents** implémente les événements spécifiques à un modèle de formulaire InfoPath lui-même :  <br/> **ContextChanged** <br/> Se produit après une modification du nœud de contexte. **Chargement** <br/> Se produit après le chargement du modèle de formulaire mais avant l'initialisation d'une vue quelconque. **Merge** <br/> Se produit lorsque la commande **Fusionner les formulaires** est invoquée à partir de l’interface utilisateur ou qu’InfoPath  `/aggregate` est démarré avec le commutateur de ligne de commande. **Save** <br/>  Se produit lorsque les commandes **Enregistrer** ou Enregistrer sous sont utilisées à partir de l’interface utilisateur ou lorsque les méthodes [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx) et [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) sont utilisées. **Sign** <br/> Se produit  une fois qu'un ensemble de données signées a été sélectionné pour une signature par l'intermédiaire de la boîte de dialogue **Signatures numériques**. **Envoyer** <br/> Se produit lorsque la commande **Envoyer** est utilisée à partir de l’interface utilisateur ou que la méthode [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) de la **classe XmlForm** est utilisée. **VersionUpgrade** <br/> Se produit lorsque le numéro de version du formulaire en cours d'ouverture est antérieur à celui du modèle de formulaire sur lequel il est basé. **ViewSwitched** <br/> Se produit lors d'un changement de vue réussi d'un formulaire. |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Modifié](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) <br/> [Modification](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) <br/> [Validation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) <br/> |Implémente les événements déclenchés par les modifications apportées aux données du document XML sous-jacent d'une instance de formulaire :  <br/> **Modifié** <br/> Se produit après l'acceptation des modifications dans le document XML sous-jacent d'un formulaire et à la suite de l'événement **Validating**. **Modification** <br/> Se produit après que des modifications ont été apportées au document XML sous-jacent d'un formulaire mais avant qu'elles aient été acceptées. **Validation** <br/> Se produit après l'acceptation des modifications effectuées dans le document XML sous-jacent d'un formulaire, mais avant l'événement **Changed**. La **classe XmlEvent** implémente également la propriété [RaiseUndoRedoForChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.RaiseUndoRedoForChanged.aspx) , qui obtient ou définit si l’événement **Changed** est déclenche lorsqu’une opération d’annuler ou de rétablissement se produit. |
   
> [!NOTE]
>  [!REMARQUE]  Les événements **Changed** et **Changing** ne se déclenchent que lorsqu'une modification est effectuée dans un champ non vide du formulaire, tandis que les événements comparables dans InfoPath 2003 et le modèle d'objet compatible InfoPath 2003 fourni par l'espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) ( [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) et [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) ) se déclenchent deux fois lorsqu'une modification est apportée à un champ non vide, lors de la suppression de l'ancienne valeur et lors de l'insertion de la nouvelle valeur. 
  
## <a name="overview-of-the-eventargs-classes"></a>Vue d'ensemble des classes EventArgs

Chacun des 12 événements ont un objet **EventArgs** associé à l'événement transmis au gestionnaire d'événements afin que l'événement fournisse des informations d'état et d'autres fonctionnalités qui peuvent être utilisées dans le code du gestionnaire d'événements. Le tableau suivant recense les événements InfoPath et les objets **EventArgs** associés, ainsi qu'une brève description des fonctionnalités fournies par les propriétés et les méthodes de l'objet. Pour plus d'informations sur les propriétés et les méthodes spécifiques de l'objet, cliquez sur le nom de l'objet **EventArgs** dans le tableau, puis cliquez sur le lien Membres dans la rubrique. 
  
|**Event**|**Classe EventsArgs**|**Description**|
|:-----|:-----|:-----|
|**Clicked** <br/> |[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |Obtient l'ID du contrôle. Obtient un objet **XPathNavigator** placé sur le nœud XML le plus au centre du document XML sous-jacent du formulaire qui contient le contrôle **Bouton**. |
|**ContextChanged** <br/> |[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |Obtient le type de modification de contexte qui a été effectué au moment où l'événement s'est produit. Obtient une valeur indiquant si l'événement de modification de contexte s'est produit en réponse à l'annulation ou au rétablissement d'une opération.  Obtient une référence à un élément **XPathNavigator** placé sur le nœud du contexte qui a déclenché l'événement.  |
|**Chargement** <br/> |[LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) <br/> |Spécifie la vue dans laquelle ouvrir le formulaire après le chargement. Obtient une référence à l'objet **XmlFormCancelEventArgs**. Obtient un **IDictionary** contenant tous les paramètres d’entrée spécifiés  `/InputParameters` à l’aide de l’option de ligne de commande, ou spécifié à l’aide de paramètres de requête dans une URL pour ouvrir le formulaire. |
|**Merge** <br/> |[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |Obtient une référence à l'objet **XmlFormCancelEventArgs**. Obtient le nombre de formulaires fusionnés dans une opération de fusion. Obtient l'index de base 0 du formulaire en cours de fusion. Obtient ou définit une valeur utilisée avec la propriété **Cancel** pour déterminer s'il faut uniquement annuler la fusion du formulaire actif ou toute l'opération de fusion.  Obtient un objet **XPathNavigator** placé au niveau du nœud racine du document XML sous-jacent du formulaire actuellement fusionné. |
|**Save** <br/> |[SaveEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.aspx) <br/> |Effectue l'opération d'enregistrement demandée par l'utilisateur. Obtient une référence à l'objet **SaveCancelEventArgs** qui peut être utilisé pour annuler l'événement. Obtient le nom de fichier à utiliser dans le gestionnaire d'événements correspondant à cet événement. Obtient les informations indiquant si l'opération d'enregistrement est de de type « Enregistrer » ou « Enregistrer sous ».  |
|**Sign** <br/> |[SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) <br/> |Obtient ou définit l'affichage de la boîte de dialogue **Signatures numériques**. Obtient le jeu de données à signer qui a déclenché l'événement. |
|**Envoyer** <br/> |[SubmitEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.aspx) <br/> |Obtient une référence à l'objet **XmlFormCancelEventArgs** pour annuler l'événement. |
|**VersionUpgrade** <br/> |[VersionUpgradeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.aspx) <br/> |Obtient une référence à l'objet **XmlFormCancelEventArgs** pour annuler l'événement. Obtient le numéro de version du document de formulaire mis à niveau. Obtient le numéro de version du modèle de formulaire associé au formulaire mis à niveau. |
|**ViewSwitched** <br/> |[ViewSwitchedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewSwitchedEventArgs.aspx) <br/> |La classe **ViewSwitchedEventArgs** ne fournit pas les propriétés et les méthodes associées aux événements autres que ceux qui sont hérités de **System.Object**. |
|**Modifié** <br/> |[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |Obtient un objet **XPathExpression** qui contient une expression XPath renvoyant le nœud actuellement modifié. Obtient la nouvelle valeur du nœud modifié. Obtient un objet **XPathNavigator** pointant sur le nœud qui est le parent du nœud en cours de suppression. Obtient la valeur d'origine du nœud modifié. Obtient [une éumération XmlOperation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.aspx) qui indique le type d’opération qui s’est produite lorsque le nœud a été modifié. Obtient un objet **XPathNavigator** pointant vers le nœud modifié. Obtient une valeur indiquant si le nœud modifié fait partie d'une opération d'annulation ou de rétablissement. |
|**Modification** <br/> |[XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) <br/> |Obtient un objet **XmlFormCancelEventArgs** associé à l'événement. Hérite de toutes les fonctionnalités énumérées ci-dessus pour l'objet **XmlEventArgs**. |
|**Validation** <br/> |[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |Crée un [objet FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) qui contient des informations d’erreur personnalisées avec les valeurs spécifiées et les ajoute à l’objet [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) du formulaire. Hérite de toutes les fonctionnalités énumérées ci-dessus pour l'objet **XmlEventArgs**. |
   
## <a name="using-the-eventargs-objects"></a>Utilisation des objets EventArgs

Lorsque vous créez un gestionnaire d'événements, InfoPath crée la déclaration de celui-ci dans le code de formulaire du projet. Dans cette déclaration, InfoPath utilise **e** comme nom du paramètre transmis au gestionnaire d'événements. Ce paramètre contient l'objet **EventArgs** qui est associé au gestionnaire d'événements pour fournir les informations d'état et d'autres fonctionnalités lorsque l'événement se produit. 
  
Par exemple, lorsque vous créez un gestionnaire d'événements pour l'événement **Loading** en mode Création (en cliquant sur le menu **Événement Chargement en cours (Loading)** sous l'onglet **Développeur**), InfoPath ajoute la déclaration du gestionnaire d'événements qui reçoit l'objet [LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) au fichier de code du formulaire, puis ouvre l'éditeur de code pour vous permettre d'ajouter votre code à la déclaration de gestionnaire d'événements qui suit. 
  
```cs
public void FormEvents_Loading(object sender, LoadingEventArgs e)
{
   // Write your code here.
}
```

```vb
Public Sub FormEvents_Loading(ByVal sender As Object, _
   ByVal e As LoadingEventArgs)
   ' Write your code here.
End Sub
```

Lorsque vous écrivez du code pour un gestionnaire d'événements, vous pouvez utiliser les propriétés et les méthodes implémentées par l'objet **EventArgs** transmis par le paramètre **e**. Par exemple, dans le gestionnaire d'événements **Changing** suivant, la propriété [NewValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.NewValue.aspx) de l'objet [XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) (hérité de la classe [XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) ) permet de vérifier la valeur du champ qui vient d'être modifié. Si l'utilisateur a modifié ce champ et l'a laissé vide, la propriété [Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.Message.aspx) de la classe [XmlFormCancelEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.aspx) est accessible à l'aide de la propriété [CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.CancelableArgs.aspx) de l'objet **XmlChangingEventArgs** pour afficher une erreur pour l'utilisateur, et la propriété **XmlFormCancelEventArgs.Cancel** est définie sur **true** pour annuler l'événement et les modifications entrées par l'utilisateur.
  
```cs
public void field1_Changing(object sender, LoadingEventArgs e)
{
   // Determine whether there is a new value.
   if (e.NewValue == "")
   {
      // The value is blank, so display an error message
      // and roll back the changes.
      e.CancelableArgs.Message = 
         "You must supply a value for this field.";
      e.CancelableArgs.Cancel = true;
      return;
   }
}
```

```vb
Public Sub field1_Changing(ByVal sender As Object, _
   ByVal e As LoadingEventArgs)
   ' Determine whether there is a new value.
   If (e.NewValue = "") Then
      ' The value is blank, so display an error message 
      ' and roll back the changes.
      e.CancelableArgs.Message = _
         "You must supply a value for this field."
      e.CancelableArgs.Cancel = True
      Return
   End If
End Sub
```


