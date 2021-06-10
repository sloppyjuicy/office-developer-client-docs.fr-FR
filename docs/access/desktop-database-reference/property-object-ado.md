---
title: Property, objet (ADO)
TOCTitle: Property object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 262f4873359508a985b27f3d4ea70a5fcbfd620f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302918"
---
# <a name="property-object-ado"></a><span data-ttu-id="dae31-102">Property, objet (ADO)</span><span class="sxs-lookup"><span data-stu-id="dae31-102">Property object (ADO)</span></span>


<span data-ttu-id="dae31-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dae31-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dae31-104">Représente une caractéristique dynamique d'un objet ADO défini par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="dae31-104">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="dae31-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="dae31-105">Remarks</span></span>

<span data-ttu-id="dae31-106">Les objets ADO possèdent deux types de propriétés : intégrées et dynamiques.</span><span class="sxs-lookup"><span data-stu-id="dae31-106">ADO objects have two types of properties: built-in and dynamic.</span></span>

<span data-ttu-id="dae31-107">Les propriétés intégrées sont les propriétés implémentées dans ADO et immédiatement disponibles pour tout nouvel objet, à l’aide de la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="dae31-107">Built-in properties are those properties implemented in ADO and immediately available to any new object, using the syntax.</span></span> <span data-ttu-id="dae31-108">Elles n'apparaissent pas en tant qu'objets **Property** dans une collection [Properties](properties-collection-ado.md) d'un objet ; ainsi, même si vous pouvez modifier leurs valeurs, vous ne pouvez pas modifier leurs caractéristiques.</span><span class="sxs-lookup"><span data-stu-id="dae31-108">They do not appear as **Property** objects in an object's [Properties](properties-collection-ado.md) collection, so although you can change their values, you cannot modify their characteristics.</span></span>

<span data-ttu-id="dae31-109">Les propriétés dynamiques sont définies par le fournisseur de données sous-jacent et apparaissent dans la collection **Properties** de l'objet ADO correspondant.</span><span class="sxs-lookup"><span data-stu-id="dae31-109">Dynamic properties are defined by the underlying data provider, and appear in the **Properties** collection for the appropriate ADO object.</span></span> <span data-ttu-id="dae31-110">Par exemple, une propriété spécifique au fournisseur peut indiquer si un objet [Recordset](recordset-object-ado.md) prend en charge les transactions ou les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="dae31-110">For example, a property specific to the provider may indicate if a [Recordset](recordset-object-ado.md) object supports transactions or updating.</span></span> <span data-ttu-id="dae31-111">Ces propriétés supplémentaires apparaissent comme des objets **Property** dans la collection **Properties** de cet objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="dae31-111">These additional properties will appear as **Property** objects in that **Recordset** object's **Properties** collection.</span></span> <span data-ttu-id="dae31-112">Les propriétés dynamiques peuvent être référencés uniquement par le biais de la collection, à l’aide de la syntaxe MyObject.Properties(0) ou MyObject.Properties(« Name »).</span><span class="sxs-lookup"><span data-stu-id="dae31-112">Dynamic properties can be referenced only through the collection, using the MyObject.Properties(0) or or MyObject.Properties("Name") syntax.</span></span>

<span data-ttu-id="dae31-113">Vous ne pouvez supprimer ni l'un ni l'autre de ces deux types de propriétés.</span><span class="sxs-lookup"><span data-stu-id="dae31-113">You cannot delete either kind of property.</span></span>

<span data-ttu-id="dae31-114">Un objet **Property** dynamique possède quatre propriétés intégrées :</span><span class="sxs-lookup"><span data-stu-id="dae31-114">A dynamic **Property** object has four built-in properties of its own:</span></span>

  - <span data-ttu-id="dae31-115">Sa propriété [Name](name-property-ado.md) est une chaîne qui identifie la propriété.</span><span class="sxs-lookup"><span data-stu-id="dae31-115">The [Name](name-property-ado.md) property is a string that identifies the property.</span></span>

  - <span data-ttu-id="dae31-116">Sa propriété [Type](type-property-ado.md) est un entier qui spécifie le type de données de la propriété.</span><span class="sxs-lookup"><span data-stu-id="dae31-116">The [Type](type-property-ado.md) property is an integer that specifies the property data type.</span></span>

  - <span data-ttu-id="dae31-p103">Sa propriété [Value](value-property-ado.md) est une variante qui contient le paramètre de la propriété. **Value** est la propriété par défaut d'un objet **Property**.</span><span class="sxs-lookup"><span data-stu-id="dae31-p103">The [Value](value-property-ado.md) property is a variant that contains the property setting. **Value** is the default property for a **Property** object.</span></span>

  - <span data-ttu-id="dae31-119">Sa propriété [Attributes](attributes-property-ado.md) est une valeur de type long qui indique les caractéristiques de la propriété spécifiques du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="dae31-119">The [Attributes](attributes-property-ado.md) property is a long value that indicates characteristics of the property specific to the provider.</span></span>

