---
title: ActualSize, propriété (ADO)
TOCTitle: ActualSize property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c13cb41299ddaf786e6412e43a50b1414ad818b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280431"
---
# <a name="actualsize-property-ado"></a><span data-ttu-id="066f9-102">ActualSize, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="066f9-102">ActualSize property (ADO)</span></span>

<span data-ttu-id="066f9-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="066f9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="066f9-104">Indique la longueur réelle de la valeur d'un champ.</span><span class="sxs-lookup"><span data-stu-id="066f9-104">Indicates the actual length of a field's value.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="066f9-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="066f9-105">Settings and return values</span></span>

<span data-ttu-id="066f9-p101">Retourne une valeur de type **Long**. Certains fournisseurs permettent parfois que la propriété soit définie afin de réserver de l'espace pour les données d'objets BLOB (Binary Large Object), auquel cas la valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="066f9-p101">Returns a **Long** value. Some providers may allow this property to be set to reserve space for BLOB data, in which case the default value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="066f9-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="066f9-108">Remarks</span></span>

<span data-ttu-id="066f9-p102">Utilisez la propriété **ActualSize** pour retourner la longueur réelle de la valeur d’un objet [Field](field-object-ado.md). Pour tous les champs, la propriété **ActualSize** est en lecture seule. Si ADO ne peut pas déterminer la longueur de la valeur de l’objet **Field**, la propriété **ActualSize** retourne **adUnknown**.</span><span class="sxs-lookup"><span data-stu-id="066f9-p102">Use the **ActualSize** property to return the actual length of a [Field](field-object-ado.md) object's value. For all fields, the **ActualSize** property is read-only. If ADO cannot determine the length of the **Field** object's value, the **ActualSize** property returns **adUnknown**.</span></span>

<span data-ttu-id="066f9-112">Les **propriétés ActualSize** et [DefinedSize](definedsize-property-ado.md) sont différentes.</span><span class="sxs-lookup"><span data-stu-id="066f9-112">The **ActualSize** and [DefinedSize](definedsize-property-ado.md) properties are different.</span></span> <span data-ttu-id="066f9-113">Un objet **Field** avec un type déclaré **adVarChar** et une longueur maximale de 50 caractères retourne la valeur 50 pour la propriété **DefinedSize**, mais la valeur de la propriété **ActualSize** renvoyée correspond à la longueur des données stockées dans le champ de l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="066f9-113">A **Field** object with a declared type of **adVarChar** and a maximum length of 50 characters returns a **DefinedSize** property value of 50, but the **ActualSize** property value it returns is the length of the data stored in the field for the current record.</span></span> <span data-ttu-id="066f9-114">Les objets **Field** avec une valeur **DefinedSize** supérieure à 255 octets sont traités comme des colonnes de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="066f9-114">**Fields** with a **DefinedSize** greater than 255 bytes are treated as variable length columns.</span></span>

