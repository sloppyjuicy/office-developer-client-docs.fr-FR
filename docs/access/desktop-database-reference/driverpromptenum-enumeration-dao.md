---
title: DriverPromptEnum, éumération (DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d4011bb2958aa1bb34dfc8255196b4e6001ba848
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615584"
---
# <a name="driverpromptenum-enumeration-dao"></a>DriverPromptEnum, éumération (DAO)


**S’applique à** : Access 2013, Office 2013

Spécifie si le système doit demander à l'utilisateur d'établir une connexion et à quel moment cette demande doit avoir lieu.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbDriverComplete</p></td>
<td><p>0</p></td>
<td><p>Si la chaîne de connexion fournie comprend le mot clé DSN, le gestionnaire de pilotes utilise la chaîne comme indiqué dans Connect. Autrement, il se comporte comme lorsque <strong>dbDriverPrompt</strong> est spécifié.</p></td>
</tr>
<tr class="even">
<td><p>dbDriverCompleteRequired</p></td>
<td><p>3</p></td>
<td><p>(Paramètre par défaut) Se comporte comme <strong>dbDriverComplete</strong>, excepté que le pilote désactive les contrôles pour les informations qui ne sont pas nécessaires à l'établissement de la connexion.</p></td>
</tr>
<tr class="odd">
<td><p>dbDriverNoPrompt</p></td>
<td><p>1</p></td>
<td><p>Le gestionnaire de pilotes utilise la chaîne de connexion fournie dans Connect. En l'absence d'informations détaillées, une erreur récupérable est renvoyée.</p></td>
</tr>
<tr class="even">
<td><p>dbDriverPrompt</p></td>
<td><p>2</p></td>
<td><p>Le gestionnaire de pilotes affiche la boîte de dialogue <strong>Sources de données ODBC</strong>. La chaîne de connexion utilisée pour établir la connexion est construite à partir du nom DSN sélectionné et fourni par l'utilisateur par le biais des boîtes de dialogue.</p></td>
</tr>
</tbody>
</table>

