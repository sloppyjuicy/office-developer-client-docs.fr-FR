---
title: DefinedSize, propriété (ADO)
TOCTitle: DefinedSize Property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8ffd8bb24abcab737ebc4bb23a0af717c02d486
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469653"
---
# <a name="definedsize-property-ado"></a><span data-ttu-id="6fcac-102">DefinedSize, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="6fcac-102">DefinedSize Property (ADO)</span></span>


<span data-ttu-id="6fcac-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fcac-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6fcac-104">Indique la capacité en données d'un objet [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6fcac-104">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="6fcac-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6fcac-105">Return Value</span></span>

<span data-ttu-id="6fcac-106">Renvoie une valeur de type **Long** qui reflète la taille définie pour un champ sous la forme d'un nombre d'octets.</span><span class="sxs-lookup"><span data-stu-id="6fcac-106">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fcac-107">Notes</span><span class="sxs-lookup"><span data-stu-id="6fcac-107">Remarks</span></span>

<span data-ttu-id="6fcac-108">Utilisez la propriété **DefinedSize** pour déterminer la capacité en données d'un objet **Field**.</span><span class="sxs-lookup"><span data-stu-id="6fcac-108">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="6fcac-p101">Les propriétés **DefinedSize** et [ActualSize](actualsize-property-ado.md) sont différentes. Par exemple, imaginez un objet **Field** avec le type déclaré **adVarChar** et une propriété **DefinedSize** de 50, contenant un caractère unique. La valeur retournée pour la propriété **ActualSize** correspond à la longueur en octets du caractère unique.</span><span class="sxs-lookup"><span data-stu-id="6fcac-p101">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

