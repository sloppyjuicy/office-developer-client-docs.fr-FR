---
title: ConnectPromptEnum (référence de base de données de bureau Access)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54643a66316d7f534553c20ecc3aafdf755fb857
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295666"
---
# <a name="connectpromptenum"></a><span data-ttu-id="2c077-102">ConnectPromptEnum</span><span class="sxs-lookup"><span data-stu-id="2c077-102">ConnectPromptEnum</span></span>

<span data-ttu-id="2c077-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c077-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2c077-104">Spécifie si une boîte de dialogue doit s'afficher pour inviter à entrer les paramètres manquants lors de l'ouverture d'une connexion à une source de données.</span><span class="sxs-lookup"><span data-stu-id="2c077-104">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to a data source.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2c077-105">Constante</span><span class="sxs-lookup"><span data-stu-id="2c077-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="2c077-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c077-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2c077-107">Description</span><span class="sxs-lookup"><span data-stu-id="2c077-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c077-108"><strong>adPromptAlways</strong></span><span class="sxs-lookup"><span data-stu-id="2c077-108"><strong>adPromptAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="2c077-109">1 </span><span class="sxs-lookup"><span data-stu-id="2c077-109">1</span></span></p></td>
<td><p><span data-ttu-id="2c077-110">Toujours demander.</span><span class="sxs-lookup"><span data-stu-id="2c077-110">Prompts always.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c077-111"><strong>adPromptComplete</strong></span><span class="sxs-lookup"><span data-stu-id="2c077-111"><strong>adPromptComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="2c077-112">2 </span><span class="sxs-lookup"><span data-stu-id="2c077-112">2</span></span></p></td>
<td><p><span data-ttu-id="2c077-113">Ne demander qu'en cas d'informations incomplètes.</span><span class="sxs-lookup"><span data-stu-id="2c077-113">Prompts if more information is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c077-114"><strong>adPromptCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="2c077-114"><strong>adPromptCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="2c077-115">3 </span><span class="sxs-lookup"><span data-stu-id="2c077-115">3</span></span></p></td>
<td><p><span data-ttu-id="2c077-116">Ne demander qu'en cas d'informations incomplètes, les paramètres optionnels n'étant pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="2c077-116">Prompts if more information is required but optional parameters are not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c077-117"><strong>adPromptNever</strong></span><span class="sxs-lookup"><span data-stu-id="2c077-117"><strong>adPromptNever</strong></span></span></p></td>
<td><p><span data-ttu-id="2c077-118">4 </span><span class="sxs-lookup"><span data-stu-id="2c077-118">4</span></span></p></td>
<td><p><span data-ttu-id="2c077-119">Ne jamais demander.</span><span class="sxs-lookup"><span data-stu-id="2c077-119">Never prompts.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2c077-120">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="2c077-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="2c077-121">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="2c077-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2c077-122">Constante</span><span class="sxs-lookup"><span data-stu-id="2c077-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c077-123">AdoEnums.ConnectPrompt.ALWAYS</span><span class="sxs-lookup"><span data-stu-id="2c077-123">AdoEnums.ConnectPrompt.ALWAYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c077-124">AdoEnums.ConnectPrompt.COMPLETE</span><span class="sxs-lookup"><span data-stu-id="2c077-124">AdoEnums.ConnectPrompt.COMPLETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c077-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span><span class="sxs-lookup"><span data-stu-id="2c077-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c077-126">AdoEnums.ConnectPrompt.NEVER</span><span class="sxs-lookup"><span data-stu-id="2c077-126">AdoEnums.ConnectPrompt.NEVER</span></span></p></td>
</tr>
</tbody>
</table>

