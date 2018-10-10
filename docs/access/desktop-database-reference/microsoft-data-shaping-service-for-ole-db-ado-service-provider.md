---
title: Microsoft Data Shaping Service pour OLE DB (fournisseur de services ADO)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a72dcc754f39144da4476c9262b93b920fbfbdf6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470983"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a><span data-ttu-id="4d345-102">Microsoft Data Shaping Service pour OLE DB (fournisseur de services ADO)</span><span class="sxs-lookup"><span data-stu-id="4d345-102">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</span></span>


<span data-ttu-id="4d345-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d345-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4d345-104">Microsoft Data Shaping Service pour le fournisseur de services OLE DB prend en charge la construction d'objets [Recordset](recordset-object-ado.md) hiérarchiques (mis en forme) provenant d'un fournisseur de données.</span><span class="sxs-lookup"><span data-stu-id="4d345-104">The Microsoft Data Shaping Service for OLE DB service provider supports the construction of hierarchical (shaped) [Recordset](recordset-object-ado.md) objects from a data provider.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="4d345-105">Mot clé du fournisseur</span><span class="sxs-lookup"><span data-stu-id="4d345-105">Provider Keyword</span></span>

<span data-ttu-id="4d345-106">Pour invoquer Microsoft Data Shaping Service pour OLE DB, spécifiez le mot clé et la valeur suivants dans la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="4d345-106">To invoke the Data Shaping Service for OLE DB, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a><span data-ttu-id="4d345-107">Propriétés dynamiques</span><span class="sxs-lookup"><span data-stu-id="4d345-107">Dynamic Properties</span></span>

<span data-ttu-id="4d345-108">Lorsque ce fournisseur de services est appelé, les propriétés dynamiques suivantes sont ajoutées à la collection [Properties](connection-object-ado.md) de l'objet [Connection](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4d345-108">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4d345-109">Nom de la propriété dynamique</span><span class="sxs-lookup"><span data-stu-id="4d345-109">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="4d345-110">Description</span><span class="sxs-lookup"><span data-stu-id="4d345-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d345-111"><strong>Unique Reshape Names</strong></span><span class="sxs-lookup"><span data-stu-id="4d345-111"><strong>Unique Reshape Names</strong></span></span></p></td>
<td><p><span data-ttu-id="4d345-112">Indique si les objets <strong>Recordset</strong> dont les valeurs dupliquées de propriétés <strong>Reshape Name</strong> sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="4d345-112">Indicates whether <strong>Recordset</strong> objects with duplicate values for their <strong>Reshape Name</strong> properties are allowed.</span></span> <span data-ttu-id="4d345-113">Si cette propriété dynamique a la <strong>valeur True</strong> et un nouveau <strong>jeu d’enregistrements</strong> est créé avec le même utilisateur reshape nom comme un <strong>jeu d’enregistrements</strong>existant, puis nom de la mise en forme du nouvel objet <strong>Recordset</strong> est modifié pour rendre unique.</span><span class="sxs-lookup"><span data-stu-id="4d345-113">If this dynamic property is <strong>True</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as an existing <strong>Recordset</strong>, then the new <strong>Recordset</strong> object's reshape name is modified to make it unique.</span></span> <span data-ttu-id="4d345-114">Si cette propriété a la <strong>valeur False</strong> et un nouveau <strong>jeu d’enregistrements</strong> est créé avec le même spécifiée par l’utilisateur crée nom en tant que le <strong>jeu d’enregistrements</strong>existant, les deux objets <strong>Recordset</strong> aura le même nom modifier la forme.</span><span class="sxs-lookup"><span data-stu-id="4d345-114">If this property is <strong>False</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as the existing <strong>Recordset</strong>, both <strong>Recordset</strong> objects will have the same reshape name.</span></span> <span data-ttu-id="4d345-115">Par conséquent, aucun <strong>jeu d’enregistrements</strong> peut être redessinée tant qu’il existe deux jeux d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="4d345-115">Therefore, neither <strong>Recordset</strong> can be reshaped as long as both recordsets exist.</span></span> <span data-ttu-id="4d345-116">La valeur par défaut de la propriété est <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d345-116">The default value of the property is <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d345-117"><strong>Data Provider</strong></span><span class="sxs-lookup"><span data-stu-id="4d345-117"><strong>Data Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="4d345-p102">Indique le nom du fournisseur qui fournira les lignes à mettre en forme.

Cette valeur sera NONE si le fournisseur n'est pas destiné à être utilisé pour fournir des lignes.</span><span class="sxs-lookup"><span data-stu-id="4d345-p102">Indicates the name of the provider that will supply rows to be shaped. This value may be NONE if a provider will not be used to supply rows.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4d345-p103">Vous pouvez aussi définir des propriétés dynamiques en écriture en spécifiant leurs noms en tant que mots clé dans la chaîne de connexion. Par exemple dans Microsoft Visual Basic, définissez la propriété dynamique **Data Provider** sur « MSDASQL » en spécifiant :</span><span class="sxs-lookup"><span data-stu-id="4d345-p103">You may also set writable dynamic properties by specifying their names as keywords in the connection string. For example, in Microsoft Visual Basic, set the **Data Provider** dynamic property to "MSDASQL" by specifying:</span></span>

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

<span data-ttu-id="4d345-p104">Vous pouvez également définir ou extraire une propriété dynamique en spécifiant son nom en tant qu'index de la propriété [Properties](properties-collection-ado.md). Par exemple, vous pouvez obtenir et imprimer la valeur actuelle de la propriété dynamique **Data Provider**, puis définir une nouvelle valeur de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="4d345-p104">You may also set or retrieve a dynamic property by specifying its name as the index to the [Properties](properties-collection-ado.md) property. For example, get and print the current value of the **Data Provider** dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

<span data-ttu-id="4d345-124">Pour plus d'informations sur la mise en forme des données, consultez la rubrique [Mise en forme des données](data-shaping-summary.md).</span><span class="sxs-lookup"><span data-stu-id="4d345-124">For more information about data shaping, see [Data Shaping](data-shaping-summary.md).</span></span>

