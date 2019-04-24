---
title: Workspace. type, propriété (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e698963d60809e8d88c4ff87532fb7b74cff275c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311304"
---
# <a name="workspacetype-property-dao"></a>Workspace. type, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type de données **Integer** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . Entrer

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

