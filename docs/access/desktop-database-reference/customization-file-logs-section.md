---
title: Section des journaux du fichier de personnalisation
TOCTitle: Customization File Logs section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4ef7b76de0acaa53eda4229659f0559bc71e4060
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462037"
---
# <a name="customization-file-logs-section"></a>Section des journaux du fichier de personnalisation

**S’applique à** : Access 2013, Office 2013

La section **logs** contient une entrée de fichier journal qui indique le nom du fichier qui enregistre les erreurs au cours du fonctionnement de l'objet **DataFactory**.

## <a name="syntax"></a>Syntaxe

Une entrée de fichier journal a la forme suivante :

`err=FileName`


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Quitter</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>err</strong></p></td>
<td><p>Chaîne littéral qui indique qu'il s'agit d'une entrée de fichier journal.</p></td>
</tr>
<tr class="even">
<td><p><em>FileName</em></p></td>
<td><p>Chemin d'accès complet et nom du fichier. Le nom de fichier habituel est <strong>c:\msdfmap.log</strong>.</p></td>
</tr>
</tbody>
</table>


Le fichier journal contient le nom de l'utilisateur, HRESULT, la date et l'heure de chaque erreur.

