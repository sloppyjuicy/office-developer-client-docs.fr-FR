---
title: XactAttributeEnum (référence de base de données du bureau Access)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 28b81c45921120b8a3cd8768d22559355d8ff623
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870491"
---
# <a name="xactattributeenum"></a><span data-ttu-id="6287e-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="6287e-102">XactAttributeEnum</span></span>

<span data-ttu-id="6287e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6287e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6287e-104">Spécifie les attributs de transaction d'un objet [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6287e-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6287e-105">Constant</span><span class="sxs-lookup"><span data-stu-id="6287e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6287e-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="6287e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6287e-107">Description</span><span class="sxs-lookup"><span data-stu-id="6287e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6287e-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="6287e-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="6287e-109">262144</span><span class="sxs-lookup"><span data-stu-id="6287e-109">262144</span></span></p></td>
<td><p><span data-ttu-id="6287e-110">Effectue des adandons de conservation ; Autrement dit, appel de <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> lance automatiquement une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="6287e-110">Performs retaining aborts; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="6287e-111">Tous les fournisseurs prennent en charge ce.</span><span class="sxs-lookup"><span data-stu-id="6287e-111">Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6287e-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="6287e-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="6287e-113">131072</span><span class="sxs-lookup"><span data-stu-id="6287e-113">131072</span></span></p></td>
<td><p><span data-ttu-id="6287e-114">Effectue des validations de conservation ; Autrement dit, appel de <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> lance automatiquement une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="6287e-114">Performs retaining commits; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="6287e-115">Tous les fournisseurs prennent en charge ce.</span><span class="sxs-lookup"><span data-stu-id="6287e-115">Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="6287e-116">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="6287e-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="6287e-117">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6287e-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6287e-118">Constante</span><span class="sxs-lookup"><span data-stu-id="6287e-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6287e-119">AdoEnums.XactAttribute.ABORTRETAINING</span><span class="sxs-lookup"><span data-stu-id="6287e-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6287e-120">AdoEnums.XactAttribute.COMMITRETAINING</span><span class="sxs-lookup"><span data-stu-id="6287e-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

