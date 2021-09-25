---
title: Fournisseurs requis pour la mise en forme des données
TOCTitle: Required providers for data shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3de8c0731a7133cb053c715ef3a2254a0cdae9e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576932"
---
# <a name="required-providers-for-data-shaping"></a>Fournisseurs requis pour la mise en forme des données

**S’applique à** : Access 2013, Office 2013

La mise en forme des données fait en général appel à deux fournisseurs. Le fournisseur de service, à savoir le [service de mise en forme des données pour OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), fournit les fonctionnalités de mise en forme des données et un fournisseur de données, tel que le fournisseur OLE DB pour SQL Server, fournit les lignes de données devant remplir l'objet [Recordset](recordset-object-ado.md) mis en forme.

Le nom du fournisseur de service (MSDataShape) peut être spécifié comme valeur de la propriété [Provider](provider-property-ado.md) de l’objet [Connection](connection-object-ado.md) ou du mot clé « Provider=MSDataShape; » dans la chaîne de connexion.

Le nom du fournisseur de données peut être spécifié comme valeur de la propriété dynamique **Data Provider**, qui est ajoutée à la collection [Properties](properties-collection-ado.md) de l’objet **Connection** par Microsoft Data Shaping Service pour OLE DB, ou par le mot-clé « **Data Provider=**_fournisseur_ » de la chaîne de connexion.

Aucun fournisseur de données n'est requis si l'objet **Recordset** est vide (comme dans un objet **Recordset** fabriqué contenant des colonnes créées avec le mot-clé NEW). Dans ce cas, spécifiez « **Data Provider=** none; ».

## <a name="example"></a>Exemple

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

