---
title: Fournisseurs OLE DB (référence de base de données de bureau Access)
TOCTitle: OLE DB providers
ms:assetid: ef412198-eac5-bf86-73fd-574e67276408
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250215(v=office.15)
ms:contentKeyID: 48548576
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 649f1db283b772a0f6798fae0d56a3a80c59e21b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288482"
---
# <a name="ole-db-providers"></a>Fournisseurs OLE DB


**S’applique à** : Access 2013, Office 2013

Le [guide](introduction-to-ado-programming.md) introduction du programmeur ADO décrit la relation entre ADO et le reste de l’architecture Microsoft Data Access. OLE DB définit un ensemble d’interfaces COM qui fournissent aux applications un accès uniforme à des données stockées dans plusieurs sources d’informations. Cette approche permet aux sources de données de partager leurs données via plusieurs interfaces qui prennent en charge les fonctionnalités SGBD appropriées pour ces sources de données. L’architecture hautement performante d’OLE DB est conçue pour utiliser un modèle de services d’une grande souplesse, basée sur des composants. Au lieu d’avoir un nombre défini de couches intermédiaires entre l’application et les données, OLE DB n’utilise que le nombre de composants strictement nécessaires à la réalisation d’une tâche précise.

Supposons, par exemple, qu'un utilisateur souhaite exécuter une requête. Plusieurs scénarios sont envisageables :

  - Les données résident dans une base de données relationnelle pour laquelle il existe un pilote ODBC mais aucun fournisseur OLE DB natif : l'application utilise ADO pour communiquer avec le fournisseur Microsoft OLE DB pour ODBC, lequel charge ensuite le pilote ODBC approprié. Le pilote passe ensuite l'instruction SQL au système SGBD, qui extrait les données.

  - Les données résident dans Microsoft SQL Server, pour lequel il existe un fournisseur OLE DB natif : l'application utilise ADO pour communiquer directement avec le fournisseur OLE DB pour SQL Server. Aucun intermédiaire n'est requis.

  - Les données résident dans Microsoft Exchange Server, pour lequel il existe un fournisseur OLE DB mais aucun moteur de traitement des requêtes SQL : l'application utilise ADO pour communiquer avec le fournisseur OLE DB pour Microsoft Exchange et appelle un composant OLE DB, plus précisément un processeur de requêtes, pour traiter la requête.

  - Les données résident dans le système de fichiers Microsoft NTFS, sous forme de documents : les données sont accessibles par l'intermédiaire d'un fournisseur OLE DB natif, via le service d'indexation Microsoft, qui indexe le contenu et les propriétés des documents stockés dans le système de fichiers, ce qui permet l'exécution de recherches efficaces sur le contenu.

Dans tous les exemples qui précèdent, l'application peut exécuter des requêtes sur les données. Ainsi, un nombre minimal de composants permet de répondre aux besoins de l'utilisateur. Dans chaque cas, des composants supplémentaires ne sont utilisés qu'en cas de nécessité, et seuls les composants requis sont appelés. Ces possibilités de chargement à la demande de composants réutilisables et partageables contribuent grandement aux performances élevées associées à OLE DB.

Les fournisseurs appartiennent à deux catégories distinctes : les fournisseurs de données et les fournisseurs de services. Un [ fournisseur de données ](data-providers.md) est propriétaire de ses données et les expose dans un format tabulaire à votre application. Un [fournisseur de services](service-providers-and-components.md) encapsule un service en produisant et en consommant des données, ce qui étend les fonctionnalités de vos applications ADO. Un fournisseur de services peut être également défini comme un [composant de service](service-providers-and-components.md), qui doit fonctionner conjointement avec d'autres composants ou fournisseurs de services.

ADO offre une interface cohérente de haut niveau aux divers fournisseurs OLE DB.

Cette section contient les rubriques suivantes :

- [Data Providers](data-providers.md)

- [Service Providers and Components](service-providers-and-components.md)
