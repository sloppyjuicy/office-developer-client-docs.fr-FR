---
title: Gérer les erreurs à l'aide du modèle objet InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, handling errors,InfoPath 2003-compatible form templates, error handling,form templates [InfoPath 2007], error handling,error handling [InfoPath 2007], InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: eeb05205-d6f4-4931-b9a9-55a663bb1a25
description: Lors de la création d'applications personnalisées, les développeurs doivent mettre en place une gestion des erreurs impliquant l'écriture de code de programmation qui leur permette de déceler les erreurs générées par l'application ou de créer et de générer des erreurs personnalisées. Le modèle objet compatible avec InfoPath 2003 prend en charge la gestion des erreurs à travers l'utilisation de l'objet ErrorObject en association avec la collection ErrorsCollection .
ms.openlocfilehash: 93991e33d8867f89454bec08b41ba83e98ab0a17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439477"
---
# <a name="handle-errors-using-the-infopath-2003-object-model"></a>Gérer les erreurs à l'aide du modèle objet InfoPath 2003

Lors de la création d'applications personnalisées, les développeurs doivent mettre en place une gestion des erreurs impliquant l'écriture de code de programmation qui leur permette de déceler les erreurs générées par l'application ou de créer et de générer des erreurs personnalisées. Le modèle objet compatible avec InfoPath 2003 prend en charge la gestion des erreurs à travers l'utilisation de l'objet [ErrorObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorObject.aspx) en association avec la collection [ErrorsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) . 
  
Dans InfoPath, une erreur se produit lorsque des données entrées dans un formulaire échouent à la validation du schéma XML, lorsqu'une contrainte de validation personnalisée échoue, lorsqu'une erreur est générée par la méthode [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReportError.aspx) de l'objet [DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) , ou lorsqu'une erreur est générée via la méthode [Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx) de la collection [ErrorsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) . 
  
## <a name="overview-of-the-errorscollection-collection"></a>Vue d'ensemble de la collection ErrorsCollection

La collection **ErrorsCollection** fournit aux développeurs les méthodes et les propriétés suivantes pour gérer les objets **ErrorObject** que contient la collection. 
  
|**Nom**|**Description**|
|:-----|:-----|
|Méthode[Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx)  <br/> |Crée un objet **ErrorObject** et l'ajoute à la collection.  <br/> |
|Méthode [Delete](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Delete.aspx)  <br/> |Supprime tous les objets **ErrorObject** associés au nœud XML et au nom de la condition spécifiés, sauf pour les erreurs personnalisées ajoutées à l'aide de la méthode **ReportError**.  <br/> |
|[DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.DeleteAll.aspx) , méthode  <br/> |Supprime tous les objets **ErrorObject** contenus dans la collection.  <br/> |
|Propriété [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Count.aspx)  <br/> |Récupère le nombre d'objets **ErrorObject** contenus dans la collection.  <br/> |
|Propriété [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Item.aspx)  <br/> |Récupère une référence à un objet **ErrorObject** en fonction du numéro d'index spécifié.  <br/> |
   
## <a name="overview-of-the-errorobject-object"></a>Vue d'ensemble de l'objet ErrorObject

L'objet **ErrorObject** fournit les propriétés suivantes, que les développeurs de formulaires peuvent utiliser pour accéder aux informations relatives à l'erreur qui vient de se produire. 
  
|**Nom**|**Description**|
|:-----|:-----|
|Propriété [ConditionName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ConditionName.aspx)  <br/> |Récupère le nom de l'erreur ou renvoie **null**, en fonction du type de l'objet **ErrorObject**.  <br/> |
|[DetailedErrorMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.DetailedErrorMessage.aspx) , propriété  <br/> |Récupère ou définit le message d'erreur détaillé de l'objet **ErrorObject**.  <br/> |
|[ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorCode.aspx) , propriété  <br/> |Récupère ou définit le code d'erreur de l'objet **ErrorObject**.  <br/> |
|[Node](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.Node.aspx) , propriété  <br/> |Récupère une référence au nœud XML associé à l'objet **ErrorObject**.  <br/> |
|[ShortErrorMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ShortErrorMessage.aspx) , propriété  <br/> |Récupère ou définit le message d'erreur court de l'objet **ErrorObject**.  <br/> |
|[ErrorType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorType.aspx) , propriété  <br/> |Récupère le type de l'objet **ErrorObject**.  <br/> |
   
## <a name="using-the-errorscollection-and-errorobject"></a>Utilisation de ErrorsCollection et ErrorObject

La collection **ErrorsCollection** est accessible via la propriété [Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.Errors.aspx) de l'objet [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) . La collection **ErrorsCollection** est associée au document XML sous-jacent du formulaire de sorte que lorsqu'une erreur se produit, elle se produit dans le document XML. L'exemple qui suit démontre comment une boucle Visual C# **foreach** peut être utilisée pour vérifier la présence d'erreur dans le document XML sous-jacent d'un formulaire. S'il existe des erreurs, la fonction crée une boucle autour d'elles et, à l'aide de la propriété **ShortErrorMessage** de l'objet **ErrorObject**, affiche un message pour l'utilisateur. 
  
```cs
public void CheckErrors(IXMLDOMNode xmlNode)
{
   foreach(ErrorObject err in thisXDocument.Errors)
   {
      if(xmlNode==err.Node)
         thisXDocument.UI.Alert("The following error has occured: "
             + err.ShortErrorMessage + ".");
   }
}
```

La fonction précédente peut être appelée à partir d'un des gestionnaires d'événements de validation des données du formulaire. Par exemple, lorsqu'il est utilisé dans le gestionnaire d'événements [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) d'un champ du formulaire, l'appel à la fonction transmet l'argument du nœud XML à l'aide de la propriété [Site](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.Site.aspx) de l'objet [DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) comme suit : 
  
```cs
CheckErrors(e.Site);
```

En plus de gérer les erreurs générées par InfoPath, les développeurs de formulaires peuvent générer des erreurs personnalisées grâce à la méthode **ReportError** de l'objet **DataDOMEventObject** ou à la méthode **Add** de la collection **ErrorsCollection**. Pour plus d'informations sur l'utilisation des méthodes **ReportError** ou **Add**, cliquez sur celles-ci au début de cette rubrique. 
  
## <a name="handling-managed-code-exceptions"></a>Gestion des exceptions de code managé

Vous pouvez utiliser la gestion d'exceptions try-catch pour gérer les exceptions qui apparaissent dans le modèle de formulaire avec code managé tel qu'illustré par l'exemple de code ci-dessous.
  
```cs
DataAdapters dataAdapters;
dataAdapters = thisXDocument.DataAdapters; 
XMLFileAdapterObject queryXMLFile = 
   (XMLFileAdapterObject)dataAdapters["form1"];
// Perform the query.
try
{
   queryXMLFile.Query();
}
catch (Exception ex)
{
   thisXDocument.UI.Alert("Failed to query.\n\n" + ex.Message);
}
// Perform the submit.
try
{
   queryXMLFile.Submit();
}
catch (Exception ex)
{
   thisXDocument.UI.Alert("Failed to submit.\n\n" + ex.Message);
}
```

Si vous n'utilisez pas la gestion d'exceptions try-catch dans le code du formulaire, InfoPath affiche des informations sur les exceptions non gérées dans la boîte de dialogue d'erreurs d'InfoPath lors du débogage et de l'aperçu. 
  

