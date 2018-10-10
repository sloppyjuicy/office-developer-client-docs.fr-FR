---
title: Optimize, propriété dynamique (ADO)
TOCTitle: Optimize Property--Dynamic (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6c31950eda813ee4f3f07145d28a83106cf86b3f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470202"
---
# <a name="optimize-property--dynamic-ado"></a><span data-ttu-id="6aaa9-102">Optimize, propriété dynamique (ADO)</span><span class="sxs-lookup"><span data-stu-id="6aaa9-102">Optimize Property--Dynamic (ADO)</span></span>


<span data-ttu-id="6aaa9-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6aaa9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6aaa9-104">Indique s'il est nécessaire de créer un index sur un champ.</span><span class="sxs-lookup"><span data-stu-id="6aaa9-104">Specifies whether an index should be created on a field.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="6aaa9-105">Paramètres et valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="6aaa9-105">Settings and Return Values</span></span>

<span data-ttu-id="6aaa9-106">Définit ou renvoie une valeur **booléenne** indiquant si un index doit être créé.</span><span class="sxs-lookup"><span data-stu-id="6aaa9-106">Sets or returns a **Boolean** value that indicates whether an index should be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="6aaa9-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="6aaa9-107">Remarks</span></span>

<span data-ttu-id="6aaa9-p101">Un index peut améliorer les performances des opérations de recherche ou de tri des valeurs d'un objet [Recordset](recordset-object-ado.md). L'index est interne à ADO : vous ne pouvez pas y accéder explicitement ni l'utiliser dans votre application.</span><span class="sxs-lookup"><span data-stu-id="6aaa9-p101">An index can improve the performance of operations that find or sort values in a [Recordset](recordset-object-ado.md). The index is internal to ADO — you cannot explicitly access or use it in your application.</span></span>

<span data-ttu-id="6aaa9-p102">Pour créer un index sur un champ, donnez à la propriété **Optimize** la valeur **True**. Pour supprimer l'index, donnez à cette propriété la valeur **False**.</span><span class="sxs-lookup"><span data-stu-id="6aaa9-p102">To create an index on a field, set the **Optimize** property to **True**. To delete the index, set this property to **False**.</span></span>

<span data-ttu-id="6aaa9-112">**Optimize** est une propriété dynamique ajoutée à la collection [Properties](field-object-ado.md) de l'objet [Field](properties-collection-ado.md) lorsque la valeur de la propriété [CursorLocation](cursorlocation-property-ado.md) est **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="6aaa9-112">**Optimize** is a dynamic property appended to the [Field](field-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

<span data-ttu-id="6aaa9-113">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="6aaa9-113">**Usage**</span></span>

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
