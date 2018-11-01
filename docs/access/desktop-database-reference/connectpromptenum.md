---
title: ConnectPromptEnum (référence de base de données du bureau Access)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 387e9a853a306b2375034359ce26db50685afcc4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887907"
---
# <a name="connectpromptenum"></a><span data-ttu-id="90e62-102">ConnectPromptEnum</span><span class="sxs-lookup"><span data-stu-id="90e62-102">ConnectPromptEnum</span></span>

<span data-ttu-id="90e62-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="90e62-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="90e62-104">Spécifie si une boîte de dialogue doit s'afficher pour inviter à entrer les paramètres manquants lors de l'ouverture d'une connexion à une source de données.</span><span class="sxs-lookup"><span data-stu-id="90e62-104">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to a data source.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90e62-105">Constante</span><span class="sxs-lookup"><span data-stu-id="90e62-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="90e62-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="90e62-106">Value</span></span></p></th>
<th><p><span data-ttu-id="90e62-107">Description</span><span class="sxs-lookup"><span data-stu-id="90e62-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90e62-108"><strong>adPromptAlways</strong></span><span class="sxs-lookup"><span data-stu-id="90e62-108"><strong>adPromptAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="90e62-109">1</span><span class="sxs-lookup"><span data-stu-id="90e62-109">1</span></span></p></td>
<td><p><span data-ttu-id="90e62-110">Toujours demander.</span><span class="sxs-lookup"><span data-stu-id="90e62-110">Prompts always.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90e62-111"><strong>adPromptComplete</strong></span><span class="sxs-lookup"><span data-stu-id="90e62-111"><strong>adPromptComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="90e62-112">2</span><span class="sxs-lookup"><span data-stu-id="90e62-112">2</span></span></p></td>
<td><p><span data-ttu-id="90e62-113">Ne demander qu'en cas d'informations incomplètes.</span><span class="sxs-lookup"><span data-stu-id="90e62-113">Prompts if more information is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90e62-114"><strong>adPromptCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="90e62-114"><strong>adPromptCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="90e62-115">3</span><span class="sxs-lookup"><span data-stu-id="90e62-115">3</span></span></p></td>
<td><p><span data-ttu-id="90e62-116">Ne demander qu'en cas d'informations incomplètes, les paramètres optionnels n'étant pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="90e62-116">Prompts if more information is required but optional parameters are not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90e62-117"><strong>adPromptNever</strong></span><span class="sxs-lookup"><span data-stu-id="90e62-117"><strong>adPromptNever</strong></span></span></p></td>
<td><p><span data-ttu-id="90e62-118">4</span><span class="sxs-lookup"><span data-stu-id="90e62-118">4</span></span></p></td>
<td><p><span data-ttu-id="90e62-119">Ne jamais demander.</span><span class="sxs-lookup"><span data-stu-id="90e62-119">Never prompts.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="90e62-120">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="90e62-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="90e62-121">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="90e62-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90e62-122">Constante</span><span class="sxs-lookup"><span data-stu-id="90e62-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90e62-123">AdoEnums.ConnectPrompt.ALWAYS</span><span class="sxs-lookup"><span data-stu-id="90e62-123">AdoEnums.ConnectPrompt.ALWAYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90e62-124">AdoEnums.ConnectPrompt.COMPLETE</span><span class="sxs-lookup"><span data-stu-id="90e62-124">AdoEnums.ConnectPrompt.COMPLETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90e62-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span><span class="sxs-lookup"><span data-stu-id="90e62-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90e62-126">AdoEnums.ConnectPrompt.NEVER</span><span class="sxs-lookup"><span data-stu-id="90e62-126">AdoEnums.ConnectPrompt.NEVER</span></span></p></td>
</tr>
</tbody>
</table>

