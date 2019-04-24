---
title: DBEngine. SetOption, méthode (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294196"
---
# <a name="dbenginesetoption-method-dao"></a><span data-ttu-id="d4528-102">DBEngine. SetOption, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="d4528-102">DBEngine.SetOption method (DAO)</span></span>

<span data-ttu-id="d4528-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d4528-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d4528-104">Remplace temporairement les valeurs des clés du moteur de base de données Microsoft Access dans le Registre de Windows (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="d4528-104">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="d4528-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4528-105">Syntax</span></span>

<span data-ttu-id="d4528-106">*expression* . SetOption (***option***, ***valeur***)</span><span class="sxs-lookup"><span data-stu-id="d4528-106">*expression* .SetOption(***Option***, ***Value***)</span></span>

<span data-ttu-id="d4528-107">*expression* Expression qui renvoie un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="d4528-107">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d4528-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4528-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d4528-109">Nom</span><span class="sxs-lookup"><span data-stu-id="d4528-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d4528-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="d4528-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="d4528-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="d4528-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="d4528-112">Description</span><span class="sxs-lookup"><span data-stu-id="d4528-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4528-113"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="d4528-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="d4528-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d4528-114">Required</span></span></p></td>
<td><p><span data-ttu-id="d4528-115"><strong>Entier long</strong></span><span class="sxs-lookup"><span data-stu-id="d4528-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="d4528-116">Constante décrite dans les Notes.</span><span class="sxs-lookup"><span data-stu-id="d4528-116">A constant as described in Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4528-117"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="d4528-117"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="d4528-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d4528-118">Required</span></span></p></td>
<td><p><span data-ttu-id="d4528-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="d4528-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d4528-120">Valeur à attribuer à l'option.</span><span class="sxs-lookup"><span data-stu-id="d4528-120">The value that you want to set option to.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d4528-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="d4528-121">Remarks</span></span>

<span data-ttu-id="d4528-122">Chaque constante fait référence à la clé de Registre correspondante dans le\_chemin\_HKEY\\local\\machine\\Software\\Microsoft\\Office 12,0 Access\\Connectivity\\Engine Engines (en d'autres termes, **dbSharedAsyncDelay** correspond à la clé HKEY\_Software\_\\\\de l'ordinateur\\local\\du\\moteur Microsoft Office\\12,0\\Access Connectivity Engine \\SharedAsyncDelay, etc.).</span><span class="sxs-lookup"><span data-stu-id="d4528-122">Each constant refers to the corresponding registry key in the path HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE (that is, **dbSharedAsyncDelay** corresponds to the key HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE\\SharedAsyncDelay, and so on).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d4528-123">Constante</span><span class="sxs-lookup"><span data-stu-id="d4528-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="d4528-124">Description</span><span class="sxs-lookup"><span data-stu-id="d4528-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4528-125"><strong>dbPageTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="d4528-125"><strong>dbPageTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="d4528-126">Clé PageTimeout</span><span class="sxs-lookup"><span data-stu-id="d4528-126">The PageTimeout key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4528-127"><strong>dbSharedAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="d4528-127"><strong>dbSharedAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="d4528-128">Clé SharedAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="d4528-128">The SharedAsyncDelay key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4528-129"><strong>dbExclusiveAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="d4528-129"><strong>dbExclusiveAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="d4528-130">Clé ExclusiveAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="d4528-130">The ExclusiveAsyncDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4528-131"><strong>dbLockRetry</strong></span><span class="sxs-lookup"><span data-stu-id="d4528-131"><strong>dbLockRetry</strong></span></span></p></td>
<td><p><span data-ttu-id="d4528-132">Clé LockRetry</span><span class="sxs-lookup"><span data-stu-id="d4528-132">The LockRetry key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4528-133"><strong>dbUserCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="d4528-133"><strong>dbUserCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="d4528-134">Clé UserCommitSync</span><span class="sxs-lookup"><span data-stu-id="d4528-134">The UserCommitSync key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4528-135"><strong>dbImplicitCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="d4528-135"><strong>dbImplicitCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="d4528-136">Clé ImplicitCommitSync</span><span class="sxs-lookup"><span data-stu-id="d4528-136">The ImplicitCommitSync key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4528-137"><strong>dbMaxBufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="d4528-137"><strong>dbMaxBufferSize</strong></span></span></p></td>
<td><p><span data-ttu-id="d4528-138">Clé MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="d4528-138">The MaxBufferSize key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4528-139"><strong>dbMaxLocksPerFile</strong></span><span class="sxs-lookup"><span data-stu-id="d4528-139"><strong>dbMaxLocksPerFile</strong></span></span></p></td>
<td><p><span data-ttu-id="d4528-140">Clé MaxLocksPerFile</span><span class="sxs-lookup"><span data-stu-id="d4528-140">The MaxLocksPerFile key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4528-141"><strong>dbLockDelay</strong></span><span class="sxs-lookup"><span data-stu-id="d4528-141"><strong>dbLockDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="d4528-142">Clé LockDelay</span><span class="sxs-lookup"><span data-stu-id="d4528-142">The LockDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4528-143"><strong>dbRecycleLVs</strong></span><span class="sxs-lookup"><span data-stu-id="d4528-143"><strong>dbRecycleLVs</strong></span></span></p></td>
<td><p><span data-ttu-id="d4528-144">Clé RecycleLVs</span><span class="sxs-lookup"><span data-stu-id="d4528-144">The RecycleLVs key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4528-145"><strong>dbFlushTransactionTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="d4528-145"><strong>dbFlushTransactionTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="d4528-146">Clé FlushTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="d4528-146">The FlushTransactionTimeout key</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d4528-p101">Utilisez la méthode **SetOption** pour remplacer les valeurs de registre lors de l'exécution. Les nouvelles valeurs définies avec la méthode **SetOption** restent activées tant qu'elles ne sont pas modifiées de nouveau par un autre appel de la méthode **SetOption** ou que l'objet **DBEngine** n'est pas fermé.</span><span class="sxs-lookup"><span data-stu-id="d4528-p101">Use the **SetOption** method to override registry values at run-time. New values established with the **SetOption** method remain in effect until changed again by another **SetOption** call, or until the **DBEngine** object is closed.</span></span>

