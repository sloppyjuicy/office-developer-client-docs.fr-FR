---
title: Optimize, propriété dynamique (ADO)
TOCTitle: Optimize Property--Dynamic (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7276e642e15137bdcfcb939330a3642d96e9a5a2
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605176"
---
# <a name="optimize-property--dynamic-ado"></a><span data-ttu-id="3e01d-102">Optimize, propriété dynamique (ADO)</span><span class="sxs-lookup"><span data-stu-id="3e01d-102">Optimize Property--Dynamic (ADO)</span></span>


<span data-ttu-id="3e01d-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e01d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3e01d-104">Indique s'il est nécessaire de créer un index sur un champ.</span><span class="sxs-lookup"><span data-stu-id="3e01d-104">Specifies whether an index should be created on a field.</span></span>

<span data-ttu-id="3e01d-105"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="3e01d-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="3e01d-106">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3e01d-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="3e01d-107">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3e01d-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="3e01d-108">master</span><span class="sxs-lookup"><span data-stu-id="3e01d-108">master</span></span>

<span data-ttu-id="3e01d-109">Définit ou renvoie une valeur **booléenne** indiquant si un index doit être créé.</span><span class="sxs-lookup"><span data-stu-id="3e01d-109">Sets or returns a **Boolean** value that indicates whether an index should be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e01d-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="3e01d-110">Remarks</span></span>

<span data-ttu-id="3e01d-p101">Un index peut améliorer les performances des opérations de recherche ou de tri des valeurs d'un objet [Recordset](recordset-object-ado.md). L'index est interne à ADO : vous ne pouvez pas y accéder explicitement ni l'utiliser dans votre application.</span><span class="sxs-lookup"><span data-stu-id="3e01d-p101">An index can improve the performance of operations that find or sort values in a [Recordset](recordset-object-ado.md). The index is internal to ADO — you cannot explicitly access or use it in your application.</span></span>

<span data-ttu-id="3e01d-p102">Pour créer un index sur un champ, donnez à la propriété **Optimize** la valeur **True**. Pour supprimer l'index, donnez à cette propriété la valeur **False**.</span><span class="sxs-lookup"><span data-stu-id="3e01d-p102">To create an index on a field, set the **Optimize** property to **True**. To delete the index, set this property to **False**.</span></span>

<span data-ttu-id="3e01d-115">**Optimize** est une propriété dynamique ajoutée à la collection [Properties](field-object-ado.md) de l'objet [Field](properties-collection-ado.md) lorsque la valeur de la propriété [CursorLocation](cursorlocation-property-ado.md) est **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="3e01d-115">**Optimize** is a dynamic property appended to the [Field](field-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

<span data-ttu-id="3e01d-116">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="3e01d-116">**Usage**</span></span>

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
