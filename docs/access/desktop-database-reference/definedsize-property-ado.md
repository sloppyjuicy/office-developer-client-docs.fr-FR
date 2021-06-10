---
title: DefinedSize, propriété (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 121e81734fc5ecc0a761dae53942f1cbed98df2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294133"
---
# <a name="definedsize-property-ado"></a><span data-ttu-id="1947d-102">DefinedSize, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="1947d-102">DefinedSize property (ADO)</span></span>


<span data-ttu-id="1947d-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1947d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1947d-104">Indique la capacité en données d'un objet [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1947d-104">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="1947d-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1947d-105">Return value</span></span>

<span data-ttu-id="1947d-106">Renvoie une valeur de type **Long** qui reflète la taille définie pour un champ sous la forme d'un nombre d'octets.</span><span class="sxs-lookup"><span data-stu-id="1947d-106">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="1947d-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="1947d-107">Remarks</span></span>

<span data-ttu-id="1947d-108">Utilisez la propriété **DefinedSize** pour déterminer la capacité en données d'un objet **Field**.</span><span class="sxs-lookup"><span data-stu-id="1947d-108">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="1947d-p101">Les propriétés **DefinedSize** et [ActualSize](actualsize-property-ado.md) sont différentes. Par exemple, imaginez un objet **Field** avec le type déclaré **adVarChar** et une propriété **DefinedSize** de 50, contenant un caractère unique. La valeur retournée pour la propriété **ActualSize** correspond à la longueur en octets du caractère unique.</span><span class="sxs-lookup"><span data-stu-id="1947d-p101">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

