---
title: Parameter, objet (ADO)
TOCTitle: Parameter object (ADO)
ms:assetid: 7577598e-3d0c-30c6-5f24-1cfe98791798
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249481(v=office.15)
ms:contentKeyID: 48545676
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d6f3acd4af280f30706e35eb7ecda1dee11aa7d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288076"
---
# <a name="parameter-object-ado"></a><span data-ttu-id="8326a-102">Parameter, objet (ADO)</span><span class="sxs-lookup"><span data-stu-id="8326a-102">Parameter object (ADO)</span></span>


<span data-ttu-id="8326a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8326a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8326a-104">Représente un paramètre ou un argument associé à un objet [Command](command-object-ado.md) basé sur une requête paramétrée ou sur une procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="8326a-104">Represents a parameter or argument associated with a [Command](command-object-ado.md) object based on a parameterized query or stored procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="8326a-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="8326a-105">Remarks</span></span>

<span data-ttu-id="8326a-p101">De nombreux fournisseurs prennent en charge les commandes paramétrées. Ces dernières sont des commandes dans lesquelles l'action désirée est définie une fois, mais qui comportent des variables (ou paramètres) permettant d'en modifier certains aspects. Par exemple, une instruction SQL SELECT peut utiliser un paramètre pour définir les critères de correspondance d'une clause WHERE, et un autre définissant le nom de colonne pour une clause SORT BY.</span><span class="sxs-lookup"><span data-stu-id="8326a-p101">Many providers support parameterized commands. These are commands in which the desired action is defined once, but variables (or parameters) are used to alter some details of the command. For example, an SQL SELECT statement could use a parameter to define the matching criteria of a WHERE clause, and another to define the column name for a SORT BY clause.</span></span>

<span data-ttu-id="8326a-p102">Les objets **Parameter** représentent des paramètres associés à des requêtes paramétrées, ou les arguments d'entrée/sortie et les valeurs de retour de procédures stockées. Selon les fonctionnalités proposées par le fournisseur, certaines collections, méthodes ou propriétés d'un objet **Parameter** risquent de ne pas être disponibles.</span><span class="sxs-lookup"><span data-stu-id="8326a-p102">**Parameter** objects represent parameters associated with parameterized queries, or the in/out arguments and the return values of stored procedures. Depending on the functionality of the provider, some collections, methods, or properties of a **Parameter** object may not be available.</span></span>

<span data-ttu-id="8326a-111">Les collections, les méthodes et les propriétés d'un objet **Parameter** vous permettent d'effectuer diverses tâches :</span><span class="sxs-lookup"><span data-stu-id="8326a-111">With the collections, methods, and properties of a **Parameter** object, you can do the following:</span></span>

  - <span data-ttu-id="8326a-112">définir ou renvoyer le nom d'un paramètre avec la propriété [Name](name-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="8326a-112">Set or return the name of a parameter with the [Name](name-property-ado.md) property.</span></span>

  - <span data-ttu-id="8326a-p103">définir ou renvoyer la valeur d'un paramètre avec la propriété [Value](value-property-ado.md) ( **Value** étant la propriété par défaut de l'objet **Parameter** ) ;</span><span class="sxs-lookup"><span data-stu-id="8326a-p103">Set or return the value of a parameter with the [Value](value-property-ado.md) property. **Value** is the default property of the **Parameter** object.</span></span>

  - <span data-ttu-id="8326a-115">définir ou renvoyer les caractéristiques des paramètres avec les propriétés [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [Size](size-property-ado.md) et [Type](type-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="8326a-115">Set or return parameter characteristics with the [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [Size](size-property-ado.md), and [Type](type-property-ado.md) properties.</span></span>

  - <span data-ttu-id="8326a-116">passer des données binaires longues ou de caractères à un paramètre avec la méthode [AppendChunk](appendchunk-method-ado.md) :</span><span class="sxs-lookup"><span data-stu-id="8326a-116">Pass long binary or character data to a parameter with the [AppendChunk](appendchunk-method-ado.md) method.</span></span>

  - <span data-ttu-id="8326a-117">accéder aux attributs spécifiques d'un fournisseur avec la collection [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8326a-117">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="8326a-p104">Si vous connaissez les noms et les propriétés des paramètres associés à la procédure stockée ou à la requête paramétrée que vous voulez appeler, vous pouvez utiliser la méthode [CreateParameter](createparameter-method-ado.md) pour créer des objets **Parameter** avec les paramètres de propriété appropriés et utiliser la méthode [Append](append-method-ado.md) pour les ajouter à la collection [Parameters](parameters-collection-ado.md). Cela vous permet de définir et de renvoyer des valeurs de paramètres sans avoir à appeler la méthode [Refresh](refresh-method-ado.md) sur la collection **Parameters** pour récupérer les informations de paramètres auprès du fournisseur, opération potentiellement gourmande en ressources.</span><span class="sxs-lookup"><span data-stu-id="8326a-p104">If you know the names and properties of the parameters associated with the stored procedure or parameterized query you wish to call, you can use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the [Append](append-method-ado.md) method to add them to the [Parameters](parameters-collection-ado.md) collection. This lets you set and return parameter values without having to call the [Refresh](refresh-method-ado.md) method on the **Parameters** collection to retrieve the parameter information from the provider, a potentially resource-intensive operation.</span></span>

