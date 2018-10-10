---
title: ALTER USER ou DATABASE (Microsoft Access SQL), instruction
TOCTitle: ALTER USER or DATABASE Statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d6e471adb7ef2c5826d24f569174b40247d0fd8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470292"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a>ALTER USER ou DATABASE (Microsoft Access SQL), instruction


**S’applique à**: Access 2013 | Office 2013

Change le mot de passe d'un utilisateur ou d'une base de données existant.

## <a name="syntax"></a>Syntaxe

ALTER DATABASE PASSWORD *NouveauMotDePasse ancienmotdepasse*

ALTER USER *utilisateur* PASSWORD *NouveauMotDePasse ancienmotdepasse*

L'instruction ALTER USER ou DATABASE est composée des arguments suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>utilisateur</em></p></td>
<td><p>Nom de l'utilisateur à ajouter au fichier d'informations du groupe de travail.</p></td>
</tr>
<tr class="even">
<td><p><em>nouveaumotdepasse </em></p></td>
<td><p>Nouveau mot de passe à associer au nom de l'<em>utilisateur</em> ou de la <em>base de données</em> spécifié.</p></td>
</tr>
<tr class="odd">
<td><p><em>ancienmotdepasse</em></p></td>
<td><p>Mot de passe existant à associer au nom de l'<em>utilisateur</em> ou du <em>groupe</em> spécifié.</p></td>
</tr>
</tbody>
</table>

