---
title: Fournisseurs requis pour la mise en forme des données
TOCTitle: Required providers for data shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ffb45599c01121204fe036cfdf60f17865388cd4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306656"
---
# <a name="required-providers-for-data-shaping"></a>Fournisseurs requis pour la mise en forme des données

**S’applique à** : Access 2013, Office 2013

La mise en forme des données fait en général appel à deux fournisseurs. Le fournisseur de service, à savoir le [service de mise en forme des données pour OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), fournit les fonctionnalités de mise en forme des données et un fournisseur de données, tel que le fournisseur OLE DB pour SQL Server, fournit les lignes de données devant remplir l'objet [Recordset](recordset-object-ado.md) mis en forme.

Le nom du fournisseur de service (MSDataShape) peut être spécifié comme valeur de la propriété [Provider](connection-object-ado.md) de l'objet [Connection](provider-property-ado.md) ou du mot clé « Provider=MSDataShape; » dans la chaîne de connexion.

Le nom du fournisseur de données peut être spécifié en tant que valeur de la propriété dynamique Data **Provider,** qui est ajoutée à la [collection](properties-collection-ado.md) **Propriétés** de l’objet Connection par le service de mise en forme des données pour OLE DB, ou le mot clé de chaîne de connexion « **Data Provider=***provider*».

Aucun fournisseur de données n'est requis si l'objet **Recordset** est vide (comme dans un objet **Recordset** fabriqué contenant des colonnes créées avec le mot-clé NEW). Dans ce cas, spécifiez « **Data Provider=** none; ».

## <a name="example"></a>Exemple

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

