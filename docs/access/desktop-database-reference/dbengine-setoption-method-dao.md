---
title: DBEngine.SetOption Method (DAO)
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
ms.openlocfilehash: 1d11d9c6e3434e635d93e9c499c6d5f7c82c6f49
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867866"
---
# <a name="dbenginesetoption-method-dao"></a><span data-ttu-id="0fa57-102">DBEngine.SetOption Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="0fa57-102">DBEngine.SetOption Method (DAO)</span></span>


<span data-ttu-id="0fa57-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0fa57-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0fa57-104">Remplace temporairement les valeurs des clés du moteur de base de données Microsoft Access dans le Registre de Windows (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="0fa57-104">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="0fa57-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fa57-105">Syntax</span></span>

<span data-ttu-id="0fa57-106">*expression* . SetOption (***Option***, ***valeur***)</span><span class="sxs-lookup"><span data-stu-id="0fa57-106">*expression* .SetOption(***Option***, ***Value***)</span></span>

<span data-ttu-id="0fa57-107">*expression* Expression qui renvoie un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="0fa57-107">*expression* An expression that returns a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="0fa57-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0fa57-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0fa57-109">Name</span><span class="sxs-lookup"><span data-stu-id="0fa57-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0fa57-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="0fa57-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="0fa57-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="0fa57-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="0fa57-112">Description</span><span class="sxs-lookup"><span data-stu-id="0fa57-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fa57-113">Option</span><span class="sxs-lookup"><span data-stu-id="0fa57-113">Option</span></span></p></td>
<td><p><span data-ttu-id="0fa57-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0fa57-114">Required</span></span></p></td>
<td><p><span data-ttu-id="0fa57-115"><strong>Entier long</strong></span><span class="sxs-lookup"><span data-stu-id="0fa57-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa57-116">Constante décrite dans les Notes.</span><span class="sxs-lookup"><span data-stu-id="0fa57-116">A constant as described in Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fa57-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0fa57-117">Value</span></span></p></td>
<td><p><span data-ttu-id="0fa57-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0fa57-118">Required</span></span></p></td>
<td><p><span data-ttu-id="0fa57-119"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="0fa57-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa57-120">La valeur que vous souhaitez définir l’option.</span><span class="sxs-lookup"><span data-stu-id="0fa57-120">The value that you want to set option to.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0fa57-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="0fa57-121">Remarks</span></span>

<span data-ttu-id="0fa57-122">Chaque constante renvoie à la clé de Registre correspondante dans le chemin d’accès HKEY\_LOCAL\_ordinateur\\logiciel\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\moteurs\\ACE (autrement dit, **dbSharedAsyncDelay** correspond à la clé HKEY\_LOCAL\_ordinateur\\logiciel\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\moteurs\\ACE \\SharedAsyncDelay, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="0fa57-122">Each constant refers to the corresponding registry key in the path HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE (that is, **dbSharedAsyncDelay** corresponds to the key HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE\\SharedAsyncDelay, and so on).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0fa57-123">Constant</span><span class="sxs-lookup"><span data-stu-id="0fa57-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="0fa57-124">Description</span><span class="sxs-lookup"><span data-stu-id="0fa57-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fa57-125"><strong>dbPageTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="0fa57-125"><strong>dbPageTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa57-126">Clé PageTimeout</span><span class="sxs-lookup"><span data-stu-id="0fa57-126">The PageTimeout key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fa57-127"><strong>dbSharedAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="0fa57-127"><strong>dbSharedAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa57-128">Clé SharedAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="0fa57-128">The SharedAsyncDelay key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fa57-129"><strong>dbExclusiveAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="0fa57-129"><strong>dbExclusiveAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa57-130">Clé ExclusiveAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="0fa57-130">The ExclusiveAsyncDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fa57-131"><strong>dbLockRetry</strong></span><span class="sxs-lookup"><span data-stu-id="0fa57-131"><strong>dbLockRetry</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa57-132">Clé LockRetry</span><span class="sxs-lookup"><span data-stu-id="0fa57-132">The LockRetry key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fa57-133"><strong>dbUserCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="0fa57-133"><strong>dbUserCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa57-134">Clé UserCommitSync</span><span class="sxs-lookup"><span data-stu-id="0fa57-134">The UserCommitSync key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fa57-135"><strong>dbImplicitCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="0fa57-135"><strong>dbImplicitCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa57-136">Clé ImplicitCommitSync</span><span class="sxs-lookup"><span data-stu-id="0fa57-136">The ImplicitCommitSync key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fa57-137"><strong>dbMaxBufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="0fa57-137"><strong>dbMaxBufferSize</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa57-138">Clé MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="0fa57-138">The MaxBufferSize key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fa57-139"><strong>dbMaxLocksPerFile</strong></span><span class="sxs-lookup"><span data-stu-id="0fa57-139"><strong>dbMaxLocksPerFile</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa57-140">Clé MaxLocksPerFile</span><span class="sxs-lookup"><span data-stu-id="0fa57-140">The MaxLocksPerFile key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fa57-141"><strong>dbLockDelay</strong></span><span class="sxs-lookup"><span data-stu-id="0fa57-141"><strong>dbLockDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa57-142">Clé LockDelay</span><span class="sxs-lookup"><span data-stu-id="0fa57-142">The LockDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fa57-143"><strong>dbRecycleLVs</strong></span><span class="sxs-lookup"><span data-stu-id="0fa57-143"><strong>dbRecycleLVs</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa57-144">Clé RecycleLVs</span><span class="sxs-lookup"><span data-stu-id="0fa57-144">The RecycleLVs key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fa57-145"><strong>dbFlushTransactionTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="0fa57-145"><strong>dbFlushTransactionTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa57-146">Clé FlushTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="0fa57-146">The FlushTransactionTimeout key</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0fa57-p101">Utilisez la méthode **SetOption** pour remplacer les valeurs de registre lors de l'exécution. Les nouvelles valeurs définies avec la méthode **SetOption** restent activées tant qu'elles ne sont pas modifiées de nouveau par un autre appel de la méthode **SetOption** ou que l'objet **DBEngine** n'est pas fermé.</span><span class="sxs-lookup"><span data-stu-id="0fa57-p101">Use the **SetOption** method to override registry values at run-time. New values established with the **SetOption** method remain in effect until changed again by another **SetOption** call, or until the **DBEngine** object is closed.</span></span>

