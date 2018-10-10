---
title: Caractéristiques de curseur et de verrou
TOCTitle: Cursor and Lock Characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 50eadc486d00436a51b9f7341ef6e0ad2587a015
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469061"
---
# <a name="cursor-and-lock-characteristics"></a>Caractéristiques de curseur et de verrou


**S’applique à**: Access 2013 | Office 2013

S'il est vrai que les caractéristiques d'un curseur dépendent des fonctionnalités du fournisseur, les avantages et inconvénients suivants s'appliquent généralement aux différents types de curseurs et de verrous.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Type de curseur ou de verrou</p></th>
<th><p>Avantages</p></th>
<th><p>Inconvénients</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p></p>
<ul>
<li><p>Ressources requises peu importantes</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Défilement arrière impossible</p></li>
<li><p>Pas d'accès concurrentiel aux données</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p></p>
<ul>
<li><p>Défilement possible</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Pas d'accès concurrentiel aux données</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p></p>
<ul>
<li><p>Accès concurrentiel aux données possible mais limité</p></li>
<li><p>Défilement possible</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Ressources requises plus importantes</p></li>
<li><p>Non disponible dans un scénario déconnecté</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p></p>
<ul>
<li><p>Accès concurrentiel aux données élevé</p></li>
<li><p>Défilement possible</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Ressources requises très importantes</p></li>
<li><p>Non disponible dans un scénario déconnecté</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockReadOnly</strong></p></td>
<td><p></p>
<ul>
<li><p>Ressources requises peu importantes</p></li>
<li><p>Hautement évolutif</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Mise à jour des données par le curseur impossible</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockBatchOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Mises à jour par lot</p></li>
<li><p>Scénarios déconnectés autorisés</p></li>
<li><p>Accès aux données par d'autres utilisateurs possible</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Données modifiables simultanément par plusieurs utilisateurs</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockPessimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Modification des données par d'autres utilisateurs impossible lorsqu'elles sont verrouillées</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Accès aux données par d'autres utilisateurs impossible lorsqu'elles sont verrouillées</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Accès aux données par d'autres utilisateurs possible</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Données modifiables simultanément par plusieurs utilisateurs</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

