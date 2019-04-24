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
# <a name="connectpromptenum"></a>ConnectPromptEnum

**S’applique à** : Access 2013, Office 2013

Spécifie si une boîte de dialogue doit s'afficher pour inviter à entrer les paramètres manquants lors de l'ouverture d'une connexion à une source de données.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adPromptAlways</strong></p></td>
<td><p>0,1</p></td>
<td><p>Toujours demander.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPromptComplete</strong></p></td>
<td><p>n°2</p></td>
<td><p>Ne demander qu'en cas d'informations incomplètes.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPromptCompleteRequired</strong></p></td>
<td><p>3</p></td>
<td><p>Ne demander qu'en cas d'informations incomplètes, les paramètres optionnels n'étant pas autorisés.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPromptNever</strong></p></td>
<td><p>4</p></td>
<td><p>Ne jamais demander.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Module : **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums. ConnectPrompt. ALWAYs</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. ConnectPrompt. complet</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. ConnectPrompt. COMPLETEREQUIRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. ConnectPrompt. NEVER</p></td>
</tr>
</tbody>
</table>

