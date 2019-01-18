---
title: ConnectOptionEnum (référence de base de données du bureau Access)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95b622d2216b085ffd0f76c8a26533187c17bd7b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699959"
---
# <a name="connectoptionenum"></a><span data-ttu-id="a1019-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="a1019-102">ConnectOptionEnum</span></span>

<span data-ttu-id="a1019-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1019-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1019-104">Indique si la méthode [Open](open-method-ado-connection.md) d'un objet [Connection](connection-object-ado.md) doit être exécutée après (de façon synchrone) ou avant (de façon asynchrone) l'établissement de la connexion.</span><span class="sxs-lookup"><span data-stu-id="a1019-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1019-105">Constante</span><span class="sxs-lookup"><span data-stu-id="a1019-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a1019-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1019-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a1019-107">Description</span><span class="sxs-lookup"><span data-stu-id="a1019-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1019-108"><strong>adAsyncConnect</strong></span><span class="sxs-lookup"><span data-stu-id="a1019-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="a1019-109">16</span><span class="sxs-lookup"><span data-stu-id="a1019-109">16</span></span></p></td>
<td><p><span data-ttu-id="a1019-p101">Ouvre la connexion de manière asynchrone. L’événement <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> peut être utilisé pour déterminer quand la connexion sera disponible.</span><span class="sxs-lookup"><span data-stu-id="a1019-p101">Opens the connection asynchronously. The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1019-112"><strong>adConnectUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="a1019-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="a1019-113">-1</span><span class="sxs-lookup"><span data-stu-id="a1019-113">-1</span></span></p></td>
<td><p><span data-ttu-id="a1019-p102">Par défaut. Ouvre la connexion de manière synchrone.</span><span class="sxs-lookup"><span data-stu-id="a1019-p102">Default. Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="a1019-116">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="a1019-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="a1019-117">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="a1019-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1019-118">Constante</span><span class="sxs-lookup"><span data-stu-id="a1019-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1019-119">AdoEnums.ConnectOption.ASYNCCONNECT</span><span class="sxs-lookup"><span data-stu-id="a1019-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1019-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="a1019-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

