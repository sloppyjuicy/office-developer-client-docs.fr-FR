---
title: Section Logs du fichier de personnalisation
TOCTitle: Customization File Logs Section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 479bac0c61718f12af8fcb1b176b91d3fc57841b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471869"
---
# <a name="customization-file-logs-section"></a>Section Logs du fichier de personnalisation

**S’applique à**: Access 2013 | Office 2013

La section **logs** contient une entrée de fichier journal qui indique le nom du fichier qui enregistre les erreurs au cours du fonctionnement de l'objet **DataFactory**.

## <a name="syntax"></a>Syntaxe

Une entrée de fichier journal a la forme suivante :

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Partie</p></th>
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

