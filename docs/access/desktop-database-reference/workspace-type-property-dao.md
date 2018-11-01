---
title: Workspace.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3293c145ae615e7373a7061e79fc7ff531c24cf8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881803"
---
# <a name="workspacetype-property-dao"></a>Workspace.Type Property (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type de données **Integer** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . Type

*expression* Variable qui représente un objet **Workspace** .

## <a name="remarks"></a>Remarques

Pour un objet **Workspace**, les valeurs des paramètres et de retour possibles sont les suivantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Type d'espace de travail</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbUseJet</strong></p></td>
<td><p>L'<strong>espace de travail</strong> est connecté au moteur de base de données Microsoft Access.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUseODBC</strong></p></td>
<td><p>L'<strong>espace de travail</strong> est connecté à une source de données ODBC.</p></td>
</tr>
</tbody>
</table>

