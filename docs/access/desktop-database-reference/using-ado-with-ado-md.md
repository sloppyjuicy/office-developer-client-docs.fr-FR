---
title: Utilisation d'ADO avec ADO MD
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 80c87f57a96f98de704e3cfa9b7689a522e4a7af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312746"
---
# <a name="using-ado-with-ado-md"></a>Utilisation d’ADO avec ADO MD


**S’applique à** : Access 2013, Office 2013

ADO et ADO MD sont des modèles d'objet apparentés mais distincts. ADO fournit des objets pour la connexion aux sources de données, l'exécution de commandes, la récupération de données tabulaires et de métadonnées de schéma sous forme de tableau et l'affichage des informations d'erreur du fournisseur. ADO MD fournit des objets pour l'extraction de données multidimensionnelles et l'affichage de métadonnées de schéma multidimensionnelles.

Si vous travaillez avec un fournisseur de données multidimensionnelles (MDP), vous pouvez choisir d'utiliser ADO, ADO MD ou les deux avec votre application. En référençant les deux bibliothèques dans votre projet, vous aurez accès à toutes les fonctionnalités fournies par votre fournisseur MDP.

Il peut souvent s'avérer utile d'obtenir une vue tabulaire et bidimensionnelle d'un jeu de données multidimensionnel. Pour cela, il vous suffit d'utiliser l'objet ADO [Recordset](recordset-object-ado.md). Spécifiez la source de votre objet [Cellset](cellset-object-ado-md.md) comme paramètre ***Source*** de la méthode [Open](open-method-ado-recordset.md) d’un objet **Recordset**, et non comme source d’un objet **Cellset** ADO MD.

Il peut également s'avérer utile de voir les métadonnées de schéma sous la forme d'un tableau au lieu d'une hiérarchie d'objets. La méthode [OpenSchema](openschema-method-ado.md) ADO de l'objet [Connection](connection-object-ado.md) vous permet d'ouvrir un objet **Recordset** contenant des informations de schéma. Le paramètre ***QueryType*** de la méthode **OpenSchema** comporte plusieurs valeurs [SchemaEnum](schemaenum.md) qui se rapportent aux fournisseurs MDP. Il s'agit des valeurs suivantes :

  - **adSchemaCubes**

  - **adSchemaDimensions**

  - **adSchemaHierarchies**

  - **adSchemaLevels**

  - **adSchemaMeasures**

  - **adSchemaMembers**

Pour utiliser les valeurs d'énumération ADO avec les propriétés ou méthodes ADO MD, votre projet doit référencer les deux bibliothèques, ADO et ADO MD. Par exemple, vous pouvez utiliser la valeur d'énumération **adState** ADO avec la propriété [State](state-property-ado-md.md) ADO MD. Pour plus d'informations sur la création de références à des bibliothèques, consultez la documentation de votre outil de développement.

Pour plus d'informations sur les objets et méthodes ADO, consultez la rubrique [Référence des API ADO](ado-api-reference.md).

