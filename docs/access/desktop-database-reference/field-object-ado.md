---
title: Field, objet - ActiveX Data Objects (ADO)
TOCTitle: Field object (ADO)
ms:assetid: 1dbd535e-48ad-a5c8-a1b2-6776c1e3e19d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248968(v=office.15)
ms:contentKeyID: 48543600
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d131f2634551c9c2538a87cdc8f15cfa6cc96430
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924869"
---
# <a name="field-object-ado"></a><span data-ttu-id="048be-102">Field, objet (ADO)</span><span class="sxs-lookup"><span data-stu-id="048be-102">Field object (ADO)</span></span>


<span data-ttu-id="048be-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="048be-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="048be-104">Représente une colonne de données avec un type de données commun.</span><span class="sxs-lookup"><span data-stu-id="048be-104">Represents a column of data with a common data type.</span></span>

## <a name="remarks"></a><span data-ttu-id="048be-105">Notes</span><span class="sxs-lookup"><span data-stu-id="048be-105">Remarks</span></span>

<span data-ttu-id="048be-p101">Chaque objet **Field** correspond à une colonne du [Recordset](recordset-object-ado.md). Vous utilisez la propriété [Value](value-property-ado.md) des objets **Field** pour définir ou renvoyer des données pour l'enregistrement actif. Selon les fonctionnalités proposées par le fournisseur, certaines collections, méthodes ou propriétés d'un objet **Field** risquent de ne pas être disponibles.</span><span class="sxs-lookup"><span data-stu-id="048be-p101">Each **Field** object corresponds to a column in the [Recordset](recordset-object-ado.md). You use the [Value](value-property-ado.md) property of **Field** objects to set or return data for the current record. Depending on the functionality the provider exposes, some collections, methods, or properties of a **Field** object may not be available.</span></span>

<span data-ttu-id="048be-109">Les collections, les méthodes et les propriétés d'un objet **Field** vous permettent d'effectuer diverses tâches :</span><span class="sxs-lookup"><span data-stu-id="048be-109">With the collections, methods, and properties of a **Field** object, you can do the following:</span></span>

  - <span data-ttu-id="048be-110">renvoyer le nom d'un champ avec la propriété [Name](name-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="048be-110">Return the name of a field with the [Name](name-property-ado.md) property.</span></span>

  - <span data-ttu-id="048be-p102">afficher ou modifier les données d'un champ avec la propriété **Value** ( **Value** étant la propriété par défaut de l'objet **Field** ) ;</span><span class="sxs-lookup"><span data-stu-id="048be-p102">View or change the data in the field with the **Value** property. **Value** is the default property of the **Field** object.</span></span>

  - <span data-ttu-id="048be-113">renvoyer les caractéristiques de base d'un champ à l'aide des propriétés [Type](type-property-ado.md), [Precision](precision-property-ado.md) et [NumericScale](numericscale-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="048be-113">Return the basic characteristics of a field with the [Type](type-property-ado.md), [Precision](precision-property-ado.md), and [NumericScale](numericscale-property-ado.md) properties.</span></span>

  - <span data-ttu-id="048be-114">renvoyer la taille déclarée d'un champ avec la propriété [DefinedSize](definedsize-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="048be-114">Return the declared size of a field with the [DefinedSize](definedsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="048be-115">renvoyer la taille réelle des données d'un champ donné au moyen de la propriété [ActualSize](actualsize-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="048be-115">Return the actual size of the data in a given field with the [ActualSize](actualsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="048be-116">déterminer quels types de fonctionnalités sont prises en charge pour un champ donné avec la propriété [Attributes](attributes-property-ado.md) et la collection [Properties](properties-collection-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="048be-116">Determine what types of functionality are supported for a given field with the [Attributes](attributes-property-ado.md) property and [Properties](properties-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="048be-117">manipuler les valeurs de champs contenant des données binaires longues ou caractères longs avec les méthodes [AppendChunk](appendchunk-method-ado.md) et [GetChunk](getchunk-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="048be-117">Manipulate the values of fields containing long binary or long character data with the [AppendChunk](appendchunk-method-ado.md) and [GetChunk](getchunk-method-ado.md) methods.</span></span>

  - <span data-ttu-id="048be-118">si le fournisseur prend en charge les mises à jour par lot, résoudre les incohérences présentes dans les valeurs des champs pendant la mise à jour par lot avec les propriétés [OriginalValue](originalvalue-property-ado.md) et [UnderlyingValue](underlyingvalue-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="048be-118">If the provider supports batch updates, resolve discrepancies in field values during batch updating with the [OriginalValue](originalvalue-property-ado.md) and [UnderlyingValue](underlyingvalue-property-ado.md) properties.</span></span>

<span data-ttu-id="048be-p103">Toutes les propriétés de métadonnées (**Name**, **Type**, **DefinedSize**, **Precision** et **NumericScale**) sont disponibles avant d'ouvrir le **Recordset** de l'objet **Field**. En les définissant à ce moment-là, vous facilitez la construction dynamique des formulaires.</span><span class="sxs-lookup"><span data-stu-id="048be-p103">All of the metadata properties (**Name**, **Type**, **DefinedSize**, **Precision**, and **NumericScale**) are available before opening the **Field** object's **Recordset**. Setting them at that time is useful for dynamically constructing forms.</span></span>

