---
title: Méthode DBEngine.SetOption (DAO)
TOCTitle: SetOption Method
ms:assetid: ea55c10c-2385-1b7e-0cba-32982c9b6643
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836236(v=office.15)
ms:contentKeyID: 48548461
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1088781
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5875a8935b1b44c3c36b29344af32df552f6e01c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699890"
---
# <a name="dbenginesetoption-method-dao"></a><span data-ttu-id="7cefb-102">Méthode DBEngine.SetOption (DAO)</span><span class="sxs-lookup"><span data-stu-id="7cefb-102">DBEngine.SetOption method (DAO)</span></span>

<span data-ttu-id="7cefb-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7cefb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7cefb-104">Remplace temporairement les valeurs des clés du moteur de base de données Microsoft Access dans le Registre de Windows (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="7cefb-104">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="7cefb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cefb-105">Syntax</span></span>

<span data-ttu-id="7cefb-106">*expression* . SetOption (***Option***, ***valeur***)</span><span class="sxs-lookup"><span data-stu-id="7cefb-106">*expression* .SetOption(***Option***, ***Value***)</span></span>

<span data-ttu-id="7cefb-107">*expression* Expression qui renvoie un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="7cefb-107">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7cefb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cefb-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7cefb-109">Nom</span><span class="sxs-lookup"><span data-stu-id="7cefb-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7cefb-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="7cefb-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="7cefb-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="7cefb-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="7cefb-112">Description</span><span class="sxs-lookup"><span data-stu-id="7cefb-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7cefb-113"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="7cefb-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="7cefb-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7cefb-114">Required</span></span></p></td>
<td><p><span data-ttu-id="7cefb-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="7cefb-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="7cefb-116">Constante décrite dans les Notes.</span><span class="sxs-lookup"><span data-stu-id="7cefb-116">A constant as described in Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cefb-117"><em>Valeur</em></span><span class="sxs-lookup"><span data-stu-id="7cefb-117"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="7cefb-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7cefb-118">Required</span></span></p></td>
<td><p><span data-ttu-id="7cefb-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7cefb-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7cefb-120">La valeur que vous souhaitez définir l’option.</span><span class="sxs-lookup"><span data-stu-id="7cefb-120">The value that you want to set option to.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7cefb-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="7cefb-121">Remarks</span></span>

<span data-ttu-id="7cefb-122">Chaque constante renvoie à la clé de Registre correspondante dans le chemin d’accès HKEY\_LOCAL\_ordinateur\\logiciel\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\moteurs\\ACE (autrement dit, **dbSharedAsyncDelay** correspond à la clé HKEY\_LOCAL\_ordinateur\\logiciel\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\moteurs\\ACE \\SharedAsyncDelay, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="7cefb-122">Each constant refers to the corresponding registry key in the path HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE (that is, **dbSharedAsyncDelay** corresponds to the key HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE\\SharedAsyncDelay, and so on).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7cefb-123">Constante</span><span class="sxs-lookup"><span data-stu-id="7cefb-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="7cefb-124">Description</span><span class="sxs-lookup"><span data-stu-id="7cefb-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7cefb-125"><strong>dbPageTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="7cefb-125"><strong>dbPageTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="7cefb-126">Clé PageTimeout</span><span class="sxs-lookup"><span data-stu-id="7cefb-126">The PageTimeout key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cefb-127"><strong>dbSharedAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="7cefb-127"><strong>dbSharedAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="7cefb-128">Clé SharedAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="7cefb-128">The SharedAsyncDelay key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cefb-129"><strong>dbExclusiveAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="7cefb-129"><strong>dbExclusiveAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="7cefb-130">Clé ExclusiveAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="7cefb-130">The ExclusiveAsyncDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cefb-131"><strong>dbLockRetry</strong></span><span class="sxs-lookup"><span data-stu-id="7cefb-131"><strong>dbLockRetry</strong></span></span></p></td>
<td><p><span data-ttu-id="7cefb-132">Clé LockRetry</span><span class="sxs-lookup"><span data-stu-id="7cefb-132">The LockRetry key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cefb-133"><strong>dbUserCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="7cefb-133"><strong>dbUserCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="7cefb-134">Clé UserCommitSync</span><span class="sxs-lookup"><span data-stu-id="7cefb-134">The UserCommitSync key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cefb-135"><strong>dbImplicitCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="7cefb-135"><strong>dbImplicitCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="7cefb-136">Clé ImplicitCommitSync</span><span class="sxs-lookup"><span data-stu-id="7cefb-136">The ImplicitCommitSync key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cefb-137"><strong>dbMaxBufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="7cefb-137"><strong>dbMaxBufferSize</strong></span></span></p></td>
<td><p><span data-ttu-id="7cefb-138">Clé MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="7cefb-138">The MaxBufferSize key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cefb-139"><strong>dbMaxLocksPerFile</strong></span><span class="sxs-lookup"><span data-stu-id="7cefb-139"><strong>dbMaxLocksPerFile</strong></span></span></p></td>
<td><p><span data-ttu-id="7cefb-140">Clé MaxLocksPerFile</span><span class="sxs-lookup"><span data-stu-id="7cefb-140">The MaxLocksPerFile key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cefb-141"><strong>dbLockDelay</strong></span><span class="sxs-lookup"><span data-stu-id="7cefb-141"><strong>dbLockDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="7cefb-142">Clé LockDelay</span><span class="sxs-lookup"><span data-stu-id="7cefb-142">The LockDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cefb-143"><strong>dbRecycleLVs</strong></span><span class="sxs-lookup"><span data-stu-id="7cefb-143"><strong>dbRecycleLVs</strong></span></span></p></td>
<td><p><span data-ttu-id="7cefb-144">Clé RecycleLVs</span><span class="sxs-lookup"><span data-stu-id="7cefb-144">The RecycleLVs key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cefb-145"><strong>dbFlushTransactionTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="7cefb-145"><strong>dbFlushTransactionTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="7cefb-146">Clé FlushTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="7cefb-146">The FlushTransactionTimeout key</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7cefb-p101">Utilisez la méthode **SetOption** pour remplacer les valeurs de registre lors de l'exécution. Les nouvelles valeurs définies avec la méthode **SetOption** restent activées tant qu'elles ne sont pas modifiées de nouveau par un autre appel de la méthode **SetOption** ou que l'objet **DBEngine** n'est pas fermé.</span><span class="sxs-lookup"><span data-stu-id="7cefb-p101">Use the **SetOption** method to override registry values at run-time. New values established with the **SetOption** method remain in effect until changed again by another **SetOption** call, or until the **DBEngine** object is closed.</span></span>

