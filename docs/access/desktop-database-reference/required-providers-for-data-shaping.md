---
title: Fournisseurs requis pour la mise en forme des données
TOCTitle: Required Providers for Data Shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de8634503c81bd2c66eeda0c64a8b1ff1b6f5363
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885351"
---
# <a name="required-providers-for-data-shaping"></a>Fournisseurs requis pour la mise en forme des données


**S’applique à**: Access 2013, Office 2013

La mise en forme des données fait en général appel à deux fournisseurs. Le fournisseur de service, à savoir le [service de mise en forme des données pour OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), fournit les fonctionnalités de mise en forme des données et un fournisseur de données, tel que le fournisseur OLE DB pour SQL Server, fournit les lignes de données devant remplir l'objet [Recordset](recordset-object-ado.md) mis en forme.

Le nom du fournisseur de service (MSDataShape) peut être spécifié comme valeur de la propriété [Provider](connection-object-ado.md) de l'objet [Connection](provider-property-ado.md) ou du mot clé « Provider=MSDataShape; » dans la chaîne de connexion.

Le nom du fournisseur de données peut être spécifié comme valeur de la propriété dynamique **Du fournisseur de données** , qui est ajoutée à la collection de [Propriétés](properties-collection-ado.md) de l’objet **Connection** par Microsoft Data Shaping Service pour OLE DB ou mot-clé de la chaîne de connexion « * *Du fournisseur de données = *** fournisseur*».

Aucun fournisseur de données n'est requis si l'objet **Recordset** est vide (comme dans un objet **Recordset** fabriqué contenant des colonnes créées avec le mot-clé NEW). Dans ce cas, spécifiez « **Data Provider=** none; ».

## <a name="example"></a>Exemples

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

