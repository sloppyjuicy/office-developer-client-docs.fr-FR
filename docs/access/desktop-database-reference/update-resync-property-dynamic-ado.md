---
title: Update Resync, propriété dynamique (ADO)
TOCTitle: Update Resync Property--Dynamic (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4eea391e99202eeb075d73daa1034dff2042e49
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604420"
---
# <a name="update-resync-property--dynamic-ado"></a><span data-ttu-id="7a620-102">Update Resync, propriété dynamique (ADO)</span><span class="sxs-lookup"><span data-stu-id="7a620-102">Update Resync Property--Dynamic (ADO)</span></span>


<span data-ttu-id="7a620-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a620-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7a620-104">Spécifie si la méthode [UpdateBatch](updatebatch-method-ado.md) est suivie d'une opération de méthode [Resync](resync-method-ado.md) implicite et, si c'est le cas, la portée de cette opération.</span><span class="sxs-lookup"><span data-stu-id="7a620-104">Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation, and if so, the scope of that operation.</span></span>

<span data-ttu-id="7a620-105"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="7a620-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="7a620-106">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="7a620-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="7a620-107">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="7a620-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="7a620-108">master</span><span class="sxs-lookup"><span data-stu-id="7a620-108">master</span></span>

<span data-ttu-id="7a620-109">Définit ou renvoie une ou plusieurs de la [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) valeurs.</span><span class="sxs-lookup"><span data-stu-id="7a620-109">Sets or returns one or more of the [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a620-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="7a620-110">Remarks</span></span>

<span data-ttu-id="7a620-111">Les valeurs de ADCPROP\_UPDATERESYNC\_ENUM peut-être être combinée, à l’exception d’adResyncAll qui représente déjà la combinaison des autres valeurs.</span><span class="sxs-lookup"><span data-stu-id="7a620-111">The values of ADCPROP\_UPDATERESYNC\_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</span></span>

<span data-ttu-id="7a620-112">La constante **adResyncConflicts** stocke les valeurs de resynchronisation comme des valeurs sous-jacentes, mais ne remplace pas les modifications en attente.</span><span class="sxs-lookup"><span data-stu-id="7a620-112">The constant **adResyncConflicts** stores the resync values as underlying values, but does not override pending changes.</span></span>

<span data-ttu-id="7a620-113">La propriété **Update Resync** est une propriété dynamique ajoutée à la collection [Properties](recordset-object-ado.md) de l'objet [Recordset](properties-collection-ado.md) lorsque la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="7a620-113">**Update Resync** is a dynamic property appended to the [Recordset](recordset-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

