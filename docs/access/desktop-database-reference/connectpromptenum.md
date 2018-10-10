---
title: ConnectPromptEnum (référence de base de données du bureau Access)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e405b1eb3a1326d56a32c432fb212de417cf3469
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472231"
---
# <a name="connectpromptenum"></a><span data-ttu-id="f727f-102">ConnectPromptEnum</span><span class="sxs-lookup"><span data-stu-id="f727f-102">ConnectPromptEnum</span></span>


<span data-ttu-id="f727f-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f727f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f727f-104">Spécifie si une boîte de dialogue doit s'afficher pour inviter à entrer les paramètres manquants lors de l'ouverture d'une connexion à une source de données.</span><span class="sxs-lookup"><span data-stu-id="f727f-104">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to a data source.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f727f-105">Constante</span><span class="sxs-lookup"><span data-stu-id="f727f-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f727f-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="f727f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f727f-107">Description</span><span class="sxs-lookup"><span data-stu-id="f727f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f727f-108"><strong>adPromptAlways</strong></span><span class="sxs-lookup"><span data-stu-id="f727f-108"><strong>adPromptAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="f727f-109">1</span><span class="sxs-lookup"><span data-stu-id="f727f-109">1</span></span></p></td>
<td><p><span data-ttu-id="f727f-110">Toujours demander.</span><span class="sxs-lookup"><span data-stu-id="f727f-110">Prompts always.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f727f-111"><strong>adPromptComplete</strong></span><span class="sxs-lookup"><span data-stu-id="f727f-111"><strong>adPromptComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="f727f-112">2</span><span class="sxs-lookup"><span data-stu-id="f727f-112">2</span></span></p></td>
<td><p><span data-ttu-id="f727f-113">Ne demander qu'en cas d'informations incomplètes.</span><span class="sxs-lookup"><span data-stu-id="f727f-113">Prompts if more information is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f727f-114"><strong>adPromptCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="f727f-114"><strong>adPromptCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="f727f-115">3</span><span class="sxs-lookup"><span data-stu-id="f727f-115">3</span></span></p></td>
<td><p><span data-ttu-id="f727f-116">Ne demander qu'en cas d'informations incomplètes, les paramètres optionnels n'étant pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="f727f-116">Prompts if more information is required but optional parameters are not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f727f-117"><strong>adPromptNever</strong></span><span class="sxs-lookup"><span data-stu-id="f727f-117"><strong>adPromptNever</strong></span></span></p></td>
<td><p><span data-ttu-id="f727f-118">4</span><span class="sxs-lookup"><span data-stu-id="f727f-118">4</span></span></p></td>
<td><p><span data-ttu-id="f727f-119">Ne jamais demander.</span><span class="sxs-lookup"><span data-stu-id="f727f-119">Never prompts.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f727f-120">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="f727f-120">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="f727f-121">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f727f-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f727f-122">Constante</span><span class="sxs-lookup"><span data-stu-id="f727f-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f727f-123">AdoEnums.ConnectPrompt.ALWAYS</span><span class="sxs-lookup"><span data-stu-id="f727f-123">AdoEnums.ConnectPrompt.ALWAYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f727f-124">AdoEnums.ConnectPrompt.COMPLETE</span><span class="sxs-lookup"><span data-stu-id="f727f-124">AdoEnums.ConnectPrompt.COMPLETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f727f-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span><span class="sxs-lookup"><span data-stu-id="f727f-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f727f-126">AdoEnums.ConnectPrompt.NEVER</span><span class="sxs-lookup"><span data-stu-id="f727f-126">AdoEnums.ConnectPrompt.NEVER</span></span></p></td>
</tr>
</tbody>
</table>

