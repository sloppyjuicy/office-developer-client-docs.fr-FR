---
title: ExecuteOptions, propriété (RDS)
TOCTitle: ExecuteOptions Property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e5a91d3941db0b7daa61b506c136dab59f24ed0
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603587"
---
# <a name="executeoptions-property-rds"></a><span data-ttu-id="e8c25-102">ExecuteOptions, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="e8c25-102">ExecuteOptions Property (RDS)</span></span>


<span data-ttu-id="e8c25-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8c25-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e8c25-104">Indique si l'exécution asynchrone est activée.</span><span class="sxs-lookup"><span data-stu-id="e8c25-104">Indicates whether asynchronous execution is enabled.</span></span>

<span data-ttu-id="e8c25-105"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="e8c25-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="e8c25-106">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e8c25-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="e8c25-107">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e8c25-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="e8c25-108">master</span><span class="sxs-lookup"><span data-stu-id="e8c25-108">master</span></span>

<span data-ttu-id="e8c25-109">Définit ou renvoie l'une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e8c25-109">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8c25-110">Constante</span><span class="sxs-lookup"><span data-stu-id="e8c25-110">Constant</span></span></p></th>
<th><p><span data-ttu-id="e8c25-111">Description</span><span class="sxs-lookup"><span data-stu-id="e8c25-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8c25-112"><strong>valeur adcExecSync</strong></span><span class="sxs-lookup"><span data-stu-id="e8c25-112"><strong>adcExecSync</strong></span></span></p></td>
<td><p><span data-ttu-id="e8c25-113">Exécute l’actualisation suivante du <a href="recordset-object-ado.md">Recordset</a> de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e8c25-113">Executes the next refresh of the <a href="recordset-object-ado.md">Recordset</a> synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8c25-114"><strong>adcExecAsync</strong></span><span class="sxs-lookup"><span data-stu-id="e8c25-114"><strong>adcExecAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="e8c25-p101">Valeur par défaut. Exécute l'actualisation suivante du <strong>Recordset</strong> de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e8c25-p101">Default. Executes the next refresh of the <strong>Recordset</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="e8c25-p102">[!REMARQUE] Chaque fichier exécutable côté client utilisant ces constantes doit fournir les déclarations correspondantes. Vous pouvez couper et coller les déclarations de constante dont vous avez besoin dans le fichier Adcvbs.inc placé dans le dossier C:\Program Files\Common Files\System\MSADC.</span><span class="sxs-lookup"><span data-stu-id="e8c25-p102">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations that you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="e8c25-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="e8c25-119">Remarks</span></span>

<span data-ttu-id="e8c25-120">Si **ExecuteOptions** est défini sur **adcExecAsync**, l'appel suivant de **Refresh** est exécuté de façon asynchrone sur le [Recordset](datacontrol-object-rds.md) de l'objet **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="e8c25-120">If **ExecuteOptions** is set to **adcExecAsync**, then this asynchronously executes the next **Refresh** call on the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset**.</span></span>

<span data-ttu-id="e8c25-121">Si vous essayez d'appeler [Reset](reset-method-rds.md),[Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md) ou [Recordset](recordset-sourcerecordset-properties-rds.md) pendant l'exécution d'une autre opération asynchrone susceptible de modifier le [Recordset](datacontrol-object-rds.md) de l'objet **RDS.DataControl**, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="e8c25-121">If you try to call [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md), or [Recordset](recordset-sourcerecordset-properties-rds.md) while another asynchronous operation that might change the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset** is executing, an error occurs.</span></span>

<span data-ttu-id="e8c25-122">S’il se produit une erreur pendant une opération asynchrone, la valeur [ReadyState](readystate-property-rds.md) de l’objet **RDS.DataControl** (**adcReadyStateLoaded**) est remplacée par **adcReadyStateComplete** et la valeur de la propriété **Recordset** reste la même : *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="e8c25-122">If an error occurs during an asynchronous operation, the **RDS.DataControl** object's [ReadyState](readystate-property-rds.md) value changes from **adcReadyStateLoaded** to **adcReadyStateComplete**, and the **Recordset** property value remains *Nothing*.</span></span>

