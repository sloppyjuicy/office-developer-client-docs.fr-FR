---
title: Fournisseurs requis pour la mise en forme des données
TOCTitle: Required providers for data shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd4460b96cf222a9c6e4f7a8ea66ed22c0f2ff10
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947636"
---
# <a name="required-providers-for-data-shaping"></a><span data-ttu-id="4769e-102">Fournisseurs requis pour la mise en forme des données</span><span class="sxs-lookup"><span data-stu-id="4769e-102">Required providers for data shaping</span></span>

<span data-ttu-id="4769e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4769e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4769e-p101">La mise en forme des données fait en général appel à deux fournisseurs. Le fournisseur de service, à savoir le [service de mise en forme des données pour OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), fournit les fonctionnalités de mise en forme des données et un fournisseur de données, tel que le fournisseur OLE DB pour SQL Server, fournit les lignes de données devant remplir l'objet [Recordset](recordset-object-ado.md) mis en forme.</span><span class="sxs-lookup"><span data-stu-id="4769e-p101">Data shaping typically requires two providers. The service provider, [Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), supplies the data shaping functionality, and a data provider, such as the OLE DB Provider for SQL Server, supplies rows of data to populate the shaped [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="4769e-106">Le nom du fournisseur de service (MSDataShape) peut être spécifié comme valeur de la propriété [Provider](connection-object-ado.md) de l'objet [Connection](provider-property-ado.md) ou du mot clé « Provider=MSDataShape; » dans la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="4769e-106">The name of the service provider (MSDataShape) can be specified as the value of the [Connection](connection-object-ado.md) object [Provider](provider-property-ado.md) property or the connection string keyword "Provider=MSDataShape;".</span></span>

<span data-ttu-id="4769e-107">Le nom du fournisseur de données peut être spécifié comme valeur de la propriété dynamique **Du fournisseur de données** , qui est ajoutée à la collection de [Propriétés](properties-collection-ado.md) de l’objet **Connection** par Microsoft Data Shaping Service pour OLE DB ou mot-clé de la chaîne de connexion « \* *Du fournisseur de données = \*\*\* fournisseur*».</span><span class="sxs-lookup"><span data-stu-id="4769e-107">The name of the data provider can be specified as the value of the **Data Provider** dynamic property, which is added to the **Connection** object [Properties](properties-collection-ado.md) collection by the Data Shaping Service for OLE DB, or the connection string keyword "\**Data Provider=\*\*\*provider*".</span></span>

<span data-ttu-id="4769e-p102">Aucun fournisseur de données n'est requis si l'objet **Recordset** est vide (comme dans un objet **Recordset** fabriqué contenant des colonnes créées avec le mot-clé NEW). Dans ce cas, spécifiez « **Data Provider=** none; ».</span><span class="sxs-lookup"><span data-stu-id="4769e-p102">No data provider is required if the **Recordset** is not populated (for example, as in a fabricated **Recordset** where columns are created with the NEW keyword). In that case, specify "**Data Provider=** none;".</span></span>

## <a name="example"></a><span data-ttu-id="4769e-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="4769e-110">Example</span></span>

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

