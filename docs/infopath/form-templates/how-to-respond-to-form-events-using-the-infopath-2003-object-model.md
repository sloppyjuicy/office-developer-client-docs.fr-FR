---
title: Répondre aux événements de formulaire à l'aide du modèle objet InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- form templates [infopath 2007], responding to events,InfoPath 2003-compatible form templates, responding to form events
localization_priority: Normal
ms.assetid: 59e9c1ed-32a8-4bcd-bdfc-9aa568a34d2a
description: Vous pouvez écrire du code pour répondre à différents événements qui se produisent lorsqu'un utilisateur remplit un formulaire. Pour utiliser des événements dans InfoPath, vous créez des gestionnaires d'événements dans le Concepteur InfoPath.
ms.openlocfilehash: b7347f882df991e64bdf4e76c471b1220a84dc58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433492"
---
# <a name="respond-to-form-events-using-the-infopath-2003-object-model"></a>Répondre aux événements de formulaire à l'aide du modèle objet InfoPath 2003

Vous pouvez écrire du code pour répondre à différents événements qui se produisent lorsqu'un utilisateur remplit un formulaire. Pour utiliser des événements dans InfoPath, vous créez des gestionnaires d'événements dans le Concepteur InfoPath.
  
Les gestionnaires d'événements InfoPath doivent être créés dans le Concepteur InfoPath car, lors de l'utilisation du modèle objet compatible InfoPath 2003, InfoPath ajoute automatiquement la déclaration appropriée et applique un attribut ([InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) dans le fichier de code de formulaire (FormCode.cs ou FormCode.vb) pour identifier et réceptionner le gestionnaire d'événements. Après avoir créé un gestionnaire d'événements, vous ne devez pas modifier sa déclaration et son attribut dans le fichier de code du formulaire. 
  
Pour plus d'informations sur la création de gestionnaires d'événements InfoPath, voir [Ajouter un gestionnaire d'événements à l'aide du modèle objet infopath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="overview-of-the-event-objects"></a>Vue d'ensemble des objets d'événement

Le modèle objet compatible InfoPath 2003 implémente neuf objets exposés dans l'espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . Le tableau ci-dessous contient une description de chacun des neuf événements InfoPath, en indiquant les gestionnaires d'événements qui lui sont associés. 
  
|**Nom**|**Gestionnaires d’événements**|**Description**|
|:-----|:-----|:-----|
|[DataDOMEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.aspx) <br/> |[OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) <br/> [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) , [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) <br/> |Renvoie une référence au document XML sous-jacent d'un formulaire, le statut de renvoi et d'autres propriétés contenant des informations relatives au nœud XML lors d'un changement de DOM (Document Object Model) XML. Comprend également une méthode pour générer une erreur.  <br/> |
|[DocActionEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocActionEvent.aspx) <br/> |[OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) <br/> |Renvoie une référence au document XML sous-jacent d'un formulaire, le statut de renvoi et le nœud XML source lors d'un clic de bouton dans la zone du formulaire.  <br/> |
|[DocContextChangeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocContextChangeEvent.aspx) <br/> |[OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx) <br/> |Renvoie des informations relatives au nœud DOM (Document Object Model) XML qui est le contexte actuel du document XML sous-jacent du formulaire.  <br/> |
|[DocEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocEvent.aspx) <br/> |[OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx) , [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) <br/> |Renvoie une référence au document XML sous-jacent d'un formulaire lors d'une opération de changement de vue ou de fusion de formulaires.  <br/> |
|[DocReturnEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocReturnEvent.aspx) <br/> |[OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) , [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) <br/> |Renvoie une référence au document XML sous-jacent du formulaire accompagnée du statut de renvoi lors du chargement ou de l'envoi d'un formulaire.  <br/> |
|[MergeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MergeEvent.aspx) <br/> |[OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) <br/> |Renvoie des propriétés et des méthodes qui peuvent être utilisées durant un événement **OnMergeRequest** pour interagir par programme avec le document XML sous-jacent d'un formulaire et déterminer des propriétés de fusion telles que le nombre de fichiers fusionnés.  <br/> |
|[SaveEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SaveEvent.aspx) <br/> |[OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) <br/> |Renvoie un certain nombre de propriétés et de méthodes qui peuvent être utilisées durant une opération d'enregistrement à partir du gestionnaire d'événements **OnSaveRequest**, afin d'interagir par programme avec le document XML sous-jacent d'un formulaire, de déterminer les propriétés d'enregistrement et d'effectuer l'opération d'enregistrement.  <br/> |
|[SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) <br/> |[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |Utilisé pour ajouter des données supplémentaires à la signature numérique.  <br/> |
|[VersionUpgradeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.VersionUpgradeEvent.aspx) <br/> |[OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) <br/> |Renvoie une référence au document XML sous-jacent d'un formulaire, le statut de renvoi et les numéros de version du document et de la solution lors d'une opération de mise à niveau de la version.  <br/> |
   
## <a name="using-the-event-objects"></a>Utilisation des objets d'événement

Lorsque vous créez un gestionnaire d'événements, InfoPath crée la déclaration de celui-ci dans le fichier de code de formulaire du projet (FormCode.cs ou FormCode.vb). Dans cette déclaration, InfoPath utilise **e** comme nom du paramètre transmis au gestionnaire d'événements. Ce paramètre contient l'objet d'événement associé au gestionnaire d'événements. 
  
Par exemple, lorsque vous créez un gestionnaire d'événements pour l'événement **OnLoad** en mode Création (en cliquant sur **Événement Sur chargement (OnLoad)** sous l'onglet **Développeur**), InfoPath ajoute la déclaration du gestionnaire d'événements qui reçoit l'objet **DocReturnEvent** au fichier de code du formulaire, puis ouvre l'éditeur de code pour vous permettre d'ajouter votre code à la déclaration de gestionnaire d'événements qui suit. 
  
```cs
// The following function handler is created by Microsoft Office 
// InfoPath. Do not modify the type or number of arguments.
[InfoPathEventHandler(EventType=InfoPathEventType.OnLoad)]
public void FormEvents_OnLoad(DocReturnEvent e)
{
   // Write your code here.
}
```

```vb
' The following function handler is created by Microsoft Office 
' InfoPath. Do not modify the type or number of arguments.
<InfoPathEventHandler(EventType:=InfoPathEventType.OnLoad)> _
Public Sub FormEvents_OnLoad(ByVal e As DocReturnEvent)
   ' Write your code here.
End Sub
```

Lorsque vous écrivez du code pour un gestionnaire d'événements, vous pouvez utiliser les propriétés et les méthodes implémentées par l'objet d'événement transmis par le paramètre **e**. Par exemple, dans le gestionnaire d'événements **OnBeforeChange** qui suit, la propriété [NewValue](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.NewValue.aspx) de l'objet d'événement **DataDOMEvent** est utilisée pour la vérification de la valeur du champ qui vient d'être modifié. S'il est vide, la propriété [ReturnMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnMessage.aspx) de l'objet d'événement **DataDOMEvent** est utilisée pour afficher une erreur dans une boîte de dialogue et la propriété [ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnStatus.aspx) est définie sur **false**, ce qui indique que les modifications de l'utilisateur ne doivent pas être acceptées.
  
```cs
[InfoPathEventHandler(MatchPath="/my:myFields/my:field1", 
    EventType=InfoPathEventType.OnBeforeChange)]
public void field1_OnBeforeChange(DataDOMEvent e)
{
   // Determine whether there is a new value.
   if ((string)e.NewValue == "")
   {
      // The value is blank, so display an error message and roll
      // back the changes.
      e.ReturnMessage = "You must supply a value for this field.";
      e.ReturnStatus = false;
      return;
   }
}
```

```vb
<InfoPathEventHandler(MatchPath:="/my:myFields/my:field1", _ EventType:=InfoPathEventType.OnBeforeChange)> _
Public Sub field1_OnBeforeChange(ByVal e As DataDOMEvent)
   ' Determine whether there is a new value.
   If (e.NewValue = "") Then
      ' The value is blank, so display an error message and roll back
      ' the changes.
      e.ReturnMessage = "You must supply a value for this field."
      e.ReturnStatus = False
      Return
   End If
End Sub
```

> [!NOTE]
> [!REMARQUE] Chaque objet d'événement InfoPath du modèle objet compatible avec InfoPath 2003 implémente différentes propriétés et méthodes. Pour plus d'informations sur un objet d'événement en particulier, cliquez dessus dans le tableau Objets d'événement présenté plus haut. 
  

