---
title: Value, propriété (ADO)
TOCTitle: Value property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a61803648a0efa5f226b222fb54ce96c8aadbfe
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999056"
---
# <a name="value-property-ado"></a><span data-ttu-id="972f0-102">Value, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="972f0-102">Value property (ADO)</span></span>

<span data-ttu-id="972f0-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="972f0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="972f0-104">Indique la valeur attribuée à un objet [Field](field-object-ado.md), [Parameter](parameter-object-ado.md) ou [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="972f0-104">Indicates the value assigned to a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="972f0-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="972f0-105">Settings and return values</span></span>

<span data-ttu-id="972f0-p101">Définit ou renvoie une valeur **Variant** qui indique la valeur de l'objet. La valeur par défaut dépend de la propriété [Type](type-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="972f0-p101">Sets or returns a **Variant** value that indicates the value of the object. Default value depends on the [Type](type-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="972f0-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="972f0-108">Remarks</span></span>

<span data-ttu-id="972f0-p102">Utilisez la propriété **Valeur** pour définir ou renvoyer des données d'objets **Field**, pour définir ou renvoyer des valeurs de paramètres avec les objets **Parameter** ou pour définir ou renvoyer des paramètres de propriété avec les objets **Property**. La propriété **Value** peut être en lecture/écriture ou en lecture seule ; cela dépend de nombreux facteurs (voir les rubriques sur les objets concernés pour plus d'informations).</span><span class="sxs-lookup"><span data-stu-id="972f0-p102">Use the **Value** property to set or return data from **Field** objects, to set or return parameter values with **Parameter** objects, or to set or return property settings with **Property** objects. Whether the **Value** property is read/write or read-only depends upon numerous factors — see the respective object topics for more information.</span></span>

<span data-ttu-id="972f0-111">ADO permet de définir et de renvoyer des données binaires longues avec la propriété **Value**.</span><span class="sxs-lookup"><span data-stu-id="972f0-111">ADO allows setting and returning long binary data with the **Value** property.</span></span>

> [!NOTE]
> <span data-ttu-id="972f0-p103">[!REMARQUE] Pour les objets **Parameter**, ADO lit la propriété **Value** une seule fois à partir du fournisseur. Si une commande contient un objet **Parameter** dont la propriété **Value** est vide et que vous créez un [Recordset](recordset-object-ado.md) à partir de la commande, veillez à fermer le **Recordset** avant d'extraire la propriété **Value**. Sinon, pour certains fournisseurs, la propriété **Value** risque d'être vide ou de ne pas contenir la bonne valeur.</span><span class="sxs-lookup"><span data-stu-id="972f0-p103">For **Parameter** objects, ADO reads the **Value** property only once from the provider. If a command contains a **Parameter** whose **Value** property is empty, and you create a [Recordset](recordset-object-ado.md) from the command, ensure that you first close the **Recordset** before retrieving the **Value** property. Otherwise, for some providers, the **Value** property may be empty, and won't contain the correct value.</span></span>

<span data-ttu-id="972f0-p104">Pour les nouveaux objets **Field** ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), la propriété **Value** doit être définie avant les propriétés **Field**. Il faut d'abord attribuer une valeur spécifique à la propriété **Value** et appeler [Update](update-method-ado.md) sur la collection **Fields**. Il sera alors possible d'accéder aux autres propriétés comme [Type](type-property-ado.md) ou [Attributes](attributes-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="972f0-p104">For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, the **Value** property must be set before any other **Field** properties can be specified. First, a specific value for the **Value** property must have been assigned and [Update](update-method-ado.md) on the **Fields** collection called. Then, other properties such as [Type](type-property-ado.md) or [Attributes](attributes-property-ado.md) can be accessed.</span></span>

