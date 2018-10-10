---
title: Attributes, propriété (ADO)
TOCTitle: Attributes Property (ADO)
ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15)
ms:contentKeyID: 48544716
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231117
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9fa17593a5606d288e519969ff63f10a1df229ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469681"
---
# <a name="attributes-property-ado"></a><span data-ttu-id="e8a65-102">Attributes, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="e8a65-102">Attributes Property (ADO)</span></span>


<span data-ttu-id="e8a65-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8a65-103">**Applies to**: Access 2013 | Office 2013</span></span>


## <a name="attributes-property"></a><span data-ttu-id="e8a65-104">Attributes, propriété</span><span class="sxs-lookup"><span data-stu-id="e8a65-104">Attributes Property</span></span>

<span data-ttu-id="e8a65-105">Indique une ou plusieurs caractéristiques d'un objet.</span><span class="sxs-lookup"><span data-stu-id="e8a65-105">Indicates one or more characteristics of an object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e8a65-106">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e8a65-106">Settings and Return Values</span></span>

<span data-ttu-id="e8a65-107">Définit ou renvoie une valeur de type **Long**.</span><span class="sxs-lookup"><span data-stu-id="e8a65-107">Sets or returns a **Long** value.</span></span>

<span data-ttu-id="e8a65-p101">Pour un objet [Connection](connection-object-ado.md), la propriété **Attributes** est en lecture/écriture et sa valeur peut être la somme d'une ou de plusieurs valeurs de [XactAttributeEnum](xactattributeenum.md). La valeur par défaut est zéro (0).</span><span class="sxs-lookup"><span data-stu-id="e8a65-p101">For a [Connection](connection-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of one or more [XactAttributeEnum](xactattributeenum.md) values. The default is zero (0).</span></span>

<span data-ttu-id="e8a65-p102">Pour un objet [Parameter](parameter-object-ado.md), la propriété **Attributes** est en lecture/écriture et sa valeur peut être la somme d'une ou de plusieurs valeurs de [ParameterAttributesEnum](parameterattributesenum.md). La valeur par défaut est **adParamSigned**.</span><span class="sxs-lookup"><span data-stu-id="e8a65-p102">For a [Parameter](parameter-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of any one or more [ParameterAttributesEnum](parameterattributesenum.md) values. The default is **adParamSigned**.</span></span>

<span data-ttu-id="e8a65-p103">Pour un objet [Field](field-object-ado.md), la propriété **Attributes** peut être la somme d'une ou de plusieurs valeurs de [FieldAttributeEnum](fieldattributeenum.md). Elle est normalement en lecture seule. Cependant, pour les nouveaux objets **Field** qui ont été ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), la propriété **Attributes** est en lecture/écriture uniquement après que la propriété [Value](value-property-ado.md) de l'objet **Field** a été spécifiée et que le nouvel objet **Field** a pu être ajouté par le fournisseur de données par un appel de la méthode [Update](update-method-ado.md) de la collection **Fields**.</span><span class="sxs-lookup"><span data-stu-id="e8a65-p103">For a [Field](field-object-ado.md) object, the **Attributes** property can be the sum of one or more [FieldAttributeEnum](fieldattributeenum.md) values. It is normally read-only, However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Attributes** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the new **Field** has been successfully added by the data provider by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="e8a65-114">Pour un objet [Property](property-object-ado.md), la propriété **Attributes** est en lecture seule et sa valeur peut être la somme d'une ou plusieurs valeurs de [PropertyAttributesEnum](propertyattributesenum.md).</span><span class="sxs-lookup"><span data-stu-id="e8a65-114">For a [Property](property-object-ado.md) object, the **Attributes** property is read-only, and its value can be the sum of any one or more [PropertyAttributesEnum](propertyattributesenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8a65-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e8a65-115">Remarks</span></span>

<span data-ttu-id="e8a65-116">Utilisez la propriété **Attributes** pour définir ou retourner les caractéristiques des objets **Connection**, **Parameter**, [Field](field-object-ado.md) ou [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e8a65-116">Use the **Attributes** property to set or return characteristics of **Connection** objects, **Parameter** objects, [Field](field-object-ado.md) objects, or [Property](property-object-ado.md) objects.</span></span>

<span data-ttu-id="e8a65-p104">Lorsque vous définissez plusieurs attributs, vous pouvez additionner les constantes appropriées. Si vous attribuez à la propriété une valeur représentant une somme qui inclut des constantes incompatibles, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="e8a65-p104">When you set multiple attributes, you can sum the appropriate constants. If you set the property value to a sum including incompatible constants, an error occurs.</span></span>

<span data-ttu-id="e8a65-119">**L’utilisation du Service de données à distance** Cette propriété n’est pas disponible sur un objet de **connexion** côté client.</span><span class="sxs-lookup"><span data-stu-id="e8a65-119">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

