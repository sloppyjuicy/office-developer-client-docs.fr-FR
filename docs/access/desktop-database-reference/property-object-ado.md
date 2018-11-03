---
title: Property, objet (ADO)
TOCTitle: Property object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b26a305557e2b7244399c6c2c5513909846eaaff
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929566"
---
# <a name="property-object-ado"></a><span data-ttu-id="4ea69-102">Property, objet (ADO)</span><span class="sxs-lookup"><span data-stu-id="4ea69-102">Property object (ADO)</span></span>


<span data-ttu-id="4ea69-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ea69-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4ea69-104">Représente une caractéristique dynamique d'un objet ADO défini par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4ea69-104">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ea69-105">Notes</span><span class="sxs-lookup"><span data-stu-id="4ea69-105">Remarks</span></span>

<span data-ttu-id="4ea69-106">Les objets ADO possèdent deux types de propriétés : intégrées et dynamiques.</span><span class="sxs-lookup"><span data-stu-id="4ea69-106">ADO objects have two types of properties: built-in and dynamic.</span></span>

<span data-ttu-id="4ea69-107">Les propriétés intégrées sont les propriétés implémentées dans ADO et immédiatement disponibles pour tout nouvel objet, en utilisant la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="4ea69-107">Built-in properties are those properties implemented in ADO and immediately available to any new object, using the syntax.</span></span> <span data-ttu-id="4ea69-108">Elles n'apparaissent pas en tant qu'objets **Property** dans une collection [Properties](properties-collection-ado.md) d'un objet ; ainsi, même si vous pouvez modifier leurs valeurs, vous ne pouvez pas modifier leurs caractéristiques.</span><span class="sxs-lookup"><span data-stu-id="4ea69-108">They do not appear as **Property** objects in an object's [Properties](properties-collection-ado.md) collection, so although you can change their values, you cannot modify their characteristics.</span></span>

<span data-ttu-id="4ea69-109">Les propriétés dynamiques sont définies par le fournisseur de données sous-jacent et apparaissent dans la collection **Properties** de l'objet ADO correspondant.</span><span class="sxs-lookup"><span data-stu-id="4ea69-109">Dynamic properties are defined by the underlying data provider, and appear in the **Properties** collection for the appropriate ADO object.</span></span> <span data-ttu-id="4ea69-110">Par exemple, une propriété spécifique au fournisseur peut indiquer si un objet [Recordset](recordset-object-ado.md) prend en charge les transactions ou les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="4ea69-110">For example, a property specific to the provider may indicate if a [Recordset](recordset-object-ado.md) object supports transactions or updating.</span></span> <span data-ttu-id="4ea69-111">Ces propriétés supplémentaires apparaissent comme des objets **Property** dans la collection **Properties** de cet objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="4ea69-111">These additional properties will appear as **Property** objects in that **Recordset** object's **Properties** collection.</span></span> <span data-ttu-id="4ea69-112">Propriétés dynamiques peuvent être référencées seulement par le biais de la collection à l’aide de la MyObject.Properties(0) ou ou MyObject.Properties("Name").</span><span class="sxs-lookup"><span data-stu-id="4ea69-112">Dynamic properties can be referenced only through the collection, using the MyObject.Properties(0) or or MyObject.Properties("Name") syntax.</span></span>

<span data-ttu-id="4ea69-113">Vous ne pouvez supprimer l'une ou l'autre propriété.</span><span class="sxs-lookup"><span data-stu-id="4ea69-113">You cannot delete either kind of property.</span></span>

<span data-ttu-id="4ea69-114">Un objet **Property** dynamique comporte quatre propriétés intégrées :</span><span class="sxs-lookup"><span data-stu-id="4ea69-114">A dynamic **Property** object has four built-in properties of its own:</span></span>

  - <span data-ttu-id="4ea69-115">La propriété [Name](name-property-ado.md) est une chaîne qui identifie la propriété.</span><span class="sxs-lookup"><span data-stu-id="4ea69-115">The [Name](name-property-ado.md) property is a string that identifies the property.</span></span>

  - <span data-ttu-id="4ea69-116">La propriété [Type](type-property-ado.md) est un entier qui spécifie le type de données de la propriété.</span><span class="sxs-lookup"><span data-stu-id="4ea69-116">The [Type](type-property-ado.md) property is an integer that specifies the property data type.</span></span>

  - <span data-ttu-id="4ea69-p103">Sa propriété [Value](value-property-ado.md) est une variante qui contient le paramètre de la propriété. **Value** est la propriété par défaut d'un objet **Property**.</span><span class="sxs-lookup"><span data-stu-id="4ea69-p103">The [Value](value-property-ado.md) property is a variant that contains the property setting. **Value** is the default property for a **Property** object.</span></span>

  - <span data-ttu-id="4ea69-119">Sa propriété [Attributes](attributes-property-ado.md) est une valeur de type long qui indique les caractéristiques de la propriété spécifiques du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4ea69-119">The [Attributes](attributes-property-ado.md) property is a long value that indicates characteristics of the property specific to the provider.</span></span>

