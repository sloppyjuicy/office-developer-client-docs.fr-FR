---
title: Utilisation d'ADO avec ADO MD
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5d74f4d587462290fa99bb2524b4dc264af9d591
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588874"
---
# <a name="using-ado-with-ado-md"></a>Utilisation d’ADO avec ADO MD


**S’applique à** : Access 2013, Office 2013

ADO et ADO MD sont des modèles d'objet apparentés mais distincts. ADO fournit des objets pour la connexion aux sources de données, l'exécution de commandes, la récupération de données tabulaires et de métadonnées de schéma sous forme de tableau et l'affichage des informations d'erreur du fournisseur. ADO MD fournit des objets pour l'extraction de données multidimensionnelles et l'affichage de métadonnées de schéma multidimensionnelles.

Si vous travaillez avec un fournisseur de données multidimensionnelles (MDP), vous pouvez choisir d'utiliser ADO, ADO MD ou les deux avec votre application. En référençant les deux bibliothèques dans votre projet, vous aurez accès à toutes les fonctionnalités fournies par votre fournisseur MDP.

Il peut souvent s'avérer utile d'obtenir une vue tabulaire et bidimensionnelle d'un jeu de données multidimensionnel. Pour cela, il vous suffit d'utiliser l'objet ADO [Recordset](recordset-object-ado.md). Spécifiez la source de votre [cellset](cellset-object-ado-md.md) comme paramètre ***Source** _ pour la méthode [Open](open-method-ado-recordset.md) d’un _*Recordset**, plutôt que comme source d’un groupe de cellules ADO **MD.**

Il peut également s'avérer utile de voir les métadonnées de schéma sous la forme d'un tableau au lieu d'une hiérarchie d'objets. La méthode [OpenSchema](openschema-method-ado.md) ADO de l'objet [Connection](connection-object-ado.md) vous permet d'ouvrir un objet **Recordset** contenant des informations de schéma. Le **_paramètre QueryType_ _ de la *méthode _* OpenSchema** possède plusieurs valeurs [SchemaEnum](schemaenum.md) qui sont spécifiquement liées à des GCP. Il s'agit des valeurs suivantes :

  - **adSchemaCubes**

  - **adSchemaDimensions**

  - **adSchemaHierarchies**

  - **adSchemaLevels**

  - **adSchemaMeasures**

  - **adSchemaMembers**

Pour utiliser les valeurs d'énumération ADO avec les propriétés ou méthodes ADO MD, votre projet doit référencer les deux bibliothèques, ADO et ADO MD. Par exemple, vous pouvez utiliser la valeur d'énumération **adState** ADO avec la propriété [State](state-property-ado-md.md) ADO MD. Pour plus d'informations sur la création de références à des bibliothèques, consultez la documentation de votre outil de développement.

Pour plus d'informations sur les objets et méthodes ADO, consultez la rubrique [Référence des API ADO](ado-api-reference.md).

