---
title: Utiliser des vues à l’aide du modèle objet InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, views,views [InfoPath 2007], InfoPath 2003-compatible form templates
ms.localizationpriority: medium
ms.assetid: feb1bfcb-1cb1-4d5c-bc84-df86a33a5934
description: Lorsque vous utilisez un modèle de formulaire InfoPath, vous pouvez écrire du code pour accéder aux vues du formulaire, puis exécuter différentes actions sur les données qu'elles contiennent. Le modèle objet compatible InfoPath 2003 prend en charge l'accès aux vues d'une forme à travers l'utilisation des membres de l'interface ViewObject .
ms.openlocfilehash: 4273ebadcf2b90cc865814f3896e3c1c9710f0de
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557448"
---
# <a name="work-with-views-using-the-infopath-2003-object-model"></a>Utiliser des vues à l’aide du modèle objet InfoPath 2003

Lorsque vous utilisez un modèle de formulaire InfoPath, vous pouvez écrire du code pour accéder aux vues du formulaire, puis exécuter différentes actions sur les données qu'elles contiennent. Le modèle objet compatible InfoPath 2003 prend en charge l'accès aux vues d'une forme à travers l'utilisation des membres de l'interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) . 
  
## <a name="overview-of-the-viewobject-interface"></a>Vue d'ensemble de l'interface ViewObject

L'interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) offre aux développeurs de formulaires les méthodes et les propriétés ci-dessous pour interagir avec une vue InfoPath. 
  
> [!NOTE]
> [!REMARQUE] Les méthodes et propriétés de l'interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) ne sont pas disponibles au cours de l'événement [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) . 
  
|**Name**|**Description**|
|:-----|:-----|
|[Méthode DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.DisableAutoUpdate.aspx)  <br/> |Désactive la synchronisation du DOM (Document Object Model) XML et de la vue.  <br/> |
|[Méthode EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.EnableAutoUpdate.aspx)  <br/> |Active la synchronisation du DOM XML et de la vue.  <br/> |
|[ExecuteAction,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ExecuteAction.aspx) méthode  <br/> |Exécute une action d'édition InfoPath.  <br/> |
|[Export,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Export.aspx) méthode  <br/> |Exporte la vue en tant que fichier au format spécifié.  <br/> |
|[Méthode ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ForceUpdate.aspx)  <br/> |Synchronise le DOM XML et la vue.  <br/> |
|[Méthode GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetContextNodes.aspx)  <br/> |Renvoie une référence à l’interface [XMLNodesCollection,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLNodesCollection.aspx) en fonction du nœud XML spécifié et du contexte d’affichage ou de la sélection actuelle dans l’affichage.  <br/> |
|[Méthode GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetSelectedNodes.aspx)  <br/> |Renvoie une référence à l'interface **XMLNodesCollection**, sur la base de la sélection en cours dans la vue.  <br/> |
|[SelectNodes,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) méthode  <br/> |Sélectionne une plage de nœuds XML dans la vue.  <br/> |
|[SelectText,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectText.aspx) méthode  <br/> |Sélectionne le texte contenu dans le nœud XML spécifié de la vue.  <br/> |
|[SwitchView,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SwitchView.aspx) méthode  <br/> |Bascule le formulaire InfoPath vers la vue spécifiée.  <br/> |
|Propriété [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Name.aspx)  <br/> |Renvoie une valeur chaîne indiquant le nom de la vue active.  <br/> |
|[Window,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) propriété  <br/> |Renvoie une référence à [l’interface WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) qui accède à **la fenêtre** associée à la vue.  <br/> |
   
> [!NOTE]
> [!REMARQUE] Le modèle objet compatible InfoPath 2003 fournit également l'interface [ViewInfosCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfosCollection.aspx) qui peut être utilisée pour obtenir des informations sur toutes les vues mises en œuvre dans un formulaire. 
  
## <a name="using-the-viewobject-interface"></a>Utilisation de l'interface ViewObject

L'interface [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) est accessible via la propriété [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) de l'interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) (accessible via la variable  `thisXDocument` initialisée dans la méthode  `_Startup` de la classe du code du formulaire). L'exemple de code suivant vous montre comment utiliser la méthode [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) de l'interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) pour afficher une boîte de message indiquant le nom de la vue active associée au document XML sous-jacent d'un formulaire. 
  
```cs
thisXDocument.UI.Alert("Current view name: " + 
   thisXDocument.View.Name);
```

```vb
thisXDocument.UI.Alert("Current view name: " &amp; _
   thisXDocument.View.Name)
```

Un formulaire InfoPath contient au moins une vue par défaut. Toutefois, InfoPath prend également en charge la création de plusieurs vues du document XML sous-jacent d'un formulaire. Lorsqu'un formulaire possède plusieurs vues, vous pouvez avoir recours à l'objet **View** pour utiliser la vue actuellement active. Vous pouvez modifier la vue active par programme à l'aide de la méthode **SwitchView** de l'objet **View**, comme illustré dans le code suivant : 
  
```cs
thisXDocument.View.SwitchView("MySecondView");
```

```vb
thisXDocument.View.SwitchView("MySecondView")
```

L'exemple précédent de basculement d'une vue fonctionne uniquement une fois le formulaire ouvert. Pour définir une vue par défaut au cours de l'événement **OnLoad**, utilisez la propriété [IsDefault](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.IsDefault.aspx) de l'interface [ViewInfoObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfoObject.aspx) , telle qu'elle est représentée dans l'exemple suivant. 
  
```cs
thisXDocument.ViewInfos["MyDefaultView"].IsDefault = true;
```

```vb
thisXDocument.ViewInfos("MyDefaultView").IsDefault = True
```


