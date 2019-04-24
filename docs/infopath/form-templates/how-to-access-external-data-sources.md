---
title: Accéder à des sources de données externes
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- data connection classes [infopath 2007],secondary data sources [InfoPath 2007],data [InfoPath 2007], secondary,DataSource class [InfoPath 2007],accessing external data sources [InfoPath 2007],DataSourceCollection class [InfoPath 2007],DataConnectionCollection class [InfoPath 2007],DataConnection class [InfoPath 2007],InfoPath 2007, accessing external data,data [InfoPath 2007], external sources
localization_priority: Normal
ms.assetid: db7c2521-a1ad-4802-b398-79575d3d310a
description: Lorsque vous travaillez avec un modèle de formulaire InfoPath, vous pouvez écrire du code pour accéder aux sources de données secondaires du formulaire et manipuler les données qu'elles contiennent.
ms.openlocfilehash: f6957c561231eef0e3e4df6deb09ae89f85afcc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300195"
---
# <a name="access-external-data-sources"></a>Accéder à des sources de données externes

Lorsque vous travaillez avec un modèle de formulaire InfoPath, vous pouvez écrire du code pour accéder aux sources de données secondaires du formulaire et manipuler les données qu'elles contiennent. 
  
Chaque source de données secondaire est représentée par un objet instancié à l'aide de la classe [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) et correspond à des données stockées, obtenues à partir d'une source de données externe, par exemple une base de données ou une requête d'un service Web. Ces sources de données sont désignées comme sources secondaires car lorsque l'utilisateur enregistre un formulaire InfoPath, il enregistre uniquement les données de la source de données principale et non les données des sources de données secondaires. La connexion à une source de données est représentée par un objet instancié à l'aide d'une des classes de « connexion de données » telles que la classe [WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) , qui représente une connexion de données à un service Web XML. 
  
L'objet instancié [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) représente le stockage de données XML renvoyées par une connexion de données (à partir d'une requête de base de données ou de service Web), et la classe de « connexion de données » représente la connexion de données elle-même (telle que définie et nommée au moyen de la commande **Connexions de données** dans l'onglet **Données**). 
  
Le modèle objet d'InfoPath prend en charge l'accès aux sources de données secondaires d'un formulaire grâce à l'utilisation de la classe [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) en association avec la classe [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) . 
  
Le modèle objet d'InfoPath fournit également un ensemble de classes de connexion de données contenant des informations relatives aux connexions de données utilisées par le formulaire.
  
> [!NOTE]
> [!REMARQUE] Dans Microsoft InfoPath 2003, une connexion de données est appelée adaptateur de données. 
  
Il existe deux types de connexions de données : les connexions de requête permettent de récupérer les données qui sont ensuite stockées dans une source de données secondaire. Les connexions d'envoi sont utilisées pour envoyer des données, par exemple à une base de données ou à un site Web. Les données envoyées sont copiées depuis la source de données principale ou la source de données secondaire. 
  
## <a name="overview-of-the-datasourcecollection-class"></a>Présentation de la classe DataSourceCollection

La classe [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) fournit aux développeurs les méthodes et propriétés suivantes pour gérer les instances d'objets [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) que contient le formulaire. 
  
|**Nom**|**Description**|
|:-----|:-----|
|Propriété [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx)  <br/> |Renvoie le nombre d'instances d'objets **DataSource** que contient la collection.  <br/> |
|[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx) , méthode  <br/> |Renvoie un **IEnumerator** qui peut être utilisé pour lancer une répétition dans la collection.  <br/> |
|Propriété [Item [Int32]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Renvoie une référence à l'objet **DataSource** spécifié par valeur d'index.  <br/> |
|Propriété [Item [String]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Renvoie une référence à l'objet **DataSource** spécifié par nom d'index.  <br/> |
   
## <a name="overview-of-the-datasource-class"></a>Présentation de la classe DataSource

La classe [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) offre aux développeurs de formulaires les méthodes et les propriétés ci-dessous pour interagir avec une source de données secondaire InfoPath. 
  
|**Nom**|**Description**|
|:-----|:-----|
|Méthode [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)  <br/> |Renvoie un objet [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) pour accéder à la source de données et la modifier  <br/> |
|[QueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx) , propriété  <br/> |Obtient une référence à l'objet de connexion de données associé.  <br/> Pour exécuter la requête sur la connexion de données et insérer les données renvoyées au format XML dans le nœud XML associé à l'objet **DataSource** , utilisez la méthode [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) de l'objet de connexion de données associé.  <br/> |
|Propriété [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx)  <br/> |Obtient le nom de l'objet **DataSource**.  <br/> |
|[ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx) , propriété  <br/> |Obtient une valeur qui indique si la source de données est en lecture seule.  <br/> |
|[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) , méthode  <br/> |Obtient la valeur d'une propriété nommée pour le nœud XML spécifié, lequel doit être un nœud **nonattribute** dans la source de données principale.  <br/> |
|[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) , méthode  <br/> |Définit la valeur d'une propriété nommée pour le nœud XML spécifié, lequel doit être un nœud **nonattribute** dans la source de données principale.  <br/> |
   
## <a name="overview-of-the-data-connection-classes"></a>Présentation des classes de connexion de données

Les classes conçues pour accéder aux connexions de données fournissent plusieurs propriétés et méthodes permettant d'échanger des données via des connexions avec des sources de données externes. La connexion de données associée à un objet **DataSource** dépend du type de connexion de données externe. InfoPath implémente les classes suivantes pour accéder aux connexions de données : 
  
|**Nom**|**Description**|
|:-----|:-----|
|Classe [AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx)  <br/> |Interroge une source de données ADO/OLEDB ; limité à Microsoft Access et Microsoft SQL Server.  <br/> |
|Classe [AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx)  <br/> |Envoie à une source de données ADO/OLEDB ; limité à Microsoft Access et Microsoft SQL Server.  <br/> |
|Classe [SharePointListRWQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWQueryConnection.aspx)  <br/> |Interroge une liste ou une bibliothèque de documents SharePoint.  <br/> |
|[SharePointListRWSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWSubmitConnection.aspx) <br/> |Envoie à une liste ou une bibliothèque de documents SharePoint.  <br/> |
|Classe [WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx)  <br/> |Établit une connexion à un service Web XML.  <br/> |
|Classe [FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx)  <br/> |Interroge un fichier XML.  <br/> |
|Classe [FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx)  <br/> |Envoie à un fichier XML.  <br/> |
|Classe [EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx)  <br/> |Envoie un formulaire sous forme de pièce jointe dans un message électronique.  <br/> |
|Classe [BdcQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcQueryConnection.aspx)  <br/> |Interroge une liste externe sur un serveur exécutant SharePoint Foundation 2010 ou SharePoint Server 2010.  <br/> |
|Classe [BdcSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcSubmitConnection.aspx)  <br/> |Envoie à une liste externe sur un serveur exécutant SharePoint Foundation 2010 ou SharePoint Server 2010.  <br/> |
   
## <a name="using-the-datasourcecollection-and-the-datasource-classes"></a>Utilisation des classes DataSourceCollection et DataSource

L'objet **DataSourceCollection** qui représente la collection de sources de données associées à un modèle de formulaire est accessible par le biais de la propriété [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Si, par exemple, vous créez une source de données secondaire nommée Employés qui extrait des données de la table Employees dans la base de données Les comptoirs, vous pouvez utiliser l'objet **DataSourceCollection** pour définir une référence à un objet **DataSource** qui représente les données extraites. 
  
Dans l'exemple de code suivant, le nom de la source de données secondaires est transmis à la propriété d'accès de la classe **DataSourceCollection**, qui renvoie une référence à l'objet **DataSource** qui représente les données extraites de la table Employés. Le nœud XML qui stocke les données extraites à partir de la source de données secondaire s'affiche dans une zone de message au moyen de la méthode **CreateNavigator** de la classe **DataSource** pour accéder à la propriété **InnerXml** de la classe **XPathNavigator**. 
  
```cs
// Instantiate a variable to access the specified data source
// from the DataSourceCollection of the form.
DataSource myDataSource = 
   this.DataSources["Employees"];
// Display the XML data from the secondary data source.
MessageBox.Show("Data source data: " +
   myDataSource.CreateNavigator().InnerXml.ToString());
```

```vb
' Instantiate a variable to access the specified data source
' from the DataSourceCollection of the form.
Dim myDataSource As DataSource = _
   Me.DataSources("Employees")
' Display the XML data from the secondary data source.
MessageBox.Show("Data source data: " &amp; _
   myDataSource.CreateNavigator().InnerXml.ToString())
```

Pour manipuler les données figurant dans une source de données secondaire, utilisez la méthode **CreateNavigator** de la classe **DataSource** pour renvoyer une référence à un objet **XPathNavigator** positionné au niveau du nœud où sont stockées les données secondaires. Vous pouvez utiliser les propriétés et méthodes de la classe **XPathNavigator** pour manipuler les données. Pour plus d'informations, consultez [la rubrique utilisation des classes XPathNavigator et XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
## <a name="using-the-dataconnectioncollection-and-the-dataconnection-classes"></a>Utilisation des classes DataConnectionCollection et DataConnection

L'objet [DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) qui représente la collection de connexions de données associées à un modèle de formulaire est accessible par le biais de la propriété [DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) de la classe **XmlForm**. Si, par exemple, vous créez une source de données secondaire nommée Employés qui extrait les données de la table Employés dans la base de données Les comptoirs, vous pouvez utiliser l'objet **DataConnectionCollection** associé au modèle de formulaire pour définir une référence à **DataConnection** qui représente la connexion à la base de données. 
  
Dans l'exemple de code qui suit, le nom de la source de données secondaire est transmis à la propriété d'accès de la classe **DataConnectionCollection**, qui, dans ce cas, renvoie une référence à l'objet **ADOQueryConnection** qui représente la connexion à la base de données Les comptoirs. Pour que cet exemple fonctionne correctement, vous devez forcer la conversion de façon explicite de l'objet renvoyé au type **ADOQueryConnection**. La propriété [Connection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) de l'interface **ADOAdapterObject** permet d'afficher la chaîne de connexion ADO dans une boîte de message. 
  
```cs
// Instantiate a variable to access the specified data connection
// from the DataConnectionCollection of the form. 
// You must cast to the specific data connection type
// (ADOQueryConnection) before you can access the data connection.
ADOQueryConnection myADOConnection = 
   (ADOQueryConnection)this.DataConnections["Employees"];
// Display the connection information for the data connection.
MessageBox.Show("Connection string: " + myADOConnection.Connection);
```

```vb
' Instantiate a variable to access the specified data connection
' from the DataConnectionCollection of the form. 
' You must cast to the specific data connection type
' (ADOQueryConnection) before you can access the data connection.
Dim myADOConnection As ADOQueryConnection = _
   DirectCast(Me.DataConnections("Employees"), ADOQueryConnection)
' Display the connection information for the data connection.
MessageBox.Show("Connection string: " &amp; myADOConnection.Connection)
```

## <a name="see-also"></a>Voir aussi



[Création de modèles de formulaires InfoPath fonctionnant avec InfoPath Forms Services](creating-infopath-form-templates-that-work-with-infopath-forms-services.md)

