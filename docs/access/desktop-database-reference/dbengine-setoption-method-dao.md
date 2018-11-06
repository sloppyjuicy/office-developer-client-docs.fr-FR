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
ms.openlocfilehash: 55baceac9523400c5e646fbc4c1e7bb411219697
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998587"
---
# <a name="dbenginesetoption-method-dao"></a><span data-ttu-id="5b836-102">Méthode DBEngine.SetOption (DAO)</span><span class="sxs-lookup"><span data-stu-id="5b836-102">DBEngine.SetOption method (DAO)</span></span>

<span data-ttu-id="5b836-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b836-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5b836-104">Remplace temporairement les valeurs des clés du moteur de base de données Microsoft Access dans le Registre de Windows (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="5b836-104">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b836-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b836-105">Syntax</span></span>

<span data-ttu-id="5b836-106">*expression* . SetOption (***Option***, ***valeur***)</span><span class="sxs-lookup"><span data-stu-id="5b836-106">*expression* .SetOption(***Option***, ***Value***)</span></span>

<span data-ttu-id="5b836-107">*expression* Expression qui renvoie un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="5b836-107">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b836-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b836-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5b836-109">Name</span><span class="sxs-lookup"><span data-stu-id="5b836-109">Name</span></span></p></th>
<th><p><span data-ttu-id="5b836-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="5b836-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="5b836-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="5b836-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="5b836-112">Description</span><span class="sxs-lookup"><span data-stu-id="5b836-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b836-113"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="5b836-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="5b836-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5b836-114">Required</span></span></p></td>
<td><p><span data-ttu-id="5b836-115"><strong>Entier long</strong></span><span class="sxs-lookup"><span data-stu-id="5b836-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="5b836-116">Constante décrite dans les Notes.</span><span class="sxs-lookup"><span data-stu-id="5b836-116">A constant as described in Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b836-117"><em>Valeur</em></span><span class="sxs-lookup"><span data-stu-id="5b836-117"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="5b836-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5b836-118">Required</span></span></p></td>
<td><p><span data-ttu-id="5b836-119"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="5b836-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="5b836-120">La valeur que vous souhaitez définir l’option.</span><span class="sxs-lookup"><span data-stu-id="5b836-120">The value that you want to set option to.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5b836-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="5b836-121">Remarks</span></span>

<span data-ttu-id="5b836-122">Chaque constante renvoie à la clé de Registre correspondante dans le chemin d’accès HKEY\_LOCAL\_ordinateur\\logiciel\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\moteurs\\ACE (autrement dit, **dbSharedAsyncDelay** correspond à la clé HKEY\_LOCAL\_ordinateur\\logiciel\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\moteurs\\ACE \\SharedAsyncDelay, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="5b836-122">Each constant refers to the corresponding registry key in the path HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE (that is, **dbSharedAsyncDelay** corresponds to the key HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE\\SharedAsyncDelay, and so on).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5b836-123">Constant</span><span class="sxs-lookup"><span data-stu-id="5b836-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="5b836-124">Description</span><span class="sxs-lookup"><span data-stu-id="5b836-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b836-125"><strong>dbPageTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="5b836-125"><strong>dbPageTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="5b836-126">Clé PageTimeout</span><span class="sxs-lookup"><span data-stu-id="5b836-126">The PageTimeout key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b836-127"><strong>dbSharedAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="5b836-127"><strong>dbSharedAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="5b836-128">Clé SharedAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="5b836-128">The SharedAsyncDelay key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b836-129"><strong>dbExclusiveAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="5b836-129"><strong>dbExclusiveAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="5b836-130">Clé ExclusiveAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="5b836-130">The ExclusiveAsyncDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b836-131"><strong>dbLockRetry</strong></span><span class="sxs-lookup"><span data-stu-id="5b836-131"><strong>dbLockRetry</strong></span></span></p></td>
<td><p><span data-ttu-id="5b836-132">Clé LockRetry</span><span class="sxs-lookup"><span data-stu-id="5b836-132">The LockRetry key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b836-133"><strong>dbUserCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="5b836-133"><strong>dbUserCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="5b836-134">Clé UserCommitSync</span><span class="sxs-lookup"><span data-stu-id="5b836-134">The UserCommitSync key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b836-135"><strong>dbImplicitCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="5b836-135"><strong>dbImplicitCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="5b836-136">Clé ImplicitCommitSync</span><span class="sxs-lookup"><span data-stu-id="5b836-136">The ImplicitCommitSync key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b836-137"><strong>dbMaxBufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="5b836-137"><strong>dbMaxBufferSize</strong></span></span></p></td>
<td><p><span data-ttu-id="5b836-138">Clé MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="5b836-138">The MaxBufferSize key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b836-139"><strong>dbMaxLocksPerFile</strong></span><span class="sxs-lookup"><span data-stu-id="5b836-139"><strong>dbMaxLocksPerFile</strong></span></span></p></td>
<td><p><span data-ttu-id="5b836-140">Clé MaxLocksPerFile</span><span class="sxs-lookup"><span data-stu-id="5b836-140">The MaxLocksPerFile key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b836-141"><strong>dbLockDelay</strong></span><span class="sxs-lookup"><span data-stu-id="5b836-141"><strong>dbLockDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="5b836-142">Clé LockDelay</span><span class="sxs-lookup"><span data-stu-id="5b836-142">The LockDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b836-143"><strong>dbRecycleLVs</strong></span><span class="sxs-lookup"><span data-stu-id="5b836-143"><strong>dbRecycleLVs</strong></span></span></p></td>
<td><p><span data-ttu-id="5b836-144">Clé RecycleLVs</span><span class="sxs-lookup"><span data-stu-id="5b836-144">The RecycleLVs key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b836-145"><strong>dbFlushTransactionTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="5b836-145"><strong>dbFlushTransactionTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="5b836-146">Clé FlushTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="5b836-146">The FlushTransactionTimeout key</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5b836-p101">Utilisez la méthode **SetOption** pour remplacer les valeurs de registre lors de l'exécution. Les nouvelles valeurs définies avec la méthode **SetOption** restent activées tant qu'elles ne sont pas modifiées de nouveau par un autre appel de la méthode **SetOption** ou que l'objet **DBEngine** n'est pas fermé.</span><span class="sxs-lookup"><span data-stu-id="5b836-p101">Use the **SetOption** method to override registry values at run-time. New values established with the **SetOption** method remain in effect until changed again by another **SetOption** call, or until the **DBEngine** object is closed.</span></span>

