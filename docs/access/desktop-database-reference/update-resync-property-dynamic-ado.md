---
title: Update Resync, propriété dynamique (ADO)
TOCTitle: Update Resync Property--Dynamic (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 16600f22084718a6b32656ebfc56d6a9be06c676
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470649"
---
# <a name="update-resync-property--dynamic-ado"></a><span data-ttu-id="7cac4-102">Update Resync, propriété dynamique (ADO)</span><span class="sxs-lookup"><span data-stu-id="7cac4-102">Update Resync Property--Dynamic (ADO)</span></span>


<span data-ttu-id="7cac4-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7cac4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7cac4-104">Spécifie si la méthode [UpdateBatch](updatebatch-method-ado.md) est suivie d'une opération de méthode [Resync](resync-method-ado.md) implicite et, si c'est le cas, la portée de cette opération.</span><span class="sxs-lookup"><span data-stu-id="7cac4-104">Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation, and if so, the scope of that operation.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7cac4-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="7cac4-105">Settings and Return Values</span></span>

<span data-ttu-id="7cac4-106">Définit ou renvoie une ou plusieurs de la [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) valeurs.</span><span class="sxs-lookup"><span data-stu-id="7cac4-106">Sets or returns one or more of the [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cac4-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="7cac4-107">Remarks</span></span>

<span data-ttu-id="7cac4-108">Les valeurs de ADCPROP\_UPDATERESYNC\_ENUM peut-être être combinée, à l’exception d’adResyncAll qui représente déjà la combinaison des autres valeurs.</span><span class="sxs-lookup"><span data-stu-id="7cac4-108">The values of ADCPROP\_UPDATERESYNC\_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</span></span>

<span data-ttu-id="7cac4-109">La constante **adResyncConflicts** stocke les valeurs de resynchronisation comme des valeurs sous-jacentes, mais ne remplace pas les modifications en attente.</span><span class="sxs-lookup"><span data-stu-id="7cac4-109">The constant **adResyncConflicts** stores the resync values as underlying values, but does not override pending changes.</span></span>

<span data-ttu-id="7cac4-110">La propriété **Update Resync** est une propriété dynamique ajoutée à la collection [Properties](recordset-object-ado.md) de l'objet [Recordset](properties-collection-ado.md) lorsque la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="7cac4-110">**Update Resync** is a dynamic property appended to the [Recordset](recordset-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

