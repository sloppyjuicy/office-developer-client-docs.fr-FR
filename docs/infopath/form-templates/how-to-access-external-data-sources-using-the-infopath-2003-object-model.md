---
title: Accéder aux sources de données externes à l’aide du modèle objet InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- data sources [infopath 2007], accessing with infopath 2003 object model,InfoPath 2003-compatible form templates, accessing external data
localization_priority: Normal
ms.assetid: 9fd9ca47-abf1-48dd-8668-dfee27161793
description: Lorsque vous travaillez à partir d'un modèle de formulaire InfoPath qui utilise le modèle objet compatible avec InfoPath 2003, vous pouvez écrire du code pour accéder aux sources de données secondaires du formulaire et manipuler les données qu'elles contiennent.
ms.openlocfilehash: 569f029b412328f4d49e3079eaf207dc1556fc4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431679"
---
# <a name="access-external-data-sources-using-the-infopath-2003-object-model"></a>Accéder aux sources de données externes à l’aide du modèle objet InfoPath 2003

Lorsque vous travaillez à partir d'un modèle de formulaire InfoPath qui utilise le modèle objet compatible avec InfoPath 2003, vous pouvez écrire du code pour accéder aux sources de données secondaires du formulaire et manipuler les données qu'elles contiennent.
  
Chaque source de données secondaire est représentée par un objet instancié à l'aide de l'interface [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) et correspond à des données stockées, obtenues d'une source de données externe, par exemple une base de données ou une requête d'un service Web. Ces sources de données sont désignées comme sources secondaires car lorsque l'utilisateur enregistre le formulaire InfoPath, il enregistre uniquement les données de la source de données principale et non les données des sources de données secondaires. La connexion à une source de données est représentée par un objet instancié à l'aide d'une des interfaces d'« adaptateur de données » telles que l'interface [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) qui représente une connexion de données à un service Web XML. 
  
L'objet [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) instancié représente le stockage des données XML renvoyées par une connexion de données (à une base de données ou une requête de service Web) et l'adaptateur de données représente la connexion de données. 
  
Le modèle objet d'InfoPath prend en charge l'accès aux sources de données secondaires d'un formulaire grâce à l'utilisation de l'interface [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) en association avec l'interface [DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) . 
  
Le modèle objet d'InfoPath fournit également un ensemble d'objets adaptateur de données contenant des informations relatives aux connexions de données utilisées par le formulaire. 
  
Il existe deux types d'adaptateurs de données : les adaptateurs de requête et les adaptateurs d'envoi. Les adaptateurs de requête permettent de récupérer les données qui sont ensuite stockées dans une source de données secondaire, tandis que les adaptateurs d'envoi sont utilisés pour envoyer des données, par exemple à une base de données ou un service Web. Les données envoyées sont copiées depuis la source de données principale ou la source de données secondaire. 
  
## <a name="overview-of-the-dataobjectscollection-interface"></a>Vue d'ensemble de l'interface DataObjectsCollection

L'interface [DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) fournit aux développeurs les méthodes et propriétés suivantes pour gérer les instances [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) que contient le formulaire. 
  
|**Name**|**Description**|
|:-----|:-----|
|Propriété [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Count.aspx)  <br/> |Renvoie le nombre d'instances **DataSourceObject** que contient la collection.  <br/> |
|[Méthode GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.GetEnumerator.aspx)  <br/> |Renvoie un **IEnumerator** qui peut être utilisé pour lancer une répétition dans la collection.  <br/> |
|Propriété [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Item.aspx)  <br/> |Renvoie une référence à l'instance **DataSourceObject** spécifiée.  <br/> |
   
## <a name="overview-of-the-datasourceobject-interface"></a>Vue d'ensemble de l'interface DataSourceObject

L'interface [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) offre aux développeurs de formulaires les méthodes et les propriétés ci-dessous pour interagir avec une source de données secondaire InfoPath. 
  
|**Name**|**Description**|
|:-----|:-----|
|[Méthode de](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Query.aspx) requête  <br/> |Exécute la requête sur un adaptateur de données et insère les données renvoyées sous forme de XML dans le DOM XML associé à l'objet **DataSourceObject**.  <br/> |
|[DoM,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.DOM.aspx) propriété  <br/> |Renvoie une référence au DOM XML utilisé pour enregistrer et manipuler les données à l'aide de l'objet **DataSourceObject**.  <br/> |
|Propriété [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Name.aspx)  <br/> |Renvoie une valeur chaîne indiquant le nom de l'objet **DataSourceObject**.  <br/> |
|[Propriété QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.QueryAdapter.aspx)  <br/> |Renvoie une référence à l'adaptateur de données associé.  <br/> |
   
## <a name="overview-of-the-data-adapter-interfaces"></a>Vue d'ensemble des interfaces d'adaptateurs de données

Les interfaces conçues pour accéder aux adaptateurs de données fournissent plusieurs propriétés et méthodes permettant d'échanger des données via des connexions avec des sources de données externes. L'adaptateur de données associé à un objet [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) dépend du type de connexion de données externe. InfoPath implémente les interfaces suivantes pour accéder aux adaptateurs de données : 
  
|**Name**|**Description**|
|:-----|:-----|
|Interface [ADOAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapterObject.aspx)  <br/> |Établit une connexion avec les sources de données ADO/OLEDB ; limité aux bases Microsoft Access et Microsoft SQL Server™.  <br/> |
|Interface [SharepointListAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SharepointListAdapterObject.aspx)  <br/> |Se connecte à une liste ou une bibliothèque de documents SharePoint.  <br/> |
|[Interface WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx)  <br/> |Établit une connexion avec des services Web XML.  <br/> |
|[Objet XMLFileAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLFileAdapterObject.aspx)  <br/> |Établit une connexion avec un fichier XML.  <br/> |
   
## <a name="using-the-datasourceobjects-and-the-datasourceobject-interfaces"></a>Utilisation des interfaces DataSourceObjects et DataSourceObject

La collection **DataSourceObjects** est accessible via la propriété [DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) de l'interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) . Par exemple, si vous créez une source de données secondaire appelée Employés qui récupère les données de la table Employés dans la base de données Access Les Comptoirs, vous pouvez utiliser la collection **DataSourceObjects** pour définir une référence à un objet **DataObject** qui représente les données récupérées. 
  
Dans l'exemple de code qui suit, le nom de la source de données secondaire est transmis à la propriété d'accès de l'interface **DataObjectsCollection**, qui renvoie une référence à l'objet **DataSourceObject**. Les données de la source de données secondaire sont affichées dans une boîte de message par le biais de la propriété **DOM** de l'interface **DataSourceObject** pour accéder à la propriété **xml** du DOM XML. 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Instantiate a variable to access the specified data object
   // from the DataObjectsCollection of the form.
   // You must explicitly cast to the DataSourceObject type 
   // before you can access the data object.
   DataSourceObject myDataObject = 
      thisXDocument.DataObjects["Employees"] as DataSourceObject;
   // Display the data from the secondary data source using the 
   // XML DOM.
   thisXDocument.UI.Alert("Data Adapter: " + myDataObject.DOM.xml);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Instantiate a variable to access the specified data object
   ' from the DataObjectsCollection of the form.
   Dim myDataObject As DataSourceObject = _
      thisXDocument.DataObjects("Employees")
   ' Display the data from the secondary data source using the 
   ' XML DOM.
   thisXDocument.UI.Alert("Data Adapter: " + myDataObject.DOM.xml)
End Sub
```

Pour manipuler les données d'une source secondaire, utilisez la propriété **DOM** de l'interface **DataSourceObject** qui renvoie une référence au DOM XML contenant les données. Dès que vous disposez de cette référence, vous pouvez utiliser l'ensemble de ses propriétés et de ses méthodes pour manipuler les données que contient le DOM XML. 
  
## <a name="using-the-dataadapterscollection-and-the-dataadapterobject-interfaces"></a>Utilisation des interfaces DataAdaptersCollection et DataAdapterObject

L'interface [DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) est accessible via la propriété [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) de l'interface **XDocument**. Par exemple, si vous créez une source de données secondaire appelée Employés qui récupère les données de la table Employés dans la base de données Access Les Comptoirs, vous pouvez utiliser la collection **DataAdapterObjects** pour définir une référence à un objet **DataAdapterObject** qui représente la connexion à la base de données. 
  
Dans l'exemple de code qui suit, le nom de la source de données secondaire est transmis à la propriété d'accès de l'interface **DataAdaptersCollection**, qui, dans ce cas, renvoie une référence à une instance de l'objet **ADOAdapterObject**. Pour que cet exemple fonctionne correctement, vous devez envoyer de façon explicite l'objet renvoyé en tant qu'objet **ADOAdapterObject**, qui représente la connexion à la base de données Microsoft Access Les Comptoirs. La propriété [Connection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapter2.Connection.aspx) de l'interface **ADOAdapterObject** permet d'afficher la chaîne de connexion ADO dans une boîte de message. 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Instantiate a variable to access the specified data object
   // from the DataAdaptersCollection of the form. 
   // You must explicitly cast to the specific adapter type
   // (ADOAdapterObject) before you can access the data adapter.
   ADOAdapterObject myADOAdapter = 
      thisXDocument.DataAdapters["Employees"] as ADOAdapterObject;
   // Display the connection information for the data adapter.
   thisXDocument.UI.Alert("Data Adapter: " + myADOAdapter.Connection);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Instantiate a variable to access the specified data object. 
   ' You must explicitly cast to the specific adapter type
   ' (ADOAdapterObject) before you can access the data adapter.
   Dim myADOAdapter As ADOAdapterObject = _
      thisXDocument.DataAdapters("Employees")
   ' Display the connection information for the data adapter.
   thisXDocument.UI.Alert("Data Adapter: " + myADOAdapter.Connection)
End Sub
```


