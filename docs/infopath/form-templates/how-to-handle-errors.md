---
title: Gérer les erreurs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- errors [infopath 2007], handling,FormErrorCollection [InfoPath 2007],InfoPath 2007, error handling,FormError [InfoPath 2007],error handling [InfoPath 2007]
localization_priority: Normal
ms.assetid: 132cb698-d9a5-4767-b3d1-5dd1343a1ff4
description: Lors de la création d'applications personnalisées, les développeurs doivent mettre en place une gestion des erreurs impliquant l'écriture du code de programmation qui leur permette de déceler les erreurs générées par l'application ou de créer et de générer des erreurs personnalisées. Le modèle objet InfoPath fourni par l'espace de noms Microsoft.Office.InfoPath prend en charge la gestion des erreurs par le biais de l'utilisation de la classe FormError en association avec la classe FormErrorCollection .
ms.openlocfilehash: 30cf649188b7e4cbc35469d2a50540bb13ecb38d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410776"
---
# <a name="handle-errors"></a>Gérer les erreurs

Lors de la création d'applications personnalisées, les développeurs doivent mettre en place une gestion des erreurs impliquant l'écriture du code de programmation qui leur permette de déceler les erreurs générées par l'application ou de créer et de générer des erreurs personnalisées. Le modèle objet InfoPath fourni par l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) prend en charge la gestion des erreurs par le biais de l'utilisation de la classe [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) en association avec la classe [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . 
  
Dans InfoPath, des erreurs peuvent se produire pour les raisons suivantes :
  
- En cas d'échec de la validation de schéma XML pour des données entrées dans un formulaire.
    
- En cas d'échec d'une contrainte de validation personnalisée.
    
- Lorsqu'une erreur est générée par la méthode [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) de l'objet d'événement [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) . 
    
- Lorsqu'une erreur utilisateur est créée au moyen de la méthode [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) de la classe [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . 
    
## <a name="overview-of-the-formerrorcollection-class"></a>Présentation de la classe FormErrorCollection

La classe [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) fournit aux développeurs de formulaires les méthodes et les propriétés suivantes pour gérer les objets [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) que contient la collection. 
  
|**Nom**|**Description**|
|:-----|:-----|
|[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) , méthode (+ 3 Overloads)  <br/> |Crée un objet **FormError** et l'ajoute à la collection.  <br/> |
|[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) , méthode (+ 1 Overload)  <br/> |Supprime de la collection l'erreur spécifiée définie par l'utilisateur.  <br/> |
|[DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx) , méthode  <br/> |Supprime tous les objets **FormError** contenus dans la collection.  <br/> |
|[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) (+ 1 surcharge)  <br/> |Renvoie tous les objets **FormError** du nom ou du type spécifié dans la collection.  <br/> |
|Propriété [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx)  <br/> |Extrait le nombre d'objets **FormError** contenus dans la collection.  <br/> |
|Propriété [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx)  <br/> |Extrait une référence à un objet **FormError** en fonction du numéro d'index spécifié.  <br/> |
   
## <a name="overview-of-the-formerror-class"></a>Présentation de la classe FormError

La classe [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) fournit aux développeurs de formulaires les propriétés suivantes pour accéder aux informations relatives à l'erreur qui vient de se produire. 
  
|**Nom**|**Description**|
|:-----|:-----|
|[DetailedMessage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx) , propriété  <br/> |Récupère ou définit le message d'erreur détaillé de l'objet **FormError**.  <br/> |
|[ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx) , propriété  <br/> |Récupère ou définit le code d'erreur de l'objet **FormError**.  <br/> |
|Propriété [site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)  <br/> |Récupère un objet **XPathNavigator** qui est placé au niveau du nœud associé à l'objet **FormError**.  <br/> |
|[Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx) , propriété  <br/> |Récupère ou définit le message d'erreur court de l'objet **FormError**.  <br/> |
|[FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx) , propriété  <br/> |Récupère le type de l'objet **FormError**.  <br/> |
   
## <a name="using-the-formerrorcollection-and-formerror-classes"></a>Utilisation des classes FormErrorCollection et FormError

L'objet **FormErrorCollection** associé à un formulaire est accessible par le biais de la propriété [Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) de l'objet [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . L'objet **FormErrorCollection** est associé au document XML sous-jacent d'un formulaire, de sorte que lorsqu'une erreur se produit, celui-ci et toutes les erreurs supplémentaires sont accessibles et peuvent être gérées à partir du document XML actuel. L'exemple suivant illustre l'utilisation d'une boucle pour vérifier les erreurs pouvant exister dans le document XML sous-jacent d'un formulaire. En cas d'erreur, la fonction effectue une boucle dans chacune d'elle et affiche une boîte de message au moyen de la propriété **Message** de l'objet **FormError**. 
  
```cs
public void CheckErrors(XPathNavigator xmlNode)
{
   foreach(FormError err in this.Errors)
   {
      if(xmlNode.InnerXml == err.Site.InnerXml)
         MessageBox.Show("The following error has occured: "
             + err.Message);
   }
}
```

```vb
Public Sub CheckErrors(ByVal xmlNode As XPathNavigator)
   Dim err As FormError
   For Each err In Me.Errors
      If xmlNode.InnerXml = err.Site.InnerXml Then
         MessageBox.Show("The following error has occured: " _
             &amp; err.Message)
   End If
End Sub
```

La fonction précédente peut être appelée à partir de l'un des gestionnaires d'événements de validation des données du formulaire. Par exemple, lorsqu'elle est utilisée dans le gestionnaire d'événements pour l'événement [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) d'un champ dans le formulaire, l'appel de la fonction transmet l'argument de nœud XML au moyen de la propriété [Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) de l'objet événement [XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) comme suit. 
  
```cs
CheckErrors(e.Site);
```

```vb
CheckErrors(e.Site)
```

Outre la gestion des erreurs générées par InfoPath, les développeurs de formulaires peuvent également générer des erreurs personnalisées grâce à la méthode [ReportError(XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) de l'objet d'événement [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) ou à la méthode [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) de la classe [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) . Pour plus d'informations sur l'utilisation des méthodes [ReportError(XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) ou [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) , cliquez sur les liens correspondants au début de cette rubrique. 
  
## <a name="handling-managed-code-exceptions"></a>Gestion des exceptions de code managé

Vous pouvez utiliser la gestion d'exceptions try-catch pour gérer les exceptions qui apparaissent dans le modèle de formulaire avec code managé tel qu'illustré par l'exemple de code ci-dessous.
  
```cs
FileQueryConnection queryXMLFile = 
   (FileQueryConnection)this.DataConnections["form1"];
// Perform the query.
try
{
   queryXMLFile.Execute();
}
catch (Exception ex)
{
   MessageBox.Show("Failed to query." + System.Environment.NewLine 
      + ex.Message);
}
```

```vb
Dim queryXMLFile As FileQueryConnection = _
   DirectCast(Me.DataConnections("form1"), FileQueryConnection)
' Perform the query.
Try
   queryXMLFile.Execute();
Catch ex As Exception
   MessageBox.Show("Failed to query." &amp; System.Environment.NewLine 
      &amp; ex.Message)
End Try
```

Si vous n'utilisez pas la gestion d'exceptions try-catch dans le code du formulaire, InfoPath affiche des informations sur les exceptions non gérées dans la boîte de dialogue d'erreurs d'InfoPath lors du débogage et de l'aperçu. De plus, par défaut, les exceptions non gérées ne sont pas affichées dans la boîte de dialogue d'erreurs d'InfoPath lors de l'exécution lorsque vous déployez votre modèle de formulaire avec code managé. Pour afficher des informations sur les exceptions non gérées à l'exécution, utilisez la procédure suivante.
  
### <a name="enable-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Activation des notifications pour les exceptions de code managé non gérées lors de l'exécution

1. Ouvrez le Concepteur InfoPath, puis cliquez sur l'onglet **Fichier**. 
    
2. Cliquez sur **Options**, puis sur **Options InfoPath** dans la catégorie **Général**. 
    
3. Sous l'onglet **Avancé**, activez la case à cocher **Afficher une notification pour les erreurs de code Visual Basic et C#**. 
    

