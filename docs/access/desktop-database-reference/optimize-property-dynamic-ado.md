---
title: Optimiser la propriété dynamique (ADO)
TOCTitle: Optimize dynamic property (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11bb7872514a828fdd97fb404f5366c35ff9a883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288251"
---
# <a name="optimize-dynamic-property-ado"></a><span data-ttu-id="10d5a-102">Optimiser la propriété dynamique (ADO)</span><span class="sxs-lookup"><span data-stu-id="10d5a-102">Optimize dynamic property (ADO)</span></span>


<span data-ttu-id="10d5a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="10d5a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="10d5a-104">Indique s'il est nécessaire de créer un index sur un champ.</span><span class="sxs-lookup"><span data-stu-id="10d5a-104">Specifies whether an index should be created on a field.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="10d5a-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="10d5a-105">Settings and return values</span></span>

<span data-ttu-id="10d5a-106">Définit ou renvoie une valeur **booléenne** indiquant si un index doit être créé.</span><span class="sxs-lookup"><span data-stu-id="10d5a-106">Sets or returns a **Boolean** value that indicates whether an index should be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="10d5a-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="10d5a-107">Remarks</span></span>

<span data-ttu-id="10d5a-p101">Un index peut améliorer les performances des opérations de recherche ou de tri des valeurs d'un objet [Recordset](recordset-object-ado.md). L'index est interne à ADO : vous ne pouvez pas y accéder explicitement ni l'utiliser dans votre application.</span><span class="sxs-lookup"><span data-stu-id="10d5a-p101">An index can improve the performance of operations that find or sort values in a [Recordset](recordset-object-ado.md). The index is internal to ADO — you cannot explicitly access or use it in your application.</span></span>

<span data-ttu-id="10d5a-p102">Pour créer un index sur un champ, donnez à la propriété **Optimize** la valeur **True**. Pour supprimer l'index, donnez à cette propriété la valeur **False**.</span><span class="sxs-lookup"><span data-stu-id="10d5a-p102">To create an index on a field, set the **Optimize** property to **True**. To delete the index, set this property to **False**.</span></span>

<span data-ttu-id="10d5a-112">**Optimize** est une propriété dynamique ajoutée à la collection [Properties](field-object-ado.md) de l'objet [Field](properties-collection-ado.md) lorsque la valeur de la propriété [CursorLocation](cursorlocation-property-ado.md) est **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="10d5a-112">**Optimize** is a dynamic property appended to the [Field](field-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

<span data-ttu-id="10d5a-113">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="10d5a-113">**Usage**</span></span>

```vb
    Dim rs As New Recordset
    Dim fld As Field
    rs.CursorLocation = adUseClient      'Enable index creation
    rs.Fields.Append "Field1", adChar, 35, adFldIsNullable
    rs.Open
    Set fld = rs.Fields(0)
    fld.Properties("Optimize") = True    'Create an index
    fld.Properties("Optimize") = False   'Delete an index
```
