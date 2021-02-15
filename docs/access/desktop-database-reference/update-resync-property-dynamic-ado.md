---
title: Update Resync dynamic property (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 653291ade258d602d7ec523dcac7e9fe51dd91fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308343"
---
# <a name="update-resync-dynamic-property-ado"></a><span data-ttu-id="ac71e-102">Update Resync dynamic property (ADO)</span><span class="sxs-lookup"><span data-stu-id="ac71e-102">Update Resync dynamic property (ADO)</span></span>


<span data-ttu-id="ac71e-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac71e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ac71e-104">Spécifie si la méthode [UpdateBatch](updatebatch-method-ado.md) est suivie d'une opération de méthode [Resync](resync-method-ado.md) implicite et, si c'est le cas, la portée de cette opération.</span><span class="sxs-lookup"><span data-stu-id="ac71e-104">Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation, and if so, the scope of that operation.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="ac71e-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="ac71e-105">Settings and return values</span></span>

<span data-ttu-id="ac71e-106">Définit ou renvoie une ou plusieurs des valeurs [ADCPROP \_ UPDATERESYNC \_ ENUM.](adcprop-updateresync-enum.md)</span><span class="sxs-lookup"><span data-stu-id="ac71e-106">Sets or returns one or more of the [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac71e-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="ac71e-107">Remarks</span></span>

<span data-ttu-id="ac71e-108">Les valeurs d’ADCPROP UPDATERESYNC ENUM peuvent être combinées, à l’exception d’adResyncAll qui représente déjà la combinaison du reste des \_ \_ valeurs.</span><span class="sxs-lookup"><span data-stu-id="ac71e-108">The values of ADCPROP\_UPDATERESYNC\_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</span></span>

<span data-ttu-id="ac71e-109">La constante **adResyncConflicts** stocke les valeurs de resynchronisation comme des valeurs sous-jacentes, mais ne remplace pas les modifications en attente.</span><span class="sxs-lookup"><span data-stu-id="ac71e-109">The constant **adResyncConflicts** stores the resync values as underlying values, but does not override pending changes.</span></span>

<span data-ttu-id="ac71e-110">La propriété **Update Resync** est une propriété dynamique ajoutée à la collection [Properties](recordset-object-ado.md) de l'objet [Recordset](properties-collection-ado.md) lorsque la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="ac71e-110">**Update Resync** is a dynamic property appended to the [Recordset](recordset-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

