---
title: XactAttributeEnum (référence de base de données de bureau Access)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e79a6143c65637660b2d59b7c7efb6a21e8935bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302568"
---
# <a name="xactattributeenum"></a><span data-ttu-id="6d7d6-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="6d7d6-102">XactAttributeEnum</span></span>

<span data-ttu-id="6d7d6-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d7d6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d7d6-104">Spécifie les attributs de transaction d’un objet [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6d7d6-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d7d6-105">Constante</span><span class="sxs-lookup"><span data-stu-id="6d7d6-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6d7d6-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d7d6-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6d7d6-107">Description</span><span class="sxs-lookup"><span data-stu-id="6d7d6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d7d6-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="6d7d6-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="6d7d6-109">262144</span><span class="sxs-lookup"><span data-stu-id="6d7d6-109">262144</span></span></p></td>
<td><p><span data-ttu-id="6d7d6-110">Effectue des abandons de rétention ; autrement dit, <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">l’appel de RollbackTrans</a> démarre automatiquement une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="6d7d6-110">Performs retaining aborts; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="6d7d6-111">Les fournisseurs ne prennent pas tous en charge cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6d7d6-111">Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d7d6-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="6d7d6-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="6d7d6-113">131072</span><span class="sxs-lookup"><span data-stu-id="6d7d6-113">131072</span></span></p></td>
<td><p><span data-ttu-id="6d7d6-114">Effectue des validations de rétention ; autrement dit, <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">l’appel de CommitTrans</a> démarre automatiquement une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="6d7d6-114">Performs retaining commits; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="6d7d6-115">Les fournisseurs ne prennent pas tous en charge cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6d7d6-115">Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="6d7d6-116">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="6d7d6-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="6d7d6-117">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6d7d6-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d7d6-118">Constante</span><span class="sxs-lookup"><span data-stu-id="6d7d6-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d7d6-119">AdoEnums.XactAttribute.ABORTRETAINING</span><span class="sxs-lookup"><span data-stu-id="6d7d6-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d7d6-120">AdoEnums.XactAttribute.COMMITRETAINING</span><span class="sxs-lookup"><span data-stu-id="6d7d6-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

