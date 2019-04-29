---
title: Accéder aux données de formulaire en utilisant le modèle objet InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- xdocument interface [infopath 2007],InfoPath 2003-compatible form templates, accessing form data,XDocumentsCollection interface [InfoPath 2007]
localization_priority: Normal
ms.assetid: e0731014-f454-4417-9f90-19f3387f5776
description: Pour rendre un formulaire InfoPath plus performant, il est souvent nécessaire d'accéder par programme aux informations sur le document XML sous-jacent du formulaire et aux données qu'il contient ou d'exécuter certaines actions sur le document XML. Le modèle objet d'InfoPath prend en charge l'accès et la manipulation du document XML sous-jacent d'un formulaire grâce à l'utilisation de l'interface XDocument en combinaison avec l'interface XDocumentsCollection .
ms.openlocfilehash: 803122c6c377686a85f11cf48b76876c056f2ec1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416474"
---
# <a name="access-form-data-using-the-infopath-2003-object-model"></a>Accéder aux données de formulaire en utilisant le modèle objet InfoPath 2003

Pour rendre un formulaire InfoPath plus performant, il est souvent nécessaire d'accéder par programme aux informations sur le document XML sous-jacent du formulaire et aux données qu'il contient ou d'exécuter certaines actions sur le document XML. Le modèle objet d'InfoPath prend en charge l'accès et la manipulation du document XML sous-jacent d'un formulaire grâce à l'utilisation de l'interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) en combinaison avec l'interface [XDocumentsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocumentsCollection.aspx) . 
  
L'interface **XDocument** est l'un des types les plus utiles du modèle objet d'InfoPath parce qu'il fournit un éventail de propriétés, de méthodes et d'événements qui non seulement interagissent avec le document XML sous-jacent d'un formulaire, mais exécutent aussi la plupart des actions disponibles dans l'interface utilisateur d'InfoPath. Dans un projet avec code managé créé avec le modèle objet compatible avec InfoPath 2003, une variable de type **XDocument** appelée  `thisXDocument` est automatiquement définie dans la méthode  `_StartUp` de la classe qui contient les gestionnaires d'événements dans le code de formulaire de votre projet. Vous pouvez utiliser la variable  `thisXDocument` dans le code du formulaire pour accéder à l'interface **XDocument** et à ses membres. 
  
## <a name="overview-of-the-xdocumentscollection-interface"></a>Vue d'ensemble de l'interface XDocumentsCollection

L'interface **XDocumentsCollection** fournit aux développeurs de formulaires les méthodes et les propriétés suivantes pour gérer les objets **XDocument** que contient la collection. 
  
|**Nom**|**Description**|
|:-----|:-----|
|Méthode [Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Close.aspx)  <br/> |Ferme le formulaire spécifié.  <br/> |
|[New](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.New.aspx) , méthode  <br/> |Crée un nouveau formulaire basé sur un formulaire existant.  <br/> |
|[NewFromSolution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolution.aspx) , méthode  <br/> |Crée un nouveau formulaire basé sur un formulaire existant.  <br/> |
|[NewFromSolutionWithData](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolutionWithData.aspx) , méthode  <br/> |Crée un formulaire InfoPath en utilisant le modèle de formulaire et les données XML spécifiés.  <br/> |
|[Open](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Open.aspx) , méthode  <br/> |Ouvre le formulaire spécifié.  <br/> |
|Propriété [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Count.aspx)  <br/> |Renvoie le nombre d'objets **XDocument** que contient la collection.  <br/> |
|Propriété [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Item.aspx)  <br/> |Renvoie une référence à l'objet **XDocument** spécifié.  <br/> |
   
## <a name="overview-of-the-xdocument-interface"></a>Vue d'ensemble de l'interface XDocument

L'interface **XDocument** fournit aux développeurs de formulaires les méthodes et les propriétés suivantes pour interagir et exécuter des actions sur le document XML sous-jacent d'un formulaire. 
  
|**Nom**|**Description**|
|:-----|:-----|
|Méthode [GetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDataVariable.aspx)  <br/> |Renvoie la valeur chaîne d'une variable de données spécifiée.  <br/> |
|[GetDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDOM.aspx) , méthode  <br/> |Renvoie une référence au DOM (Document Object Model) XML associé à l'objet **DataObject** spécifié.  <br/> |
|[ImportFile](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ImportFile.aspx) , méthode  <br/> |Importe (ou fusionne) le formulaire spécifié dans le formulaire actif.  <br/> |
|[PrintOut](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.PrintOut.aspx) , méthode  <br/> |Imprime la vue actuelle d'un formulaire.  <br/> |
|[Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Query.aspx) , méthode  <br/> |Récupère les données de l'adaptateur de données associé à un formulaire.  <br/> |
|Méthode [Save](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Save.aspx)  <br/> |Enregistre le formulaire actif.  <br/> |
|Méthode [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SaveAs.aspx)  <br/> |Enregistre le formulaire actif sous le nom spécifié.  <br/> |
|[SetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SetDataVariable.aspx) , méthode  <br/> |Définit la valeur d'une variable de données spécifiée.  <br/> |
|[Submit](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Submit.aspx) , méthode  <br/> |Envoie un formulaire selon les paramètres définis en mode Création.  <br/> |
|[DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) , propriété  <br/> |Renvoie une référence à la collection **DataObjects**.  <br/> |
|[DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) , propriété  <br/> |Renvoie une référence au DOM XML rempli par les données XML source d'un formulaire.  <br/> |
|[Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Errors.aspx) , propriété  <br/> |Renvoie une référence à la collection **Errors**.  <br/> |
|[Extension](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Extension.aspx) , propriété  <br/> |Renvoie une référence à un objet représentant l'ensemble des fonctions et des variables contenues dans le fichier de code de formulaire.  <br/> |
|[IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) , propriété  <br/> |Renvoie une valeur **Boolean** indiquant si les données du formulaire ont été modifiées.  <br/> |
|[IsDOMReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDOMReadOnly.aspx) , propriété  <br/> |Renvoie une valeur **Boolean** indiquant si le DOM XML est défini en lecture seule.  <br/> |
|[IsNew](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsNew.aspx) , propriété  <br/> |Renvoie une valeur **Boolean** indiquant si le formulaire a été enregistré après sa création.  <br/> |
|[IsReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsReadOnly.aspx) , propriété  <br/> |Renvoie une valeur **Boolean** indiquant si le formulaire est en mode lecture seule.  <br/> |
|[IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) , propriété  <br/> |Renvoie une valeur **Boolean** indiquant si le formulaire est signé numériquement.  <br/> |
|[Language](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Language.aspx) , propriété  <br/> |Spécifie ou renvoie la valeur chaîne du langage utilisé pour le formulaire.  <br/> |
|[QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.QueryAdapter.aspx) , propriété  <br/> |Renvoie une référence à l'objet adaptateur de données.  <br/> |
|[Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) , propriété  <br/> |Renvoie une référence à l'objet **Solution**.  <br/> |
|Propriété [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx)  <br/> |Renvoie une référence à l'objet **UI**.  <br/> |
|[URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.URI.aspx) , propriété  <br/> |Renvoie une valeur chaîne contenant l'URI (Uniform Resource Identifier) du formulaire.  <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) , propriété  <br/> |Renvoie une référence à l'objet **View**.  <br/> |
|[ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ViewInfos.aspx) , propriété  <br/> |Renvoie une référence à la collection **ViewInfos**.  <br/> |
   
## <a name="using-the-xdocuments-collection-and-the-xdocument-interfaces"></a>Utilisation de la collection XDocuments et des interfaces XDocument

L'interface **XDocumentsCollection** est accessible via la propriété [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.XDocuments.aspx) de l'interface [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . Dans un projet avec code managé créé en utilisant le modèle objet compatible avec InfoPath 2003, vous pouvez accéder à l'interface **XDocumentsCollection** à l'aide de la variable  `thisApplication` instanciée dans la méthode  `_StartUp` du code de formulaire de votre projet. Les lignes de code qui suivent créent une variable qui fait référence à l'interface **XDocumentsCollection** du projet actuel. 
  
```cs
XDocumentsCollection xdocs;
xdocs = thisApplication.XDocuments;
// Write code here to work with the XDocumentsCollection.
```

```vb
Dim xdocs As XDocumentsCollection
xdocs = thisApplication.XDocuments
' Write code here to work with the XDocumentsCollection.
```

Dans un projet avec code managé créé en utilisant le modèle objet compatible avec InfoPath 2003, vous pouvez accéder à l'interface **XDocument** via la variable  `thisXDocument` instanciée dans la méthode  `StartUp` du code de formulaire de votre projet. La ligne de code qui suit utilise la variable  `thisXDocument` pour accéder à l'interface **XDocument** du projet actuel et afficher l'URI du formulaire ouvert dans un message d'alerte. 
  
```cs
thisXDocument.UI.Alert(thisXDocument.URI);
```

```vb
thisXDocument.UI.Alert(thisXDocument.URI)
```

> [!NOTE]
> [!REMARQUE] Lorsque vous utilisez l'interface **XDocument** pour accéder au document XML sous-jacent d'un formulaire, vous accédez au document XML associé au formulaire ouvert. 
  
La propriété **DOM** est une des propriétés clés de l'objet **XDocument**. Cette propriété renvoie une référence au DOM XML rempli par les données XML source d'un formulaire. Lorsque vous utilisez la propriété **DOM**, vous pouvez utiliser l'ensemble des propriétés et des méthodes prises en charge par le DOM XML. Par exemple, le code suivant utilise la propriété **xml** du DOM XML pour renvoyer et afficher le contenu complet du document XML sous-jacent d'un formulaire : 
  
```cs
string xmldoc;
xmldoc = thisXDocument.DOM.xml;
// Display xml.
thisXDocument.UI.Alert(xmldoc);
```

```vb
Dim xmldoc As String
xmldoc = thisXDocument.DOM.xml
' Display xml.
thisXDocument.UI.Alert(xmldoc)
```

> [!NOTE]
> [!REMARQUE] Pour en savoir plus sur le DOM XML et sur toutes les propriétés et méthodes qu'il prend en charge, consultez le MSXML SDK sur MSDN. 
  

